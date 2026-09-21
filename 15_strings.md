# Strings
Rica em Métodos e possuir uma interface muito fácil de trabalhar

#### Métodos
* Maiúscula = Upper
Converte todos os caracteres para Maiúsculo
* Minúscula = Lower
Converte todos os caracteres para Minúsculo
* Título = Title
Converte todos os caracteres para Titulo 
* Conta = Count
Converte todos os caracteres da spring para contar o que você pede

Exemplos: 

```Python
curso = "vArIaVeL"

print(curso.upper()) #deixa em letras Maiúsculas
>>> "VARIAVEL"

print(curso.lower()) #deixa em letras Minúsculas
>>> "variavel"

print(curso.title()) #deixa como Titulo
>>> "Variavel"

print(curso.lower().count('a)) # conta o numero de As que tem na spring
>>> 2

```
* Tira = Strip
Remove os espaços em branco da esquerda e da direita
* Tira Esquerda = Lstrip
Remove só os espaços da Esquerda
* Tira Direita  Rstrip
Remove só os da Direita
* Centralização = Center
Ele centraliza a resposta
* Juntar = Join
Juntar os caracteres com algum simbolo

```Python
curso = "  Variavel  "

print(curso.strip())
>>> "Variavel"

print(curso.lstrip())
>>> "Variavel  "

print (curso.rstrip())
>>> "  Variavel"

print(curso.center(16, '-')) #ele conta quantos caracteres de resposta você vai querer e aumenta na resposta 
>>> "--  Variavel  --"        #se você não colocar nenhum simbolo ele vai deixar em branco

print(curso.center(16))
>>> "    Variavel    "

print(".".join(curso))
>>> . .v.a.r.i.a.v.e.l. . 
