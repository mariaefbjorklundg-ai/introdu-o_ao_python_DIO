## Operadores de Identidade
São utilizados para comparar se os dois objetos testados ocupam a mesma posição na memória.

Utilizando **Is**

Exemplo:
```Python
curso = "Curso de Python"
nome_curso = curso
saldo, limite = 400, 400

curso is nome_curso
>>> True

curso is not nome_curso #como tem o not temos que inverter a resposta
>>> False

saldo is limite
>>> True
```

## Operadores de Associação
São utilizados para verificar se um objeto está presente em uma seguência.
* Se está na sequência colocamos **in**
* Se não está na sequência colocamos **not in**

Exemplo:
```Python
curso = "Curso de Python"
frutas = ["maça", "banana", "melancia"]
saques = [1800, 50]

"Python" in curso #esta em curso
>>> True

"uva" not in frutas #não tem uva na sequência de frutas
>>> True

200 in saques #não tem 200 nos saques
>>> False
