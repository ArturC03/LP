# C# - Instruções

## Declaração de Variáveis/Constantes

### <span style="color:brown">**Variáveis**</span>

```C#
<Tipo> <nome_variavel>;
```

#### Exemplo

```C#
int cookie;
```

### <span style="color:brown">**Constantes**</span>

```C#
<Tipo> <nome_constante> = <valor>;
```

#### Exemplo

```C#
int pi = 3.1415926536;
```

***

## Tipos de Variáveis

1. <span style="color:white">Int</span>

```C#
int inteiro = 3; //Guarda valores Inteiros
```

2. <span style="color:white">Double</span>

```C#
double duplo = 3.14; //Guarda valores com duas casas decimais
```

3. <span style="color:white">String</span>

```C#
string corda = "Hello World"; //Guarda cadeias de carateres
```

4. <span style="color:white">Char</span>

```C#
char carater = "C"; //Guarda Carateres
```

5. <span style="color:white">Bool</span>

```C#
bool booliano = true; //Guarda valores Booleanos
```

6. <span style="color:white">Outras</span>

+ Decimal

+ Float

+ Byte

+ short

+ Long

+ DateTime

+ TimeSpan

***

## Leitura de Dados - Input

### <span style="color:brown">**Para Strings e Carateres**</span>

```C#
<variavel> = Console.Read(); //Lê o input
```

#### Exemplo

```C#
cookie = Console.ReadLine(); //Lê o input e Troca de Linha
```

### <span style="color:brown">**Para Outros Tipos**</span>

```C#
<variavel> = <tipo_variavel>.Parse(Console.Read()); //Lê o input
```

#### Exemplo

```C#
cookie = Int.Parse(Console.ReadLine()); //Lê o input e Troca de Linha
```

***

## Escrita no Ecrã

### <span style="color:brown">**Apenas Cadeia de Carateres**</span>

```C#
Console.WriteLine("<texto>");
```

#### Exemplo

```C#
Console.WriteLine("Olá");
```

### <span style="color:brown">**Apenas uma

Variável**</span>

```C#
Console.WriteLine(<variável>);
```

#### Exemplo

```C#
Console.WriteLine(cookie);
```

### <span style="color:brown">**Cadeia de Carateres e Variável**</span>

```C#
Console.WriteLine("<texto> {0} <texto>", <variável>)
```

#### Exemplo

```C#
Console.WriteLine("Cookies: {0}", cookie);
```

***

## Operadores Aritméticos

+ **+** → Soma

+ **-** → Subtração

+ **_*_** → Multiplicação

+ **/** → Divisão Real

+ **%** → Resto da Divisão

+ **//** → Divisão Inteira

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

## Atribuições

+ **=** → Atribuição Simples

+ **+=** → Incremento

+ **-=** → Decremento

+ ***=** → Multiplicação

+ **/=** → Divisão

+ **%=** → Resto

+ **<<=** → Desloca Bit para a esquerda

+ **>>=** → Desloca Bit para a direita

+ **&=** → AND

+ **|=** → OR

+ **^=** → XOR

+ **++** → Incremento de +1

+ **--** → Decremento de -1

***

## Estruturas Condicionais

### <span style="color:red">**If**</span>

```C#

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

#### Exemplo

```C#
if(cookie==3)
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

```C#
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

## Estruturas de Repetição

### <span style="color:brown">**For Loop**</span>

<span style="color:Red">**_Aviso🛑_: Para Sair de qualquer um dos loops de forma inesperada utilizar intrução "break;"**</span>

```C#
for(<inicialização>;<condição>;incremento/decremento)
{
    //bloco de instruções
} 
```

#### Exemplo

```C#
for(i=0;i<10;i++)
{
    Console.WriteLine(i);
}
```

### <span style="color:brown">**While Loop**</span>

```C#
while(<condição>)
{
    //bloco de instruções
} 
```

#### Exemplo

```C#
while(i>0)
{
    Console.WriteLine(i);
    i--;
} 
```

### <span style="color:brown">**Do While Loop**</span>

```C#
do
{
    //bloco de instruções
}while(<condição>);
```

#### Exemplo

```C#
do
{
    Console.WriteLine(i);
    i--;
}while(i>0);
```

***

## Tratamento de Excepções - Try Catch

```C#
try
{
    // bloco de código para detectar erro
}
catch (Exception ex)
{
    // bloco de código para tratar erro
}
```

***

<span style="color:white;font-size:1cm;">
© Artur Cruz
</span>
