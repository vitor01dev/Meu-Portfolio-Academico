# Retroalimentação de Dados e Engenharia de Prompt Avançada

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
| Tema | Retroalimentação de Dados e Engenharia de Prompt Avançada |
| Projeto relacionado | ConectaStart |
| Status da documentação | Provisório, arquivo original ainda não localizado |

> **Observação:** o arquivo original desta atividade ainda não foi localizado. Este README foi construído provisoriamente com base nos conceitos já documentados nas atividades anteriores da UC, principalmente refinamento de prompts, metaprompt, uso de evidências, revisão metodológica e reaproveitamento de resultados como nova entrada. Quando o arquivo original for encontrado, esta documentação deverá ser revisada para refletir exatamente o enunciado e os resultados da atividade.

## Objetivo da atividade

A atividade trabalha o uso de **retroalimentação** em processos apoiados por Inteligência Artificial.

A ideia central é que uma resposta produzida por um modelo não precisa representar o fim da interação.

Ela pode ser:

1. Avaliada.
2. Comparada com critérios.
3. Corrigida.
4. Enriquecida com novos dados.
5. Utilizada como entrada para uma nova interação.

O processo pode ser representado por:

```text
Entrada
   ↓
Prompt
   ↓
Modelo de IA
   ↓
Resposta
   ↓
Avaliação
   ↓
Feedback
   ↓
Nova entrada
   ↓
Resposta refinada
```

Esse ciclo permite transformar uma interação isolada em um processo progressivo de melhoria.

# 1. O que é retroalimentação?

Retroalimentação consiste em utilizar informações obtidas durante uma etapa anterior para modificar a etapa seguinte.

Em um sistema simples:

```text
Entrada
   ↓
Processamento
   ↓
Saída
```

Em um sistema com retroalimentação:

```text
Entrada
   ↓
Processamento
   ↓
Saída
   ↓
Avaliação
   ↓
Feedback
   └──────────────→ Nova entrada
```

A diferença principal é que o resultado anterior passa a influenciar o próximo ciclo.

# 2. Retroalimentação aplicada à Inteligência Artificial

No contexto de modelos de linguagem, o processo pode funcionar assim:

```text
Prompt inicial
     ↓
Resposta
     ↓
Usuário identifica problema
     ↓
Fornece correção
     ↓
Novo prompt
     ↓
Resposta revisada
```

O feedback pode incluir:

- Correção factual.
- Novo contexto.
- Nova evidência.
- Mudança de formato.
- Restrição adicional.
- Critério de qualidade.
- Identificação de ambiguidade.
- Solicitação de aprofundamento.

# 3. Diferença entre repetir e retroalimentar

Repetir um prompt sem acrescentar informação não representa necessariamente retroalimentação.

## Repetição simples

```text
Prompt
  ↓
Resposta

Prompt igual
  ↓
Nova resposta
```

## Retroalimentação

```text
Prompt
  ↓
Resposta
  ↓
Análise da resposta
  ↓
Feedback específico
  ↓
Prompt atualizado
  ↓
Resposta refinada
```

O elemento central é a utilização do resultado anterior como fonte de informação para a próxima interação.

# 4. Exemplo básico

## Primeira solicitação

```text
Liste problemas enfrentados por startups.
```

A resposta pode ser muito ampla.

## Feedback

```text
A resposta está genérica.

Separe apenas startups em estágio de Ideação e Validação.

Não apresente problemas como fatos sem indicar evidência.
```

## Novo resultado esperado

A segunda resposta passa a considerar:

- Estágio.
- Evidência.
- Contexto.
- Restrições.

O fluxo é:

```text
Resposta genérica
      ↓
Crítica
      ↓
Novo contexto
      ↓
Resposta mais específica
```

# 5. Relação com Engenharia de Prompt Avançada

A atividade de Engenharia de Prompt Avançada já utilizou um processo de retroalimentação.

O fluxo documentado foi:

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
Crítica
     ↓
