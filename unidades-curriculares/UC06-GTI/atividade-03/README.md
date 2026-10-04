# O Modelo Amazon de Governança e Execução em TI

[Voltar para Governança em Tecnologia da Informação](../README.md)

## Metadados

| Campo | Informação |
|---|---|
| Unidade Curricular | Governança em Tecnologia da Informação |
| Curso | Análise e Desenvolvimento de Sistemas |
| Instituição | Faculdade Senac Pernambuco |
| Período | 5º período |
| Semestre | 2026.2 |
| Tipo | Pesquisa e apresentação |
| Tema | Governança e execução em Tecnologia da Informação |
| Empresa analisada | Amazon |
| Abordagem | Governança, eficácia operacional e estratégica, melhoria contínua e planejamento de TI |
| Documento principal | GTI_Modelo_Amazon.pptx 1.pdf |
| Status | Concluído |

## Equipe

- Alisson Gustavo
- Allyson George
- Vitor Vieira
- Hericc Rocha

## Objetivo da atividade

A atividade teve como objetivo analisar o modelo de **Governança e Execução em Tecnologia da Informação da Amazon**, observando como mecanismos organizacionais, métricas, processos de revisão, autonomia das equipes e planejamento estratégico podem ser utilizados para conciliar controle e velocidade.

O estudo foi estruturado principalmente em torno de:

- Governança por mecanismos.
- Cultura Day 1.
- Guardrails corporativos.
- Líderes de thread único.
- Dimensões de governança.
- Eficácia operacional.
- Eficácia estratégica.
- Melhoria contínua.
- Working Backwards.
- Planejamento OP1 e OP2.
- Estrutura de equipes.
- Métricas e revisões.
- Relação com frameworks de Governança de TI.

O modelo apresentado pode ser sintetizado da seguinte forma:

```text
Estratégia
    ↓
Mecanismos
    ↓
Equipes autônomas
    ↓
Métricas
    ↓
Revisões
    ↓
Execução
    ↓
Aprendizado
    ↓
Melhoria contínua
```

# 1. Visão geral do modelo

A apresentação organiza a Governança de TI da Amazon em quatro elementos principais.

```text
1. Governança por mecanismos
           ↓
2. Dimensões estruturadas
           ↓
3. Eficácia operacional
           ↓
4. Planejamento estratégico formalizado
```

## Governança por mecanismos

O trabalho apresenta a ideia de substituir declarações de intenção por mecanismos formais, repetíveis e verificáveis.

## Dimensões estruturadas

O AWS Cloud Adoption Framework é utilizado como referência para organizar diferentes capacidades relacionadas à governança.

## Eficácia operacional

O AWS Well-Architected Framework é relacionado à execução e evolução consistente das cargas de trabalho.

## Planejamento estratégico

O processo Working Backwards e o ciclo OP1 e OP2 aparecem como mecanismos para conectar estratégia, metas, métricas e investimentos.

# 2. Cultura Day 1

A apresentação relaciona o modelo de governança à cultura denominada **Day 1**.

Um dos princípios destacados no material é:

> "Boas intenções não funcionam, é preciso ter bons mecanismos para fazer as coisas acontecerem."

A ideia apresentada é que a organização não deve depender exclusivamente da boa vontade das pessoas para que determinados comportamentos ocorram.

Em vez disso, são utilizados:

```text
Processos
   +
Ferramentas
   +
Métricas
   +
Auditorias
   +
Revisões
```

para criar comportamentos consistentes em escala.

## Aplicação à Governança de TI

O trabalho sintetiza essa abordagem em quatro pontos.

```text
Governança expressa em processos repetíveis
                    ↓
Métricas e revisões recorrentes
                    ↓
Equipes pequenas e autônomas
                    ↓
Guardrails corporativos
```

Estratégia, operação e melhoria contínua passam a compartilhar mecanismos de acompanhamento.

# 3. Governança por mecanismos

A governança apresentada não depende de aprovações para cada pequena decisão.

O modelo procura criar condições para que equipes possuam autonomia dentro de limites previamente estabelecidos.

A relação pode ser representada por:

```text
Autonomia
    +
Padrões
    +
Métricas
    +
Revisões
    ↓
Governança
```

A atividade destaca três mecanismos principais.

