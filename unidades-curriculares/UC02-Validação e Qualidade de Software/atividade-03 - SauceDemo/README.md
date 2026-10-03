# SauceDemo, QA Release Assessment

[Voltar para Validação e Qualidade de Software](../README.md)

## Metadados

| Campo | Informação |
|---|---|
| Unidade Curricular | Validação e Qualidade de Software |
| Curso | Análise e Desenvolvimento de Sistemas |
| Instituição | Faculdade Senac Pernambuco |
| Período | 5º período |
| Semestre | 2026.2 |
| Tipo | QA Release Assessment |
| Sistema analisado | SauceDemo, Swag Labs |
| Abordagem | Testes baseados em risco |
| Usuário designado | `standard_user` |
| Documento principal | Relatório, Casos de Testes e Critérios de Aceitação.docx |
| Status | Concluído |
| Quality Gate | GO WITH RESTRICTIONS |

## Objetivo da atividade

A atividade teve como objetivo realizar uma avaliação de qualidade de uma
versão candidata à produção do **SauceDemo, Swag Labs**, utilizando uma
abordagem de QA baseada em risco.

O cenário parte da necessidade de fornecer evidências suficientes para
apoiar uma decisão de release, considerando que não existe tempo para testar
todas as funcionalidades e combinações possíveis do sistema.

O trabalho envolveu:

- Reconhecimento inicial da aplicação.
- Identificação de funcionalidades críticas.
- Análise de riscos.
- Planejamento de testes.
- Criação de casos de teste.
- Definição de critérios de aceitação.
- Execução de testes priorizados.
- Registro de evidências.
- Investigação de comportamentos inesperados.
- Avaliação de riscos residuais.
- Definição de um Quality Gate.

# Sistema analisado

O **SauceDemo, Swag Labs** é uma aplicação de comércio eletrônico utilizada
para práticas de teste de software.

Os principais fluxos analisados foram:

```text
Login
  ↓
Catálogo
  ↓
Produto
  ↓
Carrinho
  ↓
Checkout
  ↓
Resumo da compra
  ↓
Finalização do pedido
```

Durante o reconhecimento inicial, os fluxos de login, catálogo e visualização
de produtos não apresentaram anomalias relevantes dentro do escopo executado.

Os principais pontos de atenção foram encontrados no processo de checkout.

# Estratégia de teste

A estratégia adotada priorizou funcionalidades relacionadas diretamente à
conclusão de uma compra.

O raciocínio utilizado foi:

```text
Funcionalidade
      ↓
Risco
      ↓
Impacto no usuário
      ↓
Prioridade
      ↓
Caso de teste
      ↓
Evidência
      ↓
Quality Gate
```

O objetivo não foi testar tudo, mas produzir evidências suficientes para
avaliar os riscos mais relevantes para uma possível liberação.

# Funcionalidades prioritárias

## 1. Checkout

O checkout representa uma das etapas mais críticas da jornada de compra.

Problemas nessa funcionalidade podem impedir a conclusão do pedido ou causar
perda das informações fornecidas pelo usuário.

## 2. Carrinho e valores monetários

A apresentação correta dos valores é necessária para garantir clareza durante
a compra.

Mesmo quando o cálculo interno está correto, uma apresentação monetária
inadequada pode gerar insegurança para o usuário.

## 3. Navegação durante a finalização da compra

A interação por teclado e a persistência dos dados durante mudanças de tela
foram consideradas importantes para avaliar a experiência de uso.

# Riscos de qualidade

Os principais riscos identificados durante a atividade foram:

| Risco | Impacto |
|---|---|
| Perda dos dados do formulário de checkout | Médio |
| Navegação inesperada ao utilizar a tecla Enter | Médio |
| Exibição inadequada de valores monetários | Médio |
| Encerramento da sessão após aproximadamente 2 minutos | Médio |
| Possível rollback durante o checkout | Não confirmado durante a reprodução |

# Casos de teste executados

Entre os casos planejados, quatro foram priorizados para execução e produção
de evidências.

## CT-01, Compra válida

### Objetivo

Confirmar que o fluxo principal de compra pode ser concluído corretamente.

### Procedimento geral

```text
Login
  ↓
Adicionar produto
  ↓
Carrinho
  ↓
Checkout
  ↓
Preencher dados
  ↓
Continuar
  ↓
Finalizar
```

### Comportamento observado

O fluxo principal foi concluído dentro do esperado.

Após a finalização foi apresentada a mensagem:

```text
Thank you for your order!
```

