````markdown
# Pacotes de Contexto para Inteligência Artificial

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
| Tema | Pacotes de Contexto |
| Projeto relacionado | ConectaStart |
| Status da documentação | Provisório, arquivo original ainda não localizado |

> **Observação:** o arquivo original desta atividade ainda não foi localizado. Este README foi estruturado provisoriamente a partir dos conceitos trabalhados nas demais atividades da UC, principalmente Engenharia de Prompt, contexto, restrições, evidências, retroalimentação e organização de informações. Quando o material original for encontrado, esta documentação deverá ser revisada.

## Objetivo da atividade

A atividade trabalha a organização de informações em **Pacotes de Contexto** para utilização com modelos de Inteligência Artificial.

O objetivo é fornecer ao modelo um conjunto estruturado de informações relevantes antes da execução de uma tarefa.

Em vez de explicar novamente todo o projeto a cada interação:

```text
Nova conversa
     ↓
Explicar projeto inteiro
     ↓
Explicar público
     ↓
Explicar regras
     ↓
Explicar decisões
     ↓
Executar tarefa
```

pode ser utilizado um pacote reutilizável:

```text
Pacote de Contexto
        ↓
Modelo recebe informações essenciais
        ↓
Prompt específico
        ↓
Execução da tarefa
```

O pacote funciona como uma base organizada para reduzir ambiguidades, perda de informações e respostas incompatíveis com o estado atual do projeto.

# 1. O que é um Pacote de Contexto?

Um Pacote de Contexto é um conjunto estruturado de informações fornecidas ao modelo para ajudá-lo a compreender:

```text
Quem somos?
     ↓
O que estamos fazendo?
     ↓
Qual é o problema?
     ↓
Quem são os envolvidos?
     ↓
Quais decisões já foram tomadas?
     ↓
Quais regras precisam ser respeitadas?
     ↓
O que ainda não sabemos?
```

Ele não substitui o prompt.

O pacote fornece o **contexto**.

O prompt fornece a **tarefa**.

```text
PACOTE DE CONTEXTO
        +
PROMPT
        ↓
MODELO DE IA
        ↓
RESPOSTA
```

# 2. Diferença entre Prompt e Pacote de Contexto

## Prompt

Define o que o modelo deverá fazer naquela interação.

Exemplo:

```text
Crie três critérios de aceitação para o fluxo
de matchmaking entre startup e mentor.
```

## Pacote de Contexto

Explica informações necessárias para executar corretamente essa tarefa.

Exemplo:

```text
Projeto: ConectaStart

Escopo atual:
Ideação e Validação

Usuários:
Startups e mentores

Objetivo do matchmaking:
Conectar necessidades de startups com competências
de mentores.

Regra:
Não considerar investidores no MVP atual.
```

## Relação

```text
Contexto
    ↓
Explica o cenário

Prompt
    ↓
Define a ação

Resposta
    ↓
Aplica a ação dentro do cenário
```

# 3. Problema que o Pacote de Contexto busca reduzir

Sem contexto suficiente, um modelo pode:

- Assumir regras inexistentes.
- Utilizar decisões antigas.
- Misturar versões do projeto.
- Generalizar o público.
- Inventar funcionalidades.
- Ignorar restrições.
- Produzir respostas incoerentes com o escopo atual.

Exemplo:

```text
Informação ausente:
"O ConectaStart agora trabalha apenas Ideação e Validação."

        ↓

Modelo utiliza contexto antigo

        ↓

Propõe funcionalidades para Tração e Escala
```

Com um pacote atualizado:

```text
Escopo atual:
Ideação + Validação

        ↓

Modelo recebe restrição

        ↓

Resposta permanece dentro do MVP
```

# 4. Estrutura geral de um Pacote de Contexto

Uma estrutura reutilizável pode conter:

```text
PACOTE DE CONTEXTO
│
├── Identificação
├── Objetivo
├── Problema
├── Público
├── Escopo
├── Regras
├── Requisitos
├── Dados
├── Evidências
├── Hipóteses
├── Restrições
├── Glossário
├── Decisões
├── Pendências
└── Formato esperado
```

