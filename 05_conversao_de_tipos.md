## Convertendo Tipos
Em alguns momentos vai ser necessário converter o tipo de variável para manipular de forma diferente.

Exemplo:
Variáveis do tipo **string**, que armazenam números e quando precisamos fazer alguma operação matemática com esse valor.

#### Inteiro para Float
```Python
preco = 20
print(preco)
>>> 20

preco = float(preco)
print(preco)
>>> 20.0

preco = 20 / 2
print(preco)
>>> 10.0
```

#### Float para Inteiro
```Python
preco = 20.30
print(preco)
>>> 20.3

preco = int(preco) #retorna só o número inteiro
print(preco)
>>> 20
```

#### Conversão por Divisão
```Python
preco = 20
print(preco)
>>> 20

print(preco / 2) #não retorna o número inteiro
>>> 10.0

print(preco // 2) #volta só o número inteiro
>>> 10
```

#### Numérico para String
```Python
preco = 20.30
idade = 55

print(str(preco))
>>> 20.3

print(str(idade))
>>> 55

texto = f'idade {idade} preço {preco}'
print(texto)
>>> idade 55 preço 20.3
```

#### String para Número
```Python
preco = "20.30"
idade = "55"

print(float(preco))
>>> 20.30

print(int(idade))
>>> 55
```

* Nem sempre vai dar para converter uma um tipo para o outro
Exemplo:
```Python
preco = "python"
print(float(print))
>>> erro #daria erro pois o valor do preço seria um carácter e não um numero, por causa disso não daria para fazer essa conversão
