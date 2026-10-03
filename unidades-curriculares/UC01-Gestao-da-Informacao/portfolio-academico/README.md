# Meu Repositório Acadêmico no GitHub

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
| Tema | Arquitetura da Informação |
| Plataforma | GitHub |
| Responsável | Vitor Vieira |
| Repositório | Portfólio Acadêmico |
| Status | Em desenvolvimento |

## Objetivo da atividade

A atividade consiste na criação de um repositório organizado no **GitHub** que funcione simultaneamente como:

- Portfólio acadêmico.
- Repositório das atividades desenvolvidas nas Unidades Curriculares.
- Espaço de documentação do Projeto Integrador.
- Registro das competências desenvolvidas durante o curso.
- Ambiente para organização e recuperação de documentos acadêmicos.

A estrutura do repositório deve aplicar conceitos estudados em **Arquitetura da Informação**, principalmente:

- Classificação.
- Taxonomia.
- Metadados.
- Navegação.
- Encontrabilidade.
- Relações entre conteúdos.

## Contexto

Durante o curso de **Análise e Desenvolvimento de Sistemas**, diferentes atividades são produzidas em formatos variados, como:

- Documentos.
- Relatórios.
- Apresentações.
- Pesquisas.
- Códigos.
- Evidências de testes.
- Diagramas.
- Projetos.

Quando esses arquivos são armazenados sem um padrão de organização, torna-se mais difícil identificar sua origem, finalidade e relação com outros conteúdos.

O portfólio acadêmico foi criado para resolver esse problema por meio de uma estrutura padronizada e navegável.

## Problema informacional

O principal problema identificado é a dispersão das atividades acadêmicas em diferentes arquivos, pastas e formatos sem uma estrutura única de organização.

Essa situação pode causar:

- Dificuldade para localizar atividades antigas.
- Duplicação de arquivos.
- Falta de contexto sobre cada documento.
- Dificuldade para relacionar uma atividade à sua Unidade Curricular.
- Perda do histórico acadêmico.
- Dificuldade para apresentar projetos e competências desenvolvidas.
- Baixa encontrabilidade das informações.

## Solução proposta

A solução consiste na criação de um repositório estruturado no GitHub utilizando uma arquitetura hierárquica de informações.

O repositório organiza os conteúdos por:

```text
Portfólio Acadêmico
        │
        ├── Unidades Curriculares
        │
        ├── Projeto Integrador
        │
        ├── Documentação
        │
        └── Recursos
```

Cada Unidade Curricular possui seu próprio espaço e suas atividades são organizadas dentro dela.

## Estrutura geral do repositório

```text
portfolio-academico-vitor-vieira/
│
├── README.md
├── INDEX.md
│
├── docs/
│   ├── arquitetura-da-informacao.md
│   ├── mapa-de-conteudos.md
│   └── glossario.md
│
├── unidades-curriculares/
│   │
│   ├── uc01-gestao-da-informacao/
│   │
│   ├── uc02-validacao-e-qualidade-de-software/
│   │
│   ├── uc03-empreendedorismo-e-planos-de-negocios/
│   │
│   ├── uc04-high-tech/
│   │
│   ├── uc05-inteligencia-artificial/
│   │
│   └── uc06-governanca-em-tecnologia-da-informacao/
│
├── projeto-integrador/
│   ├── 01-contextualizacao/
│   ├── 02-pesquisa/
│   ├── 03-requisitos/
│   ├── 04-arquitetura/
│   ├── 05-desenvolvimento/
│   ├── 06-testes/
│   ├── 07-documentacao/
│   └── 08-entrega-final/
│
└── assets/
    ├── imagens/
    ├── diagramas/
    └── documentos/
```

# Aplicação dos conceitos de Arquitetura da Informação

## 1. Classificação

A classificação é utilizada para separar os conteúdos de acordo com sua natureza e finalidade.

Foram definidas quatro categorias principais:

| Categoria | Finalidade |
|---|---|
| Unidades Curriculares | Armazenar atividades e trabalhos acadêmicos |
| Projeto Integrador | Centralizar os documentos do ConectaStart |
| Documentação | Explicar a organização e arquitetura do portfólio |
| Recursos | Armazenar imagens, diagramas e documentos compartilhados |

A classificação permite que cada informação seja armazenada em um local coerente com sua função.

### Exemplo

```text
unidades-curriculares/
        │
        ├── Gestão da Informação
        ├── Validação e Qualidade de Software
        ├── Empreendedorismo
        ├── High Tech
        ├── Inteligência Artificial
        └── Governança de TI
```

## 2. Taxonomia

A taxonomia define a estrutura hierárquica e a padronização utilizada para nomear e organizar os conteúdos.

A estrutura principal segue os níveis:

```text
Nível 1
Portfólio

        ↓

Nível 2
Categoria

        ↓

Nível 3
Unidade Curricular

        ↓

Nível 4
Atividade

        ↓

Nível 5
Artefato
```

Exemplo:

```text
Portfólio
   │
   └── Unidades Curriculares
           │
           └── Gestão da Informação
                   │
                   └── Qualidade Informacional
                           │
                           └── README.md
```

Também foi adotado um padrão para nomes de diretórios.

```text
uc01-gestao-da-informacao

uc02-validacao-e-qualidade-de-software

uc03-empreendedorismo-e-planos-de-negocios

uc04-high-tech

uc05-inteligencia-artificial

uc06-governanca-em-tecnologia-da-informacao
```

O uso de letras minúsculas e hífens facilita a leitura e mantém consistência entre os caminhos.

## 3. Metadados

Os metadados fornecem contexto adicional sobre os conteúdos armazenados.

Cada atividade pode conter informações como:

| Metadado | Exemplo |
|---|---|
| Unidade Curricular | Gestão da Informação |
| Professor | André Silva |
| Semestre | 2026.2 |
| Tipo | Atividade prática |
| Tema | Qualidade da Informação |
| Projeto relacionado | ConectaStart |
| Status | Concluído |
| Tecnologias | Git e GitHub |

Exemplo de metadados utilizados em um arquivo:

```text
Unidade Curricular: Gestão da Informação
Professor: André Silva
Semestre: 2026.2
Atividade: Qualidade Informacional
Projeto relacionado: ConectaStart
Status: Concluído
```

Os metadados ajudam o usuário a compreender rapidamente:

```text
O que é?
Quem produziu?
Em qual disciplina?
Quando?
Sobre qual assunto?
Qual projeto está relacionado?
```

## 4. Navegação

A navegação do repositório é realizada principalmente por meio de arquivos `README.md` e links relativos.

O fluxo principal pode ser representado por:

```text
README principal
      ↓
Unidade Curricular
      ↓
Atividade
      ↓
Documento ou evidência
```

Também são disponibilizados caminhos de retorno.

```text
Atividade
   ↑
Unidade Curricular
   ↑
Portfólio
```

Exemplos:

```markdown
[Voltar para Gestão da Informação](../README.md)

[Voltar ao Portfólio](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)
```

Esse modelo reduz a necessidade de utilizar apenas a árvore de diretórios do GitHub para localizar conteúdos.

## 5. Encontrabilidade

A encontrabilidade representa a facilidade com que uma informação pode ser localizada.

No portfólio, ela é favorecida por diferentes mecanismos.

### Padronização de nomes

Exemplo:

```text
qualidade-informacional/

radar-problemas-informacionais/

inventario-informacoes-ciclo-de-vida/
```

Os nomes indicam diretamente o conteúdo armazenado.

### Índice geral

O arquivo:

```text
INDEX.md
```

funciona como catálogo dos conteúdos do portfólio.

Ele permite localizar atividades por:

- Unidade Curricular.
- Tema.
- Projeto.
- Tipo de documento.
- Área de conhecimento.

### README

Cada nível importante possui um `README.md`.

```text
README principal
      ↓
README da UC
      ↓
README da atividade
```

### Metadados

Os metadados permitem identificar rapidamente a natureza de cada conteúdo.

### Pesquisa do GitHub

A utilização de nomes descritivos também facilita a localização dos conteúdos utilizando a ferramenta de pesquisa do próprio GitHub.

## 6. Relações entre conteúdos

Uma atividade acadêmica pode estar relacionada a diferentes disciplinas, projetos e competências.

Por isso, o portfólio não organiza os conteúdos apenas de forma hierárquica.

Também são criadas relações entre eles.

Exemplo:

```text
Gestão da Informação
        │
        ├── Qualidade Informacional
        │
        ▼
   ConectaStart
        ▲
        │
        ├── Mapa de Empatia
        │
Empreendedorismo
```

Outro exemplo:

```text
Validação e Qualidade
        │
        ├── Testes
        ├── Evidências
        └── Critérios de Aceitação
                │
                ▼
          Projeto Integrador
```

Essas relações permitem compreender como conhecimentos desenvolvidos em diferentes Unidades Curriculares contribuem para projetos comuns.

# Unidades Curriculares

O portfólio do semestre 2026.2 reúne as seguintes Unidades Curriculares:

| Código | Unidade Curricular |
|---|---|
| UC01 | Gestão da Informação |
| UC02 | Validação e Qualidade de Software |
| UC03 | Empreendedorismo e Planos de Negócios |
| UC04 | High Tech |
| UC05 | Inteligência Artificial |
| UC06 | Governança em Tecnologia da Informação |

## UC01, Gestão da Informação

Entre as atividades registradas estão:

```text
Radar de Problemas Informacionais

Qualidade Informacional

Inventário de Informações e Ciclo de Vida Informacional

Meu Repositório Acadêmico no GitHub
```

## UC02, Validação e Qualidade de Software

Entre os conteúdos estão:

```text
PulseTickets

ParaBank

MedSupply

Casos de Teste

Critérios de Aceitação

Evidências de Testes
```

## UC03, Empreendedorismo e Planos de Negócios

Entre as atividades estão:

```text
Mapa de Empatia, ConectaStart

Apresentação LOGGI
```

## UC04, High Tech

Entre os conteúdos estão:

```text
ObraLoop

Plano de Marketing Digital

Bras Machines

Seminário de Inteligência Artificial
```

## UC05, Inteligência Artificial

Entre os conteúdos estudados estão:

```text
Engenharia de Prompt

Engenharia de Prompt Avançada

Retroalimentação de Dados

Pacotes de Contexto
```

## UC06, Governança em Tecnologia da Informação

Entre as atividades estão:

```text
Indicadores de TI utilizando BSC

Relatório de Governança de TI
```

# Projeto Integrador

## ConectaStart

O **ConectaStart** é o Projeto Integrador relacionado a diversas atividades presentes neste portfólio.

A proposta busca apoiar startups emergentes, principalmente durante sua jornada de desenvolvimento, organizando informações, orientações e conexões relevantes.

O projeto também funciona como elemento de ligação entre diferentes Unidades Curriculares.

```text
Gestão da Informação
        │
        │
        ▼
   ConectaStart
        ▲
        │
Empreendedorismo
        │
        │
Inteligência Artificial
        │
        │
Qualidade de Software
        │
        │
Governança de TI
```

[Acessar Projeto Integrador](../../../projeto-integrador/)

# Organização por diferentes perspectivas

Um dos objetivos da Arquitetura da Informação é permitir que o mesmo conteúdo possa ser encontrado por diferentes caminhos.

## Por Unidade Curricular

```text
Gestão da Informação
        ↓
Qualidade Informacional
```

## Por projeto

```text
ConectaStart
        ↓
Qualidade Informacional
```

## Por tema

