# MedSupply Connect, Proposta de Arquitetura de Testes

[Voltar para Validação e Qualidade de Software](../README.md)

## Metadados

| Campo | Informação |
|---|---|
| Unidade Curricular | Validação e Qualidade de Software |
| Curso | Análise e Desenvolvimento de Sistemas |
| Instituição | Faculdade Senac Pernambuco |
| Período | 5º período |
| Semestre | 2026.2 |
| Tipo | Proposta de Arquitetura de Testes |
| Sistema analisado | MedSupply Connect |
| Release | 3.0 |
| Abordagem | Risk Based Testing e Quality Engineering |
| Tema principal | Arquitetura e automação de testes |
| Documento principal | Proposta - Arquitetura de teste MedSupply.odt |
| Status | Concluído |

## Objetivo da atividade

A atividade teve como objetivo elaborar uma **Arquitetura de Testes para a Release 3.0 da plataforma MedSupply Connect**, considerando uma aplicação B2B composta por múltiplos serviços, APIs, aplicações web, integrações externas e um processo de CI/CD ainda em evolução.

A proposta busca substituir uma estratégia de qualidade excessivamente dependente de testes de interface por uma arquitetura sustentável, distribuindo os testes entre diferentes camadas.

O trabalho contempla conceitos relacionados a:

- Arquitetura de testes.
- Quality Engineering.
- Risk Based Testing.
- Shift Left Testing.
- Pirâmide de testes.
- Testes unitários.
- Testes de integração.
- Testes de contrato.
- Testes de API.
- Testes end-to-end.
- Testes exploratórios.
- gTAA.
- Testabilidade.
- Gestão de massa de dados.
- CI/CD.
- Quality Gates.
- Métricas de qualidade.
- Observabilidade.
- Estratégia de migração.

# Contexto

A MedSupply Connect apresenta uma arquitetura distribuída na qual diferentes serviços precisam colaborar para completar os principais fluxos de negócio.

Entre os domínios considerados críticos estão:

```text
Pagamento
    +
Pedido
    +
Estoque
    +
Cotação e preço
    +
Frete
    +
Autorização
    +
Notificações
    +
Antifraude
    +
Auditoria
    +
Rastreamento
```

Essa característica aumenta a necessidade de testar não apenas a interface gráfica, mas também regras isoladas, comunicação entre serviços, contratos e APIs.

# Diagnóstico da arquitetura atual

A análise inicial identificou problemas estruturais na estratégia de qualidade existente.

Entre os principais pontos estavam:

| Problema | Consequência |
|---|---|
| Automação excessivamente concentrada na interface | Testes lentos e frágeis |
| E2E com duração superior a três horas | Feedback tardio |
| Regressão manual de vários dias | Entregas mais lentas |
| Testes quebrando com mudanças visuais | Alto custo de manutenção |
| Poucos testes unitários em regras críticas | Defeitos encontrados tardiamente |
| Ausência de testes de contrato | Risco entre serviços integrados |
| Massa de dados criada manualmente | Baixa repetibilidade |
| Homologação compartilhada | Interferência entre execuções |
| Pipeline sem testes automatizados | Falta de feedback contínuo |
| Ausência de Quality Gates | Releases sem critérios objetivos |
| Relatórios sem classificação adequada das falhas | Baixa rastreabilidade |

## Problema central

O principal problema arquitetural pode ser representado por:

```text
Poucos testes nas camadas inferiores
              ↓
Muitos testes na interface
              ↓
Suíte lenta
              ↓
Testes frágeis
              ↓
Feedback tardio
              ↓
Regressão manual
              ↓
Maior risco na release
```

# Antipadrão Ice Cream Cone

A arquitetura existente apresenta características do antipadrão conhecido como **Ice Cream Cone**.

Nesse modelo, grande parte da validação está concentrada nas camadas mais caras e lentas.

```text
        TESTES MANUAIS
       ███████████████

           E2E / UI
        █████████████

            API
          █████

        INTEGRAÇÃO
          ███

         UNITÁRIOS
           ██
```

A proposta busca inverter essa distribuição.

```text
           E2E / UI
              ▲
             ███

       API / CONTRATO
           ██████

         INTEGRAÇÃO
        █████████

          UNITÁRIOS
     ███████████████
```

O objetivo não é eliminar testes de interface.

O objetivo é utilizar a camada de interface somente quando ela realmente for necessária para demonstrar o comportamento esperado.

# Princípio arquitetural principal

A arquitetura segue o princípio:

> Testar cada comportamento na camada mais baixa capaz de fornecer confiança suficiente.

Isso evita executar o mesmo cenário de forma desnecessária em várias camadas.

```text
Regra isolada
      ↓
Unitário

Comunicação interna
      ↓
Integração

Interface entre serviços
      ↓
Contrato

Regra exposta por serviço
      ↓
API

Jornada completa do usuário
      ↓
E2E

Percepção humana
      ↓
Manual / Exploratório
```

# Estratégia baseada em risco

A priorização dos testes considera impactos relacionados a:

| Dimensão | Exemplo |
|---|---|
| Financeiro | Pagamentos e preços |
| Operacional | Criação e processamento de pedidos |
| Integridade | Estoque e estados dos pedidos |
| Segurança | Autenticação e autorização |
| Privacidade | Isolamento das informações |
| Disponibilidade | Serviços e integrações |
| Experiência | Fluxos críticos da aplicação |
| Compliance | Auditoria e rastreabilidade |
| Integrações externas | Pagamento, antifraude e logística |

O fluxo de rastreabilidade esperado é:

```text
Problema
    ↓
Risco
    ↓
Regra de negócio
    ↓
Camada de teste
    ↓
Automação
    ↓
Pipeline
    ↓
Quality Gate
```

# Arquitetura de testes proposta

## Testes unitários

Os testes unitários devem concentrar regras determinísticas e isoláveis.

Exemplos:

- Preço.
- Estoque.
- Cancelamento.
- Frete.
- Permissões.
- Estados do pedido.
- Idempotência.
- Regras de prioridade.
- Validações antifraude que possam ser isoladas.

O objetivo é detectar problemas rapidamente e com baixo custo de execução.

## Testes de integração

São utilizados quando o comportamento depende da comunicação real entre componentes internos.

Integrações prioritárias:

```text
Order + Payment

Order + Stock

Order + Logistics

Order + Notification

Quotation + Order

Catalog + Stock

Auth + serviços protegidos
```

Essa camada deve verificar se componentes que funcionam individualmente continuam funcionando quando utilizados em conjunto.

# Testes de contrato

Contract Testing deve proteger os contratos existentes entre serviços.

Serviços considerados especialmente importantes:

```text
Order Service
Payment Service
Stock Service
Logistics Service
Auth Service
Supplier Service
Notification Service
```

A finalidade é detectar incompatibilidades antes que elas apareçam em um fluxo completo E2E.

Exemplo:

```text
Order Service
      ↓
espera determinado contrato
      ↓
Payment Service
      ↓
altera resposta
      ↓
Contract Test falha
      ↓
Incompatibilidade detectada antes da release
```

# Testes de API

As APIs devem concentrar grande parte das validações funcionais quando a interface gráfica não for necessária para comprovar a regra.

Devem ser avaliados aspectos como:

- Autenticação.
- Autorização.
- Status HTTP.
- Schema.
- Validação.
- Regras de negócio.
- Tratamento de erros.
- Idempotência.
- Timeout.
- Concorrência quando aplicável.
- Permissões.
- Isolamento de dados.

# Testes E2E e UI

Os testes E2E devem ser utilizados em quantidade reduzida.

A prioridade é validar jornadas essenciais.

Exemplo:

```text
Hospital cria pedido
        ↓
Pagamento aprovado
        ↓
Estoque reservado
        ↓
Pedido confirmado
        ↓
Fornecedor autorizado visualiza pedido
        ↓
Pedido segue para logística
        ↓
Usuário recebe confirmação
```

Não é necessário reproduzir na interface todas as combinações já validadas por testes unitários, de integração ou API.

# Testes manuais

Alguns testes devem continuar manuais quando dependem principalmente de julgamento humano.

Entre eles:

- Testes exploratórios.
- Avaliação de usabilidade.
- Validação visual.
- Clareza das mensagens.
- Exploração de comportamentos inesperados.
- Acessibilidade exploratória.
- Avaliações contextuais da experiência.

# gTAA

A proposta também considera a **Generic Test Automation Architecture, gTAA**.

| Camada | Aplicação |
|---|---|
| Test Generation | Definição e geração dos cenários e dados |
| Test Definition | Organização dos casos, regras e comportamento esperado |
| Test Execution | Execução automatizada nos diferentes ambientes |
| Test Adaptation | Adaptação da automação às tecnologias e serviços da aplicação |

A aplicação da gTAA busca evitar que cada automação seja desenvolvida de forma isolada.

