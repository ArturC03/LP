# Memória

## Pointer

Variável que guarda a localização(byte) de um valor na memoria

***

## Endereços em C

Para escreveer no ecrã um pointer usar **%p**

```C
printf("%p", pointer);
```

& → Endereço de uma Variável

```C
int cookie = 3.14;
print("%p", &cookie);
//Output: 0x123 
//Exemplo de onde cookie pode estar na memoria
```

Se quiseres guardar uma localização numa variavel tens de dizer ao programa que vais guardar uma localização com o símbolo __*__

__*__ (Numa Declaração) → Apontador

```C
int *<pointer> = &<var>
```

Nesta declaração o __*__ ao lado do nome da variavel significa que aquela variavel vai ser um **apontador** para uma variável do **tipo integer**.

__*__ → Mostrar valor contido numa localização

Se for usado **fora** de uma Declaração, o __*__ significa "O que se encontra no endereço do apontador".

```C
int cookie = 5
int *pointer = &cookie // atribuir a localização de cookie ao pointer

printf("%p",pointer ); //Mostra localização de cookie
printf("%i",*pointer ); //Mostra Valor de cookie
```
