# Indicadores Setoriais e Governança de TI

[Voltar para Governança em Tecnologia da Informação](../README.md)

## Metadados

| Campo | Informação |
|---|---|
| Unidade Curricular | Governança em Tecnologia da Informação |
| Atividade | Laboratório 01, Prática 01 |
| Código | TADS040/5T |
| Curso | Análise e Desenvolvimento de Sistemas |
| Instituição | Faculdade Senac Pernambuco |
| Período | 5º período |
| Semestre | 2026.2 |
| Data de entrega | 22/08/2026 |
| Tipo | Atividade em grupo |
| Tema | Conceitos e Princípios da Governança em TI |
| Abordagem | Indicadores de desempenho setorial e análise comparativa |
| Empresas analisadas | Amazon Web Services e Itaú Unibanco |
| Documento principal | relatorio_governanca_ti.pdf |
| Status | Concluído |

## Objetivo da atividade

A atividade teve como objetivo compreender como **indicadores de desempenho** podem apoiar a Governança de Tecnologia da Informação.

O trabalho analisa cinco indicadores:

```text
Disponibilidade
      ↓
Cumprimento de SLA
      ↓
MTTR
      ↓
Incidentes de Segurança
      ↓
ROI de TI
```

Posteriormente, esses indicadores são relacionados a duas organizações de perfis diferentes:

```text
Amazon Web Services
        +
Itaú Unibanco
```

A comparação permite observar como características do setor e do modelo de negócio influenciam a forma como indicadores de TI são divulgados e utilizados.

# 1. Governança de TI

A atividade apresenta a Governança de TI como um conjunto de:

- Práticas.
- Políticas.
- Estruturas de decisão.
- Indicadores.
- Mecanismos de acompanhamento.

Seu objetivo é orientar o uso da Tecnologia da Informação para que ela sustente os objetivos estratégicos da organização.

O processo pode ser representado como:

```text
Estratégia organizacional
          ↓
Governança de TI
          ↓
Objetivos tecnológicos
          ↓
Indicadores
          ↓
Medição
          ↓
Decisão
```

Um dos elementos centrais dessa governança é a utilização de métricas capazes de transformar desempenho em informações observáveis.

# 2. Indicadores analisados

A atividade selecionou cinco indicadores.

| Indicador | Finalidade |
|---|---|
| Disponibilidade dos serviços de TI | Medir o tempo em que sistemas permanecem disponíveis |
| Cumprimento de SLA | Verificar o atendimento dos níveis de serviço acordados |
| MTTR | Medir o tempo médio necessário para resolução ou recuperação |
| Incidentes de segurança | Acompanhar ocorrências e riscos de segurança |
| ROI dos investimentos em TI | Avaliar o valor gerado pelos investimentos tecnológicos |

# 3. Disponibilidade dos serviços de TI

A disponibilidade mede o percentual de tempo em que determinado sistema ou serviço permanece operacional.

```text
Tempo operacional
        ↓
Comparação com tempo total
        ↓
Percentual de disponibilidade
```

Esse indicador está relacionado diretamente à continuidade operacional.

Quanto maior a dependência da organização em relação aos sistemas digitais, maior tende a ser a importância da disponibilidade.

## Pergunta de governança

```text
Os serviços estão funcionando corretamente?
```

# 4. Cumprimento de SLA

O **Service Level Agreement, SLA**, representa um acordo de nível de serviço.

O indicador verifica se os compromissos estabelecidos estão sendo cumpridos.

Pode considerar aspectos como:

- Disponibilidade.
- Tempo de resposta.
- Tempo de atendimento.
- Tempo de resolução.
- Outros níveis formalmente acordados.

O fluxo pode ser representado por:

```text
Serviço
   ↓
SLA definido
   ↓
Medição
   ↓
Resultado
   ↓
Cumpriu ou não cumpriu
```

## Pergunta de governança

```text
A TI está entregando aquilo que foi acordado?
```

# 5. MTTR