1. Guardrails.
2. Líderes de thread único.
3. Inspeção recorrente.

# 4. Guardrails, não pedágios

O trabalho utiliza a comparação entre:

```text
GUARDRAILS
Limites que permitem velocidade
```

e:

```text
PEDÁGIOS
Aprovações que interrompem o fluxo
```

A proposta é permitir que equipes tomem decisões dentro de parâmetros organizacionais definidos.

```text
Equipe
   ↓
Autonomia
   ↓
Guardrails
   ↓
Execução
```

Em vez de:

```text
Equipe
   ↓
Decisão
   ↓
Aprovação
   ↓
Outra aprovação
   ↓
Execução
```

O objetivo é preservar controle sem bloquear desnecessariamente a velocidade.

# 5. Líder de thread único

Outro mecanismo analisado é o **Single-Threaded Leader**.

A apresentação descreve esse papel como um líder dedicado integralmente a determinada iniciativa.

```text
Iniciativa
    ↓
Líder dedicado
    ↓
Responsabilidade clara
    ↓
Execução
    ↓
Resultado
```

O líder não divide sua atenção entre diversas frentes.

Sua responsabilidade está concentrada no resultado da iniciativa.

# 6. Inspeção recorrente

A governança também ocorre por meio de revisões estruturadas.

O modelo procura substituir verificações pontuais por acompanhamento recorrente.

```text
Métrica
   ↓
Revisão
   ↓
Comparação
   ↓
Desvio
   ↓
Ação
```

A liderança utiliza essas revisões para acompanhar:

- Velocidade.
- Agilidade.
- Resultados.
- Métricas.
- Foco no cliente.

# 7. Dimensões de Governança

O estudo apresenta sete dimensões relacionadas ao AWS Cloud Adoption Framework.

| Nº | Dimensão | Finalidade |
|---:|---|---|
| 1 | Gestão de programas e projetos | Coordenar iniciativas de nuvem interdependentes |
| 2 | Gestão de benefícios | Garantir realização e sustentação dos benefícios |
| 3 | Gestão de riscos | Identificar e quantificar riscos tecnológicos e de negócio |
| 4 | Gestão financeira de TI e nuvem | Planejar, medir e otimizar gastos tecnológicos |
| 5 | Gestão do portfólio de aplicações | Manter inventário para racionalização e modernização |
| 6 | Governança de dados | Definir papéis, padrões e políticas |
| 7 | Curadoria de dados | Organizar metadados e catálogos |

# 8. Gestão de programas e projetos

Essa dimensão busca coordenar diferentes iniciativas tecnológicas.

```text
Projeto A
   +
Projeto B
   +
Projeto C
   ↓
Coordenação
   ↓
Portfólio
```

O objetivo é permitir que iniciativas relacionadas evoluam de forma coordenada.

# 9. Gestão de benefícios

A tecnologia não deve ser avaliada apenas pela conclusão de projetos.

É necessário observar se os benefícios esperados realmente foram produzidos.

```text
Investimento
    ↓
Projeto
    ↓
Entrega
    ↓
Benefício
    ↓
Resultado de negócio
```

# 10. Gestão de riscos

Essa dimensão busca identificar e quantificar riscos associados à tecnologia.

Entre eles podem estar riscos:

- Operacionais.
- Tecnológicos.
- Financeiros.
- Relacionados ao negócio.

O princípio apresentado é:

```text
Risco identificado
      ↓
Avaliação
      ↓
Controle
      ↓
Monitoramento
```

# 11. Gestão financeira de TI e nuvem

A governança também envolve controle financeiro dos recursos tecnológicos.

O objetivo é:

```text
Planejar
   ↓
Medir
   ↓
Analisar
   ↓
Otimizar
```

os gastos com tecnologia e nuvem.

# 12. Gestão do portfólio de aplicações

Essa dimensão busca manter informações confiáveis sobre as aplicações existentes.

```text
Aplicações
    ↓
Inventário
    ↓
Avaliação
    ↓
Racionalização
    ↓
Modernização
```

O inventário ajuda a identificar sistemas que:

- Precisam evoluir.
- Podem ser modernizados.
- Podem ser substituídos.
- Podem ser descontinuados.

# 13. Governança de dados

A Governança de Dados define:

