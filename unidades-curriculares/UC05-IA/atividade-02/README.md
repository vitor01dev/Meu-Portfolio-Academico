# Engenharia de Prompt Avançada, Investigação de Oportunidades e Hipótese de Problema

[Voltar para Inteligência Artificial](../README.md)

## Metadados

| Campo | Informação |
|---|---|
| Unidade Curricular | Inteligência Artificial |
| Código | TADS040 |
| Professor | Rodrigo Rios |
| Curso | Análise e Desenvolvimento de Sistemas |
| Instituição | Faculdade Senac Pernambuco |
| Período | 5º período |
| Semestre | 2026.2 |
| Tipo | Atividade prática |
| Tema | Engenharia de Prompt Avançada |
| Projeto relacionado | ConectaStart |
| Contexto | Porto Digital e ecossistema local de startups |
| Status | Concluído |

## Equipe

- Alisson Gustavo
- Allyson George
- Hericc Rocha
- Vitor Vieira
- Willami Durand

## Objetivo da atividade

A atividade teve como objetivo aplicar técnicas de **Engenharia de Prompt Avançada** para investigar oportunidades relacionadas ao Projeto Integrador.

A proposta inicial considerava uma plataforma de matchmaking capaz de conectar startups nascentes do Porto Digital a mentores e investidores-anjo do Nordeste.

Entretanto, essa solução não foi tratada como resposta definitiva.

O objetivo foi investigar primeiro:

```text
Tema do PI
   ↓
Possíveis envolvidos
   ↓
Possíveis dores
   ↓
Evidências
   ↓
Lacunas
   ↓
Oportunidades
   ↓
Hipótese de problema
```

A atividade reforça que uma ideia de solução não deve ser tratada automaticamente como um problema validado.

# 1. Contexto da investigação

O tema do Projeto Integrador foi definido como:

```text
Startups
   +
Economia Criativa
   +
Ecossistema do Porto Digital
```

A solução inicial considerada foi:

```text
Plataforma de matchmaking
          ↓
Startups
Mentores
Investidores-anjo
```

Porém, durante esta etapa, o matchmaking foi tratado apenas como uma **hipótese inicial de solução**.

A investigação deveria identificar oportunidades antes de propor funcionalidades.

# 2. Solicitação inicial

O primeiro prompt utilizado foi espontâneo:

```text
Quero criar uma plataforma que conecte startups do Porto Digital
a mentores e investidores anjo.

Me dê ideias de funcionalidades e me diga quais problemas
essas startups costumam enfrentar.
```

## Resposta obtida

A resposta inicial sugeriu funcionalidades como:

- Cadastro de startups.
- Cadastro de mentores e investidores.
- Sistema de recomendação.
- Painel de mentorias.
- Espaço para pitch decks.
- Fórum de dúvidas.

Também apresentou problemas genéricos, como:

- Falta de capital.
- Dificuldade de validação.
- Falta de experiência em gestão.
- Dificuldade de conexão com investidores.

# 3. Diagnóstico do primeiro prompt

A equipe identificou quatro problemas principais na resposta inicial.

## Problema 1, mistura problema e solução

A IA começou a sugerir funcionalidades antes que qualquer problema tivesse sido investigado.

```text
Problema ainda desconhecido
        ↓
IA sugere funcionalidades
        ↓
Solução prematura
```

## Problema 2, generalização

A resposta tratava todas as startups como um grupo homogêneo.

Não distinguia aspectos como:

- Estágio.
- Situação.
- Tipo de empreendedor.
- Necessidade.
- Contexto.

## Problema 3, ausência de fontes

As afirmações pareciam plausíveis, mas não estavam acompanhadas de evidências.

```text
Afirmação plausível
      ≠
Fato comprovado
```

## Problema 4, ausência de critérios

Não existiam critérios definidos para avaliar se a resposta era adequada.

Isso dificultava determinar objetivamente a qualidade da saída.

# 4. Construção do prompt estruturado

Após o diagnóstico, foi construído um prompt mais controlado.

A estrutura utilizada incluiu:

| Componente | Conteúdo |
|---|---|
| Objetivo | Explorar o tema do PI e identificar oportunidades reais sem propor solução |
| Papel | Facilitador socrático especializado em discovery |
| Tarefa | Fazer perguntas, organizar hipóteses e apontar lacunas |
| Entradas | Tema do PI e hipótese inicial de matchmaking |
| Contexto | Ecossistema de startups do Porto Digital |
| Restrições | Não responder pela equipe, não inventar dados e não propor funcionalidades |
| Critérios | Relacionar envolvido, situação, possível dor, impacto, alternativa atual e evidência |
| Formato | Tabela estruturada |
| Início | Levantar hipóteses e selecionar oportunidades para validação |

A lógica passou a ser:

```text
Objetivo
   ↓
Contexto
   ↓
Restrições
   ↓
Critérios
   ↓
Formato
   ↓
Investigação
```

# 5. Primeira rodada estruturada

A primeira rodada produziu hipóteses relacionadas a diferentes envolvidos.

## Startups early-stage

Possível dor:

```text
Dificuldade de encontrar mentor
com expertise no setor adequado
```

Evidência inicial:

```text
Suposição da equipe
sem fonte externa
```

## Investidores-anjo

Possível dor:

```text
Dificuldade de triagem
por falta de padronização
dos pitch decks
```

Evidência inicial:

```text
Suposição da equipe
sem fonte externa
```

## Gestores do Porto Digital

Possível dor:

```text
Falta de dados centralizados
sobre conexões geradas
```

Evidência inicial:

```text
Suposição da equipe
sem fonte externa
```

# 6. Problema encontrado na primeira rodada

A própria estrutura do prompt exigia uma coluna de evidências.

Entretanto:

```text
Hipóteses
   ↓
Nenhuma evidência real
   ↓
Apenas suposições
```

Isso criou uma inconsistência entre os critérios definidos e a resposta produzida.

A principal lacuna passou a ser:

> Nenhuma das oportunidades possuía evidência externa suficiente.

# 7. Refinamento do prompt

O prompt foi modificado para exigir fontes públicas sempre que possível.

A nova regra foi:

```text
Existe evidência pública?
       ↓
      Sim
       ↓
Registrar fonte

       ou

      Não
       ↓
Marcar como
"suposição não verificada"
```

Essa mudança evitou que hipóteses fossem apresentadas como fatos.

# 8. Pesquisa de evidências

Após o refinamento, foram utilizados dados provenientes de fontes externas, incluindo:

- Pesquisa sobre Investimento Anjo no Brasil de 2025.
- Observatório Sebrae Startups.
- Anjos do Brasil.
- Informações sobre programas do Porto Digital.

A pesquisa permitiu substituir parte das suposições iniciais por evidências rastreáveis.

# 9. Mapa de oportunidades

A versão final do mapa considerou cinco oportunidades.

## Oportunidade 1, Mentoria especializada

### Envolvido

Startups early-stage.

### Situação

Busca por mentoria especializada por área.

### Possível dor

Dificuldade de encontrar mentor com expertise adequada.

### Evidência

Programas locais oferecem mentorias, porém não havia evidência pública suficiente sobre a adequação entre mentor e startup.

### Lacuna

Não existiam dados públicos sobre a taxa de adequação do pareamento.

### Oportunidade percebida

Investigar critérios utilizados no pareamento entre startup e mentor.

---

## Oportunidade 2, Triagem por investidores-anjo

### Envolvido

Investidores-anjo.

### Situação

Avaliação de startups candidatas a investimento.

### Possível dor

Dificuldade de triagem devido à falta de informações comparáveis entre propostas.

### Evidência

A pesquisa Sebrae e Anjos do Brasil de 2025 foi utilizada como evidência externa.

O material registra que:

```text
92% dos investidores pesquisados
relatam dificuldade em localizar
startups qualificadas
```

e:

```text
59,5%
relatam dificuldade em acessar
boas oportunidades
```

### Lacuna

Ainda não estava claro se o principal problema era:

- Volume.
- Qualidade das informações.
- Canal de acesso.
- Padronização.

