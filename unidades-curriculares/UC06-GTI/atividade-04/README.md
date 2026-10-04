# Governança Ágil, Magazine Luiza e Loggi

[Voltar para Governança em Tecnologia da Informação](../README.md)

## Metadados

| Campo | Informação |
|---|---|
| Unidade Curricular | Governança em Tecnologia da Informação |
| Curso | Análise e Desenvolvimento de Sistemas |
| Instituição | Faculdade Senac Pernambuco |
| Período | 5º período |
| Semestre | 2026.2 |
| Tipo | Pesquisa e análise comparativa |
| Tema | Governança Ágil e Métricas de TI |
| Empresas analisadas | Magazine Luiza e Loggi |
| Documento principal | Governanca_Agil_Magazine_Luiza_Loggi.pdf |
| Status | Concluído |

## Equipe

- Alisson Gustavo
- Allyson George
- Hericc Rocha
- Vitor Vieira

## Objetivo da atividade

A atividade teve como objetivo analisar como princípios de **Governança Ágil** podem ser aplicados a organizações que dependem fortemente de tecnologia, utilizando como referência o **Magazine Luiza**, por meio do LuizaLabs, e a **Loggi**.

O trabalho também explora métricas utilizadas para acompanhar:

- Velocidade de entrega.
- Frequência de implantação.
- Recuperação após falhas.
- Qualidade das mudanças.
- Retrabalho.
- Confiabilidade.
- Monitoramento.
- Melhoria contínua.

A análise parte da ideia de que Governança Ágil precisa equilibrar:

```text
Autonomia
   +
Velocidade
   +
Qualidade
   +
Controle de riscos
   +
Alinhamento com o negócio
```

# 1. O que é Governança Ágil?

A atividade apresenta a Governança Ágil como uma abordagem que procura conciliar autonomia das equipes e velocidade de desenvolvimento com controle, qualidade e alinhamento estratégico.

O objetivo não é eliminar governança.

O objetivo é evitar que os mecanismos de controle impeçam a capacidade de entrega.

```text
Governança tradicional excessiva
        ↓
Muitas aprovações
        ↓
Baixa velocidade
```

Enquanto a Governança Ágil procura:

```text
Autonomia
   ↓
Métricas
   ↓
Monitoramento
   ↓
Responsabilidade
   ↓
Melhoria contínua
```

# 2. Papel dos indicadores

Os indicadores permitem acompanhar objetivamente o desempenho dos processos de Tecnologia da Informação.

Eles ajudam a:

- Identificar gargalos.
- Medir velocidade.
- Avaliar qualidade.
- Analisar falhas.
- Acompanhar recuperação.
- Avaliar retrabalho.
- Apoiar decisões.

O fluxo pode ser representado por:

```text
Processo
   ↓
Métrica
   ↓
Resultado
   ↓
Análise
   ↓
Decisão
```

# 3. Métricas DORA analisadas

O trabalho apresenta cinco métricas relacionadas à Governança Ágil.

| Métrica | O que mede | Objetivo |
|---|---|---|
| Lead Time for Changes | Tempo entre alteração no código e produção | Reduzir tempo de entrega |
| Deployment Frequency | Frequência de implantações | Aumentar capacidade de entrega |
| Failed Deployment Recovery Time | Tempo para recuperar após falha de implantação | Reduzir impacto das falhas |
| Change Failure Rate | Percentual de implantações que causam falhas | Aumentar qualidade |
| Deployment Rework Rate | Percentual de implantações motivadas por retrabalho | Reduzir desperdícios |

O trabalho destaca que essas métricas precisam ser observadas em conjunto.

```text
Mais velocidade
      ≠
Melhor desempenho automaticamente
```

Se a frequência de implantação aumenta, mas também crescem falhas e retrabalho, a situação não representa necessariamente melhoria.

# 4. Lead Time for Changes

O **Lead Time for Changes** mede o tempo necessário para que uma alteração percorra o processo de desenvolvimento até chegar à produção.

Exemplo apresentado:

