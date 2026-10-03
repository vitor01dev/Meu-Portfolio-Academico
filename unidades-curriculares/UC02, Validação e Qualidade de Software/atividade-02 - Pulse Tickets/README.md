# PulseTickets, Avaliação de Qualidade para Release

[Voltar para Validação e Qualidade de Software](../README.md)

## Metadados

| Campo | Informação |
|---|---|
| Unidade Curricular | Validação e Qualidade de Software |
| Curso | Análise e Desenvolvimento de Sistemas |
| Instituição | Faculdade Senac Pernambuco |
| Período | 5º período |
| Semestre | 2026.2 |
| Tipo | Atividade prática de QA |
| Sistema analisado | PulseTickets |
| Tema | Priorização de testes e decisão de release |
| Abordagem | Testes baseados em risco |
| Documento principal | Relatório QA - Pulse Tickets.docx |
| Status | Concluído |

## Objetivo da atividade

A atividade teve como objetivo assumir a perspectiva de uma equipe de
**Quality Assurance** responsável por avaliar uma versão candidata à
produção da plataforma **PulseTickets**.

O cenário apresentava uma restrição importante, não havia tempo nem
recursos suficientes para testar todas as funcionalidades.

A equipe deveria selecionar apenas **10 novos cenários de teste** e,
com base nos riscos e nas evidências disponíveis, emitir um parecer
sobre a liberação da versão.

O exercício trabalha principalmente os conceitos de:

- Testes baseados em risco.
- Priorização de cenários.
- Análise de requisitos.
- Teste de valores limite.
- Testes negativos.
- Segurança.
- Desempenho.
- Experiência do usuário.
- Rastreabilidade.
- Avaliação de release.
- Gestão de riscos residuais.

# Contexto

A **PulseTickets** é uma plataforma de venda e gerenciamento de
ingressos digitais.

No cenário analisado, um festival com aproximadamente **45 mil
participantes** aconteceria em quatro dias.

A nova versão da plataforma estava prevista para entrar em produção
no dia seguinte, às 22h.

O parecer final da equipe de QA deveria ser entregue até as 19h.

```text
Festival
   ↓
aproximadamente 45 mil participantes
   ↓
Release no dia seguinte
   ↓
Tempo limitado para QA
   ↓
Somente 10 novos testes
   ↓
Decisão de release baseada em risco
```

## Funcionalidades envolvidas

A release possuía funcionalidades relacionadas a:

- Compra de ingressos.
- Aplicação de cupons.
- Transferência de ingressos.
- QR Code.
- Autenticação.
- Carteira digital.

# Regras identificadas

## Compra de ingressos

Cada usuário poderia adquirir entre:

```text
Mínimo: 1 ingresso

Máximo: 6 ingressos
```

A documentação não apresentava uma regra suficientemente clara para
quantidades como:

- Zero.
- Valores negativos.
- Quantidades superiores a seis.

Essa ausência de especificação exige cuidado para não classificar
automaticamente um comportamento inesperado como defeito.

## Cupom FEST20

O cupom **FEST20** possuía as seguintes regras:

```text
Desconto: 20%

Valor mínimo da compra: R$ 300,00

Desconto máximo: R$ 100,00

Uso: uma vez por cliente
```

Um ponto de ambiguidade identificado foi a expressão:

```text
"uma vez por cliente"
```

Não estava claramente definido se "cliente" correspondia a:

- Conta.
- CPF.
- Cartão.
- Pedido.
- Outro identificador.

## Transferência de ingressos

A transferência possuía regras relacionadas à janela disponível para
realização da operação.

Durante a análise, foi identificada uma inconsistência relacionada ao
limite de **120 minutos**, exigindo esclarecimento antes que determinado
comportamento pudesse ser classificado definitivamente como correto ou
incorreto.

## QR Code

Após uma transferência, o ingresso deveria possuir um novo QR Code.

O código anterior deveria deixar de permitir acesso, evitando que duas
pessoas utilizassem credenciais referentes ao mesmo ingresso.

## Autenticação

O cenário também previa mecanismo de autenticação utilizando código
temporário.

Entre as características consideradas estavam:

```text
Código: 6 dígitos

Validade: 5 minutos

Limite: 5 tentativas
```

## Desempenho

Entre os requisitos de desempenho analisados estava:

```text
95% das consultas em até 3 segundos
```

O cenário de carga considerado para a plataforma previa até:

```text
20 mil usuários simultâneos
```

## Experiência de compra

Também foi considerado um requisito relacionado ao tempo necessário
para finalizar uma compra.