O **Mean Time to Repair/Recover, MTTR**, mede quanto tempo a equipe leva, em média, para identificar e resolver um incidente ou recuperar um serviço.

```text
Incidente
   ↓
Identificação
   ↓
Tratamento
   ↓
Recuperação
   ↓
MTTR
```

Quanto menor o tempo de recuperação, maior tende a ser a capacidade operacional de resposta.

## Pergunta de governança

```text
A TI consegue responder aos problemas de maneira eficiente?
```

# 6. Incidentes de segurança

O indicador acompanha a quantidade e, idealmente, a gravidade dos incidentes relacionados à segurança da informação.

Pode incluir ocorrências relacionadas a:

- Acesso indevido.
- Vazamento de dados.
- Indisponibilidade.
- Ataques.
- Violação de políticas.
- Outros eventos de segurança.

Esse indicador também está relacionado à gestão de riscos e à conformidade.

No contexto brasileiro, o relatório relaciona o tema à **Lei Geral de Proteção de Dados, LGPD**.

## Pergunta de governança

```text
Os riscos relacionados à TI estão sendo controlados?
```

# 7. ROI dos investimentos em TI

O **Retorno sobre o Investimento, ROI**, procura avaliar o valor produzido pelos investimentos realizados em tecnologia.

Esse valor pode aparecer de forma:

```text
Financeira
    +
Operacional
    +
Estratégica
```

Exemplos de benefícios possíveis:

- Redução de custos.
- Aumento de produtividade.
- Redução de tempo.
- Automação.
- Aumento de receita.
- Melhoria operacional.

## Pergunta de governança

```text
Os investimentos em TI estão gerando valor?
```

# 8. Empresas analisadas

O trabalho utilizou duas empresas com características bastante diferentes.

## Amazon Web Services

A AWS atua como provedora global de infraestrutura e serviços de computação em nuvem.

Seu próprio modelo de negócio depende fortemente de:

- Disponibilidade.
- Continuidade.
- Confiabilidade.
- Desempenho.

## Itaú Unibanco

O Itaú utiliza Tecnologia da Informação como elemento essencial de operações financeiras e serviços digitais.

Nesse contexto, aspectos como:

- Segurança.
- Privacidade.
- Disponibilidade.
- Conformidade.
- Modernização.

possuem papel relevante.

# 9. Amazon Web Services

O relatório destaca que a AWS publica formalmente SLAs específicos para diversos serviços.

Em vez de uma única meta global:

```text
AWS
 ↓
Serviço A → SLA próprio
Serviço B → SLA próprio
Serviço C → SLA próprio
```

## Disponibilidade

Segundo o documento, serviços de computação analisados possuem metas mensais que podem variar entre:

```text
99,9%
   e
99,99%
```

dependendo da forma de implantação e do serviço.

Exemplos mencionados incluem:

- Amazon EC2.
- Amazon ECS.
- Amazon EKS.
- Amazon CloudFront.
- Amazon EMR.

# 10. Cumprimento de SLA na AWS

Quando a meta contratada não é atingida, o relatório registra a existência de mecanismos de compensação conhecidos como:

```text
Service Credits
```

O fluxo pode ser resumido como:

```text
SLA contratado
      ↓
Meta não atingida
      ↓
Crédito de serviço
```

Isso transforma o SLA em um compromisso mensurável e formalizado.

# 11. MTTR e eventos operacionais da AWS

O relatório utiliza como exemplo um incidente ocorrido na região:

```text
us-east-1
```

em outubro de 2025.

Segundo o trabalho, o evento durou aproximadamente:

```text
15 horas
```

e esteve relacionado a uma falha de DNS envolvendo o Amazon DynamoDB.

O documento utiliza esse tipo de evento para demonstrar a importância de:

- Registro da linha do tempo.
- Identificação da causa.
- Recuperação.
- Documentação pós-incidente.

# 12. Post-Event Summaries

A AWS também é analisada pelo uso de relatórios públicos posteriores a incidentes.