Prompt 5
Refinamento
```

Cada saída influenciou a etapa seguinte.

Isso caracteriza uma forma de retroalimentação.

# 6. Metaprompt como mecanismo de feedback

O metaprompt pode ser utilizado para avaliar uma resposta anterior.

Exemplo:

```text
Analise criticamente a resposta anterior.

Identifique:
- generalizações;
- ambiguidades;
- falta de evidências;
- suposições;
- possíveis vieses.

Não proponha uma nova solução ainda.
```

O resultado dessa análise passa a funcionar como feedback.

```text
Resposta inicial
      ↓
Metaprompt
      ↓
Crítica
      ↓
Problemas encontrados
      ↓
Novo prompt
```

# 7. Refinamento orientado por falhas

O refinamento não deve consistir apenas em pedir:

```text
"Melhore a resposta."
```

Uma abordagem mais controlada é indicar exatamente o que precisa ser corrigido.

Exemplo:

```text
Revise a resposta anterior considerando:

1. A evidência utilizada é nacional, não local.
2. Separe investidor individual de rede organizada.
3. Não trate hipótese como fato.
4. Defina melhor o termo "padronização".
```

Esse processo gera uma retroalimentação específica e verificável.

# 8. Retroalimentação com novos dados

O ciclo também pode utilizar dados externos.

```text
Hipótese inicial
      ↓
Resposta da IA
      ↓
Pesquisa
      ↓
Novo dado
      ↓
Prompt atualizado
      ↓
Nova interpretação
```

Exemplo aplicado às atividades da UC:

```text
"Empresas recentes têm dificuldade de acesso a financiamento."
        ↓
Análise de dados públicos
        ↓
Limitações encontradas
        ↓
Hipótese não confirmada
        ↓
Nova pergunta para entrevistas
```

# 9. Evidência como feedback

Um dado novo pode confirmar, enfraquecer ou rejeitar uma hipótese.

```text
Hipótese
   ↓
Evidência
  /       \
apoia   contradiz
  \       /
   ↓     ↓
Reavaliar hipótese
```

Esse processo impede que a IA seja utilizada apenas para confirmar ideias existentes.

# 10. Feedback positivo e negativo

## Feedback positivo

Indica que determinada parte da resposta deve ser preservada.

Exemplo:

```text
Mantenha a separação entre fato, hipótese e suposição.
```

## Feedback corretivo

Indica uma falha que precisa ser modificada.

Exemplo:

```text
A resposta tratou dados nacionais como se fossem específicos do Recife.
Corrija o escopo.
```

## Feedback adicional

Fornece nova informação.

Exemplo:

```text
Considere agora que o escopo do ConectaStart foi reduzido para Ideação e Validação.
```

# 11. Ciclo de refinamento

Um ciclo completo pode ser estruturado da seguinte forma:

```text
1. Formular prompt
       ↓
2. Gerar resposta
       ↓
3. Avaliar resposta
       ↓
4. Identificar falhas
       ↓
5. Fornecer feedback
       ↓
6. Refinar prompt
       ↓
7. Gerar nova resposta
       ↓
8. Comparar versões
```

# 12. Comparação entre versões

A retroalimentação ganha valor quando é possível observar o que mudou.

Exemplo:

| Aspecto | Versão inicial | Versão refinada |
|---|---|---|
| Escopo | Amplo | Delimitado |
| Evidência | Ausente | Identificada |
| Hipóteses | Misturadas a fatos | Separadas |
| Formato | Livre | Estruturado |
| Restrições | Poucas | Explícitas |

O objetivo é avaliar se a nova versão corrigiu os problemas encontrados.

# 13. Retroalimentação e critérios

Para que o ciclo funcione bem, é necessário ter critérios de avaliação.

Sem critérios:

```text
Resposta
   ↓
"Parece boa"
```

Com critérios:

```text
Resposta
   ↓
