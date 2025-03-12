## Pasta: minhasoperacoes/

# minhasoperacoes/__init__.py
__all__ = ["operacoes", "utils"]

# minhasoperacoes/operacoes.py
def soma(a, b):
    return a + b

def subtracao(a, b):
    return a - b

def multiplicacao(a, b):
    return a * b

def divisao(a, b):
    if b == 0:
        return "Erro: divisão por zero."
    return a / b

# minhasoperacoes/utils.py
def exibir_resultado(operacao, resultado):
    print(f"Resultado da {operacao}: {resultado}")

## Arquivo principal: main.py
from minhasoperacoes import operacoes, utils

op = input("Escolha uma operação (+, -, *, /): ")
num1 = float(input("Digite o primeiro número: "))
num2 = float(input("Digite o segundo número: "))

if op == "+":
    resultado = operacoes.soma(num1, num2)
    utils.exibir_resultado("soma", resultado)
elif op == "-":
    resultado = operacoes.subtracao(num1, num2)
    utils.exibir_resultado("subtração", resultado)
elif op == "*":
    resultado = operacoes.multiplicacao(num1, num2)
    utils.exibir_resultado("multiplicação", resultado)
elif op == "/":
    resultado = operacoes.divisao(num1, num2)
    utils.exibir_resultado("divisão", resultado)
else:
    print("Operação inválida.")

## Exercícios de Linguagem de Programação

# Exercício 1: If e If-Else em Python
def verifica_numero(n):
    if n > 0:
        print("Número positivo")
    elif n < 0:
        print("Número negativo")
    else:
        print("Zero")

n = int(input("Digite um número: "))
verifica_numero(n)

# Exercício 1: If e If-Else em C
c_code_if = '''
#include <stdio.h>
int main() {
    int n;
    printf("Digite um número: ");
    scanf("%d", &n);
    if (n > 0) {
        printf("Número positivo\n");
    } else if (n < 0) {
        printf("Número negativo\n");
    } else {
        printf("Zero\n");
    }
    return 0;
}
'''

# Exercício 2: Loops em Python
i = 0
while i < 5:
    print(f"While Loop: {i}")
    i += 1

for i in range(5):
    print(f"For Loop: {i}")

# Exercício 2: Loops em C
do_while_c = '''
#include <stdio.h>
int main() {
    int i = 0;
    do {
        printf("Do-While Loop: %d\n", i);
        i++;
    } while (i < 5);
    return 0;
}
'''

for_loop_c = '''
#include <stdio.h>
int main() {
    for (int i = 0; i < 5; i++) {
        printf("For Loop: %d\n", i);
    }
    return 0;
}
'''

print("Código C If-Else:\n", c_code_if)
print("Código C Do-While:\n", do_while_c)
print("Código C For:\n", for_loop_c)