Esses documentos podem registrar:

```text
Evento
  ↓
Impacto
  ↓
Causa
  ↓
Recuperação
  ↓
Ações corretivas
```

O relatório destaca a manutenção de um arquivo de **Post-Event Summaries** para eventos de impacto relevante.

Essa prática contribui para:

- Transparência.
- Aprendizado.
- Melhoria contínua.
- Gestão de incidentes.

# 13. ROI na AWS

O trabalho informa que não foi localizado um valor público específico de ROI referente aos investimentos internos da própria AWS.

Por isso, a análise não cria uma estimativa.

```text
Dado público não localizado
        ↓
Não inventar valor
```

Essa decisão metodológica é relevante porque evita apresentar números não verificáveis.

# 14. Itaú Unibanco

O relatório destaca que o Itaú não divulga publicamente, de forma detalhada, determinados indicadores operacionais internos, como:

- Percentual exato de disponibilidade.
- Cumprimento de SLA.
- MTTR.

Essas informações podem ser tratadas como estratégicas.

A análise foi concentrada principalmente em evidências públicas relacionadas a:

```text
Segurança
   +
Conformidade
   +
Modernização tecnológica
   +
Eficiência
```

# 15. Segurança da Informação no Itaú

O trabalho registra certificações relacionadas a:

```text
ISO 27001:2022

ISO 27701:2019
```

associadas a práticas de:

- Governança da segurança.
- Gestão de riscos.
- Privacidade.
- Tratamento de incidentes.

O documento também menciona estruturas como:

```text
SOC
Security Operations Center
```

e mecanismos de tratamento de incidentes.

# 16. LGPD e comunicação de incidentes

O relatório também relaciona a governança do Itaú às responsabilidades previstas na LGPD.

Entre os elementos apresentados estão:

- Encarregado de Dados.
- DPO.
- Comunicação de incidentes.
- ANPD.

O fluxo pode ser representado por:

```text
Incidente envolvendo dados
          ↓
Processo interno
          ↓
DPO
          ↓
ANPD
```

conforme aplicável às obrigações legais.

# 17. Modernização tecnológica no Itaú

Um dos principais exemplos utilizados para demonstrar geração de valor foi a migração de sistemas para nuvem.

Segundo o relatório:

```text
aproximadamente 187
sistemas e subsistemas
```

foram migrados de uma nuvem privada para a AWS em parceria com a GFT Technologies.

# 18. Ganhos operacionais reportados

O documento registra dois resultados principais.

## Redução de lead time

```text
99%
```

de redução no tempo entre a solicitação de uma entrega e sua entrada em produção.

## Redução do ambiente legado

```text
93%
```

do ambiente OpenStack teria sido desativado ao longo de dois anos.

# 19. ROI como proxy

O relatório não apresenta esses valores como um percentual financeiro formal de ROI.

Eles são utilizados como um **proxy de retorno do investimento tecnológico**.

```text
Investimento em modernização
        ↓
Redução do lead time
        +
Redução de infraestrutura legada
        ↓
Ganho operacional
        ↓
Indício de geração de valor
```

Essa distinção é importante.

```text
Ganho operacional
      ≠
ROI financeiro formal
```

# 20. Análise comparativa

| Indicador | AWS | Itaú Unibanco |
|---|---|---|
| Disponibilidade | Publicada por serviço, com metas entre 99,9% e 99,99% | Não divulgada publicamente em números |
| Cumprimento de SLA | Formalizado com créditos de serviço | Não divulgado publicamente |
| MTTR | Evidenciado por relatórios públicos de eventos | Não divulgado publicamente |
| Incidentes de segurança | Post-Event Summaries | Certificações, processos de segurança e DPO |
| ROI de TI | Não apresentado como ROI interno da própria AWS | Ganhos operacionais utilizados como proxy |

# 21. Diferenças entre as empresas

A principal diferença não deve ser interpretada automaticamente como uma diferença de maturidade.

Ela também decorre do modelo de negócio.

## AWS

```text
Disponibilidade
é parte do próprio produto
        ↓
Maior necessidade de publicar
metas e compromissos
```

## Itaú

```text
TI sustenta serviços financeiros
        ↓
Indicadores operacionais
podem ser estratégicos
        ↓
Maior divulgação pública de
conformidade e transformação
```

# 22. Governança e contexto organizacional

A atividade demonstra que os mesmos indicadores podem possuir níveis diferentes de exposição conforme:

- Setor.
- Modelo de negócio.
- Regulação.
- Estratégia.
- Confidencialidade.
- Público interessado.

Portanto:

```text
Mesmo indicador
      ↓
Contextos diferentes
      ↓
Formas diferentes de evidenciar
```

# 23. Relação entre indicadores e perguntas de governança

| Indicador | Pergunta que ajuda a responder |
|---|---|
| Disponibilidade | Os serviços estão funcionando corretamente? |
| Cumprimento de SLA | A TI está entregando o que foi acordado? |
| MTTR | A TI responde aos problemas de forma eficiente? |
| Incidentes de segurança | Os riscos estão sendo controlados? |
| ROI de TI | Os investimentos estão gerando valor? |

# 24. Dimensões cobertas

Os indicadores analisados cobrem diferentes dimensões.

```text
Disponibilidade
      ↓
Operacional

SLA
      ↓
Contratual

MTTR
      ↓
Operacional

Segurança
      ↓
Risco

ROI
      ↓
Financeira e estratégica
```

Em conjunto, permitem uma visão mais ampla da Governança de TI.

# 25. Importância dos indicadores

Sem indicadores, torna-se difícil verificar se a Tecnologia da Informação realmente está contribuindo para a organização.

```text
Governança sem métricas
        ↓
Percepções
        ↓
Baixa verificabilidade
```

Com indicadores:

```text
Métrica
  ↓
Evidência
  ↓
Comparação
  ↓
Decisão
```

# 26. Apoio à alta administração

Indicadores permitem que:

- Alta administração.
- Auditores.
- Gestores.
- Áreas de negócio.

acompanhem resultados com base em evidências.

Isso pode apoiar decisões relacionadas a:

```text
Investimentos

Riscos

Prioridades

Capacidade operacional
```

# 27. Tomada de decisão baseada em evidências

A atividade reforça a diferença entre:

```text
"Acredito que o serviço está estável."
```

e:

```text
"O serviço apresentou
99,95% de disponibilidade."
```

O segundo cenário cria uma base mensurável para decisão.

# 28. Transparência metodológica

Um aspecto importante do relatório é evitar inventar indicadores que as empresas não divulgam publicamente.

O princípio seguido é:

```text
Existe dado público?
      ↓
Sim
→ utilizar

Não
→ declarar ausência
```

e não:

```text
Não existe dado
      ↓
Criar estimativa
```

Essa abordagem aumenta a confiabilidade da análise.

# 29. Síntese da comparação

```text
AWS
│
├── SLA
├── Disponibilidade
├── Eventos operacionais
└── Post-Event Summaries

Itaú
│
├── Segurança
├── Privacidade
├── Compliance
└── Modernização tecnológica
```

Apesar das diferenças, ambos os casos demonstram a utilização de tecnologia em ambientes nos quais:

```text
Desempenho
    +
Risco
    +
Valor
```

precisam ser acompanhados.

# 30. Relação com o Projeto Integrador

Os conceitos podem ser aplicados futuramente ao **ConectaStart**.

> Esta seção representa uma aplicação acadêmica dos conceitos da atividade e não faz parte da análise original da AWS e do Itaú.

## Disponibilidade

```text
Quanto tempo o ConectaStart
permanece disponível?
```

## SLA

Caso existam serviços externos ou compromissos formais:

```text
O serviço atende
o nível acordado?
```

## MTTR

```text
Quanto tempo a equipe leva
para recuperar o sistema
após uma falha?
```

## Segurança

Podem ser monitorados:

- Falhas de autenticação.
- Incidentes.
- Acessos indevidos.
- Eventos relacionados a dados.

## ROI

Futuramente pode ser avaliado se os investimentos tecnológicos produzem:

- Economia.
- Eficiência.
- Crescimento.
- Valor para startups e mentores.

# 31. Exemplo de painel conceitual para o ConectaStart

| Indicador | Exemplo de objetivo |
|---|---|
| Disponibilidade | Monitorar continuidade da plataforma |
| MTTR | Reduzir tempo de recuperação |
| Incidentes | Acompanhar riscos de segurança |
| Satisfação | Avaliar percepção dos usuários |
| Matchmaking | Avaliar eficiência do serviço principal |

O último indicador não faz parte do relatório original, mas representa uma adaptação possível ao produto.

[Acessar Projeto Integrador](../../../projeto-integrador/)

# 32. Relação com Qualidade de Software

A atividade também possui relação com a UC de **Validação e Qualidade de Software**.

Por exemplo:

```text
Testes
   ↓
Detectam problemas antes da release
```

Enquanto:

```text
Indicadores
   ↓
Monitoram comportamento
durante a operação
```

As duas perspectivas são complementares.

```text
QUALIDADE
Antes da produção
      +
GOVERNANÇA
Durante a operação
```

[Consultar Validação e Qualidade de Software](../../uc02-validacao-e-qualidade-de-software/)

# 33. Relação com Gestão da Informação

Para produzir indicadores confiáveis é necessário possuir informações confiáveis.

```text
Dados
  ↓
Qualidade da informação
  ↓
Indicadores
  ↓
Decisão
```

Informações:

- Incompletas.
- Desatualizadas.
- Inconsistentes.
- Imprecisas.

podem prejudicar a análise gerencial.

[Consultar Gestão da Informação](../../uc01-gestao-da-informacao/)

# 34. Principais aprendizados

A atividade permitiu compreender que Governança de TI não pode se apoiar exclusivamente em percepções.

É necessário transformar aspectos relevantes do desempenho em indicadores.

```text
Disponibilidade
      ↓
Continuidade

SLA
      ↓
Compromisso

MTTR
      ↓
Recuperação

Segurança
      ↓
Risco

ROI
      ↓
Valor
```

Outro aprendizado importante foi compreender que:

```text
Ausência de dado público
      ≠
Ausência de governança
```

Empresas podem utilizar indicadores internamente sem divulgá-los publicamente.

Por isso, análises externas precisam reconhecer suas limitações.

# 35. Conclusão

Os cinco indicadores analisados permitem observar a Governança de TI sob perspectivas:

```text
Operacional
     +
Contratual
     +
Risco
     +
Financeira
```

A análise da AWS e do Itaú demonstra que a forma de evidenciar esses indicadores varia conforme o contexto organizacional.

A lógica central permanece:

```text
Medir
  ↓
Compreender
  ↓
Gerir
  ↓
Gerar valor
```

# Competências desenvolvidas

A atividade contribuiu para o desenvolvimento de competências relacionadas a:

- Governança de TI.
- Indicadores de desempenho.
- Disponibilidade.
- SLA.
- MTTR.
- Segurança da Informação.
- LGPD.
- ROI.
- Gestão de riscos.
- Análise comparativa.
- Gestão de incidentes.
- Cloud computing.
- Continuidade operacional.
- Tomada de decisão baseada em evidências.
- Análise crítica de dados públicos.

# Organização dos arquivos

```text
indicadores-governanca-ti/
│
├── README.md
└── relatorio_governanca_ti.pdf
```

# Documento original

```text
relatorio_governanca_ti.pdf
```

# Navegação

[Voltar para Governança em Tecnologia da Informação](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)

[Atividade anterior, Indicadores de TI com BSC](../indicadores-ti-bsc/)

[Próxima atividade, Modelo Amazon de Governança](../governanca-amazon/)
