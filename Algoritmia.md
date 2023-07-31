Algoritmos - Básico

> [!NOTE]
> Define-se como algoritmo um conjunto finito de regras através das quais se pode dar execução a um dado processo.

## Um algoritmo deve satisfazer os seguintes atributos:

+ Ser Finito

Terminar após um nº finito de ações

+ Ser Intiligível

As ações evocadas serem finitas, sem ambiguidade.

+ Ser Exequível

As ações evocadas poderem realizar-se num lapso de tempo satisfatório.

+ Ser Caracterizável

Existir um conjunto de entradas (eventualmente vazio) do qual o processo dependa;
Existir  um conjunto de saídas (resultados) de que se conheça a relação funcional com as entradas.

## Um algoritmo pode ser representado das seguintes formas:

+ A forma narrativa comum

+ O Fluxograma (flowchart)

Forma gráfica de representação independente da sua implementação

+ O Pseudo código

Forma narrativa sucinta que exprima sem redundâcia a sequência de ações e os critérios de decisão envolvidos no algoritmo.

+ As Linguagens de Programação

Formas efetivas de código de algoritmos, obedecendo a regras sintáticas e semânticas perfeitamente definidas, nas quais se podem descrever os algoritmos, e delas (de forma automática) se pode extrair código que torne esse algoritmo executável por um computador.

## S

**S** é um conjunto de primitivas de controlo com um único ponto de entrada e um único ponto de saída, um algoritmo explicitado exclusivamente com essas primitivas diz-se estrturado em relação ao conjunto **S**.

O conjunto S normalmente adoptado envolve as seguintes primitivas:

+ Decisão Binária

```cpp
If (condição) ação1 else ação2
```

+ Repetição condicional

```Cpp
while (condição) ação
```

+ Decisão Multipla

```Cpp
switch (expressão) {

case expressão1: ação1

case expressão2: ação2

...
}

```

## Constituintes dos Algoritmos

+ Parâmetros do Processo ou Entradas

Valores ou objetos sobre os quais se irá exercer o processo

+ Resultados Finais ou Saídas

Valores Numéricos ou objetos resultantes do processo.

+ Variáveis intermediárias

Variáveis representadas por nomes ou menemónicas, que após iniciadas irão  evoluindo de valor ao longo do processo.

+ Índices de Iteração

Variáveis inteiras que ao longo dos ciclos de repetição irão sofrendo incrementos ou decrementos, e sobre cujo valor se exercerem teste de decisão.

+ Ações primitivas

Ações ou operacões que se pressupõe ser executadas pelos dispositivos disponíveis. No caso de um programa, as ações primiticas são genericamente referidas como instruções (operações básicas da linguagem, invocação de funções de biblioteca ou funções previamente definidas para se contituírem auxiliares do algoritmo).