- Papéis.
- Padrões.
- Políticas.
- Responsabilidades.
- Ciclo de vida.

O fluxo pode ser representado por:

```text
Dados
  ↓
Políticas
  ↓
Papéis
  ↓
Responsabilidade
  ↓
Uso controlado
```

# 14. Curadoria de dados

A curadoria complementa a Governança de Dados ao trabalhar elementos como:

- Metadados.
- Catálogos.
- Organização.
- Descoberta.

```text
Dados
  ↓
Metadados
  ↓
Catálogo
  ↓
Encontrabilidade
  ↓
Uso
```

Essa dimensão também possui relação com conceitos estudados em Gestão da Informação.

# 15. Eficácia operacional

O trabalho apresenta oito princípios associados à eficácia operacional.

```text
1. Organizar equipes em torno de resultados de negócio

2. Implementar observabilidade para decisões acionáveis

3. Automatizar com segurança sempre que possível

4. Fazer mudanças frequentes, pequenas e reversíveis

5. Refinar procedimentos operacionais regularmente

6. Antecipar falhas antes que ocorram

7. Aprender com eventos operacionais

8. Utilizar serviços gerenciados para reduzir carga operacional
```

# 16. Resultados de negócio

A organização das equipes deve ocorrer em torno dos resultados esperados, e não somente de componentes técnicos.

```text
Tecnologia
    ↓
Resultado de negócio
```

Isso aproxima a execução da estratégia.

# 17. Observabilidade

A observabilidade aparece como mecanismo para apoiar decisões.

```text
Sistema
   ↓
Métricas
   ↓
Logs e sinais
   ↓
Análise
   ↓
Decisão
```

O objetivo não é apenas coletar informações, mas produzir dados acionáveis.

# 18. Automação

A atividade apresenta automação como instrumento para reduzir esforço operacional e aumentar consistência.

```text
Processo repetitivo
      ↓
Automação
      ↓
Padronização
      ↓
Menor carga operacional
```

A automação deve ocorrer de forma segura.

# 19. Mudanças pequenas e reversíveis

Outro princípio é realizar alterações frequentes, pequenas e, sempre que possível, reversíveis.

```text
Mudança pequena
      ↓
Menor impacto
      ↓
Mais facilidade para avaliar
      ↓
Mais facilidade para reverter
```

Esse modelo reduz o risco de mudanças extensas realizadas de uma única vez.

# 20. Antecipação de falhas

A eficácia operacional também envolve pensar sobre possíveis problemas antes que eles ocorram.

```text
Risco
  ↓
Antecipação
  ↓
Preparação
  ↓
Resposta
```

# 21. Aprendizado com eventos operacionais

Falhas e eventos não devem ser tratados apenas como problemas que precisam desaparecer.

Eles também podem gerar aprendizado.

```text
Evento
  ↓
Investigação
  ↓
Aprendizado
  ↓
Mudança
  ↓
Prevenção
```

# 22. Eficácia estratégica

A apresentação estrutura a eficácia estratégica em três mecanismos principais.

1. S-team Goals.
2. Revisões WBR, MBR e QBR.
3. Autonomia com prestação de contas.

# 23. S-team Goals

A liderança sênior seleciona metas anuais e acompanha sua evolução.

A apresentação destaca principalmente métricas de entrada.

```text
Meta anual
    ↓
Métrica
    ↓
Acompanhamento
    ↓
Resultado
```

O acompanhamento ocorre mensal e trimestralmente.

# 24. Revisões de negócio

O modelo inclui diferentes ciclos de revisão.

```text
WBR
Weekly Business Review

MBR
Monthly Business Review

QBR
Quarterly Business Review
```

Cada revisão atua em uma escala temporal diferente.

## WBR

Revisão semanal do estado do negócio, produto ou projeto.

A apresentação menciona uma tabela de métricas-chave denominada:

```text
Page Zero
```

## MBR

Revisão mensal utilizada para consolidar tendências e ajustar prioridades de curto prazo.

## QBR

Revisão trimestral que conecta a execução aos objetivos e resultados-chave definidos no planejamento.

# 25. S-team Goal Reviews

Além das revisões operacionais, o trabalho apresenta revisões das metas selecionadas pela liderança executiva.

```text
S-team Goals
     ↓
Revisão
     ↓
Progresso
     ↓
Ajustes
```

O acompanhamento ocorre mensal e trimestralmente.

# 26. Autonomia com prestação de contas

A autonomia apresentada no modelo não significa ausência de responsabilidade.

```text
Autonomia
    +
Responsabilidade
    +
Métricas
    ↓
Execução
```

Equipes e líderes possuem liberdade para executar, porém precisam responder pelos resultados.

# 27. Melhoria contínua

O processo de melhoria contínua foi organizado em quatro etapas.

```text
Identificar
    ↓
Investigar
    ↓
Corrigir
    ↓
Compartilhar
```

# 28. Identificar

O primeiro passo consiste em registrar o evento e medir seu impacto.

```text
Evento
  ↓
Registro
  ↓
Impacto
```

O foco apresentado está especialmente no impacto causado aos clientes.

# 29. Investigar, 5 Porquês

A investigação utiliza a técnica dos **5 Porquês**.

```text
Problema
   ↓
Por quê?
   ↓
Por quê?
   ↓
Por quê?
   ↓
Causa raiz
```

O objetivo é evitar correções superficiais focadas apenas nos sintomas.

# 30. Corrigir

Após encontrar as causas, são definidos itens de ação.

Esses itens devem possuir:

- Responsável.
- Prazo.
- Ação definida.

```text
Causa raiz
    ↓
Ação
    ↓
Responsável
    ↓
Prazo
```

# 31. Compartilhar

A última etapa procura espalhar o aprendizado para outras equipes.

```text
Problema em uma equipe
        ↓
Aprendizado
        ↓
Compartilhamento
        ↓
Prevenção em outras equipes
```

Dessa forma, o valor da investigação não fica restrito ao grupo diretamente afetado pelo problema.

# 32. Planejamento estratégico de TI

A apresentação organiza o planejamento em diferentes mecanismos.

```text
Working Backwards
        ↓
OP1
        ↓
Revisão Executiva
        ↓
OP2
        ↓
OKRs
```

# 33. Working Backwards

O processo Working Backwards começa antes da construção da tecnologia.

A equipe produz:

```text
PR
Press Release

+

FAQ
Frequently Asked Questions
```

antes de especificar ou desenvolver a solução.

O fluxo apresentado é:

```text
Necessidade do cliente
        ↓
PR/FAQ
        ↓
Proposta
        ↓
Validação da ideia
        ↓
Tecnologia
```

Isso mantém a discussão inicial focada no valor esperado para o cliente.

# 34. OP1

Entre agosto e outubro, segundo a linha do tempo apresentada, cada unidade de negócio ou função prepara um plano narrativo.

O material informa que o plano possui:

```text
6 páginas
```

e inclui:

- Metas.
- Iniciativas.
- Métricas.
- Planejamento para o ano seguinte.

# 35. Revisão executiva

Após o OP1, a liderança realiza uma revisão detalhada.

```text
Plano
  ↓
Revisão
  ↓
Premissas
  ↓
Investimentos
  ↓
Recursos
```

O objetivo é testar premissas antes de aprovar investimentos e recursos.

# 36. OP2

O OP2 recalibra o planejamento com base nos resultados reais do fim do ano fiscal.

```text
OP1
 ↓
Resultados reais
 ↓
Recalibração
 ↓
OP2
```

O OP2 passa a funcionar como plano de registro.

# 37. OKRs trimestrais

Ao longo do ano, metas anuais são traduzidas em resultados-chave trimestrais.

```text
Meta anual
    ↓
Resultado-chave
    ↓
Trimestre
    ↓
Acompanhamento semanal
```

Isso aproxima o planejamento de longo prazo da execução cotidiana.

# 38. Estrutura organizacional

A apresentação destaca dois elementos.

```text
Two Pizza Teams
      +
Single-Threaded Leader
```

# 39. Equipes "duas pizzas"

As equipes são descritas como pequenas, normalmente com algo entre:

```text
5 e 10 pessoas
```

e responsáveis de ponta a ponta por determinado produto ou serviço.

O raciocínio apresentado é que o número de canais de comunicação cresce com o tamanho da equipe.

```text
Equipe menor
      ↓
Menos canais de comunicação
      ↓
Decisões mais rápidas
      ↓
Maior responsabilização
```

# 40. Relação entre autonomia e controle

