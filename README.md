# E-Science

## Resumo

## Aula 1: Apresentação da disciplina

### E-Science

Definição:

> E-Science is the application of **computer technology** to the undertaking 
> of **modern scientific investigation** and all materials generated through the **scientific process**.

## Aula 2: Método Científico

### Ciência

Envolve:

- Corpo de conhecimento; e
- Processo (de descoberta para interligar fatos/conhecimentos a novos conhecimentos).

Desafios e características:

- Olhar o passado, compreender o presente e indicar o futuro;
- Desenvolver conhecimento confiável; e
- Colaboração global.

### Método Científico

1. Faça uma observação/pergunta;
2. Formule uma hipótese;
3. Faça experimentos para testar a hipótese;
4. Reporte os resultados;
5. Itere o processo: usando os resultados para refinar o processo ou hipóteses;

### Testando hipóteses

> Ao testar uma hipótese os resultados podem **dar suporte** à hipótese ou
> **contradizer** a hipótese, em qualquer dos casos é preciso considerar _sempre a possibilidade
> de o teste possuir defeito ou vício_.

- A possibilidade de defeitos ou vícios durante testes de hipótese são **ameaças** ao experimento;
- Ao testar hipóteses é comum estabelecer suposições/pré-condições que não serão alvo de teste e 
si mesmas;
- Todavia, todas as suposições/pré-condições devem poder ser testadas, caso se decida;
- Em geral, tais suposições/pré-condições já foram testadas antes (por outros experimentos ou 
cientistas); e
- Precisão é chave ao fazer observações.

### Experimentos

Tipos:

- _in vivo_: conduzido em organismos vivos;
- _in vitro_: conduzido em laboratório ou ambiente controlado;
- _in virtuo_: simulação por computador com agentes interagindo com a simulução; e
- _in silico_: 100% simulado por computador, inclusive agentes.

Experimentos _in vivo_ e _in vitro_ são lentos, arriscados e custosos.

E-Science está diretamente relacionada a experimentos _in virtuo_ e _in silico_, 
mas também pode estar associada à coleta e análise de dados.

### Dados

Testes geram dados...

- Cientistas analisam e interpretam os dados a fim de entender como os mesmos estão 
relacionados às hipóteses ou previsões;
- Cálculos estatísticos, tabelas, visualizações e modelos podem apoiar tais análises;

![Reasoning Data](reason_data.png)

### Construindo um muro forte do conhecimento...

- Publicar permite que outros cientistas testem, reusem e expandam os conhecimentos;
- Para uma publicação ser aceita, rigoroso processo de avaliação é efetuado por pares;
- Ao contar a história, ela não precisa ter a ordem exata de como tudo aconteceu;
- Inverter a ordem pode tornar o entendimento mais fácil ou interessante.

### Conferência

- Autor;
- PC (Comitê de Programa) Chair (Presidente);
- Revisores;
- Submissões orientadas a deadline;
- Accept, Rebuttal, Reject

### Revistas

- Autor;
- Editor;
- Revisores;
- Fluxo contínuo de submissões;
- Accept, Minor Review, Major Review, Submit as New, Reject

### Processo de publicação

Submissão > Revisão > Resposta > Ajustes > Submissão

### Hipótese vs Teoria vs Modelo

- Hipótese: Diz respeito a fenômenos restritos;
- Teoria: Diz respeito a fenômenos mais amplos e integram ou generalizam hipóteses;
- Modelo: Diz respeito a fenômenos tão complexos que precisam ser descritos formalmente
por equações ou software.

## Aula 3: Proveniência

### Definição

> The provenance (also referred to as the audit trail, lineage, and pedigree) of a data 
> product contains **information about the process and data** used to derive the data product. 
> It provides important documentation that is key to **preserving** the data, to **determining the data's quality and authorship**, 
> and to **reproduce** as well as **validate** the results. 
> These are all important requirements of the **scientific process**. 

_(Davidson and Freire, SIGMOD 2008)_

### Ciclo de vida de experimentos

![Provenance is Key](provenance_is_key.png)

### Usos de Proveniência

- Interpretação de resultados;
- Auditoria;
- Reproducibilidade;
- _Debugging_;
- _Caching_;

### Evolução

- Cientistas sempre usaram proveniência em algum nível, porém de uma forma pouco escalável ou perceptível.
- Nos últimos anos aumentaram o número de ferramentas para auxiliar e automatizar experimentos, capturando
tipos diferentes de proveniência;

### Tipos de Proveniência

- Prospectiva: Diz respeito à especificação da tarefa/processo;
- Retrospectiva: Diz respeito à execução efetiva da tarefa, seus passos e interações com o ambiente (log detalhado da execução);

### Scripts vs Workflows

São as ferramentas através das quais os cientistas materializam seus experimentos.

![Provenance Types Perspectives](prov_types_perspectives.png)

### Gerenciamento de Proveniência

Sistemas de gerenciamento de proveniência consistem de 3 componentes:

