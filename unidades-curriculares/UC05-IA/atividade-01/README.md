# Engenharia de Prompt

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
| Tema | Engenharia de Prompt |
| Projeto relacionado | ConectaStart |
| Status da documentação | Provisório, arquivo original ainda não localizado |

> **Observação:** o arquivo original desta primeira atividade ainda não foi localizado. Este README foi estruturado apenas com os conceitos de Engenharia de Prompt que aparecem documentados nas atividades posteriores da UC. Quando o arquivo original for encontrado, esta documentação poderá ser complementada com o enunciado, exemplos e respostas específicas da atividade.

## Objetivo da atividade

A atividade introduz o uso estruturado de instruções para interação com modelos de Inteligência Artificial.

O objetivo é compreender que a qualidade de uma resposta produzida por um modelo de linguagem depende não apenas da tecnologia utilizada, mas também da maneira como:

- O objetivo é definido.
- O contexto é apresentado.
- A tarefa é explicada.
- As entradas são fornecidas.
- As restrições são estabelecidas.
- Os critérios de qualidade são definidos.
- O formato da resposta é especificado.

A Engenharia de Prompt busca transformar solicitações genéricas em instruções mais claras, controláveis e verificáveis.

# 1. O que é Engenharia de Prompt?

Engenharia de Prompt pode ser entendida, no contexto das atividades desta UC, como o processo de estruturar instruções para orientar o comportamento de um modelo de linguagem.

Um prompt não precisa ser apenas uma pergunta.

Ele pode funcionar como uma especificação da tarefa.

```text
Usuário
   ↓
Objetivo
   ↓
Contexto
   ↓
Instruções
   ↓
Modelo de IA
   ↓
Resposta
```

Quanto mais clara for a especificação, maior tende a ser a possibilidade de avaliar se a resposta realmente atende ao objetivo.

# 2. Problema de prompts vagos

Uma das diferenças exploradas nas atividades da disciplina é o contraste entre uma solicitação espontânea e uma solicitação estruturada.

Um prompt vago pode produzir:

- Generalizações.
- Suposições.
- Respostas excessivamente amplas.
- Mistura entre problema e solução.
- Informações não verificadas.
- Formatos inconsistentes.
- Dificuldade para avaliar a qualidade da resposta.

O fluxo pode ser representado por:

```text
Prompt genérico
      ↓
Muitas interpretações possíveis
      ↓
Modelo completa lacunas
      ↓
Suposições
      ↓
Resposta difícil de avaliar
```

## Exemplo

Uma solicitação como:

```text
Quero criar uma plataforma para startups.

Me diga quais problemas elas enfrentam
e quais funcionalidades eu deveria criar.
```

possui diferentes problemas.

Ela não define claramente:

- Qual tipo de startup.
- Qual estágio de desenvolvimento.
- Qual região.
- Qual público específico.
- Qual evidência deve ser utilizada.
- Se o objetivo é investigar o problema ou projetar a solução.
- Como a resposta deve ser apresentada.

Isso abre espaço para que a IA faça diversas suposições.

# 3. Prompt estruturado

Uma abordagem mais adequada consiste em dividir o prompt em componentes.

A estrutura utilizada nas atividades posteriores da disciplina considera elementos como:

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

Cada componente possui uma função específica.

# 4. Objetivo

O objetivo indica o resultado que se pretende alcançar.

Exemplo:

```text
Objetivo:

Identificar oportunidades de investigação relacionadas
ao ecossistema de startups sem propor uma solução.
```

Um objetivo claro ajuda a impedir que a resposta avance para etapas que ainda não deveriam ser executadas.

## Exemplo de diferença

### Objetivo vago

```text
Analise startups.
```

### Objetivo mais específico

```text
Identifique possíveis problemas enfrentados por startups
em estágio inicial e separe claramente hipóteses de fatos
já sustentados por evidências.
```

# 5. Papel

O papel define a perspectiva que o modelo deverá assumir durante a tarefa.

Exemplos:

```text
Atue como facilitador de discovery.
```

ou:

```text
Atue como analista de requisitos.
```

ou:

```text
Atue como revisor crítico.
```

O papel não substitui as demais instruções.

Ele funciona como orientação complementar sobre a perspectiva utilizada durante a análise.

# 6. Tarefa

A tarefa descreve exatamente o que o modelo deverá fazer.

Exemplo:

```text
Faça perguntas,
organize hipóteses
e identifique lacunas de evidência.
```

Uma tarefa bem definida evita instruções excessivamente abertas.

# 7. Entradas

As entradas representam as informações utilizadas pelo modelo durante a execução.

Exemplos:

- Descrição de um projeto.
- Documento.
- Dataset.
- Texto.
- Requisitos.
- Respostas de entrevistas.
- Informações sobre usuários.
- Resultados anteriores.

O princípio é:

```text
Entrada inadequada
      ↓
Análise limitada

Entrada adequada
      ↓
Maior contexto
      ↓
Resposta mais relevante
```

# 8. Contexto

O contexto ajuda o modelo a compreender a situação na qual a tarefa está inserida.

Exemplo aplicado ao Projeto Integrador:

```text
Contexto:

Ecossistema de startups de Recife.

O projeto investiga possíveis dificuldades de conexão
entre startups, mentores e investidores.

A solução de matchmaking deve ser tratada apenas
como hipótese inicial.
```

Sem esse contexto, o modelo poderia assumir um cenário muito mais amplo.

# 9. Restrições

As restrições definem aquilo que o modelo não deve fazer.

Exemplo:

```text
Não invente dados.

Não proponha funcionalidades.

Não apresente hipóteses como fatos.

Não responda perguntas que dependam de evidência inexistente.
```

As restrições são particularmente importantes quando a tarefa exige análise crítica.

```text
Liberdade total
      ↓
Maior possibilidade de suposição
```

Enquanto:

```text
Restrições claras
      ↓
Espaço de resposta controlado
```

# 10. Critérios

Os critérios indicam como avaliar se a resposta está adequada.

Exemplo:

```text
Para cada hipótese:

1. Identifique o envolvido.
2. Descreva a situação.
3. Explique a possível dor.
4. Informe a evidência disponível.
5. Registre a lacuna existente.
```

Com isso, deixa de existir apenas a pergunta:

```text
"A resposta parece boa?"
```

e passa a existir:

```text
"A resposta atende aos critérios definidos?"
```

# 11. Formato de saída

O formato define como a resposta deve ser organizada.

Exemplos:

- Tabela.
- JSON.
- Markdown.
- Lista.
- Relatório.
- Matriz.
- Estrutura específica de campos.

Exemplo:

```text
Retorne uma tabela com:

| Envolvido | Situação | Dor | Evidência | Lacuna |
```

Isso aumenta a previsibilidade da resposta.

# 12. Estrutura geral de um prompt

Um modelo reutilizável pode ser organizado da seguinte forma:

```text
OBJETIVO
Explique o resultado esperado.

PAPEL
Defina a perspectiva do modelo.

TAREFA
Explique exatamente o que deve ser feito.

ENTRADAS
Forneça as informações necessárias.

CONTEXTO
Apresente a situação relevante.

RESTRIÇÕES
Defina o que não pode ser feito.

CRITÉRIOS
Determine como avaliar a qualidade.

FORMATO
Defina como a resposta deverá ser apresentada.
```

# 13. Exemplo aplicado ao ConectaStart

## Prompt simples

```text
Quais problemas startups enfrentam para encontrar mentores?
```

Esse prompt pode produzir uma resposta plausível, mas não necessariamente baseada em evidências.

## Prompt estruturado

```text
OBJETIVO

Investigar possíveis dificuldades enfrentadas por startups
em estágio de Ideação ou Validação ao procurar mentores.

PAPEL

Atue como facilitador de discovery.

CONTEXTO

O Projeto Integrador ConectaStart investiga mecanismos
de conexão entre startups e mentores.

TAREFA

Liste possíveis dificuldades, mas trate todas inicialmente
como hipóteses.

RESTRIÇÕES

Não invente dados.
Não proponha funcionalidades.
Não considere a hipótese como problema validado.

CRITÉRIOS

Para cada hipótese, informe:
- envolvido;
- situação;
- possível dor;
- evidência necessária;
- lacuna de conhecimento.

FORMATO

Retorne uma tabela.
```

# 14. Comparação entre as abordagens

| Característica | Prompt simples | Prompt estruturado |
|---|---|---|
| Objetivo | Implícito | Explícito |
| Contexto | Limitado | Definido |
| Papel | Não especificado | Especificado |
| Restrições | Ausentes | Definidas |
| Critérios | Ausentes | Definidos |
| Formato | Livre | Controlado |
| Avaliação | Subjetiva | Baseada em critérios |
| Risco de suposição | Maior | Menor |

# 15. Prompt como especificação

Um dos principais aprendizados é que um prompt pode ser tratado de maneira semelhante a uma especificação.

```text
Necessidade
     ↓
Instrução
     ↓
Critérios
     ↓
Saída
     ↓
Avaliação
```

Essa lógica possui semelhança com outros conceitos estudados em desenvolvimento de software.

Por exemplo:

```text
Requisito
   ↓
Critério de aceitação
   ↓
Implementação
   ↓
Validação
```

Na Engenharia de Prompt:

```text
Prompt
   ↓
Critério de resposta
   ↓
Saída da IA
   ↓
Avaliação
```

# 16. Não aceitar a primeira resposta automaticamente

Outra prática importante é não considerar a primeira resposta como resultado definitivo.

O processo pode seguir:

```text
Prompt
   ↓
Resposta
   ↓
Avaliação
   ↓
Problemas identificados
   ↓
Refinamento
   ↓
Nova resposta
```

Esse processo serve como base para os conteúdos posteriores da disciplina relacionados a:

- Engenharia de Prompt Avançada.
- Metaprompt.
- Encadeamento.
- Retroalimentação.
- Refinamento.

# 17. Fato, hipótese e suposição

A atividade também prepara a base para uma distinção importante utilizada posteriormente.

## Fato

Possui evidência verificável.

```text
Fato
 ↓
Fonte
 ↓
Evidência
```

## Hipótese

É uma explicação possível que ainda precisa de validação.

```text
Hipótese
    ↓
Evidência parcial
    ↓
Teste
```

## Suposição

Ainda não possui sustentação suficiente.

```text
Suposição
    ↓
Sem evidência
    ↓
Precisa investigar
```

Um modelo de linguagem pode produzir afirmações plausíveis em qualquer uma dessas categorias.

Cabe ao processo de Engenharia de Prompt e revisão impedir que todas sejam apresentadas como fatos.

# 18. Relação com o Projeto Integrador

A Engenharia de Prompt foi aplicada ao processo de descoberta do **ConectaStart**.

O objetivo não era perguntar à IA:

```text
"Qual produto devemos construir?"
```

mas utilizar a IA para apoiar etapas como:

```text
Contextualizar
      ↓
Investigar
      ↓
Formular hipóteses
      ↓
Identificar lacunas
      ↓
Buscar evidências
      ↓
Preparar validação
```

Isso reduz o risco de construir uma solução baseada apenas em uma ideia inicial.

```text
Ideia
  ↓
Prompt
  ↓
Resposta da IA
  ↓
Construir produto
```

não deve ser o processo.

O processo mais adequado é:

```text
Ideia
  ↓
Investigação
  ↓
Hipóteses
  ↓
Evidências
  ↓
Validação
  ↓
Definição do problema
  ↓
Solução
```

[Acessar Projeto Integrador](../../../projeto-integrador/)

# 19. Relação com atividades posteriores

Esta atividade funciona como base para os conteúdos seguintes da UC.

```text
Engenharia de Prompt
        ↓
Engenharia de Prompt Avançada
        ↓
Decomposição
        ↓
Encadeamento
        ↓
Metaprompt
        ↓
Refinamento
        ↓
Retroalimentação
        ↓
Pacotes de Contexto
```

A primeira atividade trabalha principalmente a qualidade da **instrução inicial**.

As atividades posteriores passam a trabalhar a qualidade de todo o **processo de interação**.

# 20. Principais aprendizados

A atividade permitiu compreender que utilizar Inteligência Artificial não significa apenas escrever perguntas.

Uma interação de maior qualidade exige pensar em:

```text
O que quero?
    ↓
O que o modelo precisa saber?
    ↓
O que ele deve fazer?
    ↓
O que ele não deve fazer?
    ↓
Como deve responder?
    ↓
Como vou avaliar a resposta?
```

Outro aprendizado importante é:

```text
Prompt mais longo
      ≠
Prompt melhor
```

Um bom prompt deve conter as informações necessárias para reduzir ambiguidades e orientar a tarefa.

O objetivo é obter:

```text
Clareza
   +
Contexto
   +
Controle
   +
Critérios
   ↓
Resposta avaliável
```

# Competências desenvolvidas

A atividade contribui para o desenvolvimento de competências relacionadas a:

- Engenharia de Prompt.
- Inteligência Artificial generativa.
- Estruturação de instruções.
- Definição de objetivos.
- Organização de contexto.
- Criação de restrições.
- Definição de critérios.
- Controle de saída.
- Pensamento crítico.
- Análise de respostas.
- Identificação de hipóteses.
- Refinamento de instruções.
- Uso responsável de modelos de linguagem.

# Organização dos arquivos

Enquanto o arquivo original não estiver disponível:

```text
engenharia-de-prompt/
└── README.md
```

Quando o documento for localizado:

```text
engenharia-de-prompt/
│
├── README.md
└── arquivo-original-da-atividade.pdf
```

# Pendência documental

- [x] README estruturado
- [ ] Arquivo original da primeira atividade
- [ ] Revisar README após inclusão do documento original

# Navegação

[Voltar para Inteligência Artificial](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)

[Próxima atividade, Engenharia de Prompt Avançada](../engenharia-de-prompt-avancada/)