```text
Geração
   ↓
Definição
   ↓
Execução
   ↓
Adaptação
   ↓
Arquitetura sustentável
```

# Arquitetura da suíte

Uma organização de referência para a suíte é:

```text
tests/
│
├── unit/
│
├── integration/
│
├── contract/
│
├── api/
│
├── e2e/
│
├── fixtures/
│
├── mocks/
│
├── support/
│   └── helpers/
│
├── config/
│
├── reports/
│
└── evidence/
```

## Responsabilidade das pastas

| Diretório | Responsabilidade |
|---|---|
| `unit/` | Regras isoladas |
| `integration/` | Comunicação entre componentes |
| `contract/` | Contratos entre serviços |
| `api/` | Comportamentos expostos pelas APIs |
| `e2e/` | Jornadas críticas |
| `fixtures/` | Dados reutilizáveis |
| `mocks/` | Simulação de dependências |
| `support/` | Código compartilhado |
| `config/` | Configuração por ambiente |
| `reports/` | Relatórios de execução |
| `evidence/` | Evidências dos testes |

Essa divisão facilita manutenção, execução seletiva e integração com CI/CD.

# Testabilidade

A arquitetura também propõe aumentar a capacidade do sistema de ser testado.

Entre os mecanismos considerados estão:

```text
Mocks
Stubs
Service Virtualization
Sandboxes
Feature Flags
Dependency Injection
Logs estruturados
Correlation IDs
Observabilidade
Health Checks
Contratos de API
Seed de banco
Data Builders
Reset de estado
Controle de clock
Simulação de timeout
Simulação de erros externos
```

## Exemplo

Uma integração externa indisponível não precisa impedir todos os testes.

```text
Sistema
   ↓
Integração externa
   ↓
WireMock / Stub
   ↓
Resposta controlada
   ↓
Cenário reproduzível
```

# Estratégia de massa de dados

A criação dos dados deve evitar dependência de preparação manual.

A estratégia considera:

- Fixtures.
- Builders.
- Factories.
- Seeds.
- Dados sintéticos.
- Dados determinísticos.
- Dados descartáveis.
- Isolamento por execução.

Exemplo:

```text
Execução inicia
      ↓
Massa criada automaticamente
      ↓
Teste executado
      ↓
Resultado registrado
      ↓
Dados descartados ou restaurados
```

Essa abordagem melhora:

- Repetibilidade.
- Isolamento.
- Manutenção.
- Confiabilidade.
- Execução em pipeline.

Dados pessoais reais não devem ser utilizados quando não forem necessários.

# Estratégia de ambientes

A arquitetura considera diferentes ambientes para diferentes tipos de teste.

| Ambiente | Finalidade |
|---|---|
| Local | Desenvolvimento e testes rápidos |
| CI | Execuções automatizadas |
| Staging / Homologação | Validação integrada e E2E |
| Sandbox | Simulação ou validação de integrações externas |
| Ambiente efêmero | Validação isolada de Pull Requests quando aplicável |

Nem todos os testes precisam depender da homologação.

```text
Unitários
Integração controlada
Contratos
API isolada
        ↓
Podem executar antes de staging
```

Enquanto:

```text
Integração completa
E2E
Smoke de release
        ↓
Podem exigir staging
```

Isso reduz a dependência de um único ambiente compartilhado.

# Arquitetura em CI/CD

A execução deve fornecer feedback progressivamente mais amplo.

```text
Commit
   ↓
Build
   ↓
Lint
   ↓
Testes unitários
   ↓
Análise estática
   ↓
Pull Request
   ↓
Unitários
   ↓
Integração
   ↓
Contrato
   ↓
Segurança
   ↓
Deploy em Staging
   ↓
API crítica
   ↓
E2E Smoke
   ↓
Regressão seletiva
   ↓
Relatórios
   ↓
Quality Gates
   ↓
Decisão de Release
```

O objetivo é encontrar os problemas mais simples e baratos primeiro.

```text
Feedback rápido
      ↓
Commit / PR

Feedback mais amplo
      ↓
Integração

Confiança de release
      ↓
Staging / E2E
```

A regressão completa não precisa ser executada em todos os commits.

# Organização das suítes no pipeline

As execuções podem ser organizadas por tags.

```text
smoke
critical
regression
contract
integration
security
e2e
```

Isso possibilita escolher o conjunto adequado conforme o estágio do pipeline.

# Quality Gates

A arquitetura prevê critérios objetivos para impedir avanço quando condições
essenciais de qualidade não forem atendidas.

Os gates podem considerar:

| Área | O que avaliar |
|---|---|
| Unitários críticos | Regras críticas funcionando |
| Integração | Comunicação entre serviços |
| Contratos | Compatibilidade entre consumidores e provedores |
| API | Fluxos e regras críticas |
| E2E Smoke | Jornadas essenciais |
| Defeitos | Ausência de falhas críticas sem tratamento |
| Segurança | Problemas relevantes identificados |
| Flakiness | Confiabilidade da automação |
| Regras críticas | Cobertura dos comportamentos mais importantes |
| Análise estática | Qualidade do código |
| Pipeline | Tempo e estabilidade da execução |
| Release | Evidências suficientes para decisão |

Metas numéricas específicas devem ser tratadas como metas arquiteturais
propostas, e não como valores arbitrários.

# Métricas

A arquitetura também considera métricas capazes de apoiar decisões reais.

Entre as métricas relevantes estão:

```text
Taxa de aprovação
Tempo de execução
Flakiness
Defeitos por severidade
Defeitos escapados para produção
Defeitos por serviço
Mean Time to Detect
Mean Time to Repair da automação
Tempo médio de feedback
Cobertura de regras críticas
Cobertura de contratos
Tempo de regressão
Falhas de ambiente
Falhas de massa de dados
Testes em quarentena
```

O objetivo das métricas não é apenas gerar dashboards.

```text
Métrica
   ↓
Informação
   ↓
Análise
   ↓
Decisão
```

# Classificação das falhas

Uma execução com falha não significa automaticamente que existe um defeito
na aplicação.

A arquitetura deve distinguir:

```text
Falha funcional

Falha do teste

Falha de ambiente

Falha da massa de dados

Falha de integração externa
```

Isso reduz falsos positivos e melhora a investigação.

# Ferramentas consideradas

A atividade considera uma stack de ferramentas compatível com diferentes
camadas.

Entre as tecnologias avaliadas estão:

| Necessidade | Ferramentas candidatas |
|---|---|
| Unitários backend | JUnit 5, Mockito |
| Integração | Testcontainers |
| Unitários frontend | Jest ou Vitest, React Testing Library |
| API | RestAssured, Karate ou Postman/Newman |
| Contrato | Pact |
| Simulação | WireMock |
| E2E | Playwright |
| Performance | k6 |
| Segurança básica | OWASP ZAP |
| Qualidade de código | SonarQube |
| Relatórios | Allure e JUnit XML |
| Gestão de testes | Xray ou Zephyr |
| Pipeline | GitHub Actions, GitLab CI ou Jenkins |

Essas ferramentas representam opções arquiteturais.

A seleção final deve priorizar uma stack enxuta e sustentável, evitando
ferramentas redundantes com a mesma finalidade.

# Plano de migração

A mudança da arquitetura de testes não deve ocorrer de uma única vez.

A proposta trabalha com quatro fases de evolução.

```text
FASE 1
Diagnóstico e fundação
        ↓
FASE 2
Testes das camadas inferiores
        ↓
FASE 3
Integração com CI/CD
        ↓
FASE 4
Evolução e otimização
```

A restrição de **30 dias** deve ser interpretada como período para estruturação
e início da nova abordagem, e não como prazo para reconstruir toda a
arquitetura de qualidade.

## Fase 1, Fundação

Prioridades:

- Organizar a suíte.
- Definir convenções.
- Identificar fluxos críticos.
- Criar estratégia de dados.
- Estabelecer execução básica no pipeline.

## Fase 2, Shift Left

Prioridades:

- Aumentar testes unitários.
- Implementar integrações críticas.
- Criar testes de contrato.
- Migrar validações da interface para API.

## Fase 3, Pipeline

Prioridades:

- Criar execução progressiva.
- Implementar relatórios.
- Adicionar Quality Gates.
- Automatizar smoke tests.

## Fase 4, Evolução

Prioridades:

- Reduzir flakiness.
- Melhorar métricas.
- Ampliar testabilidade.
- Evoluir observabilidade.
- Revisar cobertura e riscos residuais.

# Testes que permanecem manuais

A arquitetura não propõe automatizar tudo.

Algumas atividades continuam tendo maior valor quando executadas por pessoas.

Exemplos:

```text
Testes exploratórios

Avaliação de UX

Validação visual

Clareza das mensagens

Exploração de comportamentos inesperados

Acessibilidade exploratória

Avaliação contextual
```

A automação deve ser utilizada onde oferece repetibilidade, velocidade e
confiança.

# Riscos da própria arquitetura

