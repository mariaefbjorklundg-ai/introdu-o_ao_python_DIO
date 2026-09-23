## Listas em Python
As Listas em Python podem armazenar de maneira sequencial qualquer tipo de objeto. 

Podemos criar listas utilizando o **list**, a função range ou colocando valores separados por vírgula dentro do colchetes.

Listas são objetos mutáveis, podemos alterar seus valores após a criação.

Exemplo:
```Python
frutas = ["laranja", "maca", "uva"]
>>> ['laranja', 'maca', 'uva']

frutas[0] #maçã
frutas[2] # uva
frutas = []
>>> []

letras = list("Pyhon") #ele criaria uma lista aonde cada letra é um elemento
>>> ['p', 'y', 't', 'h', 'o', 'n']

numeros = list(range(10)) #colocariam cada numero ate o numero 9
>>> [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

carro = ["Ferrari", "F8", 420000, 2020, 2900, "São Paulo", True]
>>> ['Ferrari', 'F8', 4200000, 2020, 2900, 'São Paulo', True]

# Índices negativos
frutas = ["laranja", "maca", "uva", "pera"]
#olharia ao contrario
frutas[-1] #pera
frutas[-3] #laranja
```

### Listas Aninhadas
Como listas podem armazenar todos os tipos de objetos em Python, podemos ter listas quearmazenam outras listas.

Com isso podemo criar estruturas bidimensionais (tabelas), e acessar informando os índices de linha e coluna.
```Python
matriz = [
    [1, "a", 2],
    ["b", 3, 4],
    [6, 5,"c" ]
]

print(matriz[0])
>>> [1, 'a', 2]

print(matriz[0][0])
>>> 1

print(matriz[0][-1])
>>> 2

print(matriz[-1][-1])
>>> c
```

### Fatiamento
Pode acessar elementos diretamente, e podemos extrair um conjunto de valores de uma sequência. 

Para isso basta passar o índice inicial e/ou final para acessar o conjunto. 

Podemos ainda informar quantas posições o cursor deve "pular" no acesso.
```Python
lista = ["p", "y", "t", "h", "o", "n"]

print(lista[2:]) #se eu passo o : e nao informo aonde quero parar ele vai ate o final
>>> ['t', 'h', 'o', 'n']

print(lista[:2]) 
>>> ['p', 'y']

print(lista[1:3])
>>> ['y', 't']

print(lista[0:3:2])
>>> ['p', 't']

print(lista[ :: ])
>>> ['p', 'y', 't', 'h', 'o', 'n']

print(lista[ ::-1])        
>>> ['n', 'o', 'h', 't', 'y', 'p']
```
### Iterar Listas
Para percorrer os dados de uma lista é mais comum usar o comendo **for**
```Python
carros = ["gol", "civic", "palio"]
for carro in carros:
    print(carros)
>>>> ['gol', 'civic', 'palio']
```
### Função Enumerate
É necessário ás vezes saber qual o índice do objeto dentro do laço **for**.

Podemos usar a função **enumerate**
```Python
carros = ["gol", "civic", "palio"]

for indice, carro in enumerate (carros):
    print(f"{indice}: {carros}")
>>> 0: ['gol', 'civic', 'palio']
1: ['gol', 'civic', 'palio']
2: ['gol', 'civic', 'palio']
```
### Compreensão de Listas
Ela oferece uma sintaxe mais curta quando você deseja: criar uma lista nova com base nos valores de uma lista com base nos valore de uma lista existente (filtro) ou gerar uma nova lista aplicando alguma modificação nos elementos de uma lista existente.
```Python
# Filtro versão 1
numeros = [1, 30, 21, 2, 9, 65, 34]
pares = []

for numero in numeros:
    if numero % 2 == 0:
        pares.append(numero)

print(pares)
>>> [30, 2, 34]

# Filtro versão 2
pares = [numero for numero in numeros if numero % 2 == 0]

print(pares)
>>> [30, 2, 34]

# Modificando Valores versão 1
numeros = [1, 30, 21, 2, 9, 65, 34]
quadrado = []

for numero in numeros:
    quadrado.append(numero ** 2)

print(quadrado)
>>> [1, 900, 441, 4, 81, 4225, 1156]

# Modificando Valores versão 2
numeros = [1, 30, 21, 2, 9, 65, 34]
quadrado = [numero ** 2 for numero in numeros]


print(quadrado)
>>> [1, 900, 441, 4, 81, 4225, 1156]
