## Tuplas
São estruturas de dados muito parecidos com as listas, as tuplas são imutáveis diferentes das listas que são mutáveis.

Criamos as tuplas através da classe **tuple**, ou colocando valores separados por vírgula de parenteses.

Exemplo:
```Python

frutas = ( "laranja", "pera", "uva",)
print(frutas)
>>> ('laranja', 'pera', 'uva')

letras = tuple("python")
print(letras)
>>> ('p', 'y', 't', 'h', 'o', 'n')

numeros = tuple([1, 2, 3, 4])
print(numeros)
>>> (1, 2, 3, 4)

pais = ("Brasil",)
print(pais)
>>> ('Brasil',)
```
* Acesso Direto
```Python
frutas = ( "laranja", "pera", "uva", "morango",)
print(frutas[0])
>>> laranja
print(frutas[2])
>>> uva
```
* Índices Negativos
```Python
frutas = ( "laranja", "pera", "uva", "morango",)
print(frutas[-1])
>>> morango
print(frutas[-3])
>>> pera
```
* Tuplas Aninhadas
```Pyhon
#faço quando o valor da matriz não vai mudar, não vai sofrer alteração
matriz = (
    (1, "a", 2),
    ("b", 3, 4),
    (6, 5, "c"),
)

print(matriz[0])
>>> (1, "a", 2)
print(matriz[0][0])
>>> 1
print(matriz[0][-1])
>>> 2
print(matriz[-1][-1])
>>> "c"
```
* Fatiamento
```Python
#bem parecido com as listas
tupla = ("p", "y", "t", "h", "o", "n",)

print(tupla[2:])
>>> ("t", "h", "o", "n")
print(tupla[:2])
>>> ("p", "y")
print(tupla[1:3])
>>> ("y", "t")
print(tupla[0:3:2])
>>> ("p", "t")
print(tupla[::])
>>> ("p", "y", "t", "h", "o", "n")
print(tupla[::-1])
>>> ("n", "o", "h", "t", "y", "p")
```
* Iterar
```Python
carros = ("gol", "celta", "palio",)

for carro in carros:
    print(carro)
>>> gol
celta
palio
 # Com Enumerate
for indice, carro in enumerate(carros):
    print(f"{indice}: {carro}")
>>> 0: gol
1: celta
2: palio
```
### Métodos 
Como as tuplas são imutáveis tem menos métodos do que as listas

* [].count
```Python
cores = ("vermelho", "azul", "verde", "azul",)

print(cores.count("vermelho"))
>>> 1
print(cores.count("azul"))
>>> 2
print(cores.count("verde"))
>>> 1
```
* [].index
```Python
#em qual posição o objeto esta dentro da minha tupla
linguagens = ("python", "js", "c", "java", "csharp",)

print(linguagens.index("java"))
>>> 3
print(linguagens.index("python"))
>>> 0
```
* Len
```Python
#vai contar quantos objetos tem na minha tupla
linguagens = ("python", "js", "c", "java", "csharp",)

print(len(linguagens))
>>> 5
