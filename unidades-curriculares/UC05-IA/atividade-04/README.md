# Prompts e Dados Públicos, Oportunidade a Investigar

[Voltar para Inteligência Artificial](../README.md)

## Metadados

| Campo | Informação |
|---|---|
| Unidade Curricular | Inteligência Artificial |
| Professor | Rodrigo Rios |
| Curso | Análise e Desenvolvimento de Sistemas |
| Instituição | Faculdade Senac Pernambuco |
| Período | 5º período |
| Semestre | 2026.2 |
| Tipo | Atividade prática |
| Tema | Engenharia de Prompt e análise de dados públicos |
| Projeto relacionado | Projeto Integrador |
| Contexto | Empresas de tecnologia, economia criativa e serviços digitais de Recife |
| Objetivo | Identificar uma oportunidade relevante para investigação |
| Status | Concluído |

## Equipe

**Los Hermanos**

- Alisson Gustavo
- Allyson George
- Vitor Vieira
- Hericc Rocha
- Williami Durand

## Objetivo da atividade

A atividade teve como objetivo utilizar **Engenharia de Prompt associada à análise de dados públicos** para investigar oportunidades relacionadas ao Projeto Integrador.

O trabalho buscou evitar que uma hipótese de negócio fosse definida apenas a partir de percepções ou respostas produzidas por Inteligência Artificial.

O processo utilizado foi:

```text
Dados públicos
     ↓
Tratamento metodológico
     ↓
Evidências
     ↓
Hipóteses
     ↓
Evidências contrárias
     ↓
Decisão
     ↓
Próximo teste com usuários
```

A proposta central foi utilizar os dados como ponto de partida para investigação, sem afirmar como fato aquilo que as bases não conseguiam comprovar.

# 1. Bases analisadas

Foram utilizadas três bases principais.

```text
01_Empresas_Recife_Reais.xlsx

02_Credito_BNDES_PE_2020_2025.xlsx

03_Contratos_Recife_Reais.xlsx
```

As bases representam perspectivas diferentes.

## Empresas recentes de Recife

A primeira base foi utilizada para analisar empresas abertas entre 2022 e 2025 em atividades relacionadas principalmente a:

- Tecnologia.
- Serviços de informação.
- Publicidade.
- Atividades profissionais.
- Economia criativa.

## Crédito do BNDES

A segunda base permitiu analisar operações de crédito realizadas em Pernambuco e no Recife.

## Contratos municipais

A terceira base foi utilizada para investigar a presença de empresas recentes como fornecedoras em contratos públicos municipais.

# 2. Cuidados metodológicos

Um dos principais aprendizados da atividade foi compreender que os registros das bases não poderiam ser interpretados de maneira direta.

Foram estabelecidos diferentes cuidados.

## Linha não significa empresa

A base de empresas possuía:

```text
31.683 registros
```

mas esses registros correspondiam a:

```text
11.591 CNPJs distintos
```

Uma mesma empresa poderia aparecer mais de uma vez por possuir diferentes atividades econômicas.

Portanto:

```text
Linha da planilha
      ≠
Empresa distinta
```

## Empresa de tecnologia não significa startup

Outro cuidado importante foi:

```text
CNPJ em atividade tecnológica
        ≠
Startup
```

A classificação CNAE, isoladamente, não permite determinar se determinada empresa funciona como startup.

## Crédito não significa investimento-anjo

Também foi necessário diferenciar:

```text
Crédito BNDES
      ≠
Investimento-anjo
```

As duas formas de capital possuem naturezas diferentes.

## Contrato e aditivo não devem ser somados indiscriminadamente

A análise também considerou que aditivos poderiam multiplicar registros relacionados ao mesmo contrato.

Por isso, foi necessário evitar contagens duplicadas.

# 3. Evidência 1, público recente e numeroso

A primeira evidência analisada foi a existência de um conjunto relevante de empresas recentes nas áreas investigadas.

A base possuía:

```text
31.683 registros
```

correspondentes a:

```text
11.591 CNPJs distintos
```

considerando empresas abertas entre 2022 e 2025.

Os grupos com maior número de empresas distintas estavam associados principalmente a:

- Atividades profissionais.
- Publicidade.
- Tecnologia da Informação.
- Serviços de informação.

## Cálculo utilizado

```text
31.683 registros
÷
11.591 CNPJs
≈
2,73 registros por CNPJ
```

Esse cálculo reforçou a necessidade de não tratar cada linha da planilha como uma empresa diferente.