Avaliar:
- aderência;
- evidência;
- estrutura;
- clareza;
- restrições;
- precisão.
```

Isso torna o feedback menos subjetivo.

# 14. Rubricas

Uma rubrica pode ser utilizada para avaliar respostas produzidas por IA.

Exemplo:

| Critério | 0 | 1 | 2 |
|---|---|---|---|
| Aderência | Não atende | Parcial | Atende |
| Evidências | Ausentes | Parciais | Claras |
| Estrutura | Inadequada | Parcial | Correta |
| Restrições | Ignoradas | Parciais | Respeitadas |
| Incerteza | Não indicada | Parcial | Explícita |

O resultado pode orientar o próximo ciclo de refinamento.

# 15. Retroalimentação com dados de usuários

A retroalimentação não precisa vir apenas do próprio modelo ou da equipe.

Pode vir de usuários reais.

Exemplo:

```text
Hipótese
   ↓
Entrevista
   ↓
Resposta do usuário
   ↓
Novo dado
   ↓
Atualização do contexto
   ↓
Nova hipótese
```

Essa abordagem é particularmente importante em processos de discovery.

# 16. Aplicação ao ConectaStart

No Projeto Integrador, a retroalimentação pode ser utilizada em diferentes momentos.

## Discovery

```text
Hipótese
   ↓
Entrevista
   ↓
Feedback
   ↓
Revisão da hipótese
```

## Matchmaking

```text
Match sugerido
     ↓
Startup interage com mentor
     ↓
Feedback
     ↓
Qualidade do match
     ↓
Ajuste dos critérios
```

## Produto

```text
Funcionalidade
     ↓
Uso
     ↓
Dados
     ↓
Feedback
     ↓
Melhoria
```

# 17. Exemplo aplicado ao matchmaking

Suponha que inicialmente o ConectaStart utilize:

```text
Segmento
+
Estágio
+
Especialidade do mentor
```

como critérios de matchmaking.

Após as interações, os usuários fornecem feedback.

```text
Match 1
  ↓
Baixa utilidade

Match 2
  ↓
Alta utilidade
```

A equipe pode investigar quais características estão associadas aos melhores resultados.

```text
Feedback
   ↓
Análise
   ↓
Novo peso dos critérios
   ↓
Novo matchmaking
```

# 18. Retroalimentação não significa aprendizado automático

É importante distinguir duas coisas.

## Feedback utilizado manualmente

```text
Dados
  ↓
Equipe analisa
  ↓
Regras são atualizadas
```

## Sistema de aprendizado automático

```text
Dados
  ↓
Algoritmo
  ↓
Modelo atualizado
```

Nem todo sistema com retroalimentação precisa utilizar Machine Learning.

O ConectaStart pode inicialmente utilizar processos manuais ou regras explícitas.

# 19. Controle de qualidade do feedback

Nem todo feedback deve ser aceito automaticamente.

Ele pode ser:

- Incompleto.
- Contraditório.
- Subjetivo.
- Inconsistente.
- Pouco representativo.

Portanto:

```text
Feedback
   ↓
Validação
   ↓
Classificação
   ↓
Uso
```

# 20. Risco de retroalimentação inadequada

Se informações incorretas forem utilizadas como nova entrada:

```text
Erro
 ↓
Feedback incorreto
 ↓
Nova resposta
 ↓
Erro reforçado
```

Esse fenômeno pode criar um ciclo de degradação.

Por isso, é necessário verificar a qualidade das informações reutilizadas.

# 21. Rastreabilidade

Um processo de retroalimentação deve permitir identificar:

```text
Versão inicial
      ↓
Problema encontrado
      ↓
Feedback aplicado
      ↓
Mudança realizada
      ↓
Versão final
```

Isso facilita compreender por que uma resposta ou decisão mudou.

# 22. Registro de versões

Uma forma simples de documentar o processo é:

```text
v1
Prompt inicial

v2
Prompt + restrições

v3
Prompt + evidências

v4
Prompt + crítica

v5
Prompt refinado
```

Esse histórico permite acompanhar a evolução da interação.

# 23. Relação com dados públicos

A atividade de **Prompts e Dados Públicos** também utilizou retroalimentação.

```text
Primeira análise
      ↓
Possíveis interpretações incorretas
      ↓
Prompt de revisão
      ↓
Controles metodológicos
      ↓
Nova análise
```

Foram adicionados controles relacionados a:

- CNPJs distintos.
- Datas.
- Duplicidades.
- Crédito.
- Investimento-anjo.
- Limitações das bases.

[Consultar Prompts e Dados Públicos](../prompts-e-dados-publicos/)

# 24. Relação com Engenharia de Prompt Avançada

A retroalimentação também aparece no processo de metaprompt.

```text
Investigação
   ↓
Crítica
   ↓
Feedback
   ↓
Refinamento
```

[Consultar Engenharia de Prompt Avançada](../engenharia-de-prompt-avancada/)

# 25. Relação com Pacotes de Contexto

A retroalimentação também pode modificar um pacote de contexto.

Exemplo:

```text
Pacote de contexto v1
        ↓
Nova decisão do projeto
        ↓
Atualização
        ↓
Pacote de contexto v2
```

Isso permite manter o modelo alinhado à situação mais recente do projeto.

# 26. Fluxo consolidado

A relação entre os conteúdos da UC pode ser representada assim:

```text
Engenharia de Prompt
        ↓
Criar instrução

Engenharia de Prompt Avançada
        ↓
Decompor e criticar

Dados Públicos
        ↓
Adicionar evidências

Retroalimentação
        ↓
Reutilizar resultados e feedback

Pacotes de Contexto
        ↓
Manter conhecimento organizado
```

# 27. Relação com o Projeto Integrador

A retroalimentação tem relação direta com a evolução do ConectaStart.

O projeto passou por diferentes hipóteses e ajustes de escopo.

```text
Ideia inicial
      ↓
Matchmaking amplo
      ↓
Pesquisa
      ↓
Dados
      ↓
Entrevistas e análises
      ↓
Feedback
      ↓
Redução de escopo
      ↓
Ideação + Validação
```

Esse processo é um exemplo de retroalimentação aplicada à gestão do próprio projeto.

[Acessar Projeto Integrador](../../../projeto-integrador/)

# 28. Principais aprendizados

A atividade permite compreender que uma boa interação com IA não deve ser tratada como:

```text
Pergunta
   ↓
Resposta final
```

O processo mais adequado pode ser:

```text
Pergunta
   ↓
Resposta
   ↓
Crítica
   ↓
Evidência
   ↓
Feedback
   ↓
Refinamento
   ↓
Nova resposta
```

Outro aprendizado importante é:

```text
Feedback
   ≠
Aceitação automática
```

O feedback também precisa ser analisado e validado.

# Competências desenvolvidas

A atividade contribui para o desenvolvimento de competências relacionadas a:

- Inteligência Artificial.
- Engenharia de Prompt.
- Engenharia de Prompt Avançada.
- Retroalimentação.
- Refinamento.
- Metaprompting.
- Avaliação de respostas.
- Controle de versões.
- Uso de evidências.
- Validação.
- Pensamento crítico.
- Discovery.
- Melhoria contínua.
- Rastreabilidade.
- Organização de contexto.

# Organização dos arquivos

Enquanto o arquivo original não estiver disponível:

```text
retroalimentacao-de-dados/
└── README.md
```

Quando o material original for encontrado:

```text
retroalimentacao-de-dados/
│
├── README.md
└── arquivo-original-da-atividade.pdf
```

# Pendência documental

- [x] README provisório
- [ ] Arquivo original da atividade
- [ ] Conferir o enunciado original
- [ ] Substituir exemplos provisórios pelos exemplos reais, quando necessário
- [ ] Revisar metadados e nomenclatura da atividade

# Navegação

[Voltar para Inteligência Artificial](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)

[Atividade anterior, Prompts e Dados Públicos](../prompts-e-dados-publicos/)

[Próxima atividade, Pacotes de Contexto](../pacotes-de-contexto/)
