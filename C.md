# C - Instruções básicas

## Comentários

Para inicializar **Comentários** de apenas uma linha usar os carateres **//**.

### Exemplo:

```C
//Isto é um Comentário
```

Para criar Um Comentário que preencha mais do que uma linha escrever **/*** para começar e ***/** para terminar.

### Exemplo:

```C
/*
    Este comentário está:
    a ocupar
    mais do que
    uma linha
*/
```

***

## Escrita no ecrã

### Para apresentar texto no ecrã

```C
printf("<texto>");
```

### Para apresentar texto e trocar de linha Usar **/n**:

```C
printf("<texto>\n");
```

### Para apresentar texto e variável:

+ Para strings **%s**:

```C
printf("Hello, %s\n", var);
//Output: Hello, <valor de var>
```

+ Para inteiros **%i**:

```C
printf("Hello, %i\n", var);
//Output: Hello, <valor de var>
```

+ Para carateres/Chars **%c**:

```C
printf("Hello, %c\n", var);
//Output: Hello, <valor de var>
```

+ Para floats/doubles **%f**:

```C
printf("Hello, %f\n", var);
//Output: Hello, <valor de var>
```

+ Para long integers **%li**:

```C
printf("Hello, %li\n", var);
//Output: Hello, <valor de var>
```

<span style="color:Red">**_Aviso🛑_: Para números reais ao usar um "." mais um número pode ser especificado a quantidade de casas decimais que é desejado apresentar**</span>

#### Exemplo:

```C
double pi = 3.14;
printf("%.1f",pi); //Output: 3.1

```

***

## Variáveis/Constantes

### Syntax

```C
<tipo> <nome> = <valor>;
```

### Exemplo:

```C
string var = "Hello World";
```

Tipos de Variaveis:

+ bool → booliano
+ char → carater
+ double → real com **2 casas** decimais
+ float → real com **1 casa** decimal
+ int → inteiro
+ long → inteiro com **mais possibilidades** de numeros
+ string → **cadeia** de carateres

### Constantes

Utilizar const para indentificar variavel como constante

#### Syntax:

```C
const <tipo> <nome_variavel> = <valor>;
```

#### Exemplo:

```C
const int pi = 3.1415916;
```

***

## Operadores Aritméticos

+ **_+_** → Soma
+ **_-_** → Subtração
+ **_*_** → Multiplicação
+ **_/_** → Divisão
+ **%** → Resto

***

## Atribuições

+ **=** → atribuição simples
+ **+=** → incrementação
+ **++** → incrementação de 1
+ **-=** → decrementação
+ **--** → decrementação de 1

***

## Operadores Relacionais

+ **==** → Igualdade
+ **!=** → Diferença
+ **>** → Maior Que
+ **<** → Menor Que
+ **>=** → Maior ou Igual
+ **<=** → Menor ou Igual

***

## Operadores Lógicos

+ **&&** → E
+ **||** → OU
+ **!** → Negação

***

## Estruturas Condicionais

### <span style="color:red">**If**</span>

```C
if(<condição1>)
{
    //bloco de código
}
else if(<condição2>)
{
    //bloco de código
}
else
{
    //bloco de código
}
```

#### Exemplo:

```C
if(cookie == 3)
{
    Console.WriteLine("Há 3 cookies.");
}
else if(cookie > 0)
{
    Console.WriteLine("Há {0} cookies", cookie);
}
else
{
    Console.WriteLine("Não há mais cookies.");
}
```

### <span style="color:brown">**Switch**</span>

```C
switch(<expressão>)
{
    case <valor1>:
        //bloco de código

        break;
    case <valor2>:
        //bloco de código

        break;

    default:
        //bloco de código a executar se nenhum dos valores acima for o resultado da <expressão>

        break;
}
```

***

## Estruturas de Repetição

### <span style="color:brown">**For Loop**</span>