### Oportunidade percebida

Investigar se informações mais comparáveis poderiam reduzir o esforço de triagem.

---

## Oportunidade 3, Métricas do ecossistema

### Envolvido

Gestores e curadores do Porto Digital.

### Situação

Acompanhamento dos resultados dos programas.

### Possível dor

Dificuldade para medir conexões geradas entre startups, mentores e investidores.

### Lacuna

A hipótese ainda não possuía evidência suficiente.

---

## Oportunidade 4, Feedback estruturado

### Envolvido

Empreendedores em validação.

### Situação

Busca por feedback estruturado.

### Possível dor

Dependência de redes informais e mentorias pontuais.

### Evidência

Programas locais possuem duração limitada.

### Lacuna

Não estava claro o que acontece após o encerramento dos programas.

### Oportunidade percebida

Investigar a continuidade do acompanhamento.

---

## Oportunidade 5, Relacionamento com investidores

### Envolvido

Startups pós-incubação.

### Situação

Busca por novos aportes.

### Possível dor

Dificuldade de acompanhar relacionamento e due diligence com diferentes investidores.

### Evidência

Não foi encontrada evidência local suficiente.

### Classificação

```text
Suposição não verificada
```

# 10. Priorização das oportunidades

As oportunidades priorizadas para aprofundamento foram:

```text
1. Mentoria especializada

2. Triagem de startups por investidores-anjo

3. Feedback estruturado e continuidade
```

As oportunidades relacionadas a métricas de gestão e relacionamento pós-investimento ficaram fora da priorização por falta de evidências suficientes ou menor relação com o núcleo do PI.

# 11. Oportunidade escolhida

A equipe selecionou a **Oportunidade 2**.

A razão principal foi a existência de uma base de evidência externa mais consistente.

A oportunidade escolhida foi:

> Investidores-anjo podem enfrentar dificuldade de triagem eficiente de startups candidatas devido à falta de informações comparáveis entre propostas.

A atividade manteve a regra:

```text
Investigar problema
      ↓
Não propor solução
```

# 12. Engenharia de Prompt Avançada aplicada

Para aprofundar a investigação, foram utilizados cinco prompts encadeados.

```text
Prompt 1
Decomposição
     ↓
Prompt 2
Encadeamento
     ↓
Prompt 3
Evidências
     ↓
Prompt 4
Metaprompt
     ↓
Prompt 5
Refinamento
```

# 13. Prompt 1, Decomposição

A primeira técnica consistiu em decompor a oportunidade.

O prompt solicitava analisar:

- Quem é afetado.
- Qual é a dor.
- Possíveis causas.
- Evidências necessárias.
- O que ainda precisa ser validado.

## Afetado direto

```text
Investidor-anjo
```

## Afetado indireto

```text
Startup early-stage
```

Uma startup poderia ser prejudicada caso a forma de apresentação das informações dificultasse sua avaliação.

## Dor

Tempo e esforço gastos na triagem de propostas heterogêneas.

## Possíveis causas

Foram levantadas hipóteses como:

1. Ausência de formato ou conteúdo comparável.
2. Startups não sabem quais dados apresentar.
3. Alto volume de propostas.
4. Falta de dados de tração em fases muito iniciais.

# 14. Prompt 2, Classificação das causas

A saída do primeiro prompt foi utilizada como entrada para o segundo.

Cada causa foi classificada como:

```text
Fato

Hipótese razoável

Hipótese com apoio parcial

Suposição não verificada
```

## Exemplo

### Alto volume de propostas

Foi classificado como:

```text
Fato com evidência externa
```

A atividade registrou que 75% dos investidores pesquisados recebiam oportunidades com frequência mensal ou superior.

### Falta de dados de tração

Foi classificada como:

```text
Suposição não verificada
```

Não havia evidência específica suficiente para sustentá-la.

# 15. Prompt 3, Busca de evidências externas

O terceiro prompt solicitou evidências públicas sobre dificuldades de investidores-anjo durante a avaliação de startups.

Entre as evidências utilizadas estavam:

```text
92%
dificuldade em localizar startups qualificadas
```

e:

```text
59,5%
dificuldade em acessar boas oportunidades
```

Também foram considerados:

- Guias de análise de pitch.
- Programas de preparação de startups.
- Programas de pré-incubação do Porto Digital.

# 16. Prompt 4, Metaprompt

A próxima etapa foi solicitar que a IA criticasse a própria investigação.

O metaprompt buscava encontrar:

- Ambiguidades.
- Generalizações.
- Vieses.
- Lacunas de evidência.
- Problemas conceituais.

## Problemas identificados

### Evidência nacional

As principais estatísticas disponíveis eram nacionais.

Elas não demonstravam automaticamente que o mesmo comportamento ocorria no Porto Digital.

```text
Evidência nacional
      ≠
Evidência local
```

### Tipos diferentes de investidores

A investigação tratava inicialmente investidores-anjo como um grupo único.

Entretanto, poderiam existir diferenças entre:

```text
Investidor individual

e

Rede organizada de investidores
```

### Falta de evidência qualitativa

Ainda não existiam entrevistas locais suficientes para confirmar a hipótese.

### Conceito de padronização

O termo estava pouco definido.

Poderia significar:

- Formato visual.
- Conteúdo.
- Canal.
- Campos obrigatórios.

# 17. Prompt 5, Refinamento

O quinto prompt revisou a hipótese considerando as críticas produzidas pelo metaprompt.

Foram realizadas três mudanças principais.

## 1. Escopo da evidência

Antes:

```text
Evidência apresentada
como aplicável ao ecossistema
```

Depois:

```text
Evidência nacional
com validação local pendente
```

## 2. Tipo de investidor

Antes:

```text
Investidores-anjo
```

Depois:

```text
Investidor individual
        +
Rede organizada
```

## 3. Definição de padronização

Antes:

```text
Formato do pitch
```

Depois:

```text
Conteúdo mínimo comparável
entre propostas
```

# 18. Saída estruturada

A investigação também foi organizada em um formato estruturado.

Exemplo simplificado:

```json
{
  "oportunidade": "triagem de startups por investidores anjo",
  "envolvido_principal": "investidor anjo",
  "envolvido_secundario": "startup early-stage",
  "dor": "dificuldade de triagem eficiente",
  "evidencias": [],
  "lacunas": [],
  "status": "hipótese de problema, não validada"
}
```

A saída estruturada facilita:

- Comparação.
- Reuso.
- Processamento.
- Avaliação.
- Integração futura com sistemas.

# 19. Rubrica de avaliação

A equipe criou uma rubrica para avaliar a qualidade da investigação.

| Critério | Nota |
|---|---:|
| Aderência ao tema | 2 |
| Evidências | 2 |
| Estrutura | 2 |
| Técnica | 2 |
| Refinamento | 2 |
| Total | 10/10 |

Os critérios avaliaram se a investigação:

- Respeitou o escopo.
- Utilizou evidências.
- Seguiu o formato.
- Aplicou corretamente as técnicas.
- Refinou a resposta com base em crítica explícita.

# 20. Comparação entre versões

A atividade comparou a investigação antes e depois do metaprompt.

| Aspecto | Versão 1 | Versão 2 |
|---|---|---|
| Evidência | Tratada de forma ampla | Escopo nacional explicitado |
| Investidores | Grupo único | Individual e rede |
| Padronização | Conceito vago | Conteúdo mínimo comparável |
| Incerteza | Misturada às afirmações | Separada como ponto a validar |

O objetivo da comparação não era verificar qual texto era maior.

O objetivo era identificar quais falhas haviam sido corrigidas.

```text
Qualidade
   ≠
Quantidade de texto
```

# 21. Hipótese final de problema

A investigação chegou à hipótese de que investidores-anjo que avaliam startups do ecossistema do Porto Digital **podem** enfrentar dificuldade de triagem eficiente.

Entre os fatores investigados estavam:

- Volume de oportunidades.
- Canais informais.
- Falta de conteúdo mínimo comparável.
- Heterogeneidade dos pitches.