Mesmo uma arquitetura de testes bem estruturada possui riscos.

Entre os principais estão:

- Excesso de automação sem manutenção.
- Testes instáveis.
- Dados não isolados.
- Dependência excessiva de staging.
- Ambientes compartilhados.
- Simulações que não representam corretamente serviços reais.
- Contratos desatualizados.
- Pipeline excessivamente lento.
- Métricas sem uso prático.
- Testes duplicados em várias camadas.
- Falta de conhecimento da equipe.
- Crescimento descontrolado da suíte.

Esses riscos precisam ser monitorados durante a evolução da estratégia.

# Rastreabilidade arquitetural

Um dos pontos centrais da atividade é estabelecer relações entre problemas,
riscos e controles de qualidade.

Exemplo conceitual:

```text
Problema
   ↓
Risco financeiro
   ↓
Regra crítica
   ↓
Integração + API + Contrato
   ↓
Pipeline
   ↓
Quality Gate
```

Outro exemplo:

```text
Falha de autorização
        ↓
Risco de segurança
        ↓
Unitário + Integração + API
        ↓
E2E mínimo
        ↓
Gate de segurança
```

Essa rastreabilidade ajuda a justificar por que cada teste existe.

# Principais aprendizados

A atividade demonstrou que **arquitetura de testes não significa apenas
escolher uma ferramenta de automação**.

Uma estratégia sustentável precisa considerar:

```text
Riscos
   ↓
Camadas
   ↓
Testabilidade
   ↓
Dados
   ↓
Ambientes
   ↓
Automação
   ↓
Pipeline
   ↓
Quality Gates
   ↓
Métricas
   ↓
Evolução contínua
```

Também foi possível compreender que uma grande quantidade de testes E2E não
representa necessariamente maior qualidade.

Uma suíte menor, distribuída corretamente entre as camadas, pode produzir
feedback mais rápido e confiável.

Outro aprendizado importante foi o conceito de **Shift Left**, trazendo
validações para etapas anteriores do desenvolvimento.

```text
Defeito encontrado na interface
            ↓
Muito tarde

Defeito encontrado no unitário
            ↓
Feedback rápido
```

# Competências desenvolvidas

A atividade contribuiu para desenvolver competências relacionadas a:

- Arquitetura de testes.
- Quality Engineering.
- Risk Based Testing.
- Pirâmide de testes.
- Shift Left Testing.
- gTAA.
- Testes unitários.
- Testes de integração.
- Contract Testing.
- Testes de API.
- Automação E2E.
- Testes exploratórios.
- Gestão de massa de dados.
- Testabilidade.
- CI/CD.
- Quality Gates.
- Métricas.
- Observabilidade.
- Planejamento de migração.
- Rastreabilidade técnica.

# Relação com o Projeto Integrador

Os princípios desta atividade podem ser aplicados diretamente ao
**ConectaStart**.

Em vez de construir a estratégia de qualidade do ConectaStart apenas com
testes de interface, seria possível distribuir os testes por camada.

```text
ConectaStart
     │
     ├── Unitários
     │     └── regras de estágio e matchmaking
     │
     ├── Integração
     │     └── serviços + banco de dados
     │
     ├── API
     │     └── cadastro, perfis e oportunidades
     │
     ├── Contrato
     │     └── comunicação entre serviços
     │
     ├── E2E
     │     └── jornadas críticas
     │
     └── Manual
           └── UX e exploração
```

Exemplo para matchmaking:

```text
Regra de compatibilidade
        ↓
Teste unitário

Startup + Mentor + Persistência
        ↓
Teste de integração

Endpoint de matchmaking
        ↓
Teste de API

Usuário solicita e visualiza um match
        ↓
E2E mínimo
```

Esse modelo evita uma futura pirâmide invertida de testes no Projeto
Integrador.

[Acessar Projeto Integrador](../../../projeto-integrador/)

# Organização dos arquivos

Sugestão para o repositório:

```text
medsupply/
│
├── README.md
│
└── Proposta - Arquitetura de teste MedSupply.odt
```

Caso os diagramas, evidências ou outros artefatos sejam separados do documento:

```text
medsupply/
│
├── README.md
├── Proposta - Arquitetura de teste MedSupply.odt
│
├── diagramas/
├── arquitetura/
├── evidencias/
└── referencias/
```

# Documento original

O documento principal da atividade é:

```text
Proposta - Arquitetura de teste MedSupply.odt
```

# Navegação

[Voltar para Validação e Qualidade de Software](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)