# 4. Evidência 2, baixa presença em contratos municipais

A segunda análise cruzou:

```text
Empresas recentes
       +
Fornecedores de contratos municipais
```

utilizando o CNPJ completo.

Inicialmente foram encontrados:

```text
40 CNPJs em comum
```

Após considerar somente contratos cuja vigência começou depois da abertura da empresa, restaram:

```text
34 empresas distintas
```

com:

```text
70 registros de contratos
```

## Percentual calculado

```text
34 ÷ 11.591 × 100
≈
0,29%
```

Isso significa que aproximadamente:

```text
0,29%
```

dos CNPJs distintos analisados apareceram como fornecedores com contrato iniciado após a abertura da empresa.

Consequentemente:

```text
≈ 99,71%
```

não apareceram nessa condição específica dentro da base analisada.

# 5. Interpretação correta da Evidência 2

A atividade enfatizou que esse resultado não permite concluir:

```text
"99,71% das empresas têm dificuldade
para conseguir contratos públicos."
```

Os dados apenas demonstram:

```text
Baixa presença na base
```

e não:

```text
Motivo da baixa presença
```

Não era possível saber, apenas com os dados disponíveis, se as empresas:

- Tentaram participar de licitações.
- Tinham interesse nesse mercado.
- Atendiam aos requisitos.
- Conheciam as oportunidades.
- Encontraram dificuldades durante o processo.

Portanto:

```text
Correlação observada
      ≠
Causa comprovada
```

# 6. Perfil dos contratos encontrados

Entre os 70 contratos das 34 empresas identificadas, aproximadamente:

```text
61,4%
```

estavam relacionados a:

- Eventos.
- Produção cultural.
- Audiovisual.
- Atividades criativas.

Esse resultado mostrou que existe um pequeno grupo de empresas recentes que conseguiu acessar o mercado público dentro do recorte analisado.

# 7. Evidência 3, operações do BNDES

A terceira análise utilizou dados de crédito do BNDES.

Foram identificadas em Pernambuco:

```text
2.622 operações automáticas

50 registros de operações não automáticas
```

No recorte de operações automáticas no Recife foram encontradas:

```text
628 operações
```

envolvendo:

```text
319 clientes distintos
```

# 8. Distribuição por porte

Entre as 628 operações analisadas:

| Porte | Operações |
|---|---:|
| Médio | 311 |
| Pequeno | 162 |
| Micro | 22 |
| Grande | 133 |

Também foram identificadas:

```text
73 operações
```

com indicador de inovação igual a **SIM**.

# 9. Participação de microempresas

Foram identificadas:

```text
22 operações de microporte
```

entre:

```text
628 operações
```

O cálculo foi:

```text
22 ÷ 628 × 100
≈
3,5%
```

Portanto, aproximadamente 3,5% das operações do recorte pertenciam a clientes classificados como microempresa.

# 10. Cruzamento com operações não automáticas

Ao comparar os:

```text
11.591 CNPJs
```

da base de empresas recentes com os clientes das operações não automáticas do BNDES, não foi encontrada correspondência por CNPJ completo.

Entretanto, a atividade deixou claro que isso não permite afirmar que essas empresas não possuem acesso a financiamento.

Existiam limitações importantes:

- Operações automáticas utilizavam identificadores mascarados.
- As bases analisadas não representam todas as fontes de financiamento.
- Crédito bancário não equivale a investimento-anjo.

Portanto:

```text
Nenhuma correspondência encontrada
        ≠
Nenhuma empresa financiada
```

# 11. Hipótese 1, acesso a contratos públicos

A primeira hipótese formulada foi:

> Empresas recentes de tecnologia e economia criativa podem ter dificuldade para acessar oportunidades de contratação pública.

## Evidência favorável

Apenas:

```text
34 de 11.591 CNPJs
```

apareceram com contratos iniciados após a abertura da empresa.

Percentual:

```text
≈ 0,29%
```

## Evidência contrária

As 34 empresas identificadas demonstram que empresas recentes conseguem acessar esse mercado.

Além disso, os dados não indicam:

- Quantas empresas tentaram participar.
- Quantas tiveram interesse.
- Quantas foram rejeitadas.
- Quais barreiras enfrentaram.

## Conclusão

```text
Hipótese possível
      ↓
Ainda não comprovada
```

Os dados mostram baixa presença, mas não explicam sua causa.

# 12. Hipótese 2, dificuldade de acesso a financiamento

A segunda hipótese foi:

> O principal problema dessas empresas pode ser a falta de acesso a financiamento.

## Evidências favoráveis

No recorte automático do BNDES:

```text
22 de 628 operações
```

eram de clientes classificados como microporte.

Também não houve correspondência por CNPJ completo entre empresas recentes e operações não automáticas.

## Evidência contrária

Esses resultados não demonstram ausência de financiamento.

As limitações incluem:

- CNPJs mascarados nas operações automáticas.
- Outras instituições financeiras não analisadas.
- Outras formas de capital.
- Diferença entre crédito e investimento-anjo.

## Conclusão

```text
Hipótese possível
      ↓
Necessita validação com usuários
```

# 13. Comparação das hipóteses

| Hipótese | Evidência favorável | Limitação |
|---|---|---|
| Dificuldade de acesso a contratos públicos | Baixa presença entre fornecedores | Não sabemos se as empresas tentaram acessar esse mercado |
| Falta de acesso a financiamento | Baixa participação de microporte e ausência de correspondência direta em parte da base | Dados não representam todas as formas de financiamento |

A atividade mostra que dados públicos podem gerar boas perguntas sem necessariamente fornecer respostas definitivas.

# 14. Público escolhido

Após a análise, o público selecionado foi:

> Empresas recentes de Recife ligadas à tecnologia, economia criativa e serviços digitais, especialmente aquelas abertas entre 2022 e 2025.

O trabalho manteve a ressalva:

```text
Empresa recente
      +
CNAE tecnológico
      ≠
Startup comprovada
```

Essa característica precisaria ser confirmada diretamente durante a pesquisa com usuários.

# 15. Oportunidade escolhida

A oportunidade selecionada foi investigar:

> Como empresas recentes conseguem acesso a financiamento, investidores e oportunidades de mercado, e quais dificuldades enfrentam para apresentar o negócio e encontrar parceiros adequados.

A escolha foi baseada principalmente em:

- Tamanho do público identificado.
- Baixa presença nos contratos municipais analisados.
- Baixa presença direta nas operações não automáticas do BNDES.
- Necessidade de compreender as causas por meio de pesquisa qualitativa.

# 16. O que os dados permitiram concluir

Os dados permitiram observar:

```text
Existe um público relevante
        ↓
Pouca presença nas bases analisadas
        ↓
Existem perguntas importantes
```

Mas não permitiram afirmar:

```text
Qual é a principal dor desse público?
```

Por isso, o próximo passo deixou de ser uma nova análise quantitativa e passou a ser uma investigação com usuários reais.

# 17. Próximo teste

A atividade propôs realizar entrevistas com aproximadamente:

```text
10 a 15 empresas
```

recentes das áreas de:

- Tecnologia.
- Economia criativa.
- Serviços digitais.

# 18. Perguntas propostas para entrevistas

## Pergunta 1

```text
A empresa já tentou conseguir investimento ou financiamento?
```

## Pergunta 2

```text
Qual foi a maior dificuldade encontrada?
```

## Pergunta 3

```text
Já procurou investidores-anjo?
```

## Pergunta 4

```text
Como atualmente encontra investidores ou parceiros?
```

## Pergunta 5

```text
Já tentou participar de contratos ou licitações públicas?
```

## Pergunta 6

```text
Qual dessas oportunidades é mais importante atualmente?

Investimento?
Crédito?
Clientes?
Parcerias?
```

## Pergunta 7

```text
O que faria a empresa confiar em uma plataforma
de conexão com investidores?
```

## Pergunta 8

```text
Quais informações sobre um investidor seriam necessárias
antes de iniciar uma conversa?
```

# 19. Objetivo das entrevistas

O objetivo da pesquisa qualitativa é descobrir se existe realmente uma dor relacionada a:

```text
Capital
   +
Investidores
   +
Parceiros
   +
Clientes
```

em vez de assumir a existência dessa necessidade apenas a partir dos dados públicos.

O fluxo esperado é:

```text
Dados quantitativos
        ↓
Indício
        ↓
Hipótese
        ↓
Entrevistas
        ↓
Evidência qualitativa
        ↓
Validação
```

# 20. Prompt 1, Decomposição

A primeira técnica utilizada foi a **decomposição do problema**.

O prompt solicitava analisar as três bases em etapas.

A estrutura incluía:

```text
1. Identificar recorte e unidade de análise
              ↓
2. Contar CNPJs distintos
              ↓
3. Cruzar empresas e contratos
              ↓
4. Verificar datas
              ↓
5. Cruzar dados do BNDES
              ↓
6. Analisar limitações
              ↓
7. Produzir evidências
              ↓
8. Formular hipóteses
              ↓
9. Buscar evidências contrárias
              ↓
10. Escolher oportunidade
```

# 21. Restrições do primeiro prompt

O prompt incluiu regras importantes.

## Não considerar empresa como startup automaticamente

```text
Empresa cadastrada
      ≠
Startup
```

## Não considerar crédito como investimento-anjo

```text
BNDES
  ≠
Investimento-anjo
```

## Não contar duplicidades

Era necessário controlar:

- Múltiplas atividades.
- Contratos.
- Aditivos.

Essas restrições reduziram o risco de interpretações incorretas.

# 22. Prompt 2, Saída estruturada e revisão

O segundo prompt utilizou duas técnicas:

```text
Saída estruturada
        +
Rubrica de revisão
```

A estrutura obrigatória solicitava:

```text
EVIDÊNCIA 1

EVIDÊNCIA 2

EVIDÊNCIA 3

HIPÓTESE 1

HIPÓTESE 2

DECISÃO

PRÓXIMO TESTE
```

Isso tornou a análise mais previsível e comparável.

# 23. Revisão metodológica

O segundo prompt também solicitou revisão explícita de possíveis erros.

Entre os pontos verificados estavam:

```text
Linhas versus CNPJs

CNPJ completo

Data do contrato

Contratos versus aditivos

Contratado versus desembolsado

Identificadores mascarados

Crédito versus investimento-anjo
```

A instrução central foi:

> Não apresentar como fato aquilo que os dados não conseguem comprovar.

# 24. Primeira análise versus resposta revisada

A primeira análise conseguia identificar tendências, mas corria o risco de gerar interpretações excessivamente amplas.

Após a revisão, foram incorporados controles adicionais.

## Antes

```text
Empresas recentes
      ↓
Possivelmente startups
```

## Depois

```text
Empresas recentes
      ↓
Não classificadas automaticamente como startups
```

## Antes

```text
Crédito
   ↓
Possivelmente relacionado diretamente
a investimento
```

## Depois

```text
Crédito
   ≠
Investimento-anjo
```

# 25. Melhorias introduzidas

A resposta revisada passou a:

- Contar CNPJs distintos.
- Considerar a data de abertura da empresa.
- Separar contratos de aditivos.
- Utilizar CNPJ completo quando disponível.
- Separar operações automáticas e não automáticas.
- Procurar evidências contrárias.
- Registrar limitações.
- Separar fatos de hipóteses.

# 26. Evidência contrária como técnica de qualidade

Um elemento relevante da atividade foi exigir evidência que pudesse contrariar a própria hipótese.

O raciocínio passa a ser:

```text
Tenho uma hipótese
      ↓
Procuro evidência favorável
      +
Procuro evidência contrária
      ↓
Comparo
      ↓
Conclusão provisória
```

Essa abordagem reduz o risco de procurar apenas informações que confirmem uma ideia inicial.

# 27. Controle de viés de confirmação

Sem esse cuidado:

```text
Hipótese
   ↓
Buscar somente dados favoráveis
   ↓
Confirmação aparente
```

Com a abordagem da atividade:

```text
Hipótese
   ↓
Dados favoráveis
   +
Dados contrários
   ↓
Análise crítica
```

# 28. Papel da Inteligência Artificial

A IA foi utilizada como ferramenta de apoio para:

- Decompor a análise.
- Organizar etapas.
- Estruturar evidências.
- Comparar hipóteses.
- Revisar interpretações.
- Controlar o formato da saída.

Entretanto, a IA não substituiu os controles metodológicos.

```text
IA
 ↓
Auxilia análise

Humano
 ↓
Define critérios
 ↓
Valida interpretação
 ↓
Controla conclusões
```

# 29. Relação com Engenharia de Prompt

A atividade demonstra uma evolução em relação a prompts simplesmente textuais.

Um bom prompt de análise de dados precisa controlar:

```text
Fonte
 ↓
Unidade de análise
 ↓
Filtros
 ↓
Cálculos
 ↓
Limitações
 ↓
Interpretação
```

Não basta solicitar:

```text
"Analise esses dados."
```

É necessário definir como a análise deve ocorrer.

# 30. Relação com o Mapa de Oportunidades

A atividade anterior trabalhou possíveis oportunidades no ecossistema.

