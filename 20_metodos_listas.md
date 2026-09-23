## Métodos da Classe Listas
* [].append
```Python
lista = []

lista.append(1)
lista.append("Python")
lista.append([40, 30, 20])

print(lista)
>>> [1, 'Python', [40, 30, 20]]
```
* [].clear
```Python
lista = [1, 'Python', [40, 30, 20]]

print(lista) 
>>> [1, 'Python', [40, 30, 20]]

lista.clear()
#vai limpar a lista
print(lista)
>>> [] #depois de ter a lista apagada
```
* [].copy
```Python
lista = [1, 'Python', [40, 30, 20]]

lista.copy() #copia a lisa "original" sem sofrer alterações

print(lista)
>>> [1, 'Python', [40, 30, 20]]
```
* [].count
```Python
#conta quantas vezes a palavra/numero apareceu na sua lista

cores = ["vermelho", "azul", "cinza", "vermelho", "azul"]

print(cores.count("vermelho"))
>> 2
print(cores.count("azul"))
>> 2
print(cores.count("cinza"))
>> 1
```
* [].extend
```Python
#acrescentar coisas na lista e juntar uma lista com outra
linguagens = ["python", "js", "c"]

print(linguagens)
>>> ['python', 'js', 'c']

linguagens.extend(["java", "kotlin"])

print(linguagens)
>>> ['python', 'js', 'c', 'java', 'kotlin']
#se tiver valores duplicados ele não vai cortar esses valores, vai deixar duplicado
```
* [].index
```Python
#qual que o numero que aparece o pedido, aonde aparece a primeira ocorrencia
linguagens = ["python", "js", "c", "java", "kotlin"]

print(linguagens.index("java"))
>>> 3
print(linguagens.index("python"))
>>> 0

linguagens = ["python", "java", "c", "java", "kotlin"]
print(linguagens.index("java")) #ele encontra a primeira só occorencia, ele não vai mostrar qunantas vezes ele apareceu
>>> 1 #se quissese saber quantas vezes ele apareceu teria que juntas os metodos
```
* [].pop
```Python
#vai tirando os últimos elementos adicionados na lista, e também posso especificar qual índice eu quero remeover
linguagens = ["python", "js", "c", "java", "kotlin"]

print(linguagens.pop()) #tirou kotlin
print(linguagens.pop()) #tirou java
print(linguagens.pop()) #tirou c
print(linguagens.pop(0)) #tirou python
#sobrou só js na lista
```
* [].remove
```Python
#parecido com o pop, mas esse vc passa especificado o que vc quer tirar
linguagens = ["python", "js", "c", "java", "kotlin"]

linguagens.remove("c")

print(linguagens)
>>> ['python', 'js', 'java', 'kotlin']
```
* [].reverse
```Python
# Inverte a ordem da sua lista
linguagens = ["python", "js", "c", "java", "kotlin"]

linguagens.reverse()

print(linguagens)
>>> ['kotlin', 'java', 'c', 'js', 'python']
```
* [].sort
```Python
#ordena a sua lista
linguagens = ["python", "js", "c", "java", "kotlin"]

linguagens.sort() #alfabetica
print(linguagens)
>>> ['c', 'java', 'js', 'kotlin', 'python']

linguagens.sort(reverse=True) #vai inverter a ordem, de trás para a frente
print(linguagens)
>>> ['python', 'kotlin', 'js', 'java', 'c']

linguagens.sort(key=lambda x: len(x)) #coloca em ordem crescente  #lando é uma função anonima
print(linguagens)
>>> ['c', 'js', 'java', 'python', 'kotlin']

linguagens.sort(key=lambda x: len(x), reverse=True)
print(linguagens)
>>> ['python', 'kotlin', 'java', 'js', 'c']
```
* Len
```Python
#conta quantos elementos tem dentro da lista
linguagens = ["python", "js", "c", "java", "kotlin"]

print(len(linguagens))
>>> 5
```
* Sorted
```Python
#ordena íteraveis
linguagens = ["python", "js", "c", "java", "kotlin"]

print(sorted(linguagens, key=lambda x: len(x)))
>>> ['c', 'js', 'java', 'python', 'kotlin']

linguagens.sorted(key=lambda x: len(x), reverse=True)
print(linguagens)
>>> ['python', 'kotlin', 'java', 'js', 'c']

linguagens = ["python", "js", "c", "java", "kotlin"]

print(sorted(linguagens))
>>> ['c', 'java', 'js', 'kotlin', 'python']