### Resultado

**Aprovado.**

---

## CT-02, Checkout sem dados obrigatórios

### Objetivo

Verificar o comportamento do sistema quando o usuário tenta avançar no
checkout sem fornecer os dados obrigatórios.

### Comportamento observado

O sistema bloqueou corretamente o avanço para a próxima etapa quando os
campos obrigatórios estavam vazios.

### Resultado

**Aprovado.**

### Evidência relacionada

```text
Evidência_campos_vazios.jpg
```

---

## CT-05, Valores monetários

### Objetivo

Verificar se os valores apresentados durante o checkout possuem formatação
monetária adequada.

### Produtos utilizados

```text
Sauce Labs Fleece Jacket: $49,99

Sauce Labs Onesie: $7,99

Taxa: $4,64
```

Durante o cenário foi observada a apresentação de um valor intermediário
com precisão decimal inadequada:

```text
57,98000000000004
```

O problema identificado está relacionado à **apresentação do valor**.

O cálculo final da compra não foi identificado como incorreto durante a
execução.

### Resultado

**Reprovado.**

### Análise

Valores monetários apresentados ao usuário devem possuir representação
consistente.

Exemplo esperado:

```text
57,98
```

Em vez de:

```text
57,98000000000004
```

Esse comportamento pode reduzir a confiança do usuário no processo de compra,
mesmo quando o cálculo final está correto.

---

## CT-06, Navegação por teclado

### Objetivo

Avaliar o comportamento do formulário de checkout quando o usuário utiliza
a tecla **Enter**.

### Comportamento observado

Após preencher os dados do checkout e pressionar a tecla Enter, o sistema
retornou para a tela anterior.

Além disso, os dados preenchidos foram perdidos.

```text
Formulário preenchido
        ↓
Tecla Enter
        ↓
Retorno à tela anterior
        ↓
Dados do formulário perdidos
```

### Resultado

**Reprovado.**

### Evidência relacionada

```text
Evidencia_Tecla_Enter_RollBack.jpg
```

# Persistência dos dados

Durante a investigação do checkout também foi observado que os dados
preenchidos não são preservados quando o usuário sai da tela e retorna
posteriormente.

Exemplo:

```text
Usuário preenche:
Nome
Sobrenome
CEP

        ↓

Sai da tela

        ↓

Retorna ao checkout

        ↓

Campos vazios
```

Esse comportamento representa risco para a experiência do usuário, pois exige
o preenchimento repetido das mesmas informações.

# Timeout de sessão

Durante os testes foi observado encerramento da sessão após aproximadamente:

```text
2 minutos
```

A evidência correspondente foi registrada no arquivo:

```text
Evidência_TimeOut.jpg
```

Esse comportamento foi tratado como ponto de atenção para o Quality Gate.

Como o comportamento esperado da duração da sessão dependia de requisito
específico, o resultado precisa ser analisado considerando a especificação
aplicável ao sistema.

# Rollback durante o checkout

Também havia relato de ocorrência de rollback durante o preenchimento ou
transição do checkout.

Entretanto, esse comportamento não foi reproduzido de forma consistente
durante a investigação.

Por isso, ele não foi tratado como defeito confirmado.

```text
Comportamento relatado
        ↓
Tentativa de reprodução
        ↓
Não reproduzido de forma consistente
        ↓
Risco permanece
        ↓
Necessita investigação adicional
```

Essa distinção é importante em QA.

Um relato de comportamento não deve ser automaticamente registrado como
defeito confirmado sem evidência suficiente.

# Critérios de aceitação

Foram definidos quatro critérios de aceitação para apoiar a avaliação do
checkout.

## Critério 1, Comportamento esperado

**Tipo:** BDD

```gherkin
Dado que o usuário está na página de checkout
Quando ele preencher corretamente os dados de envio
E avançar para a próxima etapa
Então o sistema deve permitir a continuidade do processo de compra
mantendo os dados necessários ao fluxo.
```

## Critério 2, Regra negativa

**Tipo:** BDD

```gherkin
Dado que o usuário está na página de checkout
Quando tentar avançar sem preencher os campos obrigatórios
Então o sistema deve impedir a continuidade
E apresentar a validação correspondente.
```

## Critério 3, Persistência de dados

**Tipo:** Regra de negócio e experiência

Os dados informados pelo usuário durante o checkout devem permanecer
disponíveis quando ele navegar entre etapas relacionadas ao processo de compra,
desde que a sessão continue válida.

Os dados considerados são:

- Nome.
- Sobrenome.
- CEP.

## Critério 4, Apresentação monetária

**Tipo:** Experiência e qualidade

Os valores monetários apresentados durante a compra devem utilizar formatação
consistente e apropriada para valores financeiros.

Exemplo:

```text
Correto:
57,98

Inadequado:
57,98000000000004
```

# Evidências

As evidências produzidas durante a atividade foram organizadas junto ao
relatório.

```text
saucedemo/
│
├── README.md
│
├── Relatório - Casos de Testes e Critérios de Aceitação.docx
│
└── evidencias/
    ├── Evidência_campos_vazios.jpg
    ├── Evidencia_Tecla_Enter_RollBack.jpg
    ├── Evidencia_Tela_checkout.jpg
    ├── Evidencia_Tela_Compra_Finalizada.jpg
    └── Evidência_TimeOut.jpg
```

## Evidência, campos vazios

```text
Evidência_campos_vazios.jpg
```

Relacionada ao **CT-02**, demonstra a validação do sistema quando os campos
obrigatórios do checkout não são preenchidos.

## Evidência, tecla Enter

```text
Evidencia_Tecla_Enter_RollBack.jpg
```

Relacionada ao **CT-06**, registra o comportamento observado durante a
navegação utilizando o teclado.

## Evidência, checkout

```text
Evidencia_Tela_checkout.jpg
```

Registra a tela utilizada durante a investigação do fluxo de checkout.

## Evidência, compra finalizada

```text
Evidencia_Tela_Compra_Finalizada.jpg
```

Relacionada ao fluxo principal aprovado, demonstrando a conclusão da compra.

## Evidência, timeout

```text
Evidência_TimeOut.jpg
```

Registra o comportamento de encerramento da sessão observado durante a
execução.

# Resumo dos testes priorizados

| ID | Cenário | Resultado |
|---|---|---|
| CT-01 | Compra válida | Aprovado |
| CT-02 | Checkout sem dados obrigatórios | Aprovado |
| CT-05 | Formatação dos valores monetários | Reprovado |
| CT-06 | Navegação utilizando Enter | Reprovado |

```text
4 testes executados

2 aprovados

2 reprovados
```

# Ocorrências identificadas

## Ocorrência 1, Formatação monetária inconsistente

**Funcionalidade:** Carrinho e checkout.

**Comportamento observado:**

```text
57,98000000000004
```

**Impacto:** Médio.

O cálculo da compra foi considerado correto, mas a apresentação do valor não
estava adequada.

---

## Ocorrência 2, Tecla Enter altera inesperadamente a navegação

**Funcionalidade:** Checkout.

**Comportamento observado:**

Ao pressionar Enter, o usuário retorna para a etapa anterior e os dados
preenchidos são perdidos.

**Impacto:** Médio.

---

## Ocorrência 3, Dados do checkout não são preservados

**Funcionalidade:** Checkout.

**Comportamento observado:**

Os campos preenchidos são apagados quando o usuário sai da tela e retorna.

**Impacto:** Médio.

---

## Ocorrência 4, Timeout de sessão

**Funcionalidade:** Sessão.

**Comportamento observado:**

A sessão foi encerrada após aproximadamente dois minutos.

**Impacto:** Médio.

O comportamento exige comparação com o requisito de sessão aplicável antes de
uma classificação definitiva.

# Quality Gate

Com base nos testes executados e nas evidências registradas, a decisão foi:

## GO WITH RESTRICTIONS

A aplicação apresentou funcionamento adequado no fluxo principal e nas
validações obrigatórias avaliadas.

Entretanto, foram encontrados comportamentos que precisam ser corrigidos ou
esclarecidos antes que a versão seja considerada livre de restrições.

| Elemento | Resultado |
|---|---|
| Decisão | GO WITH RESTRICTIONS |
| Evidência 1 | CT-01 confirmou que a compra pode ser concluída |
| Evidência 2 | CT-05 identificou apresentação monetária inadequada |
| Evidência 3 | CT-06 identificou problema de navegação e perda dos dados |
| Risco residual 1 | Possível rollback relatado, mas não reproduzido consistentemente |
| Risco residual 2 | Timeout de aproximadamente 2 minutos necessita validação contra requisito |
| Ação 1 | Corrigir o comportamento da tecla Enter e executar novo teste de regressão |
| Ação 2 | Corrigir a formatação monetária e esclarecer o requisito de duração da sessão |

# Rastreabilidade

