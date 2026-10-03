# Atividade 01, Verificação e Validação

[Voltar para Validação e Qualidade de Software](../README.md)

## Metadados

| Campo | Informação |
|---|---|
| Unidade Curricular | Validação e Qualidade de Software |
| Curso | Análise e Desenvolvimento de Sistemas |
| Instituição | Faculdade Senac Pernambuco |
| Período | 5º período |
| Semestre | 2026.2 |
| Tipo | Atividade prática |
| Tema | Verificação e Validação de Software |
| Sistema analisado | AgendaFácil |
| Status | Concluído |

## Objetivo da atividade

A atividade tem como objetivo aplicar conceitos introdutórios de
**Verificação e Validação de Software** por meio da análise de requisitos,
classificação de situações e aplicação de princípios de teste.

O exercício também trabalha a importância da participação da equipe de
Qualidade desde as etapas iniciais do desenvolvimento.

## Contexto

A empresa fictícia **AgendaFácil** está desenvolvendo um sistema web
para agendamento de consultas médicas.

O sistema possui como funcionalidades iniciais:

1. Cadastro de paciente.
2. Login do paciente.
3. Consulta de horários disponíveis.
4. Agendamento de consulta.
5. Cancelamento de consulta.
6. Envio de confirmação por e-mail.

## Requisitos iniciais

| Código | Requisito |
|---|---|
| RQ-01 | O paciente deve conseguir se cadastrar no sistema |
| RQ-02 | O sistema deve permitir login com e-mail e senha |
| RQ-03 | O sistema deve mostrar horários disponíveis para consulta |
| RQ-04 | O paciente deve conseguir agendar uma consulta facilmente |
| RQ-05 | O paciente pode cancelar uma consulta quando necessário |
| RQ-06 | O sistema deve enviar confirmação por e-mail após o agendamento |
| RQ-07 | O sistema deve ser rápido e seguro |

## 1. Análise inicial de qualidade

Durante uma reunião, foi apresentada a seguinte afirmação:

> "Não precisamos testar agora. Quando o sistema estiver pronto,
> a equipe de QA procura os bugs."

### Qual é o problema dessa abordagem?

A equipe de QA não deve participar apenas após a conclusão do
desenvolvimento.

A qualidade precisa ser acompanhada durante todo o ciclo do projeto,
desde a análise dos requisitos até a implementação e validação final.

```text
Requisitos
    ↓
Planejamento
    ↓
Desenvolvimento
    ↓
Testes
    ↓
Entrega
```

O trabalho de qualidade deve ocorrer ao longo desse fluxo e não somente
na última etapa.

### Por que o QA deve participar antes do sistema ficar pronto?

A participação antecipada permite verificar se os padrões de qualidade
definidos nos requisitos estão sendo considerados durante o
desenvolvimento.

Isso também permite identificar problemas antes que eles se propaguem
para outras etapas.

### Riscos de testar apenas no final

Entre os riscos identificados estão:

- Erros de lógica.
- Problemas em validações.
- Implementação incorreta de regras de negócio.
- Necessidade de retrabalho.
- Descoberta tardia de defeitos.
- Aumento do custo de correção.

## 2. Verificação dos requisitos

A atividade solicitou a identificação de requisitos que apresentam
problemas de clareza, precisão ou testabilidade.

Foram analisados três requisitos.

### RQ-04

**Requisito original**

> O paciente deve conseguir agendar uma consulta facilmente.

### Problema encontrado

O requisito utiliza o termo subjetivo **"facilmente"**.

Não existe um critério mensurável que determine quando o agendamento
pode ser considerado fácil.

### Por que é difícil testar?

Sem uma métrica objetiva, diferentes pessoas podem interpretar
"facilmente" de maneiras diferentes.

### Versão melhorada

> O paciente deve conseguir agendar uma consulta em até 3 cliques ou toques.

---

### RQ-05

**Requisito original**

> O paciente pode cancelar uma consulta quando necessário.

### Problema encontrado

A expressão **"quando necessário"** é ambígua.

