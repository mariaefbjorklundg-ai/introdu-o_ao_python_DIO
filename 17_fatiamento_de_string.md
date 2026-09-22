## Fatiamento de Strings
É uma técnica utilizada para retornar substrings (partes da string original), informando inicio (start), fim (stop) e passo (step): [start: stop[, step]].

* Fatiamento
```Python
nome = "Maria Eduarda Garcia"

print(nome [0])
>>> M
print(nome[:9])
>>> Maria Edu
print(nome[10:])
>>> rda Garcia
print(nome[10:16])
>>> rda Ga
print(nome[10:16:2])
>>> raG
print(nome[ : ])
>>> Maria Eduarda Garcia
print(nome[:: -1])
>>> aicraG adraudE airaM
