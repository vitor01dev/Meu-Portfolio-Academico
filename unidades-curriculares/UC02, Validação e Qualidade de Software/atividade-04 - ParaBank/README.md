# ParaBank, Dossiê de Testes da Release

[Voltar para Validação e Qualidade de Software](../README.md)

## Metadados

| Campo | Informação |
|---|---|
| Unidade Curricular | Validação e Qualidade de Software |
| Curso | Análise e Desenvolvimento de Sistemas |
| Instituição | Faculdade Senac Pernambuco |
| Período | 5º período |
| Semestre | 2026.2 |
| Tipo | Dossiê de Testes |
| Sistema analisado | ParaBank |
| Abordagem | Testes baseados em risco |
| Objetivo | Avaliação funcional, de usabilidade e segurança |
| Situação da rodada | Inconclusiva para liberação definitiva |
| Status final | Não recomendado para homologação definitiva ou produção |

## Objetivo da atividade

A atividade teve como objetivo avaliar a qualidade da release do sistema
**ParaBank**, considerando principalmente aspectos funcionais, de usabilidade
e segurança.

A estratégia adotada utilizou **testes baseados em risco**, priorizando
cenários capazes de revelar problemas com maior impacto para uma aplicação
financeira.

A avaliação considerou somente casos de teste que possuíam evidências de
execução efetiva.

## Resumo da rodada

Durante a rodada analisada foram registrados:

```text
4 casos de teste executados
        ↓
3 defeitos identificados
        ↓
1 ponto dependente de esclarecimento do negócio
        ↓
0 casos aprovados integralmente
```

A rodada foi considerada **inconclusiva para liberação definitiva**, pois:

- Foram identificadas falhas de segurança.
- Foram identificadas falhas de validação.
- Foram encontrados problemas de usabilidade.
- Uma regra de transferência permaneceu sem definição suficiente.
- Fluxos importantes de movimentação financeira não possuíam evidências de execução.

## Escopo efetivamente avaliado

Os casos de teste com evidência registrada foram:

| Caso | Funcionalidade | Classificação | Resultado |
|---|---|---|---|
| CT-003 | Acesso sem login | Crítica, Segurança | Reprovado, necessita confirmação |
| CT-005 | Transferência para outra conta | Crítica, Regra de negócio | Necessita esclarecimento |
| CT-008 | Cadastro com números nos campos | Alta, Funcional negativo | Reprovado |
| CT-012 | Links da página inicial | Média, Usabilidade e Exploratório | Reprovado |

# 1. CT-003, Acesso sem login

## Objetivo

Verificar se uma área que deveria exigir autenticação pode ser acessada sem
que o usuário realize login previamente.

## Classificação

```text
Prioridade: Crítica
Área: Segurança
Vínculo: HU-01 / CA-03
```

## Comportamento observado

Durante a execução foi possível acessar uma conta sem realizar login.

Também foram exibidos dados que não haviam sido inseridos pelo usuário
durante aquela interação.

## Resultado esperado

O sistema deveria:

```text
Usuário não autenticado
        ↓
Tenta acessar área protegida
        ↓
Acesso bloqueado
        ↓
Redirecionamento para login
```

## Resultado obtido

```text
Usuário sem login
        ↓
Acesso à área da conta
        ↓
Dados apresentados
```

## Status

**Reprovado, necessita confirmação.**

## Evidência

```text
Print da conta
```

## Observação importante

O resultado precisa ser reproduzido em uma nova execução para descartar a
possibilidade de resíduos de sessão anteriores no navegador.

Dessa forma, o comportamento observado representa um risco crítico, mas sua
causa deve ser confirmada antes de uma conclusão definitiva sobre a origem
da falha.

# 2. CT-005, Transferência para outra conta

## Objetivo

Verificar o comportamento da funcionalidade de transferência bancária ao
tentar movimentar valores para outra conta.

## Classificação

```text
Prioridade: Crítica
Área: Regra de negócio
Vínculo: HU-02 / CA-05 / CA-06
```

## Comportamento observado

Foi observado que a funcionalidade de transferência aparenta permitir
movimentações apenas entre contas pertencentes ao próprio usuário logado.

## Problema identificado

Não havia informação suficiente para determinar se esse comportamento era:

```text
Regra correta do sistema

ou

Limitação incorreta da funcionalidade
```