- Mecanismo de captura
  - Baseado em Sistema Operacional (SO);
  - Baseado em Workflow; e
  - Baseado em Processo.
- Modelo de representação; e
- Infraestrutura (armazenamento, acesso e consulta).

### Mecanismo de captura - Baseado em SO

- [+] Não é necessário fazer modificações no script do experimento;
- [-] Possui grão fino (rico em detalhes) de informações; e
- [-] Apenas proveniência retrospectiva é capturada.

### Mecanismo de captura - Baseado em Workflow

- [+] Captura da proveniência é implícita/direta;
- [+] Proveniência retrospectiva e prospectiva são capturadas;
- [+] Proveniência retrospectiva e prospectiva são integradas; e
- [-] Precisa rodar em um sistema de workflow.

### Mecanismo de captura - Baseado em Processo

- [-] A captura deve ser especificada em suas atividades (necessita de instrumentação);
- [-] Apenas proveniência retrospectiva é capturada, _exceto se houver captura da instrumentação_; e
- [+] Funciona em sistemas de workflow.

### Granularidade da proveniência

- Grossa: Menos informações, menos espaço;
- Fina: Mais informações/detalhes, mais espaço.

### Modelos de Representação

Surgiram através dos desafios de proveniências (4 ao todo), que evoluíram:

OPM (Open Provenance Model) => PROV (Modelo criado pela W3C)

![Evolution](evolution.png)

### Relações de Causalidade de PROV

![Prov Relationships](relations.png)

### Workflow Prov vs Data Prov

- Workflow Prov: O que foi visto até aqui;
- Data Prov: Contém proveniência capaz de responder "Por quê?", "Como?" e "Onde?" de cada item de dado (Ex: tuplas) da proveniência;
  - Why Provenance;
  - How Provenance;
  - Where Provenance;

## Aula 4: Workflows e Scripts

### Composição: concebendo experimentos

Cientista planeja o experimento em uma representação (abstrata) que depois será materializada 
como um workflow ou script (concreta);

### Workflow

Cadeia de atividades representadas como **fluxos de dados**:

Entradas de dados > Atividade > Saídas de Dados > Atividade > ...

_Dados que não possuem dependência podem começar a fluir paralelamente!_

### Script

Conjunto de programas integrados para uma determinada atividade baseando-se em **fluxos de controle**...

- Everything is Object
- Multiparadigm
- Typeless (dynamically typed)
- Interpreted
- Automatic memory management
- Extensive component library

_Podem ser interativos!_

### Executando experimentos

Scripts e Workflows auxiliam na automatização dos experimentos. Cada execução do experimento é um trial (ensaio).

### White Box vs Black Box

- Caixa Branca: Atividades/funções em que se pode ver o que acontece entre os dados de entrada e saída;
  - Ex.: funções definidas em scripts;
- Caixa Preta: Atividades/funções em que **NÃO** se pode ver o que acontece entre os dados de entrada e saída. 
São mais sensíveis a proveniências implícitas;
  - Ex.: workflows,funções de bibliotecas importadas em scripts.
  
## Aula 6: Reprodutibilidade

### Definição

> Um experimento **R** composto por **S** passos
> executados em um momento **T** e em um ambiente **E** a partir de dados **D** é dito reprodutível 
> *se e somente se* existe uma reprodução **R'** que pode ser executada por uma sequência de passos **S'** 
> (S'≠S ou S'=S) em um momento **T'** > **T**, em um ambiente **E'** (E'≠E ou E'=E) e a partir de dados 
> **D'** (D'≠D ou D'=D) com resultados consistentes, onde R' ~ R.

```
Reprodução exata: T'>T, S'=S, D'=D, E'=E => R'=R (Repetibilidade)
```

### Reproduzir vs Replicar

- Reproduzir: Mesmo código, mesmos dados (mesmo experimento);
- Replicar: Código diferente, dados diferentes (investigação independente);

### R*

![Prov Relationships](r.png)

### Reexecutar, R¹

- Deve ser capaz de reexecutar a qualquer tempo (futuro);
- E' ~ E, S' = S e D' = D;
- Resultado não importa; e
- Desafios: montar um ambiente (original) que permita a execução e o código não ficar obsoleto.

### Repetível, R²

- Mesmos resultados para mesmas repetições, comportamento determinístico;
- E' ~ E, S' = S, D' = D e R' = R;

### Reprodutível, R³

- Resultados compatíveis;
- E' = E, S' = S, D' = D e R' ~ R;

### Reprodutibilidade, R³

- Implica **reexecução**, **repetibilidade** e **disponibilidade**, além impor condições adicionais:
  - Dependencies and platforms must be described as precisely and as specifically as possible;
  - Parameters values, the version of the code, and inputs should accompany the result files; e
  - The data and scripts behind the graphs must be published.
  
### Resumo

![Summary](summary1.png)

### Requisitos mínimos

![Minimum Standard](summary2.png)