```text
Alteração feita na segunda-feira
        ↓
Produção na terça-feira
        ↓
Lead Time aproximado de 1 dia
```

## Importância

A métrica ajuda a identificar gargalos em etapas como:

- Desenvolvimento.
- Testes.
- Aprovação.
- Implantação.

Quanto menor o Lead Time, maior tende a ser a capacidade de resposta às necessidades do negócio.

# 5. Deployment Frequency

A **Deployment Frequency** mede quantas vezes uma equipe consegue implantar alterações em produção em determinado período.

Exemplo conceitual:

```text
Equipe
  ↓
Entrega pequenas mudanças
  ↓
Implanta frequentemente
  ↓
Feedback mais rápido
```

Uma frequência maior pode indicar maior capacidade de entrega, desde que a qualidade seja preservada.

# 6. Failed Deployment Recovery Time

Essa métrica mede quanto tempo a equipe leva para recuperar o sistema depois de uma implantação que gerou falha.

Exemplo apresentado:

```text
Falha às 14h
      ↓
Sistema normalizado às 15h
      ↓
Recovery Time = 1 hora
```

## Importância

Uma organização não precisa apenas evitar falhas.

Também precisa possuir capacidade de:

```text
Detectar
   ↓
Responder
   ↓
Recuperar
```

# 7. Change Failure Rate

O **Change Failure Rate, CFR**, representa o percentual de alterações implantadas que provocam falha e exigem intervenção.

## Fórmula

```text
CFR =
Número de implantações com falha
÷
Número total de implantações
×
100
```

## Exemplo

```text
100 implantações

8 apresentaram falhas
```

Resultado:

```text
Change Failure Rate = 8%
```

Essa métrica ajuda a observar a estabilidade das entregas.

# 8. Deployment Rework Rate

O **Deployment Rework Rate** mede quanto das implantações realizadas corresponde a retrabalho não planejado.

Exemplo:

```text
50 implantações
      ↓
10 destinadas a corrigir
problemas anteriores
```

Resultado:

```text
Rework Rate = 20%
```

Essa métrica permite identificar esforço desperdiçado em correções.

# 9. Relação entre as métricas

As métricas podem ser agrupadas da seguinte forma:

```text
VELOCIDADE
│
├── Lead Time
└── Deployment Frequency

QUALIDADE
│
├── Change Failure Rate
└── Rework Rate

RESILIÊNCIA
│
└── Failed Deployment Recovery Time
```

A Governança Ágil precisa acompanhar as três dimensões.

# 10. Aplicação no Magazine Luiza

O trabalho utiliza o **LuizaLabs** como referência da estrutura tecnológica do Magazine Luiza.

A análise apresenta evidências públicas relacionadas ao uso de métricas como:

- Lead Time.
- Throughput.
- Monitoramento.
- Observabilidade.

O objetivo dessas métricas é apoiar:

- Previsibilidade.
- Saúde das entregas.
- Identificação de gargalos.
- Melhoria contínua.

# 11. Lead Time no Magazine Luiza

No contexto analisado, o Lead Time pode ser utilizado para verificar quanto tempo uma demanda leva para percorrer o fluxo até sua conclusão.

```text
Demanda
   ↓
Desenvolvimento
   ↓
Validação
   ↓
Entrega
   ↓
Lead Time
```

Esse indicador ajuda a identificar atrasos no processo.

# 12. Deployment Frequency no Magazine Luiza

A métrica pode ser aplicada para acompanhar a capacidade de realizar entregas frequentes.

```text
Mudanças pequenas
      ↓
Entregas frequentes
      ↓
Feedback
      ↓
Melhoria
```

# 13. Recovery Time no Magazine Luiza

O Recovery Time pode ser utilizado para avaliar a capacidade de recuperação diante de falhas.

A lógica é:

```text
Falha
 ↓
Detecção
 ↓
Recuperação
 ↓
Tempo de recuperação
```

# 14. Change Failure Rate no Magazine Luiza

Essa métrica pode apoiar a avaliação da qualidade e estabilidade das mudanças realizadas.

