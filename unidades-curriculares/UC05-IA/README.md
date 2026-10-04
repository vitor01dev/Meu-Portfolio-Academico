# UC05, Inteligência Artificial

[Voltar ao Portfólio Acadêmico](../../README.md)

## Metadados

| Campo | Informação |
|---|---|
| Unidade Curricular | Inteligência Artificial |
| Professor | Rodrigo Rios |
| Curso | Análise e Desenvolvimento de Sistemas |
| Instituição | Faculdade Senac Pernambuco |
| Período | 5º período |
| Semestre | 2026.2 |
| Área | Inteligência Artificial, Engenharia de Prompt e análise de dados |
| Projeto relacionado | ConectaStart |
| Status | Em andamento |

## Sobre a Unidade Curricular

A Unidade Curricular de **Inteligência Artificial** trabalha conceitos e práticas relacionados ao uso de sistemas de IA, especialmente modelos de linguagem, Engenharia de Prompt, estruturação de contexto, refinamento de respostas, análise crítica de evidências e aplicação da IA como apoio à investigação de problemas.

Durante as atividades, a Inteligência Artificial não é utilizada apenas como ferramenta para gerar respostas.

O foco está em aprender a estruturar interações que permitam:

- Definir objetivos.
- Fornecer contexto.
- Estabelecer restrições.
- Controlar o formato da saída.
- Decompor problemas.
- Encadear prompts.
- Refinar respostas.
- Identificar suposições.
- Separar fatos de hipóteses.
- Utilizar dados públicos.
- Avaliar criticamente resultados produzidos por IA.

# Organização da UC

Com os arquivos atualmente disponíveis, a estrutura pode ser organizada da seguinte forma:

```text
uc05-inteligencia-artificial/
│
├── README.md
│
├── engenharia-de-prompt/
│   └── README.md
│
├── engenharia-de-prompt-avancada/
│   ├── README.md
│   └── Atividade sobre engenharia de prompt avançada(1).pdf
│
├── mapa-de-oportunidades-matchmaking/
│   ├── README.md
│   └── Entrega_Mapa_de_Oportunidades_Matchmaking (1) (1)-1.pdf
│
├── prompts-e-dados-publicos/
│   ├── README.md
│   └── PI - Prompts e Dados Públicos- oportunidade a investigar.docx
│
├── retroalimentacao-de-dados/
│   └── README.md
│
└── pacotes-de-contexto/
    └── README.md
```

> Alguns arquivos ainda não foram localizados. Eles poderão ser adicionados posteriormente sem necessidade de alterar a estrutura principal da UC.

# Conteúdos estudados

## 1. Engenharia de Prompt

A Engenharia de Prompt trabalha a construção de instruções capazes de orientar modelos de linguagem de forma mais controlada.

Um prompt pode ser estruturado considerando elementos como:

```text
Objetivo
   ↓
Papel
   ↓
Tarefa
   ↓
Entradas
   ↓
Contexto
   ↓
Restrições
   ↓
Critérios
   ↓
Formato de saída
```

A qualidade da resposta depende não apenas do modelo utilizado, mas também da clareza das instruções e das informações fornecidas.

## Problema de prompts vagos

Um prompt pouco específico pode gerar:

- Generalizações.
- Suposições.
- Respostas inconsistentes.
- Informações não verificadas.
- Falta de critérios de avaliação.

Exemplo:

```text
Prompt vago
    ↓
Modelo interpreta livremente
    ↓
Suposições
    ↓
Resposta difícil de avaliar
```

## Prompt estruturado

```text
Objetivo claro
      +
Contexto
      +
Restrições
      +
Critérios
      +
Formato
      ↓
Resposta mais controlável
```

---

# 2. Engenharia de Prompt Avançada

A atividade de Engenharia de Prompt Avançada foi aplicada ao contexto do **Projeto Integrador ConectaStart**.

O tema analisado foi:

```text
Startups
   +
Mentores
   +
Investidores-anjo
   +
Ecossistema de inovação
   ↓
Investigação de oportunidades
```

A atividade parte de uma premissa importante:

> A solução inicialmente imaginada não deve ser tratada automaticamente como resposta correta para o problema.

O matchmaking foi utilizado inicialmente apenas como hipótese.

## Prompt espontâneo

A primeira solicitação foi semelhante a:

```text
Quero criar uma plataforma que conecte startups do Porto Digital
a mentores e investidores-anjo.

Me dê ideias de funcionalidades e diga quais problemas essas
startups costumam enfrentar.
```

O resultado apresentou problemas metodológicos.

Entre eles:

- Mistura entre problema e solução.
- Sugestão prematura de funcionalidades.
- Generalização de startups.
- Falta de fontes.
- Ausência de critérios de avaliação.

O aprendizado foi:

```text
Solução imaginada
      ≠
Problema validado
```

## Prompt estruturado

A atividade evoluiu para uma estrutura mais controlada.

| Componente | Função |
|---|---|
| Objetivo | Investigar oportunidades reais |
| Papel | Facilitador especializado em discovery |
| Tarefa | Fazer perguntas e organizar hipóteses |
| Entradas | Tema do PI e contexto |
| Contexto | Ecossistema de startups |
| Restrições | Não inventar dados ou propor solução |
| Critérios | Separar fatos, hipóteses e lacunas |
| Saída | Tabela estruturada |

O princípio utilizado foi:

```text
Problema
   ↓
Hipótese
   ↓
Evidência
   ↓
Lacuna
   ↓
Validação
```

## Separação entre fatos e hipóteses

Um dos elementos centrais da atividade foi evitar apresentar suposições como fatos.

A classificação utilizada incluiu:

```text
FATO
Possui evidência verificável

HIPÓTESE
Possui algum apoio, mas precisa de validação

SUPOSIÇÃO
Ainda não possui evidência
```

Essa distinção contribui para reduzir respostas excessivamente confiantes produzidas por IA.

---

# 3. Mapa de Oportunidades

Outra atividade relacionada ao Projeto Integrador consistiu na construção de um **Mapa de Oportunidades**.

O objetivo não era definir imediatamente o produto final.

A intenção era identificar situações que mereciam investigação.

## Participantes do ecossistema

Foram identificados:

- Startups.
- Investidores.
- Mentores.
- Aceleradoras.
- Hubs de inovação.
- Instituições de apoio.

## Estrutura utilizada

```text
Envolvido
   ↓
Situação
   ↓
Possível dor
   ↓
Evidência ou lacuna
   ↓
Oportunidade percebida
```

## Oportunidades analisadas

Entre as oportunidades investigadas estavam:

### Encontrar investidores compatíveis

Hipótese:

Startups podem enfrentar dificuldade para encontrar investidores alinhados a:

- Setor.
- Estágio.
- Necessidade financeira.
- Tipo de negócio.

### Encontrar startups compatíveis

Hipótese:

Investidores podem enfrentar dificuldade para localizar startups compatíveis com seus critérios.

### Primeiro contato

Hipótese:

Mesmo quando existe interesse, pode haver dificuldade em estabelecer o primeiro contato entre as partes.

### Apresentação das startups

Hipótese:

Startups podem não saber quais informações são mais importantes para avaliação de investidores.

### Processo de captação

Hipótese:

Existem diferentes gargalos possíveis ao longo da jornada de busca por capital.

## Priorização

As três oportunidades inicialmente priorizadas foram:

```text
1. Encontrar investidores compatíveis

2. Encontrar startups compatíveis

3. Melhorar o primeiro contato
```

O documento reforça que essas dores ainda deveriam ser validadas com os envolvidos antes de serem tratadas como problemas comprovados.

---

# 4. Da oportunidade à hipótese de problema

A investigação foi aprofundada utilizando técnicas de Engenharia de Prompt Avançada.

Foram utilizados cinco prompts encadeados.

```text
Prompt 1
Decomposição
    ↓
Prompt 2
Classificação
    ↓
Prompt 3
Busca de evidências
    ↓
Prompt 4
Metaprompt
    ↓
Prompt 5
Refinamento
```

# Decomposição

A oportunidade foi dividida em:

- Quem é afetado.
- Dor.
- Possíveis causas.
- Evidências necessárias.
- Pontos ainda não validados.

Exemplo:

```text
Investidor
    ↓
Recebe propostas
    ↓
Precisa avaliar
    ↓
Informações heterogêneas
    ↓
Maior esforço de triagem
```

# Encadeamento de prompts

A saída de um prompt foi utilizada como entrada para o próximo.

```text
Prompt A
   ↓
Resposta
   ↓
Entrada do Prompt B
   ↓
Resposta refinada
```

Essa técnica permite aprofundar progressivamente a análise.

# Metaprompt

O metaprompt foi utilizado para pedir que o próprio modelo criticasse a investigação.

A instrução buscava identificar:

- Ambiguidades.
- Generalizações.
- Vieses.
- Lacunas.
- Suposições.
- Fragilidade das evidências.

O processo pode ser representado por:

```text
Resposta
   ↓
Crítica da própria resposta
   ↓
Problemas encontrados
   ↓
Refinamento
```

# Refinamento

Após a crítica, a hipótese foi modificada.

Entre as correções realizadas estavam:

