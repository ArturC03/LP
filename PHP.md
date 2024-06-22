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

### Para apresentar texto e trocar de linha usar **\n**:

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

+ **+** → Soma
+ **-** → Subtração
+ __*__ → Multiplicação
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
> Para fazer **referência** às **variáveis da estrutura**/**atributos**, usar **->** e o nome da variável da estrutura.

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

## PHP na Web

### Incorporando PHP no HTML

É possível incorporar código PHP diretamente em ficheiros HTML para criar conteúdo dinâmico. Isso é feito utilizando tags especiais como `<?php ?>`.

Exemplo simples de página HTML com PHP:

```php
<!DOCTYPE html>
<html>
<head>
    <title>Página PHP</title>
</head>
<body>
    <h1>Olá, <?php echo "visitante"; ?>!</h1>
    <p>A data atual é <?php echo date('d/m/Y'); ?>.</p>
</body>
</html>
```

### Trabalhar com HTML

PHP é frequentemente usado para processar dados de formulários HTML. Aqui está um exemplo básico de como lidar com um formulário simples:

```php
<!DOCTYPE html>
<html>
<head>
    <title>Formulário PHP</title>
</head>
<body>
    <form method="post" action="processar.php">
        Nome: <input type="text" name="nome"><br>
        E-mail: <input type="text" name="email"><br>
        <input type="submit" value="Enviar">
    </form>
</body>
</html>
```

No arquivo `processar.php`, é possível recuperar os dados do formulário assim:

```php
<?php
$nome = $_POST['nome'];
$email = $_POST['email'];

echo "Nome: $nome<br>";
echo "E-mail: $email";
?>
```

### Gerenciando Sessões e Cookies

PHP permite gerenciar sessões de utilizadores e cookies para manter o estado entre as páginas. Exemplo básico de uso de sessões:

```php
<?php
session_start();

$_SESSION['usuario'] = "Artur";

echo "Bem-vindo, " . $_SESSION['usuario'];
?>
```

### Conexão com a Base de Dados

Em PHP pode-se conectar a banses de dados para armazenar e recuperar informações. Exemplo básico de conexão com MySQL:

```php
<?php
$servername = "localhost";
$username = "username";
$password = "password";
$dbname = "nome_database";

// Criar conexão
$conn = new mysqli($servername, $username, $password, $dbname);

// Verificar conexão
if ($conn->connect_error) {
  die("Conexão falhou: " . $conn->connect_error);
}

echo "Conectado com sucesso!";
?>
```

### Manipulação de ficheiros

PHP é eficiente para manipulação de ficheiros no servidor. Exemplo de leitura de um ficheiros de texto:

```php
<?php
$file = fopen("exemplo.txt", "r") or die("Não foi possível abrir o arquivo!");

// Ler e exibir o conteúdo linha por linha
while(!feof($file)) {
  echo fgets($file) . "<br>";
}

fclose($file);
?>
```

### Bibliotecas e Frameworks

Existem diversas bibliotecas e frameworks em PHP que facilitam o desenvolvimento web, como:

- **Laravel**: Um framework PHP robusto e elegante para desenvolvimento ágil de aplicações web.
- **Symfony**: Um conjunto de componentes PHP reutilizáveis e um framework de aplicação web.
- **CodeIgniter**: Um framework PHP poderoso e leve, com uma curva de aprendizado pequena.
- **Zend Framework**: Um framework PHP orientado a objetos e de código aberto.
- **Slim**: Um micro-framework PHP para construção de APIs e aplicações web simples e poderosas.

### Segurança

É fundamental considerar a segurança ao desenvolver aplicações web com PHP. Algumas práticas comuns incluem:

- Validar e filtrar todas as entradas do usuário.
- Evitar consultas SQL diretamente concatenadas com dados do usuário.
- Usar funções de hash seguras para senhas, como `password_hash()` e `password_verify()`.
- Manter todas as bibliotecas e frameworks atualizados com as últimas versões de segurança.

### Depuração e Logging

Para facilitar o desenvolvimento e depuração de aplicações PHP, é importante usar técnicas de logging e depuração eficazes, como:

- Usar funções de logging como `error_log()` para registrar mensagens de erro.
- Habilitar e configurar o display de erros no ambiente de desenvolvimento (`display_errors` no php.ini).
- Usar ferramentas de debuggers como Xdebug para rastreamento de código e inspeção de variáveis.

### Hospedagem e Implantação

Ao implantar aplicações PHP, considere as melhores práticas de hospedagem:

- Escolher um provedor de hospedagem que suporte as versões mais recentes do PHP e tenha boa reputação de uptime.
- Configurar corretamente as permissões de arquivo e diretório para garantir a segurança.
- Implementar um sistema robusto de backup e recuperação de dados para proteger contra perda de dados.

***

© Artur Cruz
