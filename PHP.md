# PHP - Instruções básicas

## Comentários
> [!NOTE]
> Para inicializar **comentários** de apenas uma linha usar os caracteres **//** ou **#**.

### Exemplo:

```php
// Isto é um comentário
# Isto também é um comentário
```

> [!NOTE]
> Para criar um comentário que ocupe mais de uma linha, use **/*** para iniciar e ***/** para terminar.

### Exemplo:

```php
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

```php
echo "<texto>";
```

### Para apresentar texto e trocar de linha usar **/n**:

```php
echo "<texto>\n";
```

### Para apresentar texto e variável:

+ Para strings:

```php
$var = "mundo";
echo "Hello, $var\n";
// Output: Hello, mundo
```

+ Para inteiros:

```php
$var = 42;
echo "Número: $var\n";
// Output: Número: 42
```

+ Para floats:

```php
$var = 3.14;
echo "Valor: $var\n";
// Output: Valor: 3.14
```

> [!WARNING]
> Para números reais, ao usar um ponto seguido de um número, pode ser especificada a quantidade de casas decimais desejadas.

#### Exemplo:

```php
$pi = 3.14159;
echo number_format($pi, 2); // Output: 3.14
```

***

## Variáveis/Constantes

### Sintaxe

```php
$tipo = "valor";
```

### Exemplo:

```php
$var = "Hello World";
```

### Constantes

> [!NOTE]
> Utilizar **define** para definir uma constante.

#### Sintaxe:

```php
define("NOME_CONSTANTE", "valor");
```

#### Exemplo:

```php
define("PI", 3.14159);
```

***

## Operadores Aritméticos

+ **+_** → Soma
+ **-_** → Subtração
+ ***_** → Multiplicação
+ **/** → Divisão
+ **%** → Resto

***

## Atribuições

+ **=** → Atribuição simples
+ **+=** → Incrementação
+ **-=** → Decrementação
+ **++** → Incrementação de 1
+ **--** → Decrementação de 1

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

### **If**

```php
if (<condição1>) {
    // bloco de código
} elseif (<condição2>) {
    // bloco de código
} else {
    // bloco de código
}
```

#### Exemplo:

```php
if ($cookie == 3) {
    echo "Há 3 cookies.";
} elseif ($cookie > 0) {
    echo "Há $cookie cookies.";
} else {
    echo "Não há mais cookies.";
}
```

### **Switch**

```php
switch (<expressão>) {
    case <valor1>:
        // bloco de código
        break;
    case <valor2>:
        // bloco de código
        break;
    default:
        // bloco de código a executar se nenhum dos valores acima for o resultado da <expressão>
        break;
}
```

***

## Estruturas de Repetição

### **For Loop**

> [!WARNING]
> Para sair de qualquer um dos loops de forma inesperada, utilizar a instrução **break;**

```php
for (<inicialização>; <condição>; <incremento/decremento>) {
    // bloco de instruções
}
```

#### Exemplo:

```php
for ($i = 0; $i < 10; $i++) {
    echo "$i\n";
}
```

### **While Loop**

```php
while (<condição>) {
    // bloco de instruções
}
```

#### Exemplo:

```php
while ($i > 0) {
    echo "$i\n";
    $i--;
}
```

### **Do While Loop**

```php
do {
    // bloco de instruções
} while (<condição>);
```

#### Exemplo:

```php
do {
    echo "$i\n";
    $i--;
} while ($i > 0);
```

***

## Funções

> [!WARNING]
> Utilizar a instrução **function** para definir funções em PHP.

```php
function <nome>(<parâmetros>) {
    // bloco de código
    return <valor_de_retorno>; // Return é opcional
}
```

#### Exemplo:

```php
function soma($a, $b) {
    return $a + $b;
}
```

#### Exemplo sem tipo ou argumentos:

```php
function saudacao() {
    echo "Olá!";
}
```

> [!TIP]
> Para a função **main**, é possível usar dois parâmetros: **argc** e **argv**, que respectivamente indicam a quantidade total de argumentos fornecidos pelo utilizador e um array desses argumentos.

Exemplo:

```php
// nome de ficheiro exemplo.php
$argc = $argc;
$argv = $argv;

if ($argc == 2) {
    echo "Hello, " . $argv[1] . "\n";
} else {
    echo "Hello, world\n";
}

/* Exemplo de Prompt:
php exemplo.php Artur
Hello, Artur
*/

/* Exemplo de Prompt:
php exemplo.php
Hello, world
*/
```

> [!IMPORTANT]
> Utilizar a instrução **return** para sair do programa de forma prematura. Números diferentes de 0 são usados em caso de erro para que o utilizador possa identificar o problema.

***

## Arrays

### Sintaxe de Declaração:

```php
$array = array();
```

#### Exemplo

```php
$array = array(1, 2, 3, 4, 5);
// Isto cria um array com 5 posições
```

### Para fazer referência à posição:

```php
$array[posicao] = valor;
```

#### Exemplo:

```php
$array[3] = 5;
// Isto atribui 5 à posição 3 do array
```

***

## Estruturas (Classes em POO)

### Sintaxe:

```php
class NomeEstrutura {
    public $atributo1;
    public $atributo2;
    // ...
}
```

### Exemplo:

```php
class Pessoa {
    public $nome;
    public $numero;
}
```

> [!IMPORTANT]
> Para fazer **referência** às **variáveis da estrutura**, usar **->** e o nome da variável da estrutura.

#### Exemplo:

```php
$pessoa = new Pessoa();
$pessoa->nome = "Artur";
echo $pessoa->nome; // Output: Artur
```

***

## Bibliotecas
> [!NOTE]
> Para incluir novas bibliotecas em PHP, usa-se **require** ou **include**.

```php
require 'nome_biblioteca.php';
include 'nome_biblioteca.php';
```

+ **stdio.php** para input e output (implementação própria)
+ **math.php** para funções matemáticas, exemplo: round para arredondar (implementação própria)
+ **string.php** para manipulação de strings (implementação própria)

***

## Formas de compilar

```bash
php nomeFicheiro.php
```

***

© Artur Cruz
