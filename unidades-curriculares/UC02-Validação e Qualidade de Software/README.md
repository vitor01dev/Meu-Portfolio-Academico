# UC02, Validação e Qualidade de Software

[Voltar ao Portfólio Acadêmico](../../README.md)

## Metadados

| Campo | Informação |
|---|---|
| Unidade Curricular | Validação e Qualidade de Software |
| Curso | Análise e Desenvolvimento de Sistemas |
| Instituição | Faculdade Senac Pernambuco |
| Período | 5º período |
| Semestre | 2026.2 |
| Área | Engenharia e Qualidade de Software |
| Status | Em andamento |

## Sobre a Unidade Curricular

A Unidade Curricular de **Validação e Qualidade de Software** reúne atividades relacionadas à avaliação da qualidade de sistemas, definição de estratégias de teste, elaboração de casos de teste, identificação de riscos, produção de evidências e análise de critérios para liberação de software.

Os trabalhos desenvolvidos durante a UC permitem aplicar conceitos de qualidade em diferentes sistemas e cenários, desde atividades de verificação e validação até propostas de arquitetura de testes e avaliações de release.

## Objetivos da UC

As atividades desta Unidade Curricular contribuem para o desenvolvimento de competências relacionadas a:

- Verificação e validação de software.
- Planejamento e execução de testes.
- Definição de critérios de aceitação.
- Criação de casos e cenários de teste.
- Priorização baseada em risco.
- Registro e análise de defeitos.
- Produção de evidências.
- Avaliação de qualidade de releases.
- Arquitetura de testes.
- Testes manuais e automatizados.
- Documentação de processos de qualidade.
- Tomada de decisão sobre liberação de software.

# Organização da UC

Os conteúdos estão organizados por atividade ou sistema analisado.

```text
uc02-validacao-e-qualidade-de-software/
│
├── README.md
│
├── atividade-01-verificacao-validacao/
│
├── pulsetickets/
│
├── saucedemo/
│
├── parabank/
│
├── medsupply/
│
└── atividade-08-validacao-verificacao/
```

Essa organização evita que relatórios, evidências e documentos de sistemas diferentes sejam armazenados no mesmo diretório.

# Atividades e projetos

## 1. Atividade 01, Verificação e Validação

Atividade introdutória relacionada aos conceitos e práticas de verificação e validação de software.

### Arquivo associado

```text
Atividade 01 - Verificação e Validação.md
```

[Acessar atividade](./atividade-01-verificacao-validacao/)

---

## 2. PulseTickets, QA Release Assessment

Atividade de avaliação de qualidade de uma plataforma de venda e gerenciamento de ingressos digitais.

O trabalho envolve análise de riscos, priorização de testes e definição dos cenários considerados mais importantes diante de limitações de tempo e recursos.

### Arquivo associado

```text
Relatório QA - Pulse Tickets.docx
```

[Acessar atividade](./pulsetickets/)

---

## 3. SauceDemo, Casos de Teste e Critérios de Aceitação

Atividade de avaliação de uma aplicação de comércio eletrônico, envolvendo execução de testes, registro de comportamentos observados e produção de evidências.

### Conteúdos relacionados

```text
Relatório - Casos de Testes e Critérios de Aceitação.docx

Evidência_campos_vazios.jpg
Evidencia_Tecla_Enter_RollBack.jpg
Evidencia_Tela_checkout.jpg
Evidencia_Tela_Compra_Finalizada.jpg
Evidência_TimeOut.jpg
```

As evidências são mantidas junto ao contexto da atividade para preservar a relação entre o comportamento observado e sua documentação.

### Estrutura

```text
saucedemo/
│
├── README.md
├── relatorio/
└── evidencias/
```

[Acessar atividade](./saucedemo/)

---

## 4. ParaBank, Dossiê de Qualidade

Atividade relacionada à análise e documentação de testes realizados sobre o sistema ParaBank.

### Arquivo associado

```text
Dossie - ParaBank.odt
```

[Acessar atividade](./parabank/)

---

## 5. MedSupply, Arquitetura de Testes

Atividade voltada à definição de uma arquitetura de testes para o sistema MedSupply.

O trabalho busca estruturar como diferentes camadas do sistema devem ser testadas, considerando aspectos como testes manuais, automação, ferramentas, pipeline, dados e riscos.

### Arquivo associado

```text
Proposta - Arquitetura de teste MedSupply.odt
```

[Acessar atividade](./medsupply/)

---

## 6. Atividade 08, Validação e Verificação

Atividade complementar relacionada aos conteúdos de validação e verificação de software.

### Arquivo associado

```text
Atividade 08 - Validação e Verificação - ORIENTAÇÕES.txt
```

[Acessar atividade](./atividade-08-validacao-verificacao/)

# Classificação dos conteúdos

Os materiais desta UC podem ser classificados por tipo.

## Relatórios

```text
Relatório QA - Pulse Tickets.docx

Relatório - Casos de Testes e Critérios de Aceitação.docx
```

## Dossiês

```text
Dossie - ParaBank.odt
```

## Propostas de arquitetura

```text
Proposta - Arquitetura de teste MedSupply.odt
```