## Status

**Necessita esclarecimento.**

## Evidência

```text
Print da tela de transferência
```

## Pergunta para o Product Owner ou área de negócio

> A aplicação deve permitir transferências exclusivamente entre contas do
> próprio usuário ou deve ser possível transferir valores para contas de
> outros usuários?

## Aprendizado de QA

O cenário demonstra que um comportamento inesperado não deve ser
automaticamente classificado como defeito quando não existe uma regra de
negócio suficientemente clara.

```text
Comportamento observado
        ↓
Existe requisito claro?
       / \
     Sim  Não
     ↓     ↓
Comparar  Solicitar
resultado esclarecimento
```

# 3. CT-008, Cadastro com números nos campos

## Objetivo

Verificar como o sistema trata dados incompatíveis inseridos nos campos do
cadastro.

## Classificação

```text
Prioridade: Alta
Tipo: Teste funcional negativo
Vínculo: HU-03 / CA-08
```

## Cenário

Foram utilizados caracteres numéricos em campos que deveriam representar
informações textuais, como:

- Nome.
- Endereço.
- E-mail.

## Resultado esperado

O sistema deveria validar os tipos de dados e rejeitar entradas incompatíveis.

Exemplo:

```text
Campo Nome
    ↓
123456
    ↓
Validação
    ↓
Entrada rejeitada
```

## Resultado obtido

O sistema aceitou os números nos campos e permitiu o envio do cadastro.

## Status

**Reprovado.**

## Evidência

```text
Print do cadastro
```

## Impacto

O comportamento pode permitir o armazenamento de dados inválidos no banco de
dados.

# 4. CT-012, Exploração dos links da página inicial

## Objetivo

Avaliar o comportamento dos links apresentados na página inicial do sistema.

## Classificação

```text
Prioridade: Média
Tipo: Usabilidade e teste exploratório
Vínculo: HU-04 / CA-12
```

## Links avaliados

Entre os links investigados estavam:

```text
ATM Services

Online Services

Last News
```

## Resultado esperado

Os links deveriam direcionar o usuário para páginas compreensíveis e
adequadas ao contexto da aplicação.

## Resultado obtido

Os links direcionaram diretamente para conteúdos em formato XML.

## Status

**Reprovado.**

## Evidência

```text
Print do link e do destino
```

## Impacto

O comportamento compromete a usabilidade, pois usuários finais podem ser
direcionados para informações técnicas que não foram estruturadas para leitura
normal.

```text
Link da interface
      ↓
Usuário clica
      ↓
Conteúdo XML
      ↓
Dificuldade de compreensão
      ↓
Experiência prejudicada
```

# Matriz de rastreabilidade

A atividade utilizou rastreabilidade entre histórias de usuário, critérios de
aceite e casos de teste.

| História / Critério | Caso de Teste | Resultado |
|---|---|---|
| HU-01, Autenticação / CA-03, impedir acesso sem login | CT-003 | Reprovado, acesso indevido observado |
| HU-02, Transferência / CA-05 e CA-06 | CT-005 | Pendente de regra de negócio |
| HU-03, Cadastro / CA-08, validação de dados incompatíveis | CT-008 | Reprovado, falta de validação |
| HU-04, Navegação / CA-12, clareza dos destinos | CT-012 | Reprovado, redirecionamento para XML |

A relação utilizada pode ser representada por:

```text
História de Usuário
        ↓
Critério de Aceite
        ↓
Caso de Teste
        ↓
Resultado
        ↓
Evidência
        ↓
Defeito ou esclarecimento
```

# Defeitos registrados

## BUG-001, Campos do cadastro aceitam números

### Funcionalidade

Cadastro.

### Severidade

**Média.**

### Prioridade

**Alta.**

### Passos

1. Acessar a tela de cadastro.
2. Preencher campos como nome, endereço e e-mail com valores numéricos.
3. Enviar o formulário.

### Resultado esperado

O sistema deveria validar os tipos de dados e rejeitar informações
incompatíveis.

### Resultado obtido

O cadastro aceitou os números e permitiu o envio.

### Impacto

Possibilidade de armazenamento de dados inválidos.

```text
Dados incompatíveis
       ↓
Sem validação
       ↓
Cadastro aceito
       ↓
Dados inválidos armazenados
```