```text
Mapa de Oportunidades
        ↓
Possíveis dores
        ↓
Hipóteses
```

A atividade de dados públicos adiciona:

```text
Dados
  ↓
Evidências
  ↓
Controle metodológico
  ↓
Revisão das hipóteses
```

O processo completo passa a ser:

```text
Mapa de oportunidades
        ↓
Hipótese
        ↓
Dados públicos
        ↓
Evidências
        ↓
Limitações
        ↓
Entrevistas
```

[Consultar Mapa de Oportunidades](../mapa-de-oportunidades-matchmaking/)

# 31. Relação com Engenharia de Prompt Avançada

A Engenharia de Prompt Avançada trabalhou:

- Decomposição.
- Encadeamento.
- Metaprompt.
- Refinamento.
- Evidências.

Nesta atividade, esses princípios foram aplicados a bases de dados.

```text
Prompt estruturado
       ↓
Dados públicos
       ↓
Análise
       ↓
Crítica
       ↓
Revisão
```

[Consultar Engenharia de Prompt Avançada](../engenharia-de-prompt-avancada/)

# 32. Relação com o ConectaStart

Esta atividade representa uma etapa importante do discovery do Projeto Integrador.

Em vez de assumir que:

```text
Startups precisam
de investidores
       ↓
Construir matchmaking
```

a equipe passou a perguntar:

```text
Existe um público relevante?
       ↓
Quais oportunidades acessa?
       ↓
Quais dificuldades aparecem nos dados?
       ↓
O que os dados não conseguem explicar?
       ↓
O que precisamos perguntar aos usuários?
```

Esse processo ajudou a transformar uma ideia inicial em um problema de pesquisa.

[Acessar Projeto Integrador](../../../projeto-integrador/)

# 33. Relação com a evolução posterior do ConectaStart

O Projeto Integrador posteriormente passou por redução de escopo e maior concentração nas fases de:

```text
Ideação
   +
Validação
```

com atenção especial ao relacionamento com mentores.

Este documento deve ser mantido porque registra uma etapa anterior do processo de descoberta.

```text
Hipótese inicial
      ↓
Dados
      ↓
Pesquisa
      ↓
Novos aprendizados
      ↓
Mudança de escopo
```

A mudança de direção faz parte do histórico de evolução do projeto.

# 34. Principais aprendizados

A atividade permitiu compreender que uma análise de dados não termina quando um número é calculado.

É necessário responder:

```text
O que foi contado?
       ↓
Qual é a unidade?
       ↓
Existe duplicidade?
       ↓
Qual filtro foi usado?
       ↓
O que o resultado prova?
       ↓
O que ele NÃO prova?
```

Outro aprendizado importante foi:

```text
Dado
 ≠
Conclusão automática
```

O dado precisa ser contextualizado.

Também ficou evidente que:

```text
Baixa frequência
      ≠
Dificuldade comprovada
```

e:

```text
Ausência em uma base
      ≠
Ausência no mundo real
```

# 35. Competências desenvolvidas

A atividade contribuiu para o desenvolvimento de competências relacionadas a:

- Inteligência Artificial.
- Engenharia de Prompt.
- Engenharia de Prompt Avançada.
- Análise de dados.
- Dados públicos.
- Decomposição.
- Saída estruturada.
- Revisão crítica.
- Formulação de hipóteses.
- Controle de viés.
- Evidência contrária.
- Validação de dados.
- Interpretação estatística.
- Discovery.
- Pesquisa com usuários.
- Pensamento crítico.
- Uso responsável de IA.

# 36. Fontes de dados utilizadas

O trabalho registra como fontes:

```text
01_Empresas_Recife_Reais.xlsx
31.683 registros
```

```text
02_Credito_BNDES_PE_2020_2025.xlsx
2.672 registros
```

```text
03_Contratos_Recife_Reais.xlsx
7.427 contratos
11.186 aditivos
```

Também foram mencionados:

- Portal de Dados Abertos do Recife.
- BNDES Data.
- Material da atividade da Faculdade Senac Pernambuco.

# Organização dos arquivos

```text
prompts-e-dados-publicos/
│
├── README.md
└── PI - Prompts e Dados Públicos- oportunidade a investigar.docx
```

# Documento original

```text
PI - Prompts e Dados Públicos- oportunidade a investigar.docx
```

# Navegação

[Voltar para Inteligência Artificial](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)

[Atividade anterior, Mapa de Oportunidades](../mapa-de-oportunidades-matchmaking/)
