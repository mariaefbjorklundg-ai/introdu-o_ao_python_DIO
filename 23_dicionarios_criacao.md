## Dicionários
É um conjunto não-ordenado de pares chave:valor, onde as chaves são as únicas em uma dada instância do dicionário.

Dicionários são delimitados por chaves:{}, e contém uma lista de pares chaves:valor separados por vírgulas.
```Python
#todos os valores são imutáveis 
pessoa = {"nome": "Maria", "idade": 20}
print(pessoa)
>>> {'nome': 'Maria', 'idade': 20}

pessoa = dict(nome="Maria", idade=20)
print(pessoa)
>>> {'nome': 'Maria', 'idade': 20}
pessoa["telefone"] = "3333-54321"  # adiciono uma chave ao dicionario
print(pessoa)
>>> {'nome': 'Maria', 'idade': 20, 'telefone': '3333-54321'}
```
* Acesso aos Dados

São mudados e acessados através da chave.
```Python
dados = {"nome": "Maria", "idade": 20, "telefone": "3333-54321"}

print(dados["nome"])
>>> Maria
print(dados["idade"])
>>> 20
print(dados["telefone"])  
>>> 3333-54321

dados["nome"] = "Patricia"
dados["idade"] = 50
dados["telefone"] = "12345-666"

print(dados)
>>> {'nome': 'Patricia', 'idade': 50, 'telefone': '12345-666'}
```
* Dicionários Aninhados

Eles podem armazenar qualquer tipo de objeto Python como valor, desde que a chave para esse valor seja um objeto imutável como (strings e números).
```Pyhon
contatos = {
    "guilherme@gmail.com": {"nome": "Guilherme", "telefone": "3333-2221"},
    "giovanna@gmail.com": {"nome": "Giovanna", "telefone": "3443-2121"},
    "chappie@gmail.com": {"nome": "Chappie", "telefone": "3344-9871"},
    "melaine@gmail.com": {"nome": "Melaine", "telefone": "3333-7766"},
}

telefone = contatos["giovanna@gmail.com"]["telefone"]  
print(telefone)
>>> 3443-2121
telefone = contatos["chappie@gmail.com"]["telefone"]  
print(telefone)
>>> 3344-9871

nome = contatos["melaine@gmail.com"]["nome"]
print(nome)
>>> Melaine
#pode ir adicionando as informações

```
* Iterar Dicionários

Mais comum utilizando o comando **for**
```Python
contatos = {
    "guilherme@gmail.com": {"nome": "Guilherme", "telefone": "3333-2221"},
    "giovanna@gmail.com": {"nome": "Giovanna", "telefone": "3443-2121"},
    "chappie@gmail.com": {"nome": "Chappie", "telefone": "3344-9871"},
    "melaine@gmail.com": {"nome": "Melaine", "telefone": "3333-7766"},
}

for chave in contatos:
    print(chave, contatos[chave])
>>>
guilherme@gmail.com {'nome': 'Guilherme', 'telefone': '3333-2221'}
giovanna@gmail.com {'nome': 'Giovanna', 'telefone': '3443-2121'}
chappie@gmail.com {'nome': 'Chappie', 'telefone': '3344-9871'}
melaine@gmail.com {'nome': 'Melaine', 'telefone': '3333-7766'}

print("=" * 100)

for chave, valor in contatos.items():
    print(chave, valor)
>>>
====================================================================================================
guilherme@gmail.com {'nome': 'Guilherme', 'telefone': '3333-2221'}
giovanna@gmail.com {'nome': 'Giovanna', 'telefone': '3443-2121'}
chappie@gmail.com {'nome': 'Chappie', 'telefone': '3344-9871'}
melaine@gmail.com {'nome': 'Melaine', 'telefone': '3333-7766'}
