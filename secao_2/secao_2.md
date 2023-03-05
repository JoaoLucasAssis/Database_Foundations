# Seção 2

## 2.1 - Bancos de Dados Relacionais

Apresenta informações em tabelas com linhas e colunas

Cada coluna representa um tipo específico de informação e cada linha lista um registro

Tabelas são relacionadas umas com às outras por meio de um campo em comum

Um campo exclusivo chamado chave é usado para identificar cada registro em um banco de dados relacional

|studentID|name |tutorID|
|:-------:|:---:|:-----:|
|1        |joao |5      |
|2        |lucas|4      |

|tutorID|name |
|:-----:|:---:|
|1      |pedro|
|2      |paulo|

A cada tabela é atribuída uma chave primária que identifica cada linhas da tabela

A chave primária de uma tabela é designada como chave estrangeira em uma outra tabela

O relacionamento entre as tabelas `student` e `tutor` permite armazenar os dados e consultá-los

* Vantagens:

    * Menos redundância

    * Evitar inconsistência

    * Integridade dos dados

    * Confidencialidade

* Regras:

    * Cada tabela tem um nome exclusivo

    * Cada coluna de uma tabela tem um nome exclusivo

    * Campos aceitam apenas valores únicos

    * Os valores dos campos em colunas são do mesmo tipo

    * Cada tabela tem uma coluna para

## 2.2 - Modelos Físicos e Conceituais

### Modelo Conceitual

Captura as necessidades e informações de uma empresa

Identifica entidades - objetos que se tornam tabelas - e relacionamentos entre entidades

Não especifica atributos - objetos que se tornam colunas - e identificadores exclusivos(chaves primárias)

### Modelo Lógico

Inclui todas as entidades e os relacionamentos entre elas

Especifica todos os atributos em indentificadores de cada entidade

Determina se o atributo aceita valores nulos

Determina a cardinalidade dos relacionamentos

É denominado modelo entidade-relacionamento

É ilustrado em um diagrama de entidade-relacionamento

### Modelo Físico

Descreve como os objetos devem ser implementados em um banco de dados específico - entidades viram tabelas, atributos viram colunas e relacionamentos viram chaves estrangeiras

Mostra todas as estruturas da tabela, incluindo colunas e chaves