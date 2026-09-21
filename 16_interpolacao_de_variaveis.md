## Interpolação de Variáveis
Em Python há três formas de interpolar variáveis em strings, a primeira é usando o sinal de %, a segunda é utilizando o método format e a ultima é utilizando f strings

A primeira forma não é muito recomendada e o seu uso no Python 3 é raro.

* %
```Python
nome = "Maria"
idade = 20
profissao = "Programadora"
linguagem = "Python"

print("Oie, me chamo %s. Eu tenho %d anos de idade, trabalho com %s e estou matriculada no curso de %s." % (nome, idade, profissao, linguagem)) 
>>> Oie, me chamo Maria. Eu tenho 20 anos de idade, trabalho com Programadora e estou matriculada no curso de Python.
```
* Método format
```Python
#duas formas de usar
nome = "Maria"
idade = 20
profissao = "Programadora"
linguagem = "Python"
#se mudar a ordem  da formatação, muda as pocições
print("Oie, me chamo {}. Eu tenho {} anos de idade, trabalho com {} e estou matriculada no curso de {}." .format (nome, idade, profissao, linguagem))
>>> Oie, me chamo Maria. Eu tenho 20 anos de idade, trabalho com Programadora e estou matriculada no curso de Python.

print("Oie, me chamo {0}. Eu tenho {1} anos de idade, trabalho com {2} e estou matriculada no curso de {3}." .format (nome, idade, profissao, linguagem))
>>> Oie, me chamo Maria. Eu tenho 20 anos de idade, trabalho com Programadora e estou matriculada no curso de Python.

print("Oie, me chamo {nome}. Eu tenho {idade} anos de idade, trabalho com {profissao} e estou matriculada no curso de {linguagem}." .format (nome=nome, idade=idade, profissao=profissao, linguagem=linguagem))
>>> >>> Oie, me chamo Maria. Eu tenho 20 anos de idade, trabalho com Programadora e estou matriculada no curso de Python.
```

* F-string
```Python
nome = "Maria"
idade = 20
profissao = "Programadora"
linguagem = "Python"


print(f"Oie, me chamo {nome}. Eu tenho {idade} anos de idade, trabalho com {profissao} e estou matriculada no curso de {linguagem}.")
>>> Oie, me chamo Maria. Eu tenho 20 anos de idade, trabalho com Programadora e estou matriculada no curso de Python.
```

* Formatar strings com f-string
```Python
PI = 3.14159

print(f"Valor de PI: {PI:.2f}") #especifico quantos números eu quero depois do ponto
>>> Valor de PI: 3.14
print(f"Valor de PI: {PI:10.2f}") #especifico que quero 10 espaços antes de mostrar a variavel
>>> Valor de PI:       3.14

#podemos definir um dicionarrio também 
