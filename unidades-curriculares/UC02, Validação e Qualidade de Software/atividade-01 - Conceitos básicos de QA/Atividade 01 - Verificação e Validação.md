# ATIVIDADE 01

## Contexto

A empresa fictícia **AgendaFácil** está desenvolvendo um sistema web para agendamento de consultas médicas.

O sistema terá as seguintes funcionalidades iniciais:

1. Cadastro de paciente;
2. Login do paciente;
3. Consulta de horários disponíveis;
4. Agendamento de consulta;
5. Cancelamento de consulta;
6. Envio de confirmação por e-mail.

A equipe de desenvolvimento recebeu os seguintes requisitos:

| Código | Requisito                                                        |
| ------ | ---------------------------------------------------------------- |
| RQ-01  | O paciente deve conseguir se cadastrar no sistema.               |
| RQ-02  | O sistema deve permitir login com e-mail e senha.                |
| RQ-03  | O sistema deve mostrar horários disponíveis para consulta.       |
| RQ-04  | O paciente deve conseguir agendar uma consulta facilmente.       |
| RQ-05  | O paciente pode cancelar uma consulta quando necessário.         |
| RQ-06  | O sistema deve enviar confirmação por e-mail após o agendamento. |
| RQ-07  | O sistema deve ser rápido e seguro.                              |


- Durante uma reunião, o gerente afirmou: *“Não precisamos testar agora. Quando o sistema estiver pronto, a equipe de QA procura os bugs.”*

---

## Tarefas

### Parte 1 — Análise inicial de qualidade

Responda objetivamente:

**1. Qual o problema da fala do gerente?**

**R-** A fala do gerente não é profissional, pois não está seguindo as normas de qualidade, uma vez que a equipe de QA deve acompanha realizando seu trabalho desde o início, desenvolvimento e finalização do projeto.

**2. Por que o QA deveria participar antes do sistema ficar pronto?**

**R-** Para garantir que os padrões de qualidades estabelecidos nos requisitos sejam cumpridos ao longo do desenvolvimento.

**3. Cite dois riscos de deixar os testes apenas para o final.**

**R-** Os principais risco se relacionam com erros de lógica (Ex: "uma validação") e problemas de regra de negócio (Ex: "o processo é realizado sem falhas, mas de forma diferente do que foi pré-estabelecido.")

---

### Parte 2 — Verificação dos requisitos

Analise os requisitos da tabela e escolha 3 requisitos problemáticos.

Para cada requisito escolhido, preencha:

```bash
| Requisito | Problema encontrado | Por que é difícil testar? | Versão melhorada |
| --------- | ------------------- | ------------------------- | ---------------- |
```

**Exemplo:**

| Requisito | Problema encontrado                        | Por que é difícil testar?                                      | Versão melhorada |
| --------- | ------------------------------------------ | ----------------------------------------------------------     | -----------------|
| RQ-07     | Usa termos vagos como “rápido” e “seguro”. | Não define tempo, critério de segurança nem condição de teste. | O sistema deve carregar a lista de horários disponíveis em até 3 segundos para até 100 horários cadastrados. |



**Resolução**

| Requisito | Problema encontrado                        | Por que é difícil testar?                                      | Versão melhorada |
| --------- | ------------------------------------------ | -------------------------------------------------------------- | -----------------|
| RQ-04     | Usa um termo subjetivo "facilmente".   | Não metrifica passos para o a agendamento ser realizado.       | O paciente deve conseguir agendar uma consulta em até 3 cliques/toques. |
| RQ-05 | A expressão "quando necessário" é ambígua. | Permite cancelamento em qualquer momento? Há restrições de horário? A falta dessas definições pode criar conflitos entre os usuário e o sistema | "Taxa de 20% para cancelamentos com menos de 12h de antecedência" |
| RQ-01 | Não especifica quais dados são obrigatórios, se há necessidade de verificação de e-mail/telefone, ou políticas de privacidade e consentimento. | Pode gerar atrito no cadastro ou inconformidade regulatória | "O paciente deve poder se cadastrar fornecendo nome completo, e-mail, telefone e CPF, como verificação por código de confirmação enviado por e-mail e aceite explícito da Política de Privacidade" |


---

### Parte 3 — Verificação ou validação?

Classifique as atividades abaixo como verificação (VER) ou validação (VAL).

| Atividade                                                                  | Verificação ou Validação? |
| -------------------------------------------------------------------------- |:-------------------------:|
| Revisar se o requisito de cancelamento está claro.                         |         VER               |
| Executar o login com e-mail e senha válidos.                               |         VAL               |
| Conferir se o requisito de agendamento possui regra de horário disponível. |         VER               |
| Testar se o sistema envia e-mail após agendar consulta.                    |         VAL               |
| Analisar se o plano de testes cobre cadastro, login e agendamento.         |         VER               |
| Simular um paciente cancelando uma consulta pelo sistema.                  |         VAL               |

---

### Parte 4 — Erro, defeito ou falha?

Classifique cada situação como erro (E), defeito (D) ou falha (F).

| Situação                                                                                                  | Erro, Defeito ou Falha? |
| --------------------------------------------------------------------------------------------------------- |:-----------------------:|
| O analista escreveu “cancelar quando necessário”, mas não definiu prazo mínimo para cancelamento.         |           F             |
| O código permite cancelar consulta 5 minutos antes do horário, mesmo que a regra correta fosse 24h antes. |           E             |
| O paciente cancela a consulta 5 minutos antes e o sistema aceita indevidamente.                           |           D             |
| O desenvolvedor entendeu errado a regra de envio de e-mail.                                               |           F             |
| A função de envio de e-mail não é chamada após o agendamento.                                             |           D             |
| O paciente agenda a consulta, mas não recebe nenhum e-mail de confirmação.                                |           D             |

---

### Parte 5 — Aplicando princípios de teste

Responda:

**1. Por que não seria possível testar todas as combinações possíveis de cadastro, login, agendamento e cancelamento?**

**R-** Inumeras combinações, cada funcionalidade tem múltiplas variáveis, neste caso, deve-se priorizar cenários baseados em risco e valor.

**2. Qual funcionalidade deveria receber mais atenção nos testes: cadastro, login, agendamento ou e-mail? Justifique.**

**R-** Agendamento, pois é a funcionalidade principal do sistema

**3. Por que “nenhum bug encontrado” não significa que o sistema está correto?**

**R-** Testes demonstram presença, não ausência de defeitos (Dijkstra): passar nos testes conhecidos não garante que testes desconhecidos também passarão.

**4. O que poderia acontecer se a equipe sempre testasse os mesmos cenários?**

**R-** Uma validação equivocada, por justamente não avaliar os cenários atípicos.

---