A formulação foi mantida como hipótese e não como certeza.

# 22. Pontos ainda não validados

A equipe registrou três questões que ainda precisavam ser investigadas.

## 1. Validação local

É necessário confirmar se investidores que atuam especificamente no ecossistema do Porto Digital enfrentam o mesmo problema identificado em pesquisas nacionais.

## 2. Perfil do investidor

É necessário avaliar possíveis diferenças entre:

- Investidores individuais.
- Redes organizadas.

## 3. Conteúdo mínimo comparável

É necessário descobrir quais informações os investidores realmente consideram fundamentais para comparar propostas.

# 23. Princípio metodológico

A atividade reforça:

```text
Hipótese
   ≠
Certeza
```

Uma hipótese representa uma conclusão provisória baseada nas evidências atualmente disponíveis.

O fluxo adequado é:

```text
Hipótese
   ↓
Evidência
   ↓
Lacuna
   ↓
Validação
   ↓
Nova evidência
   ↓
Refinamento
```

# 24. Principais técnicas utilizadas

## Decomposição

Dividir um problema amplo em partes menores.

```text
Problema
   ↓
Envolvidos
   ↓
Dor
   ↓
Causas
   ↓
Evidências
```

## Encadeamento

Utilizar a saída de um prompt como entrada do próximo.

```text
Prompt 1
   ↓
Resposta 1
   ↓
Prompt 2
   ↓
Resposta 2
```

## Metaprompt

Pedir ao modelo que critique a investigação.

```text
Resposta
   ↓
Crítica
   ↓
Falhas
   ↓
Refinamento
```

## Saída estruturada

Definir um formato previsível para a resposta.

## Refinamento

Modificar o prompt ou a hipótese a partir das falhas encontradas.

# 25. Relação com o ConectaStart

A atividade teve impacto direto na evolução do Projeto Integrador.

O processo inicial poderia ter sido:

```text
Ideia de matchmaking
      ↓
Construir plataforma
```

A Engenharia de Prompt Avançada ajudou a substituir esse fluxo por:

```text
Ideia inicial
     ↓
Investigação
     ↓
Oportunidades
     ↓
Hipóteses
     ↓
Evidências
     ↓
Lacunas
     ↓
Validação
     ↓
Problema
     ↓
Solução
```

Isso reduz o risco de construir funcionalidades antes de compreender o problema.

[Acessar Projeto Integrador](../../../projeto-integrador/)

# 26. Principais aprendizados

A atividade permitiu compreender que Engenharia de Prompt Avançada não significa apenas escrever instruções maiores.

Ela envolve construir um processo de investigação.

```text
Perguntar
   ↓
Analisar
   ↓
Criticar
   ↓
Buscar evidência
   ↓
Refinar
   ↓
Comparar
```

Outro aprendizado importante foi a necessidade de controlar o grau de certeza das respostas.

```text
Parece verdadeiro
      ≠
Está comprovado
```

Por isso, o processo precisa distinguir:

```text
Fato
Hipótese
Suposição
Lacuna
```

Também foi possível perceber que um modelo de IA pode ajudar a organizar uma investigação, mas não substitui a necessidade de coleta de evidências com usuários reais.

# Competências desenvolvidas

A atividade contribuiu para desenvolver competências relacionadas a:

- Engenharia de Prompt Avançada.
- Decomposição.
- Encadeamento de prompts.
- Metaprompting.
- Refinamento.
- Saída estruturada.
- Discovery.
- Investigação de problemas.
- Construção de hipóteses.
- Análise de evidências.
- Identificação de vieses.
- Pensamento crítico.
- Validação.
- Uso responsável de Inteligência Artificial.

# Organização dos arquivos

```text
engenharia-de-prompt-avancada/
│
├── README.md
└── Atividade sobre engenharia de prompt avançada(1).pdf
```

# Documento original

```text
Atividade sobre engenharia de prompt avançada(1).pdf
```

# Navegação

[Voltar para Inteligência Artificial](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)

[Próxima atividade, Mapa de Oportunidades](../mapa-de-oportunidades-matchmaking/)
