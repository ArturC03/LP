# Python - Intruções Básicas

## Comentários

> [!NOTE]
> Em Python podem ser escritos comentários numa ou mais linhas:

+ Uma Linha

```python
# Isto é um comentário
```

+ Várias Linhas

```Python
"""
Este comentário 
ocupa mais 
do que 
uma Linha
"""
```

## Escrita No Ecrã

> [!NOTE]
> Em python usa-se a intrução **print** para imprimir **texto no ecrã**
> A função **print troca de linha** automaticamente

### Escrita Simples

```Python
print("Hello")
print("World")
# Output: Hello
# Output: World
```

### Escrita com **Sep**

>[!TIP]
> A função também contém o parametro **sep** que define uma string que vai estar entre cada parametro da função. Por defeito ela está definida como **' '**.

```python
print("Hello" + "World") # Output: Hello World

print("Hello" + "World", sep = '') # Output: HelloWorld
```

### Escrita Sem Trocar de Linha

> [!TIP]
> Em Python existe um argumento end que tem como função adicionar uma string no final de uma instrução print. End está por defeito = '\n' mas este valor pode ser alterado

```Python
print("Hello", end = "")
print("World") 
#Output: Hello World

```

### Escrita Com Variáveis

```Python
variavel = "World"
print("Hello " + variavel) # Output: Hello World

print("Hello ", variavel) # Output: Hello  World

print(f"Hello {variavel}") # Output: Hello World

```

## Variáveis

>[!NOTE]
> Em Python variáveis não têm tipos, por isso não é preciso declarar uma variável.

```Python
variavel = "valor"
```

## Leitura de Dados

> [!IMPORTANT]
> Input é uma função que lê um string e ao acompanhá-lo com as funções certas é possível ler qualquer tipo de dados

```Python
variavel = input("mensagem")
```

```Python
nome = input("qual é o teu nome?")
```

### Conversão de Tipos de dados

+ str → String

+ int → Número Inteiro

+ chr

+ float → Número Real(Decimal)

+ bool → Booliano

## Operadores Aritméticos

+ **+** → Soma
+ **-** → Subtração
+ ***** → Multiplicação
+ **/** → Divisão
+ **%** → Resto (Mod)
+ ****** → Expoente

## Operadores Relacionais

+ **==** → Igualdade
+ **!=** → Diferença
+ **>** → Maior que
+ **<** → Menor que
+ **>=** → Maior ou Igual
+ **<=** → Menor ou Igual

## Operadores Lógicos

+ **and** → E

+ **or** → OU

+ **not** → Negação

## Estruturas Condicionais

> [!CAUTION]
> Em python para determinar se uma linha de codigo faz parte de uma estrutura como **if** é necessário **indentar** essa linha se não o programa não funciona

+ ### If

+ Syntax:

```python
if condicao:
    #bloco de código
elif condicao:
    #bloco de código
else:
    #bloco de código
```

+ Exemplo:

```python
x = 3
y = 3

if x < y:
    print("x é menor que y")

elif x > y:
    print("x é maior que y")

else:
    print("x é igual a y")

#Output: x é igual a y
```

+ ### Match

+ Syntax

```python

match expressão:
    case valor1:
        #bloco de codigo

    case valor1:
        #bloco de codigo

    case valor1:
        #bloco de codigo

    case _: #equivalente a else 
        #bloco de codigo 
```

+ Exemplo

```python
name = input("Qual é o teu nome? ")

math name:
    case "Harry" | "Hermione" | "Ron":
        print("Gryffindor")
    
    case "Draco":
        print("Slytherin")
        
    case _:
        print("Quem?")
```

## Tratamento de Strings

Em python existem várias **Funções** e **Métodos** focadas em **strings**. Por isso vou só apresentar algumas.
> [!TIP]
> Para mais funções e métodos para strings ir ver a [Documentação Oficial da Linguagem Python](docs.python.org/3/library/stdtypes.html#string-methods)

+ **Strip**

> [!IMPORTANT]
> **Strip** Tem como função **Remover Espaços Brancos** nas estremidades de uma string.

```python
print("       Hello World        ".strip())
# Output: Hello World
```

+ Capitalize

> [!IMPORTANT]
> Tem como Função **Capitalizar** a **primeira letra** de uma **string**.

```python
print("hello world".capitalize())
#Output: Hello world
```

+ Title

> [!IMPORTANT]
>Tem como Função **Capitalizar** a **primeira letra** de **cada palavra** de uma string.

```python
print("hello world".title())
# Output: Hello World
```

+ Split

> [!IMPORTANT]
> Tem como Função Separar Uma string em várias Sub-Strings com um parametro com fator de separação

```python
variavel1, variavel2 = ("Hello World).split(" ")

print(variavel1)# Output: Hello
print(variavel2)# Output: World
```

## Funções Matemáticas

+ Round

> [!IMPORTANT]
> Tem como Função arredondar um número como parametro o número de casas decimais.

```python
print(round(3.1415, 2))
# Output: 3.14
```

## Funções

> [!NOTE]
> Para criar uma função em python usa- se a palavra-chave **def** seguida dos seus parametros

```python
def nomeFuncao(parametros)
    # Bloco de Código
```

```python
def hello()
    print("Hello World")

hello() # Output: Hello World
```
