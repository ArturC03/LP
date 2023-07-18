# Ruby - Instruções Básicas

## Comentários

Para inicializar **Comentários** de apenas uma linha usar o carater **#**.

### Exemplo

```Ruby
#Isto é um Comentário
```

Para criar Um Comentário que preencha mais do que uma linha escrever **=begin** para começar e **=end** para terminar.

### Exemplo:

```Ruby
=begin
    Este comentário está:
    a ocupar
    mais do que
    uma linha
=end 
```

***

## Variáveis

Em Ruby variáveis devem ser inicializadas com uma **letra minúscula**.

### Exemplo:

```Ruby
variavel = 6
```

***

## Constantes

Em Ruby Constantes são todas as variáveis que são inicializadas com uma letra **maiúscula** se for tentado reatribuir um valor a uma constante Ruby vai dar um **aviso** de que a Constante já foi inicializada.

```Ruby
Constante = 'Olá'
```

***

## Escrita no Ecrã

### Print

A Instrução **print** apresenta texto no ecrã sem trocar de linha.

#### Exemplo: 

```Ruby
print '<text>'
```

### Puts

A Instrução **puts** apresenta texto no ecrã e muda de linha.

#### Exemplo:

```Ruby
puts '<text>'
```

#### P.S:

Em ruby, para mostrar uma variavel usa- se o carater _**#**_ seguido no nome da variável entre **{}**

```Ruby
puts 'Variável: #{variavel}'
```

***

## Operadores Aritméticos

+ **+** → Soma

+ **-** → Subtração

+ **_*_** → Multiplicação

+ **/** → Divisão

+ **%** → Resto

+ ** → Expoente

_Aviso_:Ruby **respeita as prioridades da matemática** nas suas expressões aritméticas 

***

## Atribuições

### Tipos de Atribuições

+ **+=** → Soma

+ **-=** → Subtração

+ **_*=_** → Multiplicação

+ **/=** → Divisão

+ **%=** → Resto

+ ****=** → Expoente

### Atribuições Paralelas

Ruby também contém **atribuições paralelas**, que em outras palavras são atribuições executadas na **mesma linha de código**.

```Ruby
var, var1, var2 = 1, 2, 3
```

***

## Strings

Em Ruby é possível pôr um **'**
 no meio do texto, desde que esteja anteposto por uma \,  mesmo que o string esteja entre ' '.

```Ruby
 puts 'Theres\' s cookies in the jar'. 
 #Output: There's cookies in the jar
```

Em ruby, é possível trocar de linha a meio de um string se a string tiver um **\n** a meio da string.

```Ruby
puts '\nHello\nWorld'
#Output:
#Hello
#World
```

***

## Leitura de Dados - Input

Para Receber dados ruby utiliza a instrução **gets**, que recebe o input e cria uma nova linha.

```Ruby
variavel = gets
```

Se a criação de uma nova linha na instrução gets for indesejada pode ser usado o método chomp para excluir essa parte da instrução

```Ruby
variavel = gets.chomp
```

***

## Operadores Relacionais

+ **==** → Igualdade

+ **!=** → Diferença

+ **>** → Maior Que

+ **<** → Menor Que

+ **>=** → Maior ou Igual

+ **<=** → Menor ou Igual

Também pode ser usado o método **eql?** que só tem output **True** se os argumentos forem do mesmo _tipo_ e _iguais_.

```Ruby
puts 3.eql?(3.0)
#Output: False
```

***

## Estruturas Condicionais

### If

```Ruby
if num == 3
  
  #Bloco de Código

elsif num == 10

  #Bloco de Código
else

  #bloco de código

end
```

### Unless

Unless é uma **estrutura condicional** que funciona exatamente ao **contrário** da estrutura **If**, ou seja, só é executada se o resultado da condição for falsa

```Ruby
unless i==0

  puts 'aa'

else

  puts 'bb'

end
```

```Ruby
var = 4
puts "Não" unless var != 4
#Output: Não
```

### Case

```Ruby
case var
when 5
    #bloco de código

when 9, 10, 45
    #bloco de código
    
when !6
    #bloco de código
    
when 3
    #bloco de código
end
```

***

## Operadores Lógicos

+ **&&** → E

+ **||** → OU

+ **!** → Negação

***

## Intervalos - Ranges

Um Intervalo(Range) é uma sequência que pode ser numérica ou alfabética.<br>

Em Ruby, há dois operadores para ranges ( .. e ... ) que dependendo do utilizado o intevalo vai incluir os limites do intervalo, outro vai excluir.

Um intervalo pode ser convertido num **array(vetor)** com o método **to_a**.

```Ruby
puts (1..7).to_a  # (..) inclui os limites do intervalo.
#Output:
[1, 2, 3, 4, 5, 6, 7]

puts (a...d).to_a  # (...) exclui os limites do intervalo.
#Output:
['a','b','c',]
```

***

## Loops

### While

```Ruby
x = 0
while x < 10
    #bloco de código
end
```

### For

```ruby
for i in (i..10)
    #bloco de código
end
```

### Do

```Ruby
loop do
    #Bloco de Código
    break if i < 3
end
```

### Break e Next

Estas instruções são utlizadas no meio de um loop.

**Break** Força a **saída** de um **loop**.

<br>

<br>

**Next** pula uma parte do código e vai para o **próximo**.
***

## Vetores - Arrays Unidimensionais

Em Ruby, um vetor **não precisa ser declarado** com a sua posição, mas **precisa ser atribuído**.

```Ruby
array = []
```

Os Arrays no Ruby **não têm tipo definido** por isso podem conter **vários tipos** de variável.

