# Mineração de Dados

## Resumo

## Aula 1: Introdução

### Conceito

> Processo de descoberta de novas informações e conhecimento,
no formato de modelos, regras e padrões, a partir de bases de dados.

```
A base de dados pode ser um banco de dados tradicional, 
um data warehouse ou qualquer outra forma de repositório.
```

### Aplicações de mineração de dados

- Detecção de spam; 
- Detecção de patologias por análise de imagens;
- Detecção de fraudes;
- Mineração de regras de associação; e
- Análise de sentimentos.

### Classificação

* Mineração Preditiva; e
* Mineração Descritiva.

### Mineração Preditiva

> Deseja-se prever o valor desconhecido de um determinado atributo, a
partir da análise histórica dos dados armazenados na base (base de treinamento).

### Mineração Descritiva

> Procura-se extrair padrões e regras que descrevam características importantes
dos dados do domínio de aplicação.

### Mineração de Dados

> Etapa principal do processo de KDD (Knowledge Discovery in Databases), na qual é
realizada a busca por novas informações e conhecimento.

### KDD (Knowledge Discovery in Databases)

É composto por seis fases (Navathe):

* Seleção de dados;
* Limpeza de dados;
* Enriquecimento dos dados;
* Transformação dos dados,
* _**Mineração dos dados**_; e
* Apresentação e análise dos resultados.

### Tarefas em mineração de dados

* Regras de Associação (RA);
* Padrões de Sequências;
* Classificação; e
* Clusterização.

### Regras de Associação (RA) aka market basket analysis

> Uma RA representa um padrão de relacionamento entre itens de dados do domínio
da aplicação que ocorre com uma determinada frequência na base.

Exemplos:

```
{fralda} => {cerveja}
{pão, manteiga} => {leite} , confiança de 80%
{candidíase} => {pneumonia}
```

RAs são extraídas de bases de dados que contém transações.

Transações:

|ID|Itens comprados|
|:-:|:------------:|
|1| leite, pão, refrigerante|
|2| cerveja, carne|
|3| cerveja, fralda, leite, refrigerante|
|4| cerveja, fralda, leite, pão|
|5| fralda, leite, refrigerante|

RAs:

| RA | Confiança | Suporte |
|:--:|:---------:|:-------:|
|\{fralda} => \{cerveja}|66% (2/3)|médio (2/5)|
|\{fralda} => \{leite}|100% (1/1)|alto (3/5)|
|\{leite} => \{fralda}|75% (3/4)|alto (3/5)|
|\{carne} => \{cerveja}|100%(1/1)|baixo (1/5)|

### Padrões de Sequências

> Padrões de Sequência representam sequências de conjuntos de itens que ocorrem
nas transações de diferentes consumidores, com determinada frequência (em ordem).

Exemplo:

|Consumidor|Data/Hora|Produtos|
|:--:|:---------:|:-------:|
|João|01.08.2001/17:01|leite, pão|
|João|03.08.2001/14:25|carne, cerveja|
|João|10.08.2001/21:15|queijo, manteiga, sal|
|-|-|-|
|Marcos|05.08.2001/10:16|leite, ovos|
|Marcos|08.08.2001/18:30|leite, manteiga|

```
Padrão de Sequência: {(leite)(queijo, manteiga)}
```

### Classificação

> Um classificador estima/prevê, entre um conjunto pré-definido de classes, aquela
a qual pertence um elemento, a partir de seus atributos.

* Em última análise é uma função que realiza tal mapeamento; 
* A função é descoberta a partir de um modelo de função/técnica (escolhido) e 
uma base de treinamento.

![Classificação](classificacao.png)