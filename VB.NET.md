# Visual Basic .NET

## Comentários

Em VB.NET comentários de uma linha podem ser feitos com o uso de um **'**.

```vb
'Isto é um comentário
i = 0 
```

***

## Declaração de Variáveis/Constantes

Para declarar **variáveis** em VB.NET usa- se a palavra-chave **Dim**.

### Sintax

```vb
Dim <nomeVariavel> As <tipoVariavel>
```

### Exemplo

```vb
Dim cookie As integer
```

Para declarar **Constantes** em VB.NET usa-se a palavra-chave **Const**.

```vb
Const <nomeConstante> As <tipoConstante> = <valorConstante>
```

### Exemplo

```vb
Const pi as decimal = 3.1415
```

***

## Instruções de Leitura de Dados

Em VB.NET usa- se o método Read() para ler a linha e ReadLine() para ler e trocar a linha.

### Sintax

```vb
console.Read() 'Lê linha
console.ReadLine() 'Lê e troca de linha
```

***

## Intruções de Escrita no Ecrã

Para escrever algo no ecrã em VB.NET podem ser usadas as instruções Write() e WriteLine().

```v
console.Write("<mensagemEcrã>") ' Escreve mensagem
console.Write("<mensagemEcrã>") ' Escreve mensagem e troca de linha
```

Para incluir uma **variável** numa mensagem podem ser usados **3** métodos:

+ {}

```v
console.WriteLine("{0} {1}", variavel1 variavel2)
```

+ $

```v
console.WriteLine($"{variavel1} {variavel2}")
```

+ **+**

```v
console.WriteLine(variavel1 + variavel2 + "")
```

***

## Operadores Aritméticos

+ **+** → Soma

+ **-** → Subtração

+ **_*_** → Multiplicação

+ **/** → Divisão Real

+ **\\** → Divisão Inteira

+ **^** → Potência

+ **MOD** → Resto da Divisão Inteira

***

## Operadores Relacionais

+ **=** → Igualdade

+ **<>** → Diferença

+ **>** → Maior Que

+ **<** → Menor Que

+ **>=** → Maior ou Igual
+ **<=** → Menor ou Igual

***

## Operadores Lógicos

+ **and** → E

+ **or** → OU

+ **not** → Negação

***

## Operadores de Concatenação

+ **+**
+ **&**

***

## Atribuições

+ **=** → Atribuição Simples

+ **+=** → Incremento

+ **-=** → Decremento

+ ***=** → Multiplicação

+ **/=** → Divisão

+ **%=** → Resto

+ **&=** → Concatenação

+ **^=** → Potência

***

## Estruturas Condicionais

### <span style="color:red">**If**</span>

```vb
if(<condição1>)

    //bloco de código

elseif(<condição2>)

    //bloco de código

else

    //bloco de código
end if
```

#### Exemplo

```vb
if(cookie==3)

    Console.WriteLine("Há 3 cookies.");

else if(cookie > 0)

    Console.WriteLine("Há {0} cookies", cookie);

else

    Console.WriteLine("Não há mais cookies.");

end if
```

### <span style="color:brown">**Switch**</span>

```vb
Select case(<expressão>)

    case <valor1>:

        //bloco de código

    case <valor2>:
        
        //bloco de código

    case else:

        //bloco de código

end select
```

#### Exemplo

```vb
Select case (cookie)

    case 1 to 10:
        
        console.WriteLine("0")

    case is 25, is 50:
        
        console.writeLine("1")

    case else:

        console.writeLine("-1")

end select
```

***

## Estruturas de Repetição

### For

```vb
For <var> = numInicial to numFinal Step Incremento

    console.WriteLine(<var>)

Next
```

#### Exemplo

```vb
For i = 0 to 9 Step 1

    console.WriteLine(i)

Next
```

### While

```vb
while (<condição>)

    'bloco de código

End while
```

#### Exemplo

```vb
Dim x As Integer = 10

while x > 0

    console.WriteLine(x)
    x -= 1

End while
```

### Do While

```vb
do

    'bloco de código

Loop While (<condição>)
```

#### Exemplo

```vb
Dim x as integer = 10

do

    dim x as integer = 10
    console.WriteLine(x)
    x -= 1

loop while x > 0
```

### Do Until

```vb
do

    'bloco de código

Loop Until (<condição>)
```

#### Exemplo

```vb
Dim x as integer = 10

do

    dim x as integer = 10
    console.WriteLine(x)
    x -= 1

loop Until x <= 0
```

***

## Vetores/Matrizes - Arrays

### Declaração

```vb

Dim vet(numPosicoes) as tipoDados 'Vetor
dim mat(numlinhas, numColunas) as tipoDados 'Matriz

```

### Alterar tamanho Vetor

```vb
Redim Preserv nomeVet(novaDimensão) 
```

***

## Estrutura de Controle de Exceções - Try Catch

```vb
Try

    'Bloco de Código

catch ex as Exception

    'Bloco de Código

end Try
```

***

## Estruturas - Struct

```vb

Structure nomeEstrutura

    'Declarações

end Structure

```

***

## Procedimentos e Funções

### Procedimentos

```vb
[Private|Public] Sub nomeProcedimento([listaArgumentos])

    'Declaração de Variáveis Locais

    'Bloco de Instruções

End Sub
```

### Funções

```vb
[Private|Public] Function nomeFunção([listaArgumentos]) As tipoRetorno

    'Declaração de Variáveis Locais

    'Bloco de Instruções

    Return = valorRetorno

End Function
```

### Passagem de Argumentos

Byval para usar uma **cópia** da variável

Byref para usar **a** variável

```vb
sub nomeSub(byval nomeArgumento As Tipo, byref nomeArgumento2 As Tipo, ...)
```

### Chamada de Um Procedimento/Função

```vb
subNome(argumento1, argumento2)
```

***

## Funções/Procedimentos Pré-Definidos

+ **Asc** → Código Ascci Carater

+ **Chr** → Carater Código Ascci

+ **LCase** → String Lower Case

+ **UCase** → String Upper Case

+ **Length/Len** → Tamanho String

+ **SubString** → Retirar String de String

+ **Replace** → Trocar carater\string por outro

+ **IndexOf** → Posição da primeira ocorrência de carater\string Num Intervalo à escolha

+ **InStr** → Posição da primeira ocorrência de carater\string

+ **InStrRev** → Posição da última ocorrência de um carater\string

+ **Remove** → Remover Uma string a partir de uma posição à escolha

+ **RemoveAt** → Remover uma ou mais Posições  

+ **Insert** → Coloca numa determinada posição um carater\string

+ **Join** → Junta numa String um conjunto de Elementos de um Array, utilizando um determinado carater como separador

+ **Split** → Separa uma string num vetor com um carater\string como separador

+ **First** → Retorna Primeiro Carater de Uma String

+ **Last** → Retorna Último Carater de Uma String

+ **ToCharArray** → Cria Um Array que cada posição contêm um carater da string Determinada

+ **CInt/CDec/CStr...** → Conversão Entre Tipos de Dados

+ **IsNumeric** → Verifica se uma String Tem Valor Numérico

***

<span style="color:white;font-size:1cm;">
© Artur Cruz
</span>