| Risco | Caso de teste | Resultado | Evidência | Impacto no Quality Gate |
|---|---|---|---|---|
| Falha no fluxo principal | CT-01 | Aprovado | Tela de compra finalizada | Favorável à release |
| Campos obrigatórios não validados | CT-02 | Aprovado | Evidência de campos vazios | Favorável à release |
| Valores monetários inconsistentes | CT-05 | Reprovado | Comportamento registrado no checkout | Restrição |
| Navegação inesperada e perda de dados | CT-06 | Reprovado | Evidência da tecla Enter | Restrição |
| Timeout da sessão | Investigação exploratória | Aproximadamente 2 minutos | Evidência de timeout | Risco residual |
| Rollback | Investigação | Não reproduzido consistentemente | Sem confirmação suficiente | Risco residual |

# Interpretação do Quality Gate

A decisão **GO WITH RESTRICTIONS** significa que:

```text
Fluxo principal funciona
        +
Validações básicas funcionam
        ↓
Release tecnicamente possível

MAS

Problemas de experiência
        +
Formatação monetária
        +
Navegação pelo teclado
        +
Riscos ainda não esclarecidos
        ↓
Release com restrições
```

A decisão não significa que os problemas encontrados sejam irrelevantes.

Ela indica que, considerando o escopo de testes executado, não foi identificada
uma falha que bloqueasse completamente o fluxo principal, mas existem riscos
que precisam de tratamento e acompanhamento.

# Principais aprendizados

A atividade demonstrou que uma avaliação de release não deve ser baseada
apenas na pergunta:

```text
"O sistema funciona?"
```

Uma análise de QA precisa considerar:

```text
O fluxo funciona?
        ↓
As regras são respeitadas?
        ↓
Os dados são preservados?
        ↓
Os valores são apresentados corretamente?
        ↓
A experiência é consistente?
        ↓
Quais riscos permanecem?
        ↓
Existem evidências suficientes?
        ↓
A release pode avançar?
```

Também foi possível observar que um defeito não precisa impedir completamente
o sistema de funcionar para representar risco de qualidade.

Problemas relacionados a:

- Navegação.
- Persistência.
- Apresentação monetária.
- Sessão.
- Experiência do usuário.

também podem influenciar uma decisão de release.

# Diferenciação entre defeito e requisito não esclarecido

Outro aprendizado importante foi evitar classificar automaticamente todo
comportamento inesperado como bug.

```text
Comportamento inesperado
        ↓
Existe requisito claro?
       / \
     Sim  Não
     ↓     ↓
Comparar  Solicitar
com o     esclarecimento
esperado
```

Essa abordagem foi especialmente importante para avaliar:

- Timeout de sessão.
- Rollback relatado, mas não reproduzido.

# Competências desenvolvidas

A atividade contribuiu para desenvolver competências relacionadas a:

- QA baseado em risco.
- Release Assessment.
- Testes funcionais.
- Testes negativos.
- Testes exploratórios.
- Critérios de aceitação.
- BDD.
- Análise de experiência do usuário.
- Registro de evidências.
- Investigação de defeitos.
- Rastreabilidade.
- Gestão de riscos residuais.
- Quality Gate.
- Comunicação de decisão de release.

# Relação com o Projeto Integrador

Os conhecimentos adquiridos nesta atividade podem ser aplicados ao
**ConectaStart** durante uma futura avaliação de release.

Uma estratégia semelhante poderia avaliar fluxos como:

```text
Cadastro da startup
        ↓
Definição do estágio
        ↓
Perfil
        ↓
Matchmaking
        ↓
Conexão com mentor
        ↓
Feedback
```

Antes da liberação, poderiam ser definidos casos de teste para validar:

- Cadastro.
- Campos obrigatórios.
- Persistência dos dados.
- Autenticação.
- Navegação.
- Classificação por estágio.
- Matchmaking.
- Permissões.
- Apresentação das informações.
- Responsividade.
- Sessão.
- Integrações.

O processo poderia seguir:

```text
Riscos
   ↓
Casos de teste
   ↓
Execução
   ↓
Evidências
   ↓
Riscos residuais
   ↓
Quality Gate
   ↓
GO
GO WITH RESTRICTIONS
NO-GO
```

[Acessar Projeto Integrador](../../../projeto-integrador/)

# Documento original

O relatório completo da atividade está armazenado no arquivo:

```text
Relatório - Casos de Testes e Critérios de Aceitação.docx
```

# Navegação

[Voltar para Validação e Qualidade de Software](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)