- Identificar que determinadas evidências eram nacionais e não locais.
- Separar investidor individual de redes de investidores.
- Definir melhor o conceito de padronização.
- Registrar explicitamente pontos ainda não validados.

O aprendizado central foi:

```text
Resposta maior
   ≠
Resposta melhor

Resposta melhor
   =
Falhas identificadas e corrigidas
```

---

# 5. Uso de dados públicos

Outra atividade importante da UC utilizou dados públicos para investigar oportunidades relacionadas ao PI.

Foram analisadas bases referentes a:

- Empresas recentes de Recife.
- Operações do BNDES.
- Contratos municipais.

O objetivo era utilizar IA para apoiar análise sem ultrapassar aquilo que os dados realmente permitiam concluir.

## Controle metodológico

A atividade trabalhou questões como:

```text
Linha de planilha
      ≠
Empresa única
```

e:

```text
Crédito do BNDES
      ≠
Investimento-anjo
```

e ainda:

```text
Empresa de tecnologia
      ≠
Automaticamente uma startup
```

Essas distinções foram importantes para evitar conclusões incorretas.

# Evidência 1

A base de empresas possuía:

```text
31.683 registros
```

correspondentes a:

```text
11.591 CNPJs distintos
```

Isso demonstrou a importância de identificar corretamente a unidade de análise.

```text
Registros
    ↓
Eliminar duplicidade conceitual
    ↓
CNPJs distintos
```

# Evidência 2

O cruzamento entre empresas recentes e contratos municipais encontrou uma quantidade reduzida de correspondências.

Depois de considerar contratos iniciados após a abertura da empresa, foram identificadas:

```text
34 empresas distintas
```

dentro do universo analisado.

A conclusão correta não foi:

```text
"Essas empresas não conseguem contratos públicos."
```

A conclusão foi mais limitada:

```text
"A presença dessas empresas na base analisada é baixa,
mas os dados não demonstram a causa."
```

Essa diferença representa um aprendizado importante em análise de dados.

# Evidência 3

Os dados do BNDES também foram utilizados para investigar acesso a financiamento.

Entretanto, o próprio trabalho reconheceu limitações como:

- Identificadores mascarados.
- Diferença entre crédito e investimento.
- Impossibilidade de classificar automaticamente empresas como startups.

Portanto:

```text
Ausência de correspondência
        ≠
Ausência de financiamento
```

# 6. Construção de hipóteses

A análise produziu duas hipóteses principais.

## Hipótese 1

Empresas recentes de tecnologia e economia criativa podem enfrentar dificuldades para acessar oportunidades de contratação pública.

A evidência demonstrava baixa presença na base.

Entretanto:

```text
Baixa presença
     ≠
Dificuldade comprovada
```

Pode haver outros motivos.

## Hipótese 2

O principal problema poderia estar relacionado ao acesso a financiamento.

Novamente, os dados não permitiam confirmar essa conclusão.

Por isso:

```text
Dados
   ↓
Indício
   ↓
Hipótese
   ↓
Validação com pessoas
```

# 7. Público escolhido para investigação

O público definido foi:

> Empresas recentes de Recife ligadas à tecnologia, economia criativa e serviços digitais, principalmente empresas abertas entre 2022 e 2025.

A atividade deixou explícito que esse grupo não deve ser automaticamente classificado como startups.

# Oportunidade escolhida

A oportunidade definida foi investigar:

- Acesso a financiamento.
- Acesso a investidores.
- Acesso a clientes.
- Acesso a parceiros.
- Dificuldades na apresentação do negócio.

# Próximo teste

A proposta era realizar entrevistas com aproximadamente:

```text
10 a 15 empresas
```

As entrevistas deveriam investigar questões como:

- Tentativas anteriores de conseguir investimento.
- Dificuldades encontradas.
- Busca por investidores-anjo.
- Busca por parceiros.
- Participação em contratos públicos.
- Prioridades atuais.
- Critérios de confiança.
- Informações necessárias sobre investidores.

O princípio adotado foi:

```text
Dados públicos
      ↓
Hipótese
      ↓
Entrevista
      ↓
Evidência qualitativa
      ↓
Validação
```

---

# 8. Saída estruturada

A UC também trabalhou o conceito de controlar o formato da resposta da IA.

Exemplo:

```json
{
  "oportunidade": "triagem de startups",
  "envolvido_principal": "investidor",
  "dor": "dificuldade de análise",
  "evidencias": [],
  "lacunas": [],
  "status": "hipótese não validada"
}
```

A saída estruturada facilita:

- Comparação.
- Reuso.
- Processamento.
- Validação.
- Integração com sistemas.

# 9. Rubrica de avaliação

Uma das atividades também utilizou uma rubrica para avaliar a própria investigação.

Os critérios incluíram:

- Aderência ao tema.
- Qualidade das evidências.
- Estrutura.
- Técnica utilizada.
- Refinamento.

Isso demonstra outro princípio importante:

```text
Gerar resposta
      ↓
Definir critérios
      ↓
Avaliar
      ↓
Refinar
```

# 10. Retroalimentação de dados

Embora nem todos os arquivos dessa atividade estejam disponíveis no momento, o conceito pode ser relacionado às atividades já documentadas.

Retroalimentação significa utilizar resultados anteriores como nova entrada.

```text
Entrada
   ↓
Modelo
   ↓
Resultado
   ↓
Avaliação
   ↓
Feedback
   ↓
Nova entrada
```

No contexto de prompts:

```text
Prompt inicial
     ↓
Resposta
     ↓
Crítica
     ↓
Correção
     ↓
Prompt refinado
     ↓
Resposta melhorada
```

No ConectaStart:

```text
Match
  ↓
Interação
  ↓
Feedback
  ↓
Dados
  ↓
Análise
  ↓
Melhoria do matchmaking
```

# 11. Pacotes de contexto

O arquivo específico desta atividade ainda será adicionado posteriormente.

A ideia de pacote de contexto pode ser documentada como a organização das informações necessárias para que um modelo compreenda corretamente uma tarefa.

Uma estrutura possível é:

```text
Identidade do projeto
        +
Objetivo
        +
Contexto
        +
Dados
        +
Regras
        +
Restrições
        +
Exemplos
        +
Formato esperado
```

O objetivo é reduzir a necessidade de explicar todo o cenário novamente em cada interação.

> O README específico dessa atividade deverá ser revisado quando o arquivo original for adicionado ao portfólio.

# Relação com o Projeto Integrador

A UC de Inteligência Artificial possui forte relação com o **ConectaStart**.

As atividades contribuíram principalmente para a fase de descoberta e validação do problema.

```text
ConectaStart
     ↓
Ideia inicial
     ↓
Engenharia de Prompt
     ↓
Mapa de oportunidades
     ↓
Hipóteses
     ↓
Dados públicos
     ↓
Evidências
     ↓
Lacunas
     ↓
Entrevistas
     ↓
Validação
```

Esse processo evita um erro comum:

```text
Ideia de solução
      ↓
Construir imediatamente
```

e substitui por:

```text
Ideia
  ↓
Investigar
  ↓
Coletar evidências
  ↓
Validar
  ↓
Definir problema
  ↓
Projetar solução
```

# Competências desenvolvidas

As atividades desta Unidade Curricular contribuem para desenvolver competências relacionadas a:

- Engenharia de Prompt.
- Engenharia de Prompt Avançada.
- Decomposição de problemas.
- Encadeamento de prompts.
- Metaprompting.
- Refinamento.
- Saída estruturada.
- Uso de contexto.
- Pensamento crítico.
- Análise de evidências.
- Investigação de hipóteses.
- Uso responsável de IA.
- Análise de dados públicos.
- Identificação de limitações dos dados.
- Diferenciação entre fato e hipótese.
- Discovery.
- Validação de problemas.
- Retroalimentação.
- Organização de contexto.

# Status das atividades

## Documentos disponíveis

- [x] Engenharia de Prompt Avançada
- [x] Investigação de Oportunidades e Hipótese de Problema
- [x] Mapa de Oportunidades, Matchmaking
- [x] Prompts e Dados Públicos

## Materiais ainda a localizar

- [ ] Engenharia de Prompt, atividade inicial
- [ ] Retroalimentação de Dados, arquivo específico
- [ ] Pacotes de Contexto, arquivo específico

Esses documentos podem ser adicionados posteriormente sem alterar a arquitetura da UC.

# Organização atual

```text
uc05-inteligencia-artificial/
│
├── README.md
│
├── engenharia-de-prompt/
│
│   └── README.md
│
├── engenharia-de-prompt-avancada/
│   ├── README.md
│   └── Atividade sobre engenharia de prompt avançada(1).pdf
│
├── mapa-de-oportunidades-matchmaking/
│   ├── README.md
│   └── Entrega_Mapa_de_Oportunidades_Matchmaking (1) (1)-1.pdf
│
├── prompts-e-dados-publicos/
│   ├── README.md
│   └── PI - Prompts e Dados Públicos- oportunidade a investigar.docx
│
├── retroalimentacao-de-dados/
│   └── README.md
│
└── pacotes-de-contexto/
    └── README.md
```

# Navegação

[Voltar ao Portfólio Acadêmico](../../README.md)

[Consultar Índice Geral](../../INDEX.md)

[Acessar Projeto Integrador](../../projeto-integrador/)