```text
Alterações implantadas
        ↓
Quantas causaram problema?
        ↓
Taxa de falha
```

# 15. Rework Rate no Magazine Luiza

O Rework Rate permite identificar quanto esforço está sendo direcionado para corrigir problemas produzidos por entregas anteriores.

```text
Tempo de desenvolvimento
       ↓
Nova funcionalidade
       ou
Correção de problema anterior
```

Essa distinção ajuda a observar desperdícios.

# 16. Limitação metodológica sobre o Magazine Luiza

O próprio trabalho registra uma ressalva importante:

> Não é adequado afirmar que o Magazine Luiza publica oficialmente os cinco indicadores DORA exatamente com essas nomenclaturas.

As evidências públicas encontradas estão relacionadas principalmente a:

- Lead Time.
- Throughput.
- Métricas ágeis.
- Monitoramento.
- Observabilidade.

Portanto, a relação com as cinco métricas é apresentada como uma aplicação analítica ao contexto da empresa.

```text
Evidência pública
       ↓
Interpretação acadêmica
       ↓
Aplicação das métricas
```

# 17. Aplicação na Loggi

A Loggi foi analisada por possuir uma operação altamente dependente de tecnologia.

O trabalho destaca a existência de áreas como:

- Engenharia de Software.
- Análise de Dados.
- SRE, Site Reliability Engineering.

A estrutura de SRE é particularmente importante por atuar em:

- Desempenho.
- Monitoramento.
- Planejamento.
- Automação.
- Confiabilidade.

# 18. Estrutura ágil da Loggi

A atividade também registra a utilização de:

```text
Squads
   +
Tribos
   +
Clãs
```

como elementos da organização tecnológica.

Essas estruturas aproximam equipes da lógica de trabalho ágil e de responsabilidades distribuídas.

# 19. SRE na Loggi

O **Site Reliability Engineering** aproxima desenvolvimento e operações.

```text
Desenvolvimento
       +
Operações
       ↓
SRE
       ↓
Confiabilidade
       +
Automação
       +
Monitoramento
```

Isso possui especial importância para a Loggi porque sua operação logística depende da disponibilidade dos sistemas digitais.

# 20. Lead Time na Loggi

Pode ser utilizado para medir a velocidade entre desenvolvimento e disponibilização de alterações.

```text
Código
  ↓
Pipeline
  ↓
Produção
  ↓
Usuário
```

# 21. Deployment Frequency na Loggi

Permite acompanhar a frequência com que atualizações são disponibilizadas.

Esse indicador pode mostrar a capacidade de evolução contínua dos sistemas.

# 22. Recovery Time na Loggi

A operação logística depende fortemente da disponibilidade tecnológica.

Por isso, a velocidade de recuperação de incidentes é especialmente relevante.

```text
Falha tecnológica
       ↓
Impacto operacional
       ↓
SRE
       ↓
Recuperação
```

# 23. Change Failure Rate na Loggi

A métrica pode ajudar a acompanhar quantas mudanças introduzem problemas.

Isso permite observar a relação entre:

```text
Velocidade de mudança
        e
Estabilidade
```

# 24. Rework Rate na Loggi

Pode ser utilizado para medir o esforço direcionado a correções de problemas anteriores.

```text
Retrabalho alto
      ↓
Menor capacidade
para novas entregas
```

# 25. Por que essas métricas são relevantes para a Loggi?

A operação da empresa depende de sistemas digitais para sustentar uma atividade logística em grande escala.

Por isso, a atividade destaca quatro elementos:

```text
Escalabilidade
      +
Confiabilidade
      +
Monitoramento
      +
Automação
```

Uma falha tecnológica pode gerar impacto direto na operação física.

# 26. Análise comparativa

