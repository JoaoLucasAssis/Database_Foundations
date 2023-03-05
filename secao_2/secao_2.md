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