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