O requisito não informa:

- Até quando uma consulta pode ser cancelada.
- Se existe limite de antecedência.
- Se existe alguma penalidade.
- Se existem regras específicas.

### Por que é difícil testar?

A ausência dessas regras pode gerar diferentes interpretações entre
usuários, desenvolvedores e equipe de testes.

### Versão melhorada apresentada na atividade

> Taxa de 20% para cancelamentos com menos de 12 horas de antecedência.

---

### RQ-01

**Requisito original**

> O paciente deve conseguir se cadastrar no sistema.

### Problema encontrado

O requisito não informa quais dados são obrigatórios.

Também não especifica aspectos como:

- Verificação de e-mail.
- Verificação de telefone.
- Consentimento.
- Política de privacidade.

### Por que é difícil testar?

Sem essas definições, não é possível determinar com precisão quando
um cadastro deve ser considerado válido.

Também podem ocorrer problemas relacionados à experiência do usuário
ou à conformidade das regras do sistema.

### Versão melhorada

> O paciente deve poder se cadastrar fornecendo nome completo,
> e-mail, telefone e CPF, com verificação por código de confirmação
> enviado por e-mail e aceite explícito da Política de Privacidade.

## Síntese da análise dos requisitos

| Requisito | Problema | Principal questão |
|---|---|---|
| RQ-04 | Termo subjetivo | Testabilidade |
| RQ-05 | Regra ambígua | Clareza |
| RQ-01 | Dados obrigatórios não definidos | Completude |

A atividade demonstra que um requisito precisa ser:

```text
Claro
  +
Objetivo
  +
Mensurável
  +
Testável
```

## 3. Verificação ou Validação

A atividade também trabalhou a diferença entre **Verificação** e
**Validação**.

### Verificação

A verificação analisa artefatos do projeto, como:

- Requisitos.
- Documentação.
- Planos.
- Regras.

A principal pergunta é:

> Estamos construindo o produto corretamente?

### Validação

A validação observa o comportamento do sistema em execução.

A principal pergunta é:

> Estamos construindo o produto certo?

## Classificação das atividades

| Atividade | Classificação |
|---|---|
| Revisar se o requisito de cancelamento está claro | VER |
| Executar o login com e-mail e senha válidos | VAL |
| Conferir se o requisito de agendamento possui regra de horário disponível | VER |
| Testar se o sistema envia e-mail após agendar consulta | VAL |
| Analisar se o plano de testes cobre cadastro, login e agendamento | VER |
| Simular um paciente cancelando uma consulta pelo sistema | VAL |

## Relação entre Verificação e Validação

```text
REQUISITOS
    │
    ▼
VERIFICAÇÃO
    │
    │ análise dos artefatos
    ▼
DESENVOLVIMENTO
    │
    ▼
VALIDAÇÃO
    │
    │ execução do sistema
    ▼
COMPORTAMENTO OBSERVADO
```

## 4. Erro, defeito e falha

A atividade também apresentou situações para classificação entre
erro, defeito e falha.

As respostas registradas foram:

| Situação | Classificação |
|---|---|
| O analista escreveu "cancelar quando necessário", mas não definiu prazo mínimo | F |
| O código permite cancelar 5 minutos antes, mesmo que a regra correta fosse 24 horas | E |
| O paciente cancela 5 minutos antes e o sistema aceita | D |
| O desenvolvedor entendeu errado a regra de envio de e-mail | F |
| A função de envio de e-mail não é chamada após o agendamento | D |
| O paciente agenda, mas não recebe confirmação por e-mail | D |

## Relação conceitual

De maneira geral, problemas de software podem se propagar durante o
processo de desenvolvimento.

```text
Interpretação incorreta
        ↓
Implementação incorreta
        ↓
Comportamento inadequado
        ↓
Impacto para o usuário
```

Por isso, encontrar problemas ainda nos requisitos pode evitar que
eles sejam implementados no sistema.

## 5. Aplicação de princípios de teste

### Por que não é possível testar todas as combinações?