---

## BUG-002, Links direcionam para conteúdo XML

### Funcionalidade

Navegação e usabilidade.

### Severidade

**Média.**

### Prioridade

**Média.**

### Passos

1. Acessar a página inicial.
2. Clicar em links como ATM Services, Online Services ou Last News.
3. Observar o conteúdo apresentado.

### Resultado esperado

O usuário deveria ser direcionado para páginas explicativas e legíveis.

### Resultado obtido

O sistema apresenta diretamente arquivos ou protocolos em formato XML.

### Impacto

- Prejudica a compreensão.
- Reduz a qualidade da experiência.
- Expõe conteúdo excessivamente técnico ao usuário final.

---

## BUG-003, Acesso à conta sem realização de login

### Funcionalidade

Autenticação e segurança.

### Severidade

**Crítica.**

### Prioridade

**Alta.**

### Passos

1. Não realizar autenticação.
2. Tentar acessar diretamente uma área associada à conta.
3. Observar o comportamento.

### Resultado esperado

```text
Sem autenticação
      ↓
Área protegida
      ↓
Acesso negado
      ↓
Login
```

### Resultado obtido

Foi possível acessar uma conta e visualizar dados previamente cadastrados.

### Impacto

Existe risco potencial de exposição indevida de dados bancários de terceiros.

### Observação

A ocorrência precisa ser reproduzida novamente para eliminar a hipótese de
uma sessão anterior ainda estar válida no navegador.

Por isso, apesar da severidade potencial ser crítica, a investigação deve
continuar antes de atribuir definitivamente a causa ao controle de
autenticação.

# Ponto pendente com o negócio

## Transferência bancária

A funcionalidade analisada aparentou permitir movimentações somente entre
contas do próprio usuário.

A equipe de QA não possuía requisito suficiente para determinar se o
comportamento era correto.

A questão registrada para esclarecimento foi:

> A aplicação deve permitir transferências exclusivamente entre contas do
> próprio usuário ou deve ser possível transferir valores para contas de
> outros usuários?

## Importância do esclarecimento

Sem essa definição, não é possível construir de maneira confiável:

- Caso positivo de transferência externa.
- Caso negativo.
- Critério de aceite.
- Resultado esperado.
- Classificação definitiva do comportamento observado.

# Análise de risco

Os resultados indicaram riscos em três dimensões principais.

## Segurança

O possível acesso à área da conta sem autenticação representa o risco mais
grave da rodada.

```text
Controle de autenticação
        ↓
Possível falha
        ↓
Acesso não autorizado
        ↓
Exposição de dados
```

## Qualidade dos dados

A falta de validação do cadastro permite a entrada de informações
incompatíveis.

```text
Entrada inválida
      ↓
Ausência de validação
      ↓
Banco recebe dado inadequado
      ↓
Problemas posteriores de integridade
```

## Usabilidade

O redirecionamento para XML demonstra uma quebra de expectativa na navegação.

```text
Usuário
   ↓
Interface web
   ↓
Link
   ↓
Conteúdo técnico XML
   ↓
Confusão
```

# Cobertura da rodada

Um ponto importante da avaliação foi reconhecer que a cobertura disponível
era insuficiente para aprovar definitivamente a release.

Não foram produzidas evidências de execução para alguns fluxos importantes,
incluindo:

```text
Login regular

Efetivação de transferências

Consulta de histórico e outros fluxos financeiros
```

Isso significa que a ausência de defeitos nesses fluxos não poderia ser
assumida.

```text
Não testado
    ≠
Aprovado
```

# Parecer da rodada

A situação foi classificada como:

## INCONCLUSIVA PARA LIBERAÇÃO DEFINITIVA

A amostragem executada apresentou:

```text
4 testes
  ↓
3 reprovações
  +
1 regra não esclarecida
  +
fluxos financeiros sem evidência
```

Com base nas evidências existentes, a release não apresentava condições de
seguir para homologação definitiva ou produção.

# Justificativa da decisão

A decisão foi baseada principalmente nos seguintes fatores:

1. Possível falha crítica de autenticação.
2. Ausência de validação adequada em campos de cadastro.
3. Problemas de usabilidade na navegação.
4. Regra de transferência não suficientemente definida.
5. Ausência de evidência para fluxos financeiros importantes.
6. Nenhum dos quatro testes executados foi integralmente aprovado.

