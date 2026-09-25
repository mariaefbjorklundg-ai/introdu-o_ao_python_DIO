## Funções de Python - Parte 2
* Parâmetros Especiais

Argumentos podem ser passados para uma função Python tanto por posição quanto explicitamente pelo nome.

Para uma melhor legibilidade e desempenho, devemos restringir a maneira pela qual argumentos possam ser passados, 

assim um desenvolvedor precisa apenas olhar para a definição da função para determinar se os itens são passados **por posição,por posição e nome, ou por nome**.

* Positional Only - /

  Só pocição
```Python

def criar_carro(modelo, ano, placa, /, marca, motor, combustivel): #até a / tenho que passar sem o nome, depois posso passar com o nome 
    print(modelo, ano, placa, marca, motor, combustivel)


criar_carro("Palio", 1999, "ABC-1234", marca="Fiat", motor="1.0", combustivel="Gasolina") #só passou o nome depois do /
>>> Palio 1999 ABC-1234 Fiat 1.0 Gasolina
criar_carro(modelo="Palio", ano=1999, placa="ABC-1234", marca="Fiat", motor="1.0", combustivel="Gasolina")  #passou o nome antes e depois do /, por isso é invalido
>>> erro
```
* Keyword only - *

Só por nome
  ```Python

  def criar_carro(*, modelo, ano, placa, marca, motor, combustivel): # fala que tem que passar depois do *
    print(modelo, ano, placa, marca, motor, combustivel)
  criar_carro("Palio", 1999, "ABC-1234", marca="Fiat", motor="1.0", combustivel="Gasolina" #não é valido porque não estão todos com nome
  >>> erro
  criar_carro(modelo="Palio", ano=1999, placa="ABC-1234", marca="Fiat", motor="1.0", combustivel="Gasolina")  # valido pois estao todos com nomes
  >>> Palio 1999 ABC-1234 Fiat 1.0 Gasolina
  ```
  * Keyword and positional only - / e *
  ```Python
  def criar_carro(modelo, ano, placa, /, *, marca, motor, combustivel):
    print(modelo, ano, placa, marca, motor, combustivel)

   criar_carro("Palio", 1999, "ABC-1234", marca="Fiat", motor="1.0", combustivel="Gasolina")
  >>> Palio 1999 ABC-1234 Fiat 1.0 Gasolina
   criar_carro(modelo="Palio", ano=1999, placa="ABC-1234", marca="Fiat", motor="1.0", combustivel="Gasolina")
  >>> erro
  ```
  * Objetos de primeira classe
Tudo é objeto em Python, **funções também são objetos** o que faz delas objetos de primeira classe.

Podemos **atribuir funções a variáveis, passá-las como parâmetro para funções, usá-las como valores em estruturas de dados** (listas, tuplas, dicionários, etc) e usar como valor de retorno para uma função (closures)
```Python

def somar(a, b):
    return a + b

def subtrair(a, b):
    return a - b

def dividir(a, b):
    return a // b

def exibir_resultado(a, b, funcao): #poderia ser outro nome diferente de função
    resultado = funcao(a, b)
    print(f"O resultado da operação {a} + {b} = {resultado}")


exibir_resultado(50, 70, somar)
>>> O resultado da operação 50 + 70 = 120
exibir_resultado(43, 87, subtrair)
>>> O resultado da operação 43 + 87 = -44
exibir_resultado(50, 5, dividir)
>>> O resultado da operação 50 + 5 = 10
```
* Escopo Local e Escopo Global

Dentro do bloco da função o escopo é local.

Alterações ali feitas em objetos imutáveis serão perdidos quando o método terminar de ser executado.

Para usar objetos globais utiliza-se a palavra-chave **global**, que informa ao interpretador que a variável que está sendo manipulada no escopo local é global.
```Python
salario = 2000

def salario_bonus(bonus):
    global salario
    salario += bonus
    return salario

salario_bonus(500)  
print(salario)
>>> 2500