Cada parte possui uma função específica.

# 5. Identificação

A primeira seção identifica o projeto.

Exemplo:

```yaml
projeto:
  nome: ConectaStart
  tipo: Projeto Integrador
  curso: Análise e Desenvolvimento de Sistemas
  instituicao: Faculdade Senac Pernambuco
  semestre: 2026.2
```

Essa seção ajuda a impedir confusão com outros projetos.

# 6. Objetivo

Define a finalidade atual do projeto.

Exemplo:

```text
Objetivo:

Apoiar startups em estágio de Ideação e Validação,
organizando informações e facilitando conexões relevantes
com mentores de acordo com necessidades e competências.
```

O objetivo deve representar o estado atual do projeto.

# 7. Problema

O pacote deve registrar claramente qual problema está sendo investigado.

Exemplo:

```text
Startups em fases iniciais podem enfrentar dificuldade
para encontrar orientação e pessoas adequadas ao seu
momento de desenvolvimento.
```

É importante distinguir:

```text
PROBLEMA
   ↓
Situação que queremos compreender

SOLUÇÃO
   ↓
Resposta proposta para o problema
```

# 8. Público

O pacote pode definir os principais usuários.

Exemplo:

```yaml
publicos:
  startup:
    papel: recebe orientação e busca conexões
    estagios:
      - Ideação
      - Validação

  mentor:
    papel: oferece conhecimento e orientação
```

Isso reduz generalizações.

# 9. Escopo

O escopo define aquilo que faz parte da versão atual.

## Dentro do escopo

```text
Ideação

Validação

Cadastro de startup

Cadastro de mentor

Perfil

Necessidades

Competências

Matchmaking

Feedback
```

## Fora do escopo atual

```text
Tração

Escala

Matchmaking com investidores

Operações financeiras complexas
```

O controle de escopo ajuda a impedir que o modelo retorne propostas incompatíveis com o MVP.

# 10. Regras de negócio

O pacote também pode armazenar regras conhecidas.

Exemplo:

```text
RN-01
Toda startup deve possuir um estágio definido.

RN-02
O MVP aceita apenas os estágios Ideação e Validação.

RN-03
O mentor deve informar áreas de especialidade.

RN-04
O matchmaking deve considerar necessidades da startup
e competências do mentor.

RN-05
Feedbacks de interações podem ser registrados para
avaliação futura dos critérios de compatibilidade.
```

Essas regras passam a funcionar como restrições para outras tarefas.

# 11. Requisitos

Os requisitos também podem fazer parte do pacote.

Exemplo:

```text
RF-01
Cadastrar startup.

RF-02
Cadastrar mentor.

RF-03
Atualizar perfil.

RF-04
Classificar startup por estágio.

RF-05
Registrar necessidades da startup.

RF-06
Registrar competências do mentor.

RF-07
Gerar recomendações de compatibilidade.

RF-08
Registrar feedback.
```

# 12. Dados importantes

O pacote pode indicar quais dados são necessários para cada entidade.

## Startup

```text
Nome

Segmento

Estágio

Problema

Objetivos

Necessidades

Competências existentes

Competências necessárias
```

## Mentor

```text
Nome

Experiência

Especialidades

Segmentos

Competências

Disponibilidade

Interesses
```

# 13. Evidências

O pacote também pode armazenar aquilo que já possui evidência.

Exemplo:

```yaml
evidencias:
  - descricao: >
      Existem empresas recentes de tecnologia e economia
      criativa no Recife.
    status: evidenciado por dados públicos

  - descricao: >
      Investidores apresentam dificuldades em localizar
      determinadas oportunidades.
    status: evidência nacional, validação local pendente
```

Isso reduz o risco de transformar evidências parciais em conclusões definitivas.

# 14. Hipóteses

Hipóteses devem permanecer explicitamente separadas dos fatos.

Exemplo:

```yaml
hipoteses:
  - descricao: >
      Startups em Ideação podem ter dificuldade de identificar
      o mentor mais adequado.
    status: validar

  - descricao: >
      Feedback pós-match pode contribuir para melhorar
      os critérios de compatibilidade.
    status: investigar
```