<span style="color:Red">**_Aviso🛑_: Para Sair de qualquer um dos loops de forma inesperada utilizar intrução "break;"**</span>

```C
for(<inicialização>;<condição>;incremento/decremento)
{
    //bloco de instruções
}
```

#### Exemplo:

```C
for(i=0; i<10; i++)
{
    Console.WriteLine(i);
}
```

### <span style="color:brown">**While Loop**</span>

```C
while (<condição>)
{
    //bloco de instruções
}
```

#### Exemplo:

```C
while (i > 0)
{
    Console.WriteLine(i);
    i--;
}
```

### <span style="color:brown">**Do While Loop**</span>

```C
do
{
    //bloco de instruções
}while(<condição>);
```

#### Exemplo:

```C
do
{
    Console.WriteLine(i);
    i--;
}while (i > 0);
```

***

## Funções

<span style="color:Red">**_Aviso🛑_:  utilizar intrução "void" quando a função não tiver tipo ou quando não tiver parâmetros**</span>

```C
<tipo_de_retorno> <nome>(<parâmetros>)
{
    //bloco de código
    return <valor_de_retorno>; //Return é Opcional
}
```

#### Exemplo:

```C
int main(int i)
{
    //bloco de código
}
```

#### Exemplo sem tipo ou argumentos:

```C
void main(void)
{
    //bloco de código
}
```

Se for a Função **main** é possivel pôr dois parametros: **argc**, **argv**, que respetivamente vão nos dizer a quantidade total de palavras dadas pelo utilizador e um array dessas palavras.

Exemplo:

```C
//nome de ficheiro exemplo
int main(int argc, string argv[])
{
    if (argc == 2)
    {
        printf("Hello, %s\n",argv[1]);
    }
    else
    {
        printf("hello world\n");
    }

    /*Exemplo de Prompt:
    make exemplo
    ./exemplo Artur
    hello, Artur
    */

    /*Exemplo de Prompt:
    make exemplo
    ./exemplo
    hello world
    */
}
```

<span style="color:Red">**_Aviso🛑_:  utilizar intrução "_return_" para sair do programa de forma prematura, são usados numeros diferentes de 0 quando ocorre um erro de forma a o utilizador a reconhecer o erro.**</span>

***

## Vetores - Arrays

### Syntax de Declaração:

```C
<tipo_var> <nome_var>[num_posicoes];
```

#### Exemplo

```C
int array[10];
//Isto cria um array com 10 posições chamado "array"
```

### Para Fazer referência à posição:

```C
<nome_var>[posicao] = <valor>;
```

#### Exemplo:

```C
array[3] = 5
//Isto atribui 5 à posição 3 de "array"
```

Usar **string** como **Array** de Chars:

Exemplo:

```C
string exe = "HI!";

printf("\s\n",exe); //Output: HI!

printf("\c\n",exe[1]) //Output: I
```

***

## Estruturas

### Syntax:

```C
typedef struct
{
    <tipo> <nome>;
    <tipo> <nome>;
    <tipo> <nome>;
    ...
}
<nome_estrutura>;
```

### Exemplo:

```C
typedef struct
{
    string name;
    string number;

}
person;
```
<span style="color:Red">**_Aviso🛑_: Para fazer referência Às variaveis da estrtura por um "." e o nome da variavel da estrutura.**</span>

#### Exemplo:

```C
person eu;
//...
printf("\s\n", eu.name);
```

***

## Bibliotecas

Para Incluir nova biblioteca em C usa- se a palavra - chave #include

```C
#include <nome_biblioteca>
```

+ <stdio.h> para input e output
+ <cs50.h> para o tipo string
+ <math.h> para funções para numeros exemplo round para arredondar
+ <string.h> para manipulação de strings

***

## Formas de compilar

```Batch
make programa
./programa
```

```Bash
clang -o <'nome_programa'><'nome_ficheiro'>
```

***

<span style="color:white;font-size:1cm;">
© Artur Cruz
</span>
