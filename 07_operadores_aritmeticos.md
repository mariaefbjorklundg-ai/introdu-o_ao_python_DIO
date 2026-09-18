## Operadores Aritméticos 🟰
Eles executam operações matemáticas, como subtração, adição com operadores.
* Adição, subtração e multiplicação
```Python
# Adição
print(9 + 5)
>>> 14

# Subtração
print(45 - 23)
>>> 22

# Multiplicação
print(6 * 8)
>>> 48
```

* Divisão e divisão inteira
```Python
# Divisão
print(48 / 8)
>>> 6.0

# Divisão Inteira
print(48 // 8)
>>> 6
```

* Módulo e exponenciação
```Python
# Módulo
# O símbolo % não calcula porcentagem!
# Ele calcula o que SOBRA de uma divisão inteira (sem usar casas decimais).

# 10 dividido por 3 dá 3 para cada um (3 x 3 = 9) e sobra 1.
print(10 % 3)  
>>> 1 # Saída: 1 (é a sobra)

# 20 dividido por 3 dá 6 para cada um (3 x 6 = 18) e sobram 2.
print(20 % 3)
>>> 2  # Saída: 2 (é a sobra)

(Muito comum na prática: Saber se é Par ou Ímpar):
# Se dividir por 2 e a sobra for 0, o número é PAR.
# Se a sobra for 1, o número é ÍMPAR.
print(8 % 2)
>>> 0  # Saída: 0 -> Par (cabe certinho, sobra zero)

print(9 % 2) 
>>> 1  # Saída: 1 -> Ímpar (sobra 1)

# Exponenciação
# O operador ** significa "elevado a".
# Regra: base ** expoente (multiplica a base por ela mesma X vezes).

print(2 ** 3)
>>> 8

print(3 ** 4)
>>> 81
```
### Precedência de Operadores
Existe uma regra na matemática que indica quais operações devem ser executadas primeiro, por isso a depender da ordem das operações o valor pode ser diferente:

x = 20 - 5 * 2 

x = 10 

Mas dependendo da ordem o resultado pode ser 30, por isso tem a ordem correta:
* Parêntesis
* Expoêntes
* Multiplicações e divisões (da esquerda para a direita)
* Somas e subtrações (da esquerda para a direita)

Exemplo:
```Python
print(20 - 5 * 2)
>>> 10

print((20 - 5) * 2)
>>> 30

print(20 ** 2 * 2)
>>> 800

print(20 ** (2 * 2))
>>> 160000

print (20 / 2 * 4)
>>> 40.0
```

Exemplo na prática:
```Python
produto_1 = 50
produto_2 = 33

print(produto_1 - produto_2)
>>> 17

print(produto_1 + produto_2)
>>> 83

print(produto_1 * produto_2)
>>> 1650

print(produto_1 / produto_2)
>>. 1.5151515151515151

print(produto_1 // produto_2)
>>> 1

print(produto_1 ** produto_2)
>>> 116415321826934814453125000000000000000000000000000000000

print(produto_1 / produto_2 + 98)
>>> 99.51515151515152

x = (28 + 78) * 4
y = (28 / 7) + (76 * 86) - (2 ** 2 ) + 7

print(x)
>>> 424

print(y)
>>> 6543.0