# 15. Fatos, hipóteses e lacunas

Uma estrutura útil é:

| Tipo | Significado |
|---|---|
| Fato | Informação sustentada por evidência |
| Hipótese | Explicação ou possibilidade que precisa ser validada |
| Suposição | Ideia sem evidência suficiente |
| Lacuna | Informação ainda desconhecida |

Exemplo:

```text
FATO
O escopo atual trabalha Ideação e Validação.

HIPÓTESE
Startups valorizam matches baseados em especialidade.

SUPOSIÇÃO
Todas as startups desejam acompanhamento semanal.

LACUNA
Não sabemos quais critérios os usuários consideram
mais importantes para avaliar um mentor.
```

# 16. Restrições

O pacote pode incluir instruções permanentes.

Exemplo:

```text
Não inventar dados.

Não apresentar hipótese como fato.

Não incluir funcionalidades fora do escopo atual.

Não assumir investidor como usuário do MVP.

Indicar explicitamente quando não houver evidência.

Priorizar informações fornecidas pelo projeto.
```

# 17. Decisões já tomadas

Uma seção particularmente importante registra decisões de projeto.

Exemplo:

```text
DEC-01
O escopo foi reduzido para Ideação e Validação.

DEC-02
O MVP prioriza matchmaking com mentores.

DEC-03
Investidores permanecem como possibilidade futura.

DEC-04
Feedback será considerado como fonte de melhoria
dos critérios de matchmaking.

DEC-05
Problemas e funcionalidades devem ser diferenciados.
```

Essa seção reduz o risco de o modelo reutilizar decisões antigas.

# 18. Histórico de decisões

Quando o projeto evolui, pode ser mantido um pequeno histórico.

```text
Versão inicial
Ideação → Validação → Tração → Escala
                  ↓
Revisão de escopo
                  ↓
MVP
Ideação → Validação
```

Isso ajuda a explicar por que documentos antigos podem conter informações diferentes.

# 19. Pendências

O pacote também deve indicar aquilo que ainda precisa ser decidido.

Exemplo:

```text
PEND-01
Definir pesos finais do algoritmo de matchmaking.

PEND-02
Definir mecanismo de validação da evolução de estágio.

PEND-03
Definir quais feedbacks serão obrigatórios.

PEND-04
Validar critérios de compatibilidade com usuários reais.
```

Essa informação é útil porque impede que a IA preencha automaticamente decisões ainda abertas.

# 20. Glossário

Um glossário reduz ambiguidades.

| Termo | Significado |
|---|---|
| Startup | Negócio em desenvolvimento analisado pelo projeto |
| Ideação | Estágio inicial de definição do problema e solução |
| Validação | Estágio de teste de hipóteses com mercado e usuários |
| Mentor | Profissional que oferece orientação |
| Match | Conexão sugerida entre startup e mentor |
| Matchmaking | Processo de identificar possíveis conexões |
| Feedback | Avaliação registrada após interação |
| Compatibilidade | Nível de aderência entre necessidade e competência |

# 21. Fontes

O pacote pode registrar a origem das informações.

Exemplo:

```yaml
fontes:
  - Mapa de Empatia do ConectaStart
  - Mapa de Oportunidades
  - Engenharia de Prompt Avançada
  - Prompts e Dados Públicos
  - Project Charter
  - Entrevistas
  - Requisitos
```

Isso melhora a rastreabilidade.

# 22. Nível de confiança

Uma evolução possível consiste em atribuir nível de confiança às informações.

Exemplo:

```yaml
informacao:
  descricao: "O MVP trabalha Ideação e Validação."
  tipo: decisao
  confianca: alta
```

Outro exemplo:

```yaml
informacao:
  descricao: "Mentores preferem matches por segmento."
  tipo: hipotese
  confianca: baixa
```

# 23. Pacote de Contexto do ConectaStart

Um pacote simplificado poderia ser:

```yaml
projeto:
  nome: ConectaStart
  tipo: plataforma digital

objetivo:
  apoiar startups nas fases iniciais por meio de
  orientação e conexões relevantes

escopo:
  inclui:
    - Ideação
    - Validação
    - startups
    - mentores
    - matchmaking
    - feedback

  exclui:
    - Tração
    - Escala
    - investimento como núcleo do MVP

startup:
  dados:
    - estágio
    - segmento
    - problema
    - necessidade
    - objetivo

mentor:
  dados:
    - experiência
    - especialidade
    - competências
    - disponibilidade

matchmaking:
  finalidade:
    relacionar necessidades das startups
    às competências dos mentores

restricoes:
  - não inventar dados
  - separar hipótese de fato
  - respeitar o escopo atual
  - sinalizar lacunas

pendencias:
  - validar pesos de compatibilidade
  - validar critérios com usuários
```

# 24. Uso do Pacote de Contexto

Depois de criado, o pacote pode ser utilizado em diferentes tarefas.

## Requisitos

```text
Pacote ConectaStart
       +
"Crie requisitos funcionais"
```

## Testes

```text
Pacote ConectaStart
       +
"Crie casos de teste do matchmaking"
```

## Arquitetura

```text
Pacote ConectaStart
       +
"Proponha arquitetura técnica"
```

## Produto

```text
Pacote ConectaStart
       +
"Organize o backlog"
```

O mesmo contexto é reutilizado.

# 25. Vantagem da reutilização

Sem pacote:

```text
Prompt 1
Explicar projeto inteiro

Prompt 2
Explicar projeto inteiro

Prompt 3
Explicar projeto inteiro
```

Com pacote:

```text
          Pacote de Contexto
          /       |       \
         /        |        \
Requisitos     Testes     Arquitetura
```

Isso melhora a consistência entre diferentes tarefas.

# 26. Contexto em camadas

Nem toda tarefa precisa receber todas as informações disponíveis.

Pode ser utilizada uma arquitetura em camadas.

```text
CONTEXTO BASE
│
├── Projeto
├── Objetivo
├── Público
└── Escopo

CONTEXTO DE NEGÓCIO
│
├── Regras
├── Requisitos
└── Glossário

CONTEXTO DE DADOS
│
├── Entidades
├── Evidências
└── Métricas

CONTEXTO DA TAREFA
│
├── Objetivo específico
├── Entradas
└── Formato esperado
```

Essa abordagem reduz excesso de informação.

# 27. Contexto mínimo necessário

Um bom Pacote de Contexto não precisa conter tudo que já foi produzido sobre o projeto.

O princípio é:

```text
Contexto suficiente
        ↓
Executar corretamente a tarefa
```

e não:

```text
Todo documento já criado
        ↓
Enviar sempre
```

Informações irrelevantes podem aumentar:

- Complexidade.
- Ruído.
- Contradições.
- Custo de processamento.
- Dificuldade de interpretação.

# 28. Atualização do pacote

Pacotes de Contexto precisam acompanhar a evolução do projeto.

Exemplo:

```text
Pacote v1
4 estágios
     ↓
Decisão de redução de escopo
     ↓
Pacote v2
Ideação + Validação
```

Se o contexto não for atualizado, respostas futuras podem continuar utilizando informações antigas.

# 29. Versionamento

Um formato simples:

```text
contexto-conectastart-v1.md

contexto-conectastart-v2.md

contexto-conectastart-v3.md
```

Ou utilizando Git:

```text
Commit
   ↓
Alteração do contexto
   ↓
Histórico
   ↓
Rastreabilidade
```

Como o projeto já utiliza GitHub, o versionamento pode ser realizado pelo próprio Git.

# 30. Estrutura de diretórios

Uma organização possível seria:

```text
pacotes-de-contexto/
│
├── README.md
│
├── conectastart/
│   ├── contexto-base.md
│   ├── contexto-negocio.md
│   ├── contexto-dados.md
│   ├── glossario.md
│   └── decisoes.md
│
└── exemplos/
    ├── prompt-requisitos.md
    ├── prompt-testes.md
    └── prompt-arquitetura.md
```

# 31. Exemplo de contexto-base.md

