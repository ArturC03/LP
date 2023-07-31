## Comentários

> [!NOTE]
>Para inicializar **Comentários** de apenas uma linha usar os carateres **//**.

### Exemplo:

```Cpp
//Isto é um Comentário
```

> [!NOTE]
> Para criar Um Comentário que preencha mais do que uma linha escrever **/*** para começar e ***/** para terminar.

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

## Escrita no Ecrã

> [!WARNING]
> Para executar qualquer uma das instruções é necessário importar a biblioteca **iostream**

> [!IMPORTANT]
> Para começar a imprimir texto no ecrã usa-se a instrução **std::cout** seguida por **<<** e depois o texto que se deseja imprimir

```cpp
std::cout << "Hello World";
```

> [!NOTE]
> Para Trocar de Linha usa- se a instrução **endl** ou o carater **\n**

+ endl

```cpp
std::cout << "Hello World" << endl;
```

+ **\n**

```cpp
std::cout << "Hello World\n";
```

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

> [!NOTE]
> Utilizar **const** para indentificar variavel como constante

#### Syntax:

```C
const <tipo> <nome_variavel> = <valor>;
```

#### Exemplo:

```C
const int pi = 3.1415916;
```

> [!WARNING]
> Em C++ Há algumas palavras chave que não podem ser utilizadas como nome de uma variável, pois essas palavras já têm uma função o que faria o compilador crashar e consequentemente falhas na compilação.

### Palavras-Chave do C++

|          |          |          |          |          |          |
|----------|----------|----------|----------|----------|----------|
|asm          | auto         | bool         | break         | case         | catch         |
|char          |  class        | const         |const_cast          | continue         | default         |
|delete          |do          |double          |dynamic_cast          |else          |enum          |
| explicit         |extern          |false          |float          |for          |friend          |
|goto          |if          |inline          |int          |long          |mutable          |
|namespace          |new          |operator          |private          |protected          |public          |
|register          |reinterpret_cast          |return          |short          |signed          |sizeof          |
|static          |static_cast          |struct          |switch          |template          |this          |
|throw          |true          |try          |typedef          |typeid          |typename          |
|union          |unsigned          |using          |virtual          |void          |volatile          |
|wchar_t          |while          |--------------|--------------|--------------|--------------|

***

## Leitura de Dados

> [!NOTE]
> Em C++ Para Ler Dados usa-se a instrução **std::cin** seguida de **>>** e a **variável** que se Pretende Ler. Para Utilizar esta função é necessário importar a biblioteca **iostream**

```cpp
char carater

std::cin >> carater;
```

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
    std::cout << "Há 3 cookies.\n";
}
else if(cookie > 0)
{
    std::cout << "Há {0} cookies\n";
}
else
{
    std::cout << "Não há mais cookies.\n";
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

> [!WARNING]
> Para Sair de qualquer um dos loops de forma inesperada utilizar intrução **break;**

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
    std::cout << i;
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
    std::cout << i;
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
    std::cout << i;
    i--;
}while (i > 0);
```

***

## Funções

> [!WARNING]
> Utilizar intrução **void** quando a função não tiver tipo ou quando não tiver parâmetros

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

> [!TIP]
> Se for a Função **main** é possivel pôr dois parametros: **argc**, **argv**, que respetivamente vão nos dizer a quantidade total de palavras dadas pelo utilizador e um array dessas palavras.

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

> [!IMPORTANT]
> Utilizar intrução **return** para sair do programa de forma prematura, são usados numeros diferentes de 0 quando ocorre um erro de forma a o utilizador a reconhecer o erro.

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
> [!IMPORTANT]
> Para fazer **referência** Às **variaveis da estrutura** por um **.** e o nome da variável da estrutura.

#### Exemplo:

```C
person eu;
//...
printf("\s\n", eu.name);
```

***

## Bibliotecas
> [!NOTE]
> Para Incluir nova biblioteca em C usa- se a palavra - chave #include

```C
#include <nome_biblioteca>
```

+ **<stdio.h>** para input e output
+ **<cs50.h>** para o tipo string
+ **<math.h>** para funções para numeros exemplo round para arredondar
+ **<string.h>** para manipulação de strings

***

## Formas de compilar

```Batch
make programa
./programa
```

```Bash
clang -o <'nomePrograma'> <'nomeFicheiro'>
```

```bash
gcc <nomeFicheiro> -o <nomePrograma>
```

***

<span style="color:white;font-size:1cm;">
© Artur Cruz
</span>
