## Operadores Lógicos
Eles são utilizados em conjunto com os operadores de comparação, para montar uma lógica. Quando um operador de comparação é utilizado, o resultado retornado é um booleano, dessa forma combinamos operadores de comparação com os operadores lógicos.

Exemplo: op_comparacao = op_logico = op_comparacao...
```Python
saldo = 2000
saque = 300
limite = 10

saldo >= saque #queremos saber se saldo é maior ou igual a saque
>>> True

saque <= limite #aqui se saque é menor ou igual a limite
>>> False
```
* Operador E: Para ser True todos tem que ser True
```Python
#lógico
saldo = 2000
saque = 300
limite = 150

saldo >= saque and saque <= limite   #queremos saber se saldo é maior ou igual a saque, e se saque é menor ou igual a limite
>>> False #para ser verdadeiro todas as partes precisam ser verdadeiras e não ter nenhum falso
```
* Operador OU: Para ser True apenas um precisa ser True
```Python
saldo = 2000
saque = 300
limite = 150

saldo >= saque or saque <= limite
>>> True # para ser verdadeiro precisa pelo menos uma parte ser verdadeira e o resto pode ser falso
#para ser falso todas precisam ser falso
```
* Operador Negação: Ele inverte o valor lógico
```Python
contatos_principais = [] #valores vazios são considerados falsos, pois não tem valor

not 1000 > 1500 # como 1000 não é maior que 1500 o resultado daria falso
>>> True #mas como tem o not no inicio o falso converte para verdadeiro

not contatos_principais
>>> True #inverteu o falso para verdadeiro

not "saque 1200;" # seria true porque tem um texto dentro das ""
>>> False

not "" #como não tem caractere dentro das "" seria falso
>> True
```
* Parênteses: Ajudam e tem as regras que nem a matemática
```Python
saldo = 2000
saque = 300
limite = 100
conta_especial = True

saldo >= saque and saque <= limite or conta_especial and saldo >= saque #resolvems primeiro os and, e como a primeira parte seria verdadeira e a segunda falsa
>>> True #vemos que no meio tem or, por conta disso seria verdadeiro

(saldo >= saque and saque <= limite) or (conta_especial and saldo >= saque)
>>> True #tambem seria verdadeiro
