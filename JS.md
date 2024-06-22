# JavaScript - Instruções para Desenvolvimento Web

## Declaração de Variáveis/Constantes

### **Variáveis**

```javascript
let <nome_variavel>;
```

#### Exemplo

```javascript
let cookie;
```

### **Constantes**

```javascript
const <nome_constante> = <valor>;
```

#### Exemplo

```javascript
const pi = 3.1415926536;
```

---

## Tipos de Variáveis

1. **Número**

```javascript
let inteiro = 3; // Guarda valores inteiros
let duplo = 3.14; // Guarda valores com ponto flutuante
```

2. **String**

```javascript
let corda = "Hello World"; // Guarda cadeias de caracteres
```

3. **Booleano**

```javascript
let booliano = true; // Guarda valores booleanos
```

4. **Outros**

- Array
- Object
- Function

---

## Estruturas de Controlo

### **Condição If**

```javascript
if (<condição>) {
    // bloco de código se a condição for verdadeira
} else if (<outra_condição>) {
    // bloco de código se a outra condição for verdadeira
} else {
    // bloco de código se nenhuma das condições anteriores for verdadeira
}
```

#### Exemplo

```javascript
if (cookie === 3) {
    console.log("Há 3 cookies.");
} else if (cookie > 0) {
    console.log(`Há ${cookie} cookies`);
} else {
    console.log("Não há mais cookies.");
}
```

### **Switch**

```javascript
switch (<expressão>) {
    case <valor1>:
        // bloco de código se expressão for igual a valor1
        break;
    case <valor2>:
        // bloco de código se expressão for igual a valor2
        break;
    default:
        // bloco de código se nenhuma das expressões anteriores for verdadeira
        break;
}
```

#### Exemplo

```javascript
switch (day) {
    case 1:
        console.log("Segunda-feira");
        break;
    case 2:
        console.log("Terça-feira");
        break;
    default:
        console.log("Outro dia da semana");
        break;
}
```

---

## Estruturas de Repetição

### **Loop For**

```javascript
for (let i = 0; i < limite; i++) {
    // bloco de código a repetir enquanto a condição for verdadeira
}
```

#### Exemplo

```javascript
for (let i = 0; i < 10; i++) {
    console.log(i);
}
```

### **Loop While**

```javascript
while (<condição>) {
    // bloco de código a repetir enquanto a condição for verdadeira
}
```

#### Exemplo

```javascript
let i = 0;
while (i < 10) {
    console.log(i);
    i++;
}
```

### **Loop Do-While**

```javascript
do {
    // bloco de código a executar pelo menos uma vez e repetir enquanto a condição for verdadeira
} while (<condição>);
```

#### Exemplo

```javascript
let i = 0;
do {
    console.log(i);
    i++;
} while (i < 10);
```

---

## Tratamento de Exceções - Try Catch

```javascript
try {
    // bloco de código para detetar erro
} catch (error) {
    // bloco de código para tratar erro
}
```

---

## Leitura de Dados (de um ficheiro HTML)

### **Utilizando Elementos do Formulário**

```javascript
document.getElementById('<id_elemento>').value;
```

#### Exemplo

```javascript
let username = document.getElementById('username').value;
```

---

## Escrita na Página HTML

### **Output para HTML**

```javascript
document.getElementById('<id_elemento>').innerHTML = "<texto>";
```

#### Exemplo

```javascript
document.getElementById('result').innerHTML = "Olá";
```

---

## Manipulação do DOM em JavaScript

### **Selecionar Elementos**

```javascript
document.querySelector('<seletor>');
```

#### Exemplo

```javascript
document.querySelector('.btn');
```

### **Gestão de Eventos**

```javascript
document.getElementById('<id_elemento>').addEventListener('click', function() {
    // bloco de código a executar quando o elemento é clicado
});
```

#### Exemplo

```javascript
document.getElementById('submitBtn').addEventListener('click', function() {
    // código para processar o formulário
});
```

---


## JavaScript Assíncrono (AJAX/Fetch)

### **A utilizar Fetch API**

```javascript
fetch('<url>')
    .then(response => response.json())
    .then(data => {
        // código para lidar com os dados recebidos
    })
    .catch(error => {
        // código para lidar com erros
    });
```

#### Exemplo

```javascript
fetch('https://api.exemplo.com/dados')
    .then(response => response.json())
    .then(data => {
        console.log(data);
    })
    .catch(error => {
        console.error('Erro ao buscar dados:', error);
    });
```

---

© Artur Cruz