A governança acontece por:

- Padrões.
- Métricas.
- Revisões.
- Guardrails.

e não necessariamente por aprovação caso a caso.

```text
Equipe pequena
      ↓
Autonomia
      ↓
Guardrails
      ↓
Métricas
      ↓
Responsabilidade
```

# 41. Métricas e mecanismos de controle

A apresentação consolida quatro mecanismos principais.

| Mecanismo | Periodicidade | Finalidade |
|---|---|---|
| WBR | Semanal | Revisar estado do negócio, produto ou projeto |
| MBR | Mensal | Consolidar tendências e ajustar prioridades |
| QBR | Trimestral | Relacionar execução aos objetivos e OKRs |
| S-team Goal Reviews | Mensal e trimestral | Acompanhar metas executivas |

A estrutura demonstra que controle não precisa significar microgerenciamento.

```text
Controle
   ↓
Métricas
   +
Revisões
   +
Resultados
```

# 42. Relação com frameworks de referência

A atividade também relaciona práticas apresentadas no modelo Amazon a frameworks e normas de referência.

| Conceito de GTI | Referência | Prática relacionada no trabalho |
|---|---|---|
| Governança corporativa de TI | ISO/IEC 38500 | Guardrails, líderes dedicados e inspeção |
| Gestão de portfólio e riscos | COBIT 2019, APO | Capacidades de governança do AWS CAF |
| Melhoria contínua | ITIL 4 | Correção de Erros e 5 Porquês |
| Planejamento estratégico | Val IT e COBIT | OP1, OP2 e Working Backwards |
| Excelência operacional | ISO/IEC 20000 | AWS Well-Architected Framework |

A atividade utiliza essas relações para aproximar as práticas analisadas dos conceitos tradicionais de Governança de TI.

# 43. Lições aplicáveis a outras organizações

O trabalho apresenta seis principais aprendizados.

## 1. Criar mecanismos auditáveis

```text
Declaração de intenção
        ↓
Mecanismo
        ↓
Processo verificável
```

## 2. Definir dimensões de governança

Antes de expandir operações de nuvem, é importante definir responsabilidades e áreas de governança.

## 3. Incorporar excelência operacional ao ciclo de vida

Excelência operacional não deve funcionar apenas como checklist realizado no final.

Ela precisa fazer parte da operação.

## 4. Formalizar tratamento de erros

```text
Erro
 ↓
Causa raiz
 ↓
Ação
 ↓
Responsável
 ↓
Aprendizado
```

## 5. Relacionar planejamento a métricas

Metas anuais precisam estar associadas a indicadores acompanhados regularmente.

## 6. Equilibrar autonomia e guardrails

```text
Autonomia
    +
Limites claros
    ↓
Velocidade com controle
```

# 44. Síntese do modelo

O modelo analisado pode ser resumido como:

```text
                     ESTRATÉGIA
                         │
                         ▼
                 Working Backwards
                         │
                         ▼
                    OP1 / OP2
                         │
                         ▼
                       METAS
                         │
                         ▼
              Equipes pequenas e líderes
                         │
                         ▼
                    EXECUÇÃO
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
         Guardrails              Métricas
              │                     │
              └──────────┬──────────┘
                         ▼
                  WBR / MBR / QBR
                         │
                         ▼
                    RESULTADOS
                         │
                         ▼
               MELHORIA CONTÍNUA
                         │
                         ▼
              Identificar problemas
                         ↓
                    Investigar
                         ↓
                     Corrigir
                         ↓
                   Compartilhar
```

# 45. Conclusão da equipe

A conclusão registrada na atividade é que o modelo estudado demonstra a possibilidade de equilibrar:

```text
Controle
   +
Liberdade
```

A Amazon utiliza:

- Métricas.
- Processos.
- Revisões.

para acompanhar a relação entre tecnologia e objetivos de negócio.

Ao mesmo tempo, as equipes mantêm determinado grau de autonomia para executar atividades e procurar melhorias continuamente.

O equilíbrio pode ser resumido por:

```text
Autonomia
    +
Mecanismos
    +
Métricas
    +
Responsabilidade
    ↓
Governança
```

# 46. Relação com o Projeto Integrador

Os conceitos estudados podem ser relacionados ao **ConectaStart** como aplicação acadêmica.