```Ruby
array = [1, "hello", true]
```

Para criar um Array com **posições definidas mas vazias** usa- se o método **Array.new(<_numero_posições_>)**.

```Ruby
array = Array.new(5)
```

Para **Adicionar** novos elementos num vetor pode ser usado o método **push**,o operador **<<**, o método **concat** ou o operador **+**.

+ **Push**

```Ruby
vet = []
vet.push(1)
vet.push("hello")
vet.push(true)
puts vet
#Output: [1,"hello",true]
```

+ **<<**

```Ruby
vet = []
vet << 1
vet << "hello"
vet << true
puts vet
#Output: [1,"hello",true]
```

+ **Concat**

```Ruby
vet = []
vet.concat([1,"hello",true])
puts vet
#Output: [1,"hello",true]
```

+ **+**

```Ruby
vet = []
vet += [1,"hello",true]
puts vet
#Output: [1,"hello",true]
```

Para Trocar o valor de uma posição do array atribui- se um valor ao array fazendo- se referência à posição.

```Ruby
array = [1, 2, 3]
array[1] = "hello"
puts array
#Output: [1,"hello",3]
```

***

## Tratamento de vetores

1. length ou size: Retorna o **tamanho** do array.

```Ruby
array = [1, 2, 3, 4, 5]
puts array.length  # Output: 5
```

2. empty?: **Verifica** se o array está **vazio**.

```Ruby
array = []
puts array.empty?  # Output: true
```

1. include?: Verifica se um **elemento está presente no array**.

```Ruby
array = [1, 2, 3]
puts array.include?(2)  # Output: true
puts array.include?(4)  # Output: false
```

1. push ou <<: **Adiciona** um elemento ao final do array.

```Ruby
array = [1, 2, 3]
array.push(4)
array << 5
puts array.inspect  # Output: [1, 2, 3, 4, 5]
```

1. pop: **Remove e retorna** o **último** elemento do array.

```Ruby
array = [1, 2, 3, 4, 5]
last_element = array.pop
puts last_element  # Output: 5
puts array.inspect  # Output: [1, 2, 3, 4]
```

1. shift: **Remove e retorna** o **primeiro** elemento do array.

```Ruby
array = [1, 2, 3, 4, 5]
first_element = array.shift
puts first_element  # Output: 1
puts array.inspect  # Output: [2, 3, 4, 5]
```

1. unshift: **Adiciona** um elemento no **início** do array.

```Ruby
array = [2, 3, 4, 5]
array.unshift(1)
puts array.inspect  # Output: [1, 2, 3, 4, 5]
```

1. uniq: **Retorna** um novo array **removendo elementos duplicados**.

```Ruby
array = [1, 2, 2, 3, 3, 4, 5]
unique_array = array.uniq
puts unique_array.inspect  # Output: [1, 2, 3, 4, 5]
```

Essas são apenas algumas das **funções** e **métodos** de **tratamento de arrays** em **Ruby**. Existem muitos outros disponíveis, incluindo sort, reverse, select, map, delete, entre outros. A  [documentação oficial do Ruby](https://ruby-doc.org/core-3.0.2/Array.html) é uma ótima fonte para explorar todas as funcionalidades do tratamento de arrays em Ruby.

***

## Tratamento de Exceções

Em **Ruby**, pode- se usar o bloco **begin-rescue-ensure** para lidar com **exceções** e **capturar erros**. Aqui está a sintaxe básica do bloco begin-rescue-ensure:

```Ruby
begin
  # Código que pode gerar uma exceção
rescue ExceptionType => variavel
  # Código para lidar com a exceção
ensure
  # Código a ser executado independentemente de haver uma exceção ou não
end
```

Exemplo:

```Ruby
begin
  file = File.open("arquivo.txt", "r")
  content = file.read
  puts content
rescue Errno::ENOENT => e
  puts "O arquivo não existe."
ensure
  file.close if file
end
```

***

## Funções e Métodos

Em Ruby,pode- se criar funções e métodos usando a palavra-chave def. Aqui está a sintaxe básica para criar uma função ou método em Ruby:

```ruby
def nome_da_funcao(parametro1, parametro2, ...)
  # Corpo da função
  # Código a ser executado
  # Pode haver um retorno       opcional usando a palavra-chave 'return'
  return <valor_de_retorno>
end
```

Por **exemplo**, vamos criar uma função simples chamada saudacao que recebe um nome como parâmetro e imprime uma saudação:

```Ruby
def saudacao(nome)
  puts "Olá, #{nome}! Como você está?"
end

# Chamando a função
saudacao("João")  # Output: Olá, João! Como você está?
```

***

## Bibliotecas 

&nbsp;&nbsp;&nbsp;&nbsp;Em **Ruby**, as bibliotecas são chamadas de **"gems"** (gerenciador de pacotes RubyGems) e são pacotes que contêm código **reutilizável** que pode ser adicionado a um projeto **Ruby** para adicionar funcionalidades extras. As gems podem ser **desenvolvidas pela comunidade Ruby** ou por **terceiros** e fornecem uma ampla gama de recursos e funcionalidades prontas para uso.

<br>

&nbsp;&nbsp;&nbsp;&nbsp;Uso de **Gems** em 
um Projeto Ruby: Para usar uma gem em um projeto Ruby, você precisa primeiro requerer **(require)** a gem no arquivo onde deseja usá-la.

```Ruby
require <Gem>
```

Exemplo de utilização: 

```Ruby
require nokogiri
```

***

<span style="color:white;font-size:1cm;">
© Artur Cruz
</span>