```markdown
# Contexto Base, ConectaStart

## Projeto
ConectaStart

## Objetivo
Apoiar startups nas fases de Ideação e Validação.

## Usuários
- Startups
- Mentores

## Escopo atual
- Cadastro
- Perfis
- Estágios
- Matchmaking
- Feedback

## Fora do escopo
- Tração
- Escala
- Matchmaking com investidores
```

# 32. Exemplo de contexto-negocio.md

```markdown
# Contexto de Negócio

## Estágios

### Ideação
Startup ainda está estruturando problema, proposta e público.

### Validação
Startup está testando hipóteses com usuários ou mercado.

## Matchmaking

O matchmaking relaciona necessidades declaradas pela startup
com competências e experiências de mentores.
```

# 33. Exemplo de decisoes.md

```markdown
# Decisões do Projeto

## DEC-001
Escopo reduzido para Ideação e Validação.

## DEC-002
Mentores são o principal alvo do matchmaking no MVP.

## DEC-003
Investidores ficam para evolução futura.

## DEC-004
Feedback será utilizado para avaliar a qualidade dos matches.
```

# 34. Relação com Retroalimentação

Pacotes de Contexto e retroalimentação possuem relação direta.

```text
Pacote v1
   ↓
Uso
   ↓
Nova informação
   ↓
Feedback
   ↓
Atualização
   ↓
Pacote v2
```

O contexto deixa de ser um documento estático.

Ele evolui junto com o projeto.

[Consultar Retroalimentação de Dados](../retroalimentacao-de-dados/)

# 35. Relação com Engenharia de Prompt

A Engenharia de Prompt define a instrução.

```text
Prompt
 ↓
O que fazer?
```

O Pacote de Contexto responde:

```text
Contexto
 ↓
Com quais informações?
```

Combinados:

```text
Contexto
   +
Prompt
   ↓
Resposta contextualizada
```

[Consultar Engenharia de Prompt](../engenharia-de-prompt/)

# 36. Relação com Engenharia de Prompt Avançada

A Engenharia de Prompt Avançada utiliza técnicas como:

- Decomposição.
- Encadeamento.
- Metaprompt.
- Refinamento.

Essas técnicas funcionam melhor quando as informações de base estão claramente organizadas.

```text
Pacote de Contexto
        ↓
Prompt 1
        ↓
Prompt 2
        ↓
Metaprompt
        ↓
Refinamento
```

[Consultar Engenharia de Prompt Avançada](../engenharia-de-prompt-avancada/)

# 37. Relação com o Projeto Integrador

Pacotes de Contexto possuem aplicação direta no ConectaStart porque o projeto reúne informações produzidas em diferentes Unidades Curriculares.

```text
Gestão da Informação
        │
Empreendedorismo
        │
High Tech
        │
Inteligência Artificial
        │
Qualidade de Software
        │
Governança
        ▼
    ConectaStart
```

Um Pacote de Contexto pode consolidar as informações necessárias sem depender da leitura manual de todos os documentos.

# 38. Exemplo de pacote interdisciplinar

```text
ConectaStart
│
├── Gestão da Informação
│   ├── qualidade
│   └── ciclo de vida
│
├── Empreendedorismo
│   └── mapa de empatia
│
├── Inteligência Artificial
│   ├── hipóteses
│   ├── evidências
│   └── prompts
│
├── Qualidade
│   ├── critérios de aceitação
│   └── testes
│
└── Projeto Integrador
    ├── requisitos
    ├── arquitetura
    └── backlog
```

O modelo pode receber apenas as partes necessárias para cada tarefa.

[Acessar Projeto Integrador](../../../projeto-integrador/)

# 39. Relação com Arquitetura da Informação

Pacotes de Contexto também possuem forte relação com os conceitos estudados na UC de Gestão da Informação.

## Classificação

Separar informações por natureza.

## Taxonomia

Organizar categorias e hierarquias.

## Metadados

Registrar:

- Fonte.
- Data.
- Tipo.
- Status.
- Confiança.

## Encontrabilidade

Permitir localizar rapidamente informações necessárias.

## Relações

Conectar:

```text
Decisão
   ↓
Requisito
   ↓
Regra
   ↓
Evidência
```

[Consultar Gestão da Informação](../../uc01-gestao-da-informacao/)