## Guardrails

O projeto poderia definir padrões para:

- Desenvolvimento.
- Segurança.
- Qualidade.
- Dados.
- Arquitetura.

sem exigir aprovação individual para cada pequena alteração.

## Responsabilidade clara

Cada área poderia possuir responsáveis definidos.

```text
Produto
Desenvolvimento
Qualidade
Dados
Infraestrutura
```

## Revisões recorrentes

O projeto poderia acompanhar periodicamente:

- Backlog.
- Riscos.
- Defeitos.
- Uso.
- Matchmaking.
- Satisfação.

## Melhoria contínua

```text
Problema
   ↓
Causa
   ↓
Ação
   ↓
Responsável
   ↓
Reteste
   ↓
Aprendizado
```

## Working Backwards

Antes de criar determinada funcionalidade, a equipe poderia começar pelo valor esperado para o usuário.

```text
Necessidade da startup
        ↓
Resultado esperado
        ↓
Experiência desejada
        ↓
Funcionalidade
        ↓
Tecnologia
```

> As aplicações ao ConectaStart apresentadas nesta seção são relações acadêmicas construídas a partir dos conceitos do trabalho, e não fazem parte do conteúdo original sobre a Amazon.

[Acessar Projeto Integrador](../../../projeto-integrador/)

# 47. Relação com Gestão da Informação

As dimensões de:

```text
Governança de dados
       +
Curadoria de dados
```

possuem relação direta com os conteúdos da UC de Gestão da Informação.

Exemplos:

```text
Metadados
Taxonomias
Catálogos
Ciclo de vida
Responsabilidades
Encontrabilidade
```

[Consultar Gestão da Informação](../../uc01-gestao-da-informacao/)

# 48. Relação com Validação e Qualidade de Software

Os princípios de eficácia operacional também se relacionam a conteúdos da UC02.

Exemplos:

```text
Mudanças pequenas
Automação
Observabilidade
Recuperação
Aprendizado com falhas
Melhoria contínua
```

Esses conceitos podem complementar:

- CI/CD.
- Quality Gates.
- Testes automatizados.
- Monitoramento.
- Gestão de incidentes.

[Consultar Validação e Qualidade de Software](../../uc02-validacao-e-qualidade-de-software/)

# 49. Principais aprendizados

A atividade permitiu compreender que Governança de TI não precisa significar centralização completa das decisões.

Uma organização pode trabalhar com:

```text
Equipes autônomas
       +
Responsabilidades claras
       +
Guardrails
       +
Métricas
       +
Revisões
```

Outro aprendizado importante foi a distinção entre:

```text
Governar
   ≠
Aprovar tudo
```

A governança pode acontecer através de mecanismos que direcionam decisões sem necessariamente bloquear a execução.

Também foi possível compreender que planejamento e operação precisam permanecer conectados.

```text
Estratégia
   ↓
Metas
   ↓
Métricas
   ↓
Execução
   ↓
Revisão
   ↓
Aprendizado
```

# Competências desenvolvidas

A atividade contribuiu para o desenvolvimento de competências relacionadas a:

- Governança de TI.
- Governança corporativa.
- Gestão de riscos.
- Gestão de portfólio.
- Gestão de benefícios.
- Governança de dados.
- Curadoria de dados.
- Cloud Governance.
- AWS Cloud Adoption Framework.
- AWS Well-Architected Framework.
- Observabilidade.
- Melhoria contínua.
- Análise de causa raiz.
- 5 Porquês.
- Working Backwards.
- Planejamento estratégico.
- OKRs.
- Métricas.
- Autonomia de equipes.
- Estruturas organizacionais.
- ISO/IEC 38500.
- COBIT.
- ITIL.
- Val IT.
- ISO/IEC 20000.

# Organização dos arquivos

```text
governanca-amazon/
│
├── README.md
└── GTI_Modelo_Amazon.pptx 1.pdf
```

# Documento original

```text
GTI_Modelo_Amazon.pptx 1.pdf
```

# Navegação

[Voltar para Governança em Tecnologia da Informação](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)

[Atividade anterior, Indicadores Setoriais e Governança de TI](../indicadores-governanca-ti/)

[Próxima atividade, Governança Ágil, Magazine Luiza e Loggi](../governanca-agil-magalu-loggi/)
