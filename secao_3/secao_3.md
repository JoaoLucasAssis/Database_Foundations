# Seção 3

## 3.1 - Mais com Relacionamentos

### Relacionamentos Associativos

Um relacionamento é considerado associativo quando relaciona entidades com entidades associativas

### Relacionamento n:n

Se os atributos descreverem um relacionamento, será necessário a criação de uma entidade de interseção

|pedido  |                            
|:------:|                
|# número|                  
|* data  |                              
|* total |   

|item      |
|:--------:|  
|# n_pedido|
|# id_prod |  
|quantidade|     

|produto|  
|:-----:|    
|# id   |         
|* nome |  
|* preço|

Os relacionamentos a partir da entidade associativa são obrigatórios

`Entidades de interseção` é identificada por seus dois relacionamentos de origem

### Relacionamentos Recursivos

Uma instância de uma entidade está relacionada a outra instância na mesma entidade



### Generalização e Especialização

Generalização é uma abornagem na qual duas ou mais entidades, que possuem atributos comuns, são combinadas para formar uma entidade de nível superior

Especialização é uma abordagem na qual uma entidade de nível superior é dividida em duas ou mais entidades

### Entidades de Supertipo e Subtipo

Um supertipo tem um relacionamento pai-filho com um ou mais subtipos

Um subtipo é um subagrupamento da entidade supertipo que contém atributos distintos contidos em outros subagrupamentos

Os atributos comuns aos subtipos  devem estar contidos apenas no supertipo, mas são herdados em todos os subtipos

Um subtipo pode conter seus próprios atributos

## 3.3 - Normalização e Regras de Negócio

### Normalização

Processo de organizar os atributos e as tabelas de um banco de dados relacional para minimizar a redundância

Aumenta a integridade dos dados

Elimina inconsistências e anormalidades

#### Primeira Forma Normal

Exige que não existam atributos com vários valores

Se houver, cria-se uma entidade que se relaciona com a original com cardinalidade 1:n

|pedido      |                            
|:----------:|                
|# num pedido|                  
|* `endereço`|

|`endereço` |
|:---------:|
|cidade     |
|bairro     |
|complemento|

#### Segunda Forma Normal

Requer que todos os atributos não identificadores sejam obtidos pelos atributos identificadores

|item        |
|:----------:|  
|# n_pedido  |
|# id_prod   |  
|* qtd       |
|* nome_prod |

Não é possível acessar os valores do atributo nome_prod pelas chaves primárias n_pedido e id_prod

#### Terceira Forma Normal

Nenhum atributo não identificador deve ser depender de outro atributo não identificador

|pedido  |                            
|:------:|                
|# número|                  
|* data  |                              
|* total |
|* itemID|
|* qtd   |  
| preço  |

|item  |
|:----:|  
|# id  |
|* qtd |  
| preço|

### Regras de Negócio

É uma declaração que define ou restringe algum aspecto do negócio

Usada ára definir entidades, atributos, relacionamentos e restrições

#### Estruturais

Indicam os tipos de informações a serem armazenadas e como os seus elementos se inter-relacionam

|pedido  |                            
|:------:|                
|# número|                  
|* data  |
|* qtd   |
|* total |

|funcionário  |    
|:-----------:|                
|# cargo      |                  
|# nome       |

Cada pedido deve apresentar um número de identificação, a data do pedido, a quantidade e o total

Todo pedido deve ser tratado por um funcionário

#### Procedurais

Lidam com os pré-requisitos, etapas ou processos de uma empresa

Algumas regras procedurais não podem ser diagramadas, mas devem ser documentadas para ser programadas posteriormente

A aprovação de solicitações deve ser assinada pelo gerente

## 3.4 - Terminologia e Mapeamento da Modelagem de Dados

* Terminologia de um ERD para o modelo físico:

    * Entidade = Tabela

    * Instância = Linha

    * Atributo = Coluna

    * UID primário = Chave Primária

    * UID secundário = Chave Exclusiva(única)

    * Relacionamento = Chave Estrangeira

### Mapeamento de Relacionamentos

Os relacionamentos são mapeados entre chaves primárias e estrangeiras para permitir que uma tabela faça referência a outra

#### Muitos para Muitos

Cria-se uma entidade associativa que conterá colunas de chave estrangeiras que fazem referência às tabelas de origem

Essas colunas fazem parte da chave primária da tabela associativa

### Mapeamento Supertipo/Subtipos

#### Tabela única

Usada quando a maioria dos subtipos tem atributos em comum e relacionamentos compartilhados

#### Várias Tabelas

Cria-se uma tabela para cada subtipo

Usada quando os subtipos tem poucos atributos em comum e relacionamentos compartilhados