```text
Tempo esperado: menos de 2 minutos
```

A experiência deveria ser considerada tanto em ambiente desktop
quanto mobile.

# Estratégia de teste

Como apenas 10 cenários poderiam ser selecionados, a estratégia
utilizada foi baseada no risco.

A prioridade não foi simplesmente testar uma funcionalidade de cada
vez, mas escolher os cenários capazes de revelar problemas com maior
impacto para o evento.

```text
Probabilidade
     +
Impacto
     ↓
Risco
     ↓
Prioridade de teste
```

Foram considerados principalmente riscos relacionados a:

- Impossibilidade de comprar ingressos.
- Venda acima dos limites definidos.
- Aplicação incorreta de descontos.
- Reutilização indevida de cupons.
- Venda concorrente do último ingresso.
- Transferência inconsistente.
- Utilização de QR Code antigo.
- Acesso indevido a ingresso de outro usuário.
- Falhas de desempenho.
- Experiência inadequada em dispositivos móveis.

# 10 cenários priorizados

## T01, Quantidade mínima de ingressos

**Objetivo:** validar o limite inferior permitido para compra.

```text
Quantidade: 1 ingresso
```

### Resultado registrado

**Aprovado.**

A compra com um ingresso foi aceita conforme a regra estabelecida.

---

## T02, Quantidade máxima de ingressos

**Objetivo:** validar o limite superior permitido.

```text
Quantidade: 6 ingressos
```

### Resultado registrado

**Aprovado.**

A plataforma aceitou a quantidade máxima prevista pela regra de negócio.

---

## T03, Quantidade superior ao limite

**Objetivo:** investigar o comportamento ao solicitar quantidade acima
do máximo documentado.

```text
Quantidade: 7 ingressos
```

### Resultado observado

O sistema retornou:

```text
HTTP 500
```

### Análise

O comportamento indica um problema técnico, pois um valor fora do
intervalo esperado resultou em erro interno.

Entretanto, como o requisito não definia explicitamente qual mensagem ou
tratamento deveria ser apresentado para quantidades superiores a seis,
a avaliação funcional ficou parcialmente inconclusiva.

O resultado correto deveria ser definido formalmente no requisito.

---

## T04, Cupom abaixo do valor mínimo

**Objetivo:** validar o limite imediatamente inferior ao mínimo exigido
para aplicação do cupom.

```text
Compra: R$ 299,99

Cupom: FEST20
```

### Resultado registrado

O cupom não foi aplicado.

O comportamento foi considerado compatível com a regra de valor mínimo
de R$ 300,00.

---

## T05, Cupom exatamente no valor mínimo

**Objetivo:** validar o valor limite para ativação do cupom.

```text
Compra: R$ 300,00

Cupom: FEST20
```

### Resultado registrado

O cupom foi aplicado conforme a regra documentada.

Esse cenário representa um exemplo de **Análise de Valor Limite**.

```text
R$ 299,99
    ↓
não aplica

R$ 300,00
    ↓
aplica
```

---

## T06, Transferência no limite de 120 minutos

**Objetivo:** verificar o comportamento da transferência exatamente no
limite informado.

### Resultado observado

A transferência foi bloqueada.

### Análise

O cenário revelou uma inconsistência na interpretação do requisito.

Não havia clareza suficiente para determinar se a transferência deveria
ser permitida ou bloqueada exatamente aos 120 minutos.

Por isso, o resultado exige:

**esclarecimento de requisito.**

```text
Regra ambígua
     ↓
Comportamento observado
     ↓
Não é possível classificar com segurança
     ↓
Solicitar esclarecimento
```

---

## T07, Validade do QR Code anterior

**Objetivo:** verificar se o QR Code anterior é invalidado após a
transferência do ingresso.

### Resultado observado

O QR Code antigo permaneceu utilizável durante aproximadamente:

```text
47 segundos
```

### Impacto

Esse comportamento representa risco elevado, pois dois códigos
relacionados ao mesmo ingresso podem permanecer utilizáveis durante uma
janela de tempo.

```text
Transferência
     ↓
Novo QR Code
     ↓
QR antigo deveria ser invalidado
     ↓
QR antigo continua válido
     ↓
Risco de acesso duplicado
```

Esse foi um dos problemas mais críticos identificados na avaliação.

---

## T08, Acesso a ingresso de outro usuário

**Objetivo:** verificar se um usuário consegue acessar um ingresso que
não lhe pertence.

### Resultado registrado

O acesso indevido foi bloqueado.

O comportamento forneceu evidência favorável aos controles de
autorização do sistema.

---