# 40. Riscos dos Pacotes de Contexto

## Contexto desatualizado

```text
Regra antiga
    ↓
Resposta inadequada
```

## Informação incorreta

```text
Erro no contexto
     ↓
Erro reutilizado
     ↓
Múltiplas respostas incorretas
```

## Excesso de informação

```text
Contexto enorme
      ↓
Ruído
      ↓
Dificuldade de priorização
```

## Contradições

Documentos diferentes podem conter versões diferentes da mesma regra.

Por isso, o pacote precisa indicar qual informação é considerada vigente.

# 41. Boas práticas

Um Pacote de Contexto deve ser:

```text
Claro

Atualizado

Modular

Rastreável

Versionado

Reutilizável

Objetivo
```

Também deve diferenciar:

```text
Fato

Hipótese

Decisão

Regra

Pendência
```

# 42. Fluxo consolidado da UC05

Os conteúdos estudados podem ser relacionados da seguinte maneira:

```text
Engenharia de Prompt
        ↓
Estruturar instruções

Engenharia de Prompt Avançada
        ↓
Decompor e refinar

Mapa de Oportunidades
        ↓
Formular hipóteses

Prompts e Dados Públicos
        ↓
Adicionar evidências

Retroalimentação
        ↓
Atualizar com novos resultados

Pacotes de Contexto
        ↓
Organizar e reutilizar conhecimento
```

# 43. Principais aprendizados

A atividade permite compreender que modelos de Inteligência Artificial dependem fortemente das informações fornecidas durante a interação.

Não basta perguntar:

```text
"Crie algo para o ConectaStart."
```

É necessário fornecer contexto suficiente para que o modelo compreenda:

```text
O que é o ConectaStart?

Qual é o escopo atual?

Quem são os usuários?

Quais decisões já foram tomadas?

Quais regras existem?

O que ainda está em aberto?

Qual tarefa deverá ser executada?
```

Outro aprendizado importante é:

```text
Mais contexto
   ≠
Sempre melhor
```

O objetivo é fornecer:

```text
Contexto relevante
        +
Contexto atualizado
        +
Contexto confiável
        ↓
Melhor base para a tarefa
```

# Competências desenvolvidas

A atividade contribui para o desenvolvimento de competências relacionadas a:

- Inteligência Artificial.
- Engenharia de Prompt.
- Context Engineering.
- Organização de informações.
- Estruturação de contexto.
- Rastreabilidade.
- Versionamento.
- Gestão de conhecimento.
- Modularização.
- Metadados.
- Taxonomia.
- Retroalimentação.
- Pensamento crítico.
- Uso responsável de IA.
- Documentação de projetos.

# Organização dos arquivos

Enquanto o arquivo original não estiver disponível:

```text
pacotes-de-contexto/
└── README.md
```

Uma evolução futura pode utilizar:

```text
pacotes-de-contexto/
│
├── README.md
│
├── conectastart/
│   ├── contexto-base.md
│   ├── contexto-negocio.md
│   ├── contexto-dados.md
│   ├── decisoes.md
│   └── glossario.md
│
└── exemplos/
```

# Pendência documental

- [x] README provisório
- [ ] Localizar arquivo original da atividade
- [ ] Comparar conteúdo original com esta documentação
- [ ] Ajustar exemplos, se necessário
- [ ] Adicionar artefatos produzidos na atividade

# Navegação

[Voltar para Inteligência Artificial](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)

[Atividade anterior, Retroalimentação de Dados](../retroalimentacao-de-dados/)

---

# Status da UC05

Com este README, todas as áreas informadas inicialmente para a UC05 possuem documentação.

## Documentadas com arquivos originais

- [x] Engenharia de Prompt Avançada
- [x] Mapa de Oportunidades
- [x] Prompts e Dados Públicos

## Documentadas provisoriamente

- [x] Engenharia de Prompt
- [x] Retroalimentação de Dados
- [x] Pacotes de Contexto

## Pendências

- [ ] Localizar os arquivos originais das atividades provisórias
- [ ] Revisar os READMEs quando os materiais forem encontrados