| Aspecto | Magazine Luiza | Loggi |
|---|---|---|
| Modelo ágil | LuizaLabs e uso de métricas ágeis | Squads, tribos e SRE |
| Lead Time | Fluxo e previsibilidade das entregas | Velocidade de desenvolvimento |
| Monitoramento | Métricas e aplicações | Forte atuação de SRE |
| Confiabilidade | Monitoramento para identificar problemas | Foco explícito em confiabilidade |
| Melhoria contínua | Identificação de gargalos | Aprendizado com problemas |
| Principal característica | Transformação digital e eficiência | Escalabilidade, confiabilidade e operação |

# 27. Principal diferença entre as empresas

O trabalho destaca que a diferença principal está no contexto do negócio.

## Magazine Luiza

A tecnologia funciona como elemento central de sua transformação digital.

```text
Varejo
  ↓
Transformação digital
  ↓
LuizaLabs
  ↓
Tecnologia
```

## Loggi

A tecnologia sustenta diretamente uma operação logística de grande escala.

```text
Tecnologia
   ↓
Plataforma
   ↓
Operação logística
   ↓
Entrega física
```

Por isso, confiabilidade e recuperação possuem papel especialmente relevante na Loggi.

# 28. Governança Ágil e velocidade

A atividade demonstra que velocidade não deve ser analisada isoladamente.

```text
Entregar rápido
      +
Falhar muito
      =
Problema
```

A visão adequada é:

```text
Velocidade
    +
Qualidade
    +
Estabilidade
    +
Recuperação
```

# 29. Governança Ágil e autonomia

Governança Ágil não significa ausência de controle.

```text
Equipe autônoma
      ↓
Métricas
      ↓
Monitoramento
      ↓
Responsabilidade
```

O controle ocorre por meio de evidências e resultados.

# 30. Indicadores como apoio à decisão

Os indicadores permitem transformar o desempenho de TI em informação mensurável.

A atividade aponta que eles podem ajudar a:

- Identificar gargalos.
- Acompanhar produtividade.
- Medir velocidade.
- Monitorar riscos.
- Avaliar falhas.
- Avaliar qualidade.
- Apoiar decisões estratégicas.
- Medir evolução.
- Promover melhoria contínua.

# 31. Melhoria contínua

Os indicadores permitem comparar resultados antes e depois de uma mudança.

```text
Situação atual
      ↓
Métrica
      ↓
Mudança
      ↓
Nova métrica
      ↓
Comparação
```

Isso permite verificar se determinada iniciativa realmente melhorou o processo.

# 32. Exemplo de análise combinada

Imagine:

```text
Deployment Frequency ↑
```

Isso pode parecer positivo.

Mas se:

```text
Change Failure Rate ↑
Rework Rate ↑
Recovery Time ↑
```

a melhoria pode não ser real.

O ideal é observar o conjunto:

```text
Deployment Frequency ↑

Lead Time ↓

Change Failure Rate ↓

Recovery Time ↓

Rework Rate ↓
```

# 33. Relação entre Governança Ágil e SRE

A atividade mostra uma relação forte entre Governança Ágil e práticas de SRE.

```text
Governança Ágil
       ↓
Velocidade + controle

SRE
       ↓
Confiabilidade + automação
```

Combinados:

```text
Entrega rápida
      +
Operação confiável
```

# 34. Importância da observabilidade

A observabilidade permite identificar o estado dos sistemas e apoiar a recuperação diante de problemas.

```text
Sistema
  ↓
Métricas
  +
Logs
  +
Monitoramento
  ↓
Diagnóstico
  ↓
Ação
```

Esse elemento aparece tanto no contexto do LuizaLabs quanto da Loggi.

# 35. Relação com o Projeto Integrador

Os conceitos da atividade podem ser aplicados ao **ConectaStart** como referência acadêmica.

## Lead Time

```text
Demanda aprovada
      ↓
Desenvolvimento
      ↓
Produção
```

Pode ser medido o tempo entre a aprovação de uma alteração e sua disponibilização.

## Deployment Frequency

```text
Quantas versões
são implantadas
por período?
```

## Recovery Time

```text
Falha
  ↓
Quanto tempo até
a recuperação?
```

## Change Failure Rate

```text
Quantas alterações
provocam falhas?
```