Cada funcionalidade possui múltiplas variáveis e diferentes
possibilidades de entrada e comportamento.

Quando funcionalidades são combinadas, a quantidade de cenários cresce
rapidamente.

Exemplo:

```text
Cadastro
   +
Login
   +
Horários
   +
Agendamento
   +
Cancelamento
   +
E-mail
```

Testar todas as combinações possíveis se torna inviável.

Por isso, os testes devem ser priorizados considerando:

- Risco.
- Impacto.
- Probabilidade.
- Valor para o usuário.
- Criticidade da funcionalidade.

## Funcionalidade prioritária

A funcionalidade considerada prioritária foi:

**Agendamento de consulta.**

A justificativa é que o agendamento representa a principal
funcionalidade do AgendaFácil.

```text
AgendaFácil
     ↓
Agendamento
     ↓
Principal valor entregue
```

Uma falha nessa funcionalidade compromete diretamente o objetivo
principal do sistema.

## Ausência de bugs não significa ausência de defeitos

O fato de nenhum problema ter sido encontrado durante os testes não
significa que o sistema esteja completamente correto.

Os testes executam apenas um conjunto limitado de condições.

```text
Cenários conhecidos
       ↓
Testados
       ↓
Nenhum defeito encontrado
```

Ainda podem existir:

```text
Cenários desconhecidos
       ↓
Não testados
       ↓
Possíveis defeitos
```

Esse conceito reforça o princípio de que testes podem demonstrar a
presença de defeitos, mas não provar sua ausência.

## Repetição dos mesmos cenários

Se a equipe executar sempre os mesmos testes, novas falhas podem deixar
de ser identificadas.

```text
Mesmos testes
     ↓
Mesmas entradas
     ↓
Mesmos caminhos
     ↓
Baixa capacidade de descobrir novos problemas
```

Por isso, é importante revisar e evoluir continuamente os cenários de
teste.

Também podem ser utilizados:

- Testes exploratórios.
- Novos dados de entrada.
- Cenários negativos.
- Testes de limite.
- Variações de fluxo.
- Novas combinações.

## Competências desenvolvidas

Esta atividade contribuiu para desenvolver competências relacionadas a:

- Análise de requisitos.
- Identificação de ambiguidades.
- Escrita de requisitos testáveis.
- Diferença entre verificação e validação.
- Análise de problemas de software.
- Priorização de testes.
- Pensamento baseado em risco.
- Aplicação de princípios de teste.

## Principais aprendizados

A atividade demonstrou que a qualidade de software começa antes da
execução dos testes.

Um requisito mal definido pode gerar problemas em diversas etapas.

```text
Requisito ambíguo
       ↓
Interpretação diferente
       ↓
Implementação inadequada
       ↓
Teste inconsistente
       ↓
Comportamento diferente do esperado
```

Por isso, atividades de verificação devem ocorrer desde o início do
desenvolvimento.

Também foi possível compreender que não é viável testar tudo.

A equipe precisa utilizar critérios de risco e prioridade para
selecionar os cenários mais importantes.

## Relação com o Projeto Integrador

Os conceitos desta atividade podem ser aplicados ao **ConectaStart**,
principalmente durante a definição e validação dos requisitos.

Exemplo:

```text
Requisito do ConectaStart
        ↓
Verificação
        ↓
O requisito está claro?
        ↓
Desenvolvimento
        ↓
Validação
        ↓
O sistema executa o comportamento esperado?
```

Esses conceitos podem ser utilizados para analisar funcionalidades como:

- Cadastro de startups.
- Cadastro de mentores.
- Autenticação.
- Perfis de usuário.
- Classificação por estágio.
- Oportunidades.
- Matchmaking.
- Feedback.
- Permissões de acesso.

[Acessar Projeto Integrador](../../../projeto-integrador/)

## Arquivo original

O conteúdo desta documentação foi elaborado a partir da atividade:

```text
Atividade 01 - Verificação e Validação.md
```

## Navegação

[Voltar para Validação e Qualidade de Software](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)
