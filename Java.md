Claro! Aqui está a versão em Markdown das instruções fornecidas, adaptada para Java e em Português de Portugal:

```markdown
# Java - Instruções

## Declaração de Variáveis/Constantes

### **Variáveis**

```java
<Tipo> <nome_variavel>;
```

#### Exemplo

```java
int cookie;
```

### **Constantes**

```java
final <Tipo> <nome_constante> = <valor>;
```

#### Exemplo

```java
final int pi = 3.1415926536;
```

---

## Tipos de Variáveis

1. **Inteiro**

```java
int inteiro = 3; // Guarda valores inteiros
```

2. **Double**

```java
double duplo = 3.14; // Guarda valores com duas casas decimais
```

3. **String**

```java
String corda = "Hello World"; // Guarda cadeias de caracteres
```

4. **Char**

```java
char carater = 'C'; // Guarda caracteres
```

5. **Booleano**

```java
boolean booliano = true; // Guarda valores booleanos
```

6. **Outros**

- Decimal
- Float
- Byte
- Short
- Long
- Date
- TimeSpan

---

## Leitura de Dados - Input

### **Para Strings e Caracteres**

```java
<variavel> = System.console().readLine(); // Lê o input
```

#### Exemplo

```java
cookie = System.console().readLine(); // Lê o input e Troca de Linha
```

### **Para Outros Tipos**

```java
<variavel> = <tipo_variavel>.parse<tipo_variavel>(System.console().readLine()); // Lê o input
```

#### Exemplo

```java
cookie = Integer.parseInt(System.console().readLine()); // Lê o input e Troca de Linha
```

---

## Escrita no Ecrã

### **Apenas Cadeia de Caracteres**

```java
System.out.println("<texto>");
```

#### Exemplo

```java
System.out.println("Olá");
```

### **Apenas uma Variável**

```java
System.out.println(<variável>);
```

#### Exemplo

```java
System.out.println(cookie);
```

### **Cadeia de Caracteres e Variável**

```java
System.out.println("<texto> " + <variável>);
```

#### Exemplo

```java
System.out.println("Cookies: " + cookie);
```

---

## Operadores Aritméticos

- **+** → Soma
- **-** → Subtração
- **\*** → Multiplicação
- **/** → Divisão Real
- **%** → Resto da Divisão
- **//** → Divisão Inteira

---

## Operadores Relacionais

- **==** → Igualdade
- **!=** → Diferença
- **>** → Maior Que
- **<** → Menor Que
- **>=** → Maior ou Igual
- **<=** → Menor ou Igual

---

## Operadores Lógicos

- **&&** → E
- **||** → OU
- **!** → Negação

---

## Atribuições

- **=** → Atribuição Simples
- **+=** → Incremento
- **-=** → Decremento
- **\*=** → Multiplicação
- **/=** → Divisão
- **%=** → Resto

---

## Estruturas Condicionais

### **If**

```java
if (<condição1>) {
    // bloco de código
} else if (<condição2>) {
    // bloco de código
} else {
    // bloco de código
}
```

#### Exemplo

```java
if (cookie == 3) {
    System.out.println("Há 3 cookies.");
} else if (cookie > 0) {
    System.out.println("Há " + cookie + " cookies");
} else {
    System.out.println("Não há mais cookies.");
}
```

### **Switch**

```java
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

---

## Estruturas de Repetição

### **For Loop**

```java
for (<inicialização>; <condição>; incremento/decremento) {
    // bloco de instruções
}
```

#### Exemplo

```java
for (int i = 0; i < 10; i++) {
    System.out.println(i);
}
```

### **While Loop**

```java
while (<condição>) {
    // bloco de instruções
}
```

#### Exemplo

```java
while (i > 0) {
    System.out.println(i);
    i--;
}
```

### **Do While Loop**

```java
do {
    // bloco de instruções
} while (<condição>);
```

#### Exemplo

```java
do {
    System.out.println(i);
    i--;
} while (i > 0);
```

---

## Tratamento de Exceções - Try Catch

```java
try {
    // bloco de código para detectar erro
} catch (Exception ex) {
    // bloco de código para tratar erro
}
```

---

© Artur Cruz
```


