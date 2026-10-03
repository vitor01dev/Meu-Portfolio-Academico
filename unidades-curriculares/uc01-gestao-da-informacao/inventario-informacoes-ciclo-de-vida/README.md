```markdown
# Inventário de Informações e Ciclo de Vida Informacional

[Voltar para Gestão da Informação](../README.md)

## Metadados

| Campo | Informação |
|---|---|
| Unidade Curricular | Gestão da Informação |
| Professor | André Silva |
| Curso | Análise e Desenvolvimento de Sistemas |
| Instituição | Faculdade Senac Pernambuco |
| Período | 5º período |
| Semestre | 2026.2 |
| Tipo | Atividade prática |
| Tema | Inventário e ciclo de vida da informação |
| Projeto relacionado | ConectaStart |
| Status | Concluído |

## Integrantes

| Integrante |
|---|
| Alisson Gustavo |
| Allyson George |
| Hericc Rocha |
| Vítor Vieira |
| Willami Durand |

## Objetivo da atividade

Esta atividade aplica conceitos de Gestão da Informação ao projeto
**ConectaStart**, identificando as informações consideradas críticas
para o funcionamento da plataforma e analisando o ciclo de vida de
informações diretamente relacionadas à proposta de valor do projeto.

O ConectaStart é uma plataforma digital que busca conectar startups
a oportunidades de acordo com seu estágio de desenvolvimento.

A análise considera principalmente a relação entre:

```text
Startup
   +
Estágio
   +
Oportunidade
   ↓
Correspondência adequada
   ↓
Geração de valor
```

## 1. Inventário das informações críticas

Foram identificadas dez informações relevantes para o funcionamento
e para a validação do projeto.

| Nº | Informação | Fonte | Tipo | Produzida por | Utilizada por | Armazenamento | Atualização | Criticidade |
|---:|---|---|---|---|---|---|---|---|
| 1 | Cadastro da startup | Interna, primária | Estruturada | Empreendedor | Sistema, Administração e Organizações | PostgreSQL, Azure | Edição do perfil e revisão semestral | Alta |
| 2 | Estágio da startup | Interna, primária e autodeclarada | Estruturada | Empreendedor | Sistema e Administração | PostgreSQL, Azure | Mudança de estágio e lembrete trimestral | Alta |
| 3 | Credenciais e papéis de acesso | Interna | Estruturada | Usuário e Sistema | Módulo de autenticação | PostgreSQL, senha com hash | Cadastro e troca de senha | Alta |
| 4 | Oportunidade | Externa, organização parceira | Semiestruturada | Organização | Startups e Administração | PostgreSQL, Azure | Até a validade da oportunidade | Alta |
| 5 | Categoria da oportunidade | Interna | Estruturada | Administração | Sistema, Organizações e Startups | PostgreSQL | Revisão das categorias | Alta |
| 6 | Status da oportunidade | Interna | Estruturada | Administração e Sistema | Sistema e Organizações | PostgreSQL | Moderação ou vencimento | Alta |
| 7 | Interações | Interna, gerada pelo uso | Estruturada | Sistema | Equipe do projeto | PostgreSQL e logs | Contínua | Alta |
| 8 | Métricas de utilização | Interna, secundária | Estruturada | Equipe do projeto | Equipe e Product Owner | Relatórios e dashboard | Semanal | Alta |
| 9 | Feedback e entrevistas | Externa, primária | Não estruturada | Startups e organizações | Equipe do projeto | Drive e relatórios | Cada ciclo de validação | Alta |
| 10 | Perfil da organização | Interna | Estruturada | Organização | Startups e Administração | PostgreSQL | Edição do perfil | Média |

## Critério de criticidade

Uma informação foi considerada de **alta criticidade** quando sua
ausência compromete o funcionamento do núcleo do MVP ou impede a
obtenção das evidências necessárias para validar a proposta.

Nesse grupo estão informações relacionadas a:

```text
Startup
Estágio
Oportunidade
Interações
Métricas
Feedback
```

Informações de criticidade média apoiam a operação, mas sua ausência
não impede diretamente o teste da hipótese principal.

## 2. Informações escolhidas para o ciclo de vida

Duas informações foram selecionadas para uma análise mais detalhada:

| Informação | Papel no ConectaStart |
|---|---|
| Cadastro e estágio da startup | Representam o lado da demanda |
| Oportunidade | Representa o lado da oferta |

Essas duas informações estão diretamente relacionadas à hipótese
central da plataforma.

```text
Cadastro + Estágio
       │
       │ demanda
       ▼
   ConectaStart
       ▲
       │ oferta
       │
 Oportunidades
```

Caso uma dessas informações esteja incorreta ou desatualizada, a
startup pode receber oportunidades incompatíveis com sua realidade.

---

# 3. Ciclo de vida do cadastro e estágio da startup

O ciclo de vida identificado foi:

```text
Coleta
  ↓
Registro
  ↓
Armazenamento
  ↓
Organização
  ↓
Uso
  ↓
Compartilhamento
  ↓
Atualização
  ↓
Arquivamento ou descarte
```

## Coleta

| Campo | Informação |
|---|---|
| Responsável | Empreendedor |
| Ferramenta | Formulário de cadastro |
| Risco | Dados incompletos ou estágio escolhido sem critério claro |
| Melhoria | Campos obrigatórios e descrição dos estágios |

A primeira etapa ocorre quando o empreendedor fornece seus dados e
informa o estágio atual da startup.

Um dos principais riscos é que o estágio seja selecionado sem que o
empreendedor compreenda claramente os critérios utilizados.

## Registro

| Campo | Informação |
|---|---|
| Responsável | Sistema |
| Ferramenta | API REST |
| Risco | Startup cadastrada em duplicidade |
| Melhoria | Validação de identificador único |

A utilização de identificadores únicos, como e-mail ou outro dado
adequado ao contexto do sistema, pode ajudar a evitar registros
duplicados.

## Armazenamento

| Campo | Informação |
|---|---|
| Responsável | Equipe técnica |
| Ferramenta | PostgreSQL no Azure |
| Risco | Perda ou inconsistência dos dados |
| Melhoria | Backup automático e restrições de integridade |

As informações precisam ser armazenadas de maneira consistente e
protegidas contra perda ou alterações incompatíveis com as regras
do sistema.

## Organização

| Campo | Informação |
|---|---|
| Responsável | Sistema |
| Ferramenta | Banco de dados |
| Risco | Estágio fora dos valores previstos |
| Melhoria | Utilização de valores controlados |

Os estágios previstos no documento são:

```text
IDEALIZACAO
VALIDACAO
TRACAO
ESCALAR
```

A utilização de valores controlados reduz inconsistências de
classificação.

## Uso

| Campo | Informação |
|---|---|
| Responsável | Sistema e startup |
| Ferramenta | Central de oportunidades |
| Risco | Estágio incorreto gerar oportunidades inadequadas |
| Melhoria | Perguntas-guia para auxiliar a autoavaliação |

O estágio da startup é utilizado como um dos elementos para
selecionar e apresentar oportunidades.

Por isso, uma classificação incorreta afeta diretamente a qualidade
das recomendações.

## Compartilhamento

| Campo | Informação |
|---|---|
| Responsável | Sistema |
| Ferramenta | Perfil público e API |
| Risco | Exposição desnecessária de dados pessoais |
| Melhoria | Controle de acesso e separação entre dados públicos e privados |

O compartilhamento das informações deve considerar quais dados
realmente precisam ser disponibilizados a cada tipo de usuário.

## Atualização

| Campo | Informação |
|---|---|
| Responsável | Empreendedor |
| Ferramenta | Edição do perfil |
| Risco | Evolução da startup sem atualização do estágio |
| Melhoria | Lembretes periódicos para confirmação |

Uma startup pode evoluir durante sua jornada.

Caso seu estágio permaneça desatualizado, a plataforma pode continuar
apresentando informações e oportunidades referentes a uma fase
anterior.

## Arquivamento e descarte

| Campo | Informação |
|---|---|
| Responsável | Administração |
| Ferramenta | Banco de dados |
| Risco | Contas inativas mantidas indefinidamente |
| Melhoria | Política de retenção, anonimização e exclusão |

O ciclo de vida também precisa estabelecer regras para dados que
deixaram de ser necessários para a finalidade original.

---

# 4. Ciclo de vida das oportunidades

Para as oportunidades, foi identificado o seguinte fluxo:

```text
Criação
  ↓
Registro
  ↓
Armazenamento
  ↓
Organização
  ↓
Moderação e publicação
  ↓
Uso
  ↓
Atualização
  ↓
Arquivamento ou descarte
```

## Criação

| Campo | Informação |
|---|---|
| Responsável | Organização |
| Ferramenta | Formulário de oportunidade |
| Risco | Descrição vaga, ausência de prazo ou link |
| Melhoria | Campos obrigatórios |

Os principais campos previstos são:

```text
Título
Categoria
Prazo
Link
Estágios-alvo
```

## Registro

| Campo | Informação |
|---|---|
| Responsável | Sistema |
| Ferramenta | API REST |
| Risco | Oportunidade cadastrada mais de uma vez |
| Melhoria | Verificação de duplicidade |

O documento propõe considerar informações como título, organização
e data para identificar possíveis duplicidades.

## Armazenamento

| Campo | Informação |
|---|---|
| Responsável | Equipe técnica |
| Ferramenta | PostgreSQL no Azure |
| Risco | Inconsistência entre oportunidade e categoria |
| Melhoria | Regras de integridade e relacionamentos no banco |

## Organização

| Campo | Informação |
|---|---|
| Responsável | Organização e Administração |
| Ferramenta | Categorias e estágios |
| Risco | Oportunidade sem estágio-alvo |
| Melhoria | Seleção obrigatória de um ou mais estágios |

A classificação correta da oportunidade é fundamental para que ela
possa ser localizada pelas startups adequadas.

## Moderação e publicação

| Campo | Informação |
|---|---|
| Responsável | Administração |
| Ferramenta | Painel de moderação |
| Risco | Publicação inadequada ou demora excessiva na aprovação |
| Melhoria | Checklist e prazo para análise |

O documento utiliza como exemplo a transição:

```text
PENDENTE
    ↓
PUBLICADA
```

## Uso

| Campo | Informação |
|---|---|
| Responsável | Startup |
| Ferramenta | Central de oportunidades |
| Risco | Excesso de oportunidades irrelevantes |
| Melhoria | Filtro por estágio e categoria |

A informação sobre o estágio da startup pode ser utilizada para
reduzir a quantidade de oportunidades irrelevantes apresentadas.

## Atualização

| Campo | Informação |
|---|---|
| Responsável | Organização |
| Ferramenta | Edição da oportunidade |
| Risco | Oportunidade vencida continuar visível |
| Melhoria | Data de validade obrigatória e expiração automática |

Exemplo de mudança de status:

```text
PUBLICADA
    ↓
EXPIRADA
```

## Arquivamento e descarte

| Campo | Informação |
|---|---|
| Responsável | Sistema e Administração |
| Ferramenta | Banco de dados |
| Risco | Acúmulo de oportunidades antigas na busca |
| Melhoria | Remover expiradas da busca e preservar histórico |

O arquivamento permite retirar oportunidades antigas da experiência
principal do usuário sem necessariamente eliminar os dados utilizados
em métricas e análises históricas.

---

# 5. Principais riscos informacionais

A análise identificou a **desatualização da informação** como um dos
principais riscos para o ConectaStart.

Esse problema pode ocorrer tanto no estágio registrado pelas startups
quanto nas oportunidades publicadas pelas organizações.

```text
Estágio desatualizado
        ↓
Classificação inadequada
        ↓
Oportunidades inadequadas
        ↓
Experiência de baixo valor
```

Também pode ocorrer:

```text
Oportunidade vencida
        ↓
Permanece publicada
        ↓
Startup acessa oportunidade inválida
        ↓
Perda de confiança na plataforma
```

## 6. Melhorias prioritárias

A partir da análise realizada, três medidas foram consideradas
prioritárias:

1. Lembretes periódicos para confirmação do estágio da startup.
2. Data de validade obrigatória com expiração automática das oportunidades.
3. Moderação das oportunidades antes da publicação.

Essas medidas contribuem diretamente para aumentar a atualidade,
consistência e confiabilidade das informações utilizadas pela plataforma.

## 7. Relação com a Gestão da Informação

A atividade demonstra que a informação possui um ciclo de vida.

```text
Criação
  ↓
Registro
  ↓
Armazenamento
  ↓
Organização
  ↓
Uso
  ↓
Compartilhamento
  ↓
Atualização
  ↓
Arquivamento
```

Cada etapa apresenta responsáveis, ferramentas, riscos e necessidades
de controle.

No ConectaStart, uma informação incorreta pode produzir consequências
em etapas posteriores.

Por exemplo:

```text
Estágio incorreto
      ↓
Informação armazenada incorretamente
      ↓
Filtro utiliza dado incorreto
      ↓
Oportunidade inadequada
      ↓
Match de baixa qualidade
```

Isso demonstra que a Gestão da Informação precisa ocorrer durante
todo o ciclo e não apenas no momento em que os dados são coletados.

## 8. Relação com o Projeto Integrador

Esta atividade contribui diretamente para decisões do ConectaStart
relacionadas a:

| Área do projeto | Contribuição |
|---|---|
| Modelagem de dados | Identificação das informações essenciais |
| Arquitetura | Definição de armazenamento e fluxo das informações |
| Backend | Regras de validação, integridade e atualização |
| Experiência do usuário | Redução de informações irrelevantes |
| Segurança | Separação entre informações públicas e privadas |
| Qualidade | Identificação de riscos informacionais |
| Produto | Priorização das informações necessárias para o MVP |
| Métricas | Registro de interações, feedbacks e indicadores |

[Acessar Projeto Integrador](../../../projeto-integrador/)

## 9. Aprendizados

A atividade permitiu compreender que uma informação não deve ser
analisada apenas pelo seu conteúdo.

Também é necessário identificar:

```text
De onde vem?
      ↓
Quem produz?
      ↓
Onde é armazenada?
      ↓
Quem utiliza?
      ↓
Quando precisa ser atualizada?
      ↓
Quando deixa de ser necessária?
```

No ConectaStart, a análise mostrou que a qualidade do relacionamento
entre startups e oportunidades depende diretamente da qualidade dos
dados utilizados para estabelecer essa relação.

Informações desatualizadas podem comprometer a própria validação da
proposta de valor da plataforma.

## Documento da atividade

Caso o arquivo PDF seja armazenado nesta pasta com o nome
`conectastart-gestao-da-informacao.pdf`, ele poderá ser acessado pelo
link abaixo:

[Consultar documento completo](./conectastart-gestao-da-informacao.pdf)

## Navegação

[Voltar para Gestão da Informação](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)
```