## T09, Desempenho sob carga

**Objetivo:** avaliar o requisito de desempenho da plataforma.

### Cenário executado

```text
Carga utilizada: 5 mil usuários

Resultado:
94% das consultas abaixo de 3 segundos
```

### Requisito

```text
95% das consultas em até 3 segundos
```

### Análise

O resultado ficou abaixo do requisito estabelecido.

```text
Esperado: 95%

Obtido: 94%
```

Existe ainda uma limitação adicional.

O cenário previsto para a plataforma era de até:

```text
20 mil usuários simultâneos
```

mas o teste registrado utilizou apenas 5 mil.

Portanto, existem dois pontos de atenção:

1. O requisito de 95% não foi alcançado.
2. A carga utilizada não representa o volume máximo previsto.

---

## T10, Fluxo de compra em dispositivo móvel

**Objetivo:** avaliar a experiência do usuário durante uma compra em
smartphone.

### Resultado observado

Tempo registrado:

```text
4 minutos e 38 segundos
```

### Requisito considerado

```text
Compra em menos de 2 minutos
```

### Análise

O tempo observado ultrapassou significativamente o valor esperado.

```text
Esperado
< 2 minutos

Obtido
4 minutos e 38 segundos
```

O cenário representa risco para a experiência do usuário, principalmente
considerando o alto volume de participantes esperado para o evento.

# Resumo dos resultados

| Teste | Cenário | Resultado |
|---|---|---|
| T01 | Compra de 1 ingresso | Favorável |
| T02 | Compra de 6 ingressos | Favorável |
| T03 | Compra de 7 ingressos | HTTP 500, comportamento funcional não totalmente especificado |
| T04 | FEST20 em R$ 299,99 | Favorável |
| T05 | FEST20 em R$ 300,00 | Favorável |
| T06 | Transferência aos 120 minutos | Requisito necessita esclarecimento |
| T07 | QR Code antigo após transferência | Problema crítico |
| T08 | Acesso a ingresso alheio | Favorável |
| T09 | Desempenho com 5 mil usuários | Abaixo do requisito |
| T10 | Compra em smartphone | Acima do tempo esperado |

# Principais riscos identificados

## 1. QR Code antigo permanecer válido

A permanência do QR anterior após a transferência pode permitir
tentativas de acesso utilizando uma credencial que deveria ter sido
invalidada.

**Impacto:** crítico.

## 2. Desempenho abaixo do requisito

O sistema atingiu 94% das consultas abaixo de três segundos, enquanto o
requisito estabelecia 95%.

**Impacto:** alto.

## 3. Teste de carga insuficiente

O cenário avaliado utilizou 5 mil usuários, enquanto a plataforma
precisava considerar até 20 mil usuários simultâneos.

**Impacto:** alto.

## 4. Experiência mobile inadequada

O fluxo analisado levou 4 minutos e 38 segundos, superando o tempo
esperado de menos de dois minutos.

**Impacto:** alto.

## 5. Requisitos ambíguos

Foram encontradas regras que não permitiam determinar objetivamente o
resultado esperado.

Exemplos:

- Definição de "cliente" no FEST20.
- Comportamento exatamente aos 120 minutos.
- Tratamento esperado para mais de seis ingressos.

# Riscos não totalmente cobertos

Mesmo com os 10 testes selecionados, alguns riscos permanecem.

Isso ocorre porque:

```text
Sistema complexo
      +
Tempo limitado
      +
Somente 10 cenários
      ↓
Cobertura parcial
```

Entre os riscos residuais estão:

- Comportamentos sob carga próxima de 20 mil usuários.
- Combinações adicionais entre compra, cupom e transferência.
- Variações de dispositivos móveis.
- Falhas de rede durante operações críticas.
- Cenários adicionais de autenticação.
- Reutilização de cupom considerando diferentes definições de cliente.

# Princípios de teste aplicados

## Testes demonstram a presença de defeitos

A execução de testes pode revelar problemas, mas não provar que o
software está completamente livre deles.

## Teste exaustivo é impossível

Não seria possível testar todas as combinações entre:

```text
Quantidade
   ×
Cupom
   ×
Usuário
   ×
Transferência
   ×
QR Code
   ×
Autenticação
   ×
Dispositivo
   ×
Carga
```

Por isso, foi necessária uma estratégia de priorização.

## Testar cedo reduz riscos

Ambiguidades como a regra dos 120 minutos e a definição de "cliente"
deveriam ser esclarecidas antes da implementação ou da fase final de QA.

## Defeitos tendem a se concentrar