## Rework Rate

```text
Quanto esforço
é gasto corrigindo
entregas anteriores?
```

Essas métricas poderiam apoiar uma futura Governança Ágil do projeto.

> Esta seção representa uma aplicação acadêmica dos conceitos da atividade ao ConectaStart e não faz parte da análise original de Magazine Luiza e Loggi.

[Acessar Projeto Integrador](../../../projeto-integrador/)

# 36. Relação com Validação e Qualidade de Software

A atividade possui forte relação com a UC de **Validação e Qualidade de Software**.

Exemplo:

```text
Testes automatizados
       ↓
Menor risco de falha
       ↓
Change Failure Rate
```

Outro exemplo:

```text
Pipeline
  ↓
Feedback rápido
  ↓
Lead Time
```

E:

```text
Observabilidade
      ↓
Detecção
      ↓
Recovery Time
```

Isso demonstra que Qualidade e Governança são complementares.

[Consultar Validação e Qualidade de Software](../../uc02-validacao-e-qualidade-de-software/)

# 37. Relação com o Modelo Amazon

As duas atividades possuem um ponto em comum:

```text
Autonomia
   +
Métricas
   +
Responsabilidade
```

No modelo Amazon, isso aparece em:

- Guardrails.
- Revisões.
- Métricas.
- Equipes autônomas.

Na Governança Ágil:

- DORA.
- Observabilidade.
- SRE.
- Squads.

Ambas mostram que Governança de TI pode ocorrer sem depender de aprovação manual para cada atividade.

[Consultar Modelo Amazon de Governança](../governanca-amazon/)

# 38. Principais aprendizados

A atividade permitiu compreender que uma organização não deve medir apenas quantas entregas realiza.

É necessário observar:

```text
Quanto tempo levamos?
        ↓
Com que frequência entregamos?
        ↓
Quantas entregas falham?
        ↓
Quanto tempo levamos para recuperar?
        ↓
Quanto trabalho precisa ser refeito?
```

Outro aprendizado importante é:

```text
Mais entregas
    ≠
Mais qualidade
```

A Governança Ágil procura equilibrar:

```text
VELOCIDADE

QUALIDADE

ESTABILIDADE

RECUPERAÇÃO

MELHORIA CONTÍNUA
```

# 39. Conclusão

O trabalho conclui que Governança Ágil depende de indicadores para equilibrar velocidade, qualidade, estabilidade e recuperação.

No Magazine Luiza, a análise identifica publicamente práticas relacionadas a:

- Lead Time.
- Throughput.
- Monitoramento.
- LuizaLabs.

Na Loggi, são destacados:

- Squads.
- SRE.
- Monitoramento.
- Desempenho.
- Automação.
- Confiabilidade.

O princípio final pode ser representado como:

```text
Indicadores
    ↓
Informação
    ↓
Problemas
    ↓
Decisão
    ↓
Melhoria
```

As métricas não devem servir apenas para avaliar equipes.

Elas precisam apoiar a identificação de problemas e a evolução da Governança de TI.

# Competências desenvolvidas

A atividade contribuiu para o desenvolvimento de competências relacionadas a:

- Governança de TI.
- Governança Ágil.
- Métricas DORA.
- Lead Time for Changes.
- Deployment Frequency.
- Failed Deployment Recovery Time.
- Change Failure Rate.
- Deployment Rework Rate.
- Monitoramento.
- Observabilidade.
- SRE.
- Confiabilidade.
- Melhoria contínua.
- Análise comparativa.
- Tomada de decisão baseada em indicadores.
- Gestão de desempenho tecnológico.

# Organização dos arquivos

```text
governanca-agil-magalu-loggi/
│
├── README.md
└── Governanca_Agil_Magazine_Luiza_Loggi.pdf
```

# Documento original

```text
Governanca_Agil_Magazine_Luiza_Loggi.pdf
```

# Navegação

[Voltar para Governança em Tecnologia da Informação](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)

[Atividade anterior, Modelo Amazon de Governança](../governanca-amazon/)
