## Conjuntos - Sets
É um conjunto de objetos que não possui repetição, usamos eles para representar conjuntos matemáticos ou eliminar itens duplicados de um íteravel.

Ele geralmente não vai devolver na ordem que você passou.

Exemplo:
```Python
numeros = set([1, 2, 3, 1, 3, 4])
print(numeros)  
>>> {1, 2, 3, 4}

letras = set("abacaxi")
print(letras)  
>>> {'x', 'a', 'b', 'i', 'c'}

carros = set(("palio", "gol", "celta", "palio"))
print(carros)
>>> {'palio', 'gol', 'celta'}
```

* Acessando os dados

Conjuntos em Python não suportam indexação e nem fatiamento, para acessar os seus valores é necessário converter o conjunto para lista.
```Python
numeros = {1, 2, 3, 2}

numeros = list(numeros)

print(numeros[0])
>>> 1
```
* Iterar Valores

A forma mais comum para percorrer os dados de um conjunto é utilizando o comando **for**
```Python
carros = {"gol", "celta", "palio"}

for carro in carros:
    print(carro)
>>> 
palio
gol
celta

# Função Enumerate
for indice, carro in enumerate(carros):
    print(f"{indice}: {carro}")
>>>
0: palio
1: gol
2: celta
```
### Métodos
* {}.union

Uni os elementos
```Python
conjunto_a = {1, 2}
conjunto_b = {3, 4}

resultado = conjunto_a.union(conjunto_b)
print(resultado)
>>> {1, 2, 3, 4}
```
* {}.intersection

Junta a parte dos dois conjuntos que são iguais 
```Python
conjunto_a = {1, 2, 3}
conjunto_b = {2, 3, 4}

resultado = conjunto_a.intersection(conjunto_b)
print(resultado)
>>> {2, 3}
```
* {}.difference

Tudo que eu tenho de diferente de um conjunto que não está no outro
```Python
conjunto_a = {1, 2, 3}
conjunto_b = {2, 3, 4}

resultado = conjunto_a.difference(conjunto_b)
print(resultado)
>>> {1}
resultado = conjunto_b.difference(conjunto_a)
print(resultado)
>>> {4}
```
* {}.symmetric_difference

Queremos todos os elementos que não são iguais
```Python
conjunto_a = {1, 2, 3}
conjunto_b = {2, 3, 4}

resultado = conjunto_a.symmetric_difference(conjunto_b)
print(resultado)
>>> {1, 4}
```
* {}.issubset

Busca saber se todos os elementos deste conjunto estão presentes no outro conjunto
```Python
conjunto_a = {1, 2, 3}
conjunto_b = {4, 1, 2, 5, 6, 3}

resultado = conjunto_a.issubset(conjunto_b)  #todos os conjuntos a tem no conjunto b
print(resultado)
>>> True
resultado = conjunto_b.issubset(conjunto_a)  # Tem conjuntos no elemento b que não tem no elemento a 
print(resultado)
>>> False
```
* {}.issuperset

Verifica se um conjunto é um superconjunto do outro, se ele mantem todos os elementos do outro conjunto
```Python
conjunto_a = {1, 2, 3}
conjunto_b = {4, 1, 2, 5, 6, 3}

resultado = conjunto_a.issuperset(conjunto_b)  # A não tem todos os elementos que B
print(resultado)
>>> False
resultado = conjunto_b.issuperset(conjunto_a)  # B tem todos os conjuntos que A
print(resultado)
>>> True
```
* {}.isdisjoint

Verifica se eles não tem conjuntos em comum
```Python
conjunto_a = {1, 2, 3, 4, 5}
conjunto_b = {6, 7, 8, 9}
conjunto_c = {1, 0}

resultado = conjunto_a.isdisjoint(conjunto_b)  # Os elementos de A não tem no B
print(resultado)
>>> True
resultado = conjunto_a.isdisjoint(conjunto_c)  # Os elementos de A tem no C
print(resultado)
>>> False
```
* {}.add

Adiciona elementos no conjunto
```Python
sorteio = {1, 23}

sorteio.add(25)  
print(sorteio)
>>> {1, 25, 23}

sorteio.add(42)  
print(sorteio)
>>> {1, 42, 25, 23}

sorteio.add(25)  
print(sorteio) 
>>> {1, 42, 25, 23} #ele não duplica o numero
```
* {}.clear

Limpa
```Python
sorteio = {1, 23}

print(sorteio)  
>>> {1,23}

sorteio.clear()

print(sorteio)
>>> {}
```
* {}.copy

Copia
```Python
sorteio = {1, 23}

print(sorteio)  
>>> {1, 23}

sorteio.copy()

print(sorteio)
>>> {1, 23}
```
* {}.discard

A gente descarta um valor
```Python
numeros = {1, 2, 3, 1, 2, 4, 5, 5, 6, 7, 8, 9, 0}

print(numeros)  
>>> {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}

numeros.discard(1) #descartar o numero 1

numeros.discard(45) #mesmo não tendo o 45, ele não da nenhum erro

print(numeros)
>>> {0, 2, 3, 4, 5, 6, 7, 8, 9}
```
* {}.pop

Vai tirando os valores do conjunto, pode também especificar qual você quer tirar
```Python
numeros = {1, 2, 3, 1, 2, 4, 5, 5, 6, 7, 8, 9, 0}

print(numeros)
>>> {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}
print(numeros.pop())
>>> 0
print(numeros.pop())
>>> 1
print(numeros)
>>> {2, 3, 4, 5, 6, 7, 8, 9}
```
* {}.remove

Remover o valor especifico que você fornecer. Se o elemento não existe ele vai dar erro
```Python
numeros = {1, 2, 3, 1, 2, 4, 5, 5, 6, 7, 8, 9, 0}

print(numeros)
>>> {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}

print(numeros.remove(0))
>>> 0

print(numeros)
>>> {1, 2, 3, 4, 5, 6, 7, 8, 9}
```
* Len

Ele conta quantos elementos tem no conjunto
```Python
numeros = {1, 2, 3, 1, 2, 4, 5, 5, 6, 7, 8, 9, 0}

print(len(numeros))
>>> 10
```
* In

Verifico se um determinado elemento esta dentro do conjunto
```Python
numeros = {1, 2, 3, 1, 2, 4, 5, 5, 6, 7, 8, 9, 0}

print(1 in numeros) #está dentro do conjunto
>>> True

print(10 in numeros) #não esta dentro do conjunto
>>> False 
