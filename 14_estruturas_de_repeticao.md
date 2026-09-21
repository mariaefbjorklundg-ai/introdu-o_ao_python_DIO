## Estruturas de Repetição
São utilizadas para repetir um trecho do código em determinado número de vezes. 

Esse número conhecido previamente ou determinado através de uma expressão lógica

Exemplo sem repetição
```Python
# vai receber um número do teclado e exibir os 2 números seguidos

a = int(input("Informe um número inteiro: ")) 
print(a) #se for 4
>>> 4

a += 1 
print(a)
>>> 5

a += 1
print(a)
>>> 6
```
### Comando for
É usado para percorrer um objetivo iterável. 

Usamos quando sabemos o número exato de vezes que nosso bloco de código deve ser executado, ou quando queremos percorrer um objetivo iterável. 

#### For
```Python
texto = input("Informe um texto: ")
VOGAIS = "AEIOU"

for letra in texto:
    if letra.upper() in VOGAIS:
        print(letra, end="") #palavra: riqueza
>>> iuea
print() #adicionar uma quebra de linha
```
### Função Range
É uma função built-in do Python, é usada para produzir uma sequência de números inteiros a partir de um ínicio (incluso) para um fim (exclusivo).

Se usarmos range(i.j) será produzido: i, i+1, i+2, i+3, ..., j+1.

Ela recebe 3 argumentos: stop (obrigatório), start (opcional) e step opcional
Exemplo:
```Python
resultado = list(range(4))
print(resultado)
>>> [0, 1, 2, 3]

# Utilizando range com for

for numero in range(0, 11):
    print(numero, end=" ")
>>> 0 1 2 3 4 5 6 7 8 9 10

# Exibindo a tabuada do 5
for numero in range(0, 51, 5): # o 0 seria o start, o 51 o stop, e o 5 step
    print(numero, end=" ")
>>> 0 5 10 15 20 25 30 35 40 45 50
```
### Comando While
É usado para repetir um bloco de código várias vezes. 

Usamos o **While** quando não sabemos o número exato de vezes que nosso código deve ser executado.
Exemplo:
```Python
opcao = -1

while opcao != 0:
    opcao = int(input("[1] Sacar \n[2] Extrato \n[0] Sair \n: ")) #vai repetir as opções até digitar o 0 para sair 

    if opcao == 1:
        print("Sacando...")
    elif opcao == 2:
        print("Exibindo o extrato...")

# While/else
#não é muito utilizado o else

opcao = -1

while opcao != 0:
    opcao = int(input("[1] Sacar \n[2] Extrato \n[0] Sair \n: "))

    if opcao == 1:
        print("Sacando...")
    elif opcao == 2:
        print("Exibindo o extrato...")
else:
    print("Obrigada por usar nosso sistema, até logo!")
```
### Comando Break
Ele corta a execussão
Exemplo:
```Python
while True:
    numero = int(input("Informe um número: ")) #ele para quando o numero for 10

    if numero == 10:
        break

    print(numero)

# for com break
for numero in range(100):

    if numero == 10:
        break

    print(numero, end=" ")
>>> 0 1 2 3 4 5 6 7 8 9

# temos tambem o continue, que pula a condição
for numero in range(20):

    if numero == 10:
        continue

    print(numero, end=" ")
>>> 0 1 2 3 4 5 6 7 8 9 11 12 13 14 15 16 17 18 19  #pulou o 10

#só numeros impares
for numero in range(20):

    if numero % 2 == 0:
        continue

    print(numero, end=" ")
>>> 1 3 5 7 9 11 13 15 17 19 
