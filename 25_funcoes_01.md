## Funções de Python - Parte 1
Funções é um bloco de código identificado por um nome e pode receber uma lista de parâmetros, esses parâmetros podem ou não ter valores padrões.

Usar funções torna o código mais legível e possibilita o reaproveitamento do código.

Programar baseado em funções é a mesma coisa que estar programando de maneira estruturada.
```Python
def exibir_mensagem():
    print("Olá mundo!")


def exibir_mensagem_2(nome):
    print(f"Seja bem vindo {nome}!")


def exibir_mensagem_3(nome="Anônimo"):
    print(f"Seja bem vindo {nome}!")

#precisa executar as funções
exibir_mensagem()
>>> Olá mundo!

exibir_mensagem_2(nome="Maria") #como eu passei um valor, que seria o nome eu preciso passar um nome na função
>>> Seja bem vindo Maria!

exibir_mensagem_3() #esse eu já tinha definido o valor
>>> Seja bem vindo Anônimo!

exibir_mensagem_3(nome="Max")
>>> Seja bem vindo Max!
```
* Retornando Valores

Para retornar um valor, usamos a palavra **return**.

Toda a função Python retorna **None** por padrão. Em Python uma função pode retornar mais de um valor.

```Python

def calcular_total(numeros):
    return sum(numeros)


def retorna_antecessor_e_sucessor(numero):
    antecessor = numero - 1
    sucessor = numero + 1

    return antecessor, sucessor


print(calcular_total([33, 1, 16]))
>>> 50

print(retorna_antecessor_e_sucessor(3))
>>> (2, 4)

def func_1(): #como não tem valor especifico vai retornar o None
    print("Bem Vindo!")

print(func_1())
>>> None
```
* Argumentos Nomeados

Funções podem ser chamadas usando argumentos nomeados da forma chave=valor.

```Python

def salvar_carro(marca, modelo, ano, placa):
    # salva carro no banco de dados...
    print(f"Carro inserido com sucesso! {marca}/{modelo}/{ano}/{placa}")


salvar_carro("Fiat", "Palio", 1999, "ABC-1234") #teria que ter mais atenção na hora de preencher pois se colocar na ordem errada ficaria na ordem errada
>>> Carro inserido com sucesso! Fiat/Palio/1999/ABC-1234
salvar_carro(marca="Fiat", modelo="Palio", ano=1999, placa="ABC-1234") #desvantagem: se alterar o nome da chave, a função não vai achar e colocar a função, daria um erro
>>> Carro inserido com sucesso! Fiat/Palio/1999/ABC-1234
salvar_carro(**{"marca": "Fiat", "modelo": "Palio", "ano": 1999, "placa": "ABC-1234"})
#passaria um dicionário para a função
>>> Carro inserido com sucesso! Fiat/Palio/1999/ABC-1234
```
* Args e Kwargs

É possível combinar parâmetros obrigatórios com args e kwargs.

Quando são definidos (*args e **kwargs), o método recebe os valores como tupla e dicionário.

```Python
#exemplo da DIO
def exibir_poema(data_extenso, *args, **kwargs): #poderia trocar o args por lista e o kwargs por dicionario, que continuariam rodando
    texto = "\n".join(args)
    meta_dados = "\n".join([f"{chave.title()}: {valor}" for chave, valor in kwargs.items()])
    mensagem = f"{data_extenso}\n\n{texto}\n\n{meta_dados}"
    print(mensagem)


exibir_poema(
    "Zen of Python",
    "Beautiful is better than ugly.",
    "Explicit is better than implicit.",
    "Simple is better than complex.",
    "Complex is better than complicated.",
    "Flat is better than nested.",
    "Sparse is better than dense.",
    "Readability counts.",
    "Special cases aren't special enough to break the rules.",
    "Although practicality beats purity.",
    "Errors should never pass silently.",
    "Unless explicitly silenced.",
    "In the face of ambiguity, refuse the temptation to guess.",
    "There should be one-- and preferably only one --obvious way to do it.",
    "Although that way may not be obvious at first unless you're Dutch.",
    "Now is better than never.",
    "Although never is often better than *right* now.",
    "If the implementation is hard to explain, it's a bad idea.",
    "If the implementation is easy to explain, it may be a good idea.",
    "Namespaces are one honking great idea -- let's do more of those!",
    autor="Tim Peters",
    ano=1999,
)
>>> Zen of Python

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!

Autor: Tim Peters
Ano: 1999

#meu
def exibir_frase(data_extenso, *args, **kwargs):
    texto = "\n".join(args)
    meta_dados = "\n".join([f"{chave.title()}: {valor}" for chave, valor in kwargs.items()])
    mensagem = f"{data_extenso}\n\n{texto}\n\n{meta_dados}"
    print(mensagem)


exibir_frase(
    "Quinta-feira,24 de Stembro de 2026",
    "For my part I know nothing with any certainty ",
    "But the sight of the stars makes me dream.",
    autor="Vincent Van Gogh",
    ano=1888,
)
>>>
Quinta-feira,24 de Stembro de 2026

For my part I know nothing with any certainty 
But the sight of the stars makes me dream.

Autor: Vincent Van Gogh
Ano: 1888