## Atividades acadêmicas

```text
Atividade 01 - Verificação e Validação.md

Atividade 08 - Validação e Verificação - ORIENTAÇÕES.txt
```

## Evidências

```text
Evidência_campos_vazios.jpg

Evidencia_Tecla_Enter_RollBack.jpg

Evidencia_Tela_checkout.jpg

Evidencia_Tela_Compra_Finalizada.jpg

Evidência_TimeOut.jpg
```

# Taxonomia da UC

Os conteúdos seguem a seguinte estrutura hierárquica:

```text
Validação e Qualidade de Software
        │
        ├── Atividade
        │       │
        │       ├── README
        │       ├── Relatório
        │       ├── Evidências
        │       └── Documentos auxiliares
        │
        └── Projeto ou sistema analisado
                │
                ├── Planejamento
                ├── Testes
                ├── Resultados
                └── Evidências
```

# Tipos de teste e competências trabalhadas

As atividades da UC envolvem diferentes perspectivas de qualidade.

| Área | Aplicação |
|---|---|
| Verificação | Análise de artefatos e requisitos |
| Validação | Verificação do comportamento do sistema |
| Testes funcionais | Avaliação das funcionalidades esperadas |
| Testes negativos | Verificação de entradas ou comportamentos inválidos |
| Testes de usabilidade | Avaliação da interação com o sistema |
| Testes exploratórios | Investigação de comportamentos além do caminho principal |
| Testes automatizados | Automatização de cenários repetíveis |
| Análise de risco | Priorização de testes conforme impacto e probabilidade |
| Critérios de aceitação | Definição de condições para considerar uma funcionalidade válida |
| Quality Gate | Apoio à decisão sobre liberação de uma versão |
| Arquitetura de testes | Organização das camadas, ferramentas e estratégias de teste |

# Evidências de qualidade

Um dos princípios utilizados nesta UC é manter a relação entre uma constatação e sua evidência.

Exemplo:

```text
Comportamento observado
        ↓
Caso de teste
        ↓
Resultado
        ↓
Evidência
        ↓
Análise
        ↓
Decisão de qualidade
```

Essa organização permite que um problema identificado não seja documentado apenas como uma descrição textual.

Sempre que possível, ele é relacionado a:

- Cenário executado.
- Resultado esperado.
- Resultado observado.
- Evidência.
- Impacto.
- Severidade ou prioridade.
- Recomendação.

# Relações entre os conteúdos

As atividades trabalham competências complementares.

```text
Verificação e Validação
        │
        ▼
Casos de Teste
        │
        ▼
Execução
        │
        ▼
Evidências
        │
        ▼
Análise de Risco
        │
        ▼
Quality Gate
```

A arquitetura de testes amplia essa visão ao definir onde e como os testes devem ser executados:

```text
Requisitos
    ↓
Testes unitários
    ↓
Testes de integração
    ↓
Testes de API
    ↓
Testes de interface
    ↓
Testes end-to-end
    ↓
Pipeline
    ↓
Quality Gate
```

# Relação com o Projeto Integrador

Os conhecimentos desenvolvidos nesta UC podem ser aplicados ao **ConectaStart** durante o planejamento e validação da qualidade do produto.

Entre as aplicações possíveis estão:

- Validação dos requisitos.
- Criação de critérios de aceitação.
- Planejamento de casos de teste.
- Testes do cadastro de startups.
- Testes do cadastro de mentores.
- Testes das regras de matchmaking.
- Validação de permissões e perfis de acesso.
- Testes das APIs.
- Testes da interface.
- Testes de integração.
- Registro de defeitos.
- Produção de evidências.
- Definição de critérios para liberação.

```text
ConectaStart
     │
     ├── Requisitos
     │       ↓
     │   Critérios de aceitação
     │
     ├── Desenvolvimento
     │       ↓
     │      Testes
     │
     ├── Matchmaking
     │       ↓
     │   Validação das regras
     │
     └── Release
             ↓
         Quality Gate
```

[Acessar Projeto Integrador](../../projeto-integrador/)

# Competências desenvolvidas

Ao longo das atividades desta Unidade Curricular são desenvolvidas competências como:

- Pensamento crítico aplicado à qualidade de software.
- Identificação e análise de riscos.
- Priorização de testes.
- Escrita de cenários.
- Definição de critérios de aceitação.
- Documentação de resultados.
- Registro de evidências.
- Análise de defeitos.
- Avaliação de releases.
- Estruturação de estratégias de teste.
- Planejamento de automação.
- Comunicação de riscos para tomada de decisão.

# Navegação

[Voltar ao Portfólio Acadêmico](../../README.md)

[Consultar Índice Geral](../../INDEX.md)

[Acessar Projeto Integrador](../../projeto-integrador/)

---

# Próximo passo

Para documentarmos a UC02 no mesmo nível de detalhe da UC01, vamos construir cada atividade individualmente.

Sugestão de sequência:

1. **Atividade 01, Verificação e Validação**
2. **PulseTickets**
3. **SauceDemo**
4. **ParaBank**
5. **MedSupply**
6. **Atividade 08**