# Próximas ações recomendadas

Antes de uma nova avaliação, seria necessário:

## 1. Reexecutar o teste de autenticação

O CT-003 deve ser executado novamente utilizando uma sessão limpa.

Exemplos:

```text
Novo navegador

Modo privado

Cookies removidos

Sessão encerrada
```

O objetivo é eliminar a possibilidade de que o acesso observado tenha sido
causado por sessão residual.

## 2. Corrigir as validações do cadastro

Campos devem possuir validações compatíveis com o tipo de informação
esperada.

## 3. Revisar os links da página inicial

Os destinos devem apresentar conteúdo compreensível para usuários finais.

## 4. Formalizar a regra de transferência

O Product Owner deve esclarecer se transferências para contas de outros
usuários fazem parte da regra de negócio.

## 5. Executar os fluxos financeiros ainda não cobertos

Principalmente:

- Transferência efetiva.
- Histórico de transações.
- Outros fluxos críticos de movimentação financeira.

## 6. Executar regressão após as correções

```text
Correção
   ↓
Reteste
   ↓
Regressão
   ↓
Novas evidências
   ↓
Nova avaliação da release
```

# Principais aprendizados

A atividade demonstrou que uma decisão de qualidade precisa considerar não
apenas os defeitos encontrados, mas também a **cobertura efetivamente
executada**.

```text
Defeitos encontrados
        +
Testes não executados
        +
Requisitos indefinidos
        +
Riscos residuais
        ↓
Decisão de QA
```

Outro aprendizado importante foi distinguir três situações:

```text
Defeito confirmado

Risco que precisa de nova investigação

Regra de negócio que precisa de esclarecimento
```

No caso do acesso sem login, existe uma evidência preocupante, mas ainda é
necessário descartar resíduos de sessão.

No caso da transferência, não existe base suficiente para chamar o
comportamento de defeito sem antes obter uma definição do negócio.

# Competências desenvolvidas

A atividade contribuiu para desenvolver competências relacionadas a:

- Testes baseados em risco.
- Testes funcionais negativos.
- Testes de segurança.
- Testes exploratórios.
- Avaliação de usabilidade.
- Rastreabilidade.
- Registro de defeitos.
- Análise de severidade.
- Priorização.
- Investigação de ocorrências.
- Análise de requisitos.
- Gestão de riscos residuais.
- Comunicação com Product Owner.
- Tomada de decisão sobre release.

# Relação com o Projeto Integrador

Os conceitos utilizados nesta atividade também podem ser aplicados ao
**ConectaStart**.

Um cenário semelhante seria avaliar se determinadas áreas da plataforma podem
ser acessadas sem autenticação.

```text
ConectaStart
     ↓
Perfil da startup
     ↓
Área protegida
     ↓
Autenticação
     ↓
Autorização
```

Também podem ser aplicados testes negativos nos formulários.

Exemplo:

```text
Cadastro da startup
       ↓
Dados incompatíveis
       ↓
Validação
       ↓
Aceitar ou rejeitar
```

Outro ponto diretamente relacionado ao ConectaStart é a necessidade de
formalizar regras de negócio antes dos testes.

Por exemplo:

```text
Matchmaking
     ↓
Quais usuários podem conectar?
     ↓
Quais critérios são obrigatórios?
     ↓
Existe requisito claro?
     ↓
Criar testes
```

Assim como ocorreu no ParaBank com a regra de transferência, uma regra de
matchmaking mal definida dificultaria a determinação do resultado esperado.

[Acessar Projeto Integrador](../../../projeto-integrador/)

# Organização dos arquivos

A atividade pode ser organizada da seguinte forma:

```text
parabank/
│
├── README.md
│
├── Dossie - ParaBank.odt
│
└── evidencias/
    ├── acesso-sem-login/
    ├── transferencia/
    ├── cadastro/
    └── navegacao/
```

Caso as evidências estejam incorporadas apenas ao documento original, a pasta
`evidencias` pode ser criada posteriormente quando os arquivos individuais
forem adicionados ao repositório.

# Documento original

O documento utilizado como base para esta atividade é:

```text
Dossie - ParaBank.odt
```

# Navegação

[Voltar para Validação e Qualidade de Software](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)