Algumas áreas apresentam riscos significativamente maiores.

No PulseTickets, destacaram-se:

- Transferência.
- QR Code.
- Desempenho.
- Fluxo de compra.

## Os testes precisam evoluir

Executar sempre os mesmos cenários reduz a capacidade de encontrar
novos problemas.

Por isso, cenários de limite, concorrência, carga e experiência do
usuário precisam complementar os caminhos convencionais.

# Rastreabilidade

A atividade reforça a necessidade de manter ligação entre:

```text
Risco
  ↓
Teste
  ↓
Resultado
  ↓
Evidência
  ↓
Impacto
  ↓
Decisão de release
```

Exemplo:

| Risco | Teste | Resultado | Impacto |
|---|---|---|---|
| Compra acima do limite | T03 | HTTP 500 | Tratamento inadequado de entrada |
| Transferência ambígua | T06 | Bloqueada aos 120 min | Requisito precisa ser esclarecido |
| QR antigo reutilizável | T07 | Válido por aproximadamente 47s | Risco crítico de acesso |
| Desempenho | T09 | 94% abaixo de 3s | Requisito não atingido |
| Experiência mobile | T10 | 4min38s | Tempo acima do esperado |

# Parecer de QA

Com base nos resultados registrados na atividade, a recomendação foi:

## NÃO RECOMENDADO PARA LIBERAÇÃO

A decisão foi motivada principalmente pelos seguintes fatores:

1. O QR Code anterior permaneceu válido após a transferência.
2. O requisito de desempenho de 95% não foi atingido.
3. O teste de carga utilizou apenas 5 mil usuários diante de um cenário de até 20 mil.
4. O fluxo de compra mobile excedeu o tempo esperado.
5. O sistema apresentou HTTP 500 ao processar quantidade superior ao limite.
6. Existiam requisitos que ainda necessitavam de esclarecimento.

```text
Evidências
    ↓
Riscos críticos
    ↓
Riscos residuais
    ↓
Release
    ↓
NÃO RECOMENDADA
```

A decisão não significa que todo o sistema estava incorreto.

Ela indica que as evidências disponíveis naquele momento não eram
suficientes para considerar o risco da liberação aceitável.

# Competências desenvolvidas

A atividade contribuiu para o desenvolvimento das seguintes
competências:

- Priorização baseada em risco.
- Análise de requisitos.
- Identificação de ambiguidades.
- Testes positivos.
- Testes negativos.
- Análise de Valor Limite.
- Testes de autorização.
- Testes de desempenho.
- Testes de experiência do usuário.
- Avaliação de riscos residuais.
- Rastreabilidade.
- Comunicação de resultados.
- Tomada de decisão sobre release.

# Principais aprendizados

A atividade demonstrou que a função do QA não é simplesmente executar
o maior número possível de testes.

Quando existem restrições de tempo e recursos, é necessário identificar
quais falhas podem causar maior impacto.

```text
Não testar tudo
      ↓
Identificar riscos
      ↓
Priorizar
      ↓
Produzir evidências
      ↓
Avaliar riscos residuais
      ↓
Tomar decisão
```

Outro aprendizado importante foi a diferença entre:

```text
Defeito comprovado

e

Requisito insuficiente
```

Um comportamento inesperado não deve ser automaticamente classificado
como bug quando não existe informação suficiente para determinar o
comportamento correto.

Nesses casos, a ação adequada é registrar a necessidade de
esclarecimento do requisito.

# Relação com o Projeto Integrador

Os conceitos utilizados na atividade podem ser aplicados ao
**ConectaStart** durante a validação de uma futura release.

Uma estratégia semelhante poderia priorizar riscos associados a:

- Cadastro de startups.
- Autenticação.
- Perfis.
- Estágios de desenvolvimento.
- Matchmaking.
- Oportunidades.
- Controle de acesso.
- Dados pessoais.
- Desempenho.
- Compatibilidade mobile.

Exemplo:

```text
ConectaStart
      ↓
Identificação de riscos
      ↓
Priorização dos fluxos críticos
      ↓
Casos de teste
      ↓
Evidências
      ↓
Quality Gate
      ↓
GO / RESTRIÇÕES / NO-GO
```

[Acessar Projeto Integrador](../../../projeto-integrador/)

# Documento original

O relatório completo da atividade está armazenado no arquivo:

```text
Relatório QA - Pulse Tickets.docx
```

Sugestão de organização:

```text
pulsetickets/
│
├── README.md
└── Relatório QA - Pulse Tickets.docx
```

# Navegação

[Voltar para Validação e Qualidade de Software](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)