```text
Qualidade da Informação
        ↓
Qualidade Informacional
```

Dessa forma, o conteúdo não depende de apenas um caminho de navegação.

# Exemplo de relação entre conteúdos

A atividade **Qualidade Informacional** pertence à Unidade Curricular de Gestão da Informação.

Ao mesmo tempo, ela utiliza o ConectaStart como contexto.

```text
Gestão da Informação
        │
        ▼
Qualidade Informacional
        │
        ▼
ConectaStart
```

A atividade **Mapa de Empatia** pertence à Unidade Curricular de Empreendedorismo.

```text
Empreendedorismo
        │
        ▼
Mapa de Empatia
        │
        ▼
ConectaStart
```

Assim, as duas atividades pertencem a disciplinas diferentes, mas estão relacionadas ao mesmo projeto.

# Arquitetura do portfólio

A arquitetura pode ser representada de maneira simplificada da seguinte forma:

```text
                    PORTFÓLIO
                        │
        ┌───────────────┼───────────────┐
        │               │               │
        ▼               ▼               ▼
       UCs              PI           Documentação
        │               │
        │               ▼
        │          ConectaStart
        │               ▲
        │               │
        ├───────────────┤
        │               │
        ▼               │
   Atividades           │
        │               │
        ▼               │
   Documentos ──────────┘
```

Essa estrutura combina hierarquia com relações entre conteúdos.

# Tecnologias utilizadas

A implementação do portfólio utiliza principalmente:

| Tecnologia | Aplicação |
|---|---|
| Git | Controle de versão |
| GitHub | Hospedagem e publicação do portfólio |
| Markdown | Documentação e navegação |
| GitHub Search | Pesquisa e recuperação dos conteúdos |
| GitHub Topics | Classificação complementar do repositório |

# Benefícios da estrutura

A organização proposta permite:

- Localizar atividades rapidamente.
- Manter um histórico acadêmico.
- Relacionar conteúdos de diferentes disciplinas.
- Registrar projetos e competências.
- Reduzir arquivos dispersos.
- Facilitar futuras atualizações.
- Apresentar trabalhos acadêmicos de forma organizada.
- Utilizar o repositório como portfólio profissional.
- Demonstrar conhecimento prático de Arquitetura da Informação.

# Resultado

O resultado da atividade é um repositório acadêmico que não funciona apenas como armazenamento de arquivos.

Ele foi estruturado como um sistema de informação no qual os conteúdos são:

```text
Classificados
      ↓
Organizados
      ↓
Descritos
      ↓
Relacionados
      ↓
Navegáveis
      ↓
Encontráveis
```

A aplicação dos conceitos de Arquitetura da Informação permite que o usuário compreenda a estrutura do portfólio e encontre os conteúdos sem precisar conhecer previamente a organização interna do repositório.

# Aprendizados

A atividade permitiu aplicar conceitos de Arquitetura da Informação em um ambiente real.

Durante a construção do portfólio foi possível compreender que organizar informações não significa apenas criar pastas.

Também é necessário definir:

```text
Como classificar?
       ↓
Como nomear?
       ↓
Como descrever?
       ↓
Como navegar?
       ↓
Como encontrar?
       ↓
Como relacionar?
```

A estruturação do repositório demonstrou que classificação, taxonomia, metadados, navegação e encontrabilidade precisam funcionar de maneira integrada.

O resultado é um portfólio mais compreensível, escalável e adequado tanto para organização acadêmica quanto para apresentação profissional.

# Repositório

**GitHub:**  
https://github.com/vitor01dev/

# Navegação

[Voltar para Gestão da Informação](../README.md)

[Voltar ao Portfólio Acadêmico](../../../README.md)

[Consultar Índice Geral](../../../INDEX.md)

[Acessar Projeto Integrador](../../../projeto-integrador/)

[Consultar documentação de Arquitetura da Informação](../../../docs/arquitetura-da-informacao.md)
