## Métodos de Dicionário

* {}.clear

Ele apaga os valores do dicionário
```Python

contatos = {
    "guilherme@gmail.com": {"nome": "Guilherme", "telefone": "3333-2221"},
    "giovanna@gmail.com": {"nome": "Giovanna", "telefone": "3443-2121"},
    "chappie@gmail.com": {"nome": "Chappie", "telefone": "3344-9871"},
    "melaine@gmail.com": {"nome": "Melaine", "telefone": "3333-7766"},
}

contatos.clear()
print(contatos)
>>> {}
```
* {}.copy

Copia o dicionário
```Python

contatos = {"maria@gmail.com": {"nome": "Maria", "telefone": "3333-54321"}}

copia = contatos.copy() #quando cria uma copia nos mudamos a copia para "Ma"
copia["maria@gmail.com"] = {"nome": "Ma"}

print(contatos["maria@gmail.com"])  
>>> {'nome': 'Maria', 'telefone': '3333-54321'}

print(copia["maria@gmail.com"])
>>> {'nome': 'Ma'}
```
* {}.fromkeys

Ele cria chaves, quando queremos criar chaves mas não queremos atribulas a valores, ou quando queremos criar chaves e colocar um valor padrão nela
```Python

resultado = dict.fromkeys(["nome", "telefone"])  
print(resultado)
>>> {'nome': None, 'telefone': None}

resultado = dict.fromkeys(["nome", "telefone"], "vazio")  
print(resultado)
>>> {'nome': 'vazio', 'telefone': 'vazio'}
```
* {}.get

Acessa valores ao dicionário
```Python

contatos = {"maria@gmail.com": {"nome": "Maria", "telefone": "3333-54321"}}

# contatos["chave"]  # KeyError

resultado = contatos.get("chave") 
print(resultado)
>>> None

resultado = contatos.get("chave", {})  #se ele não achar uma chave com o nome "chave é para voltar o resultado em {}
print(resultado)
>>> {}

resultado = contatos.get("maria@gmail.com", {})
print(resultado)
>>> {'nome': 'Maria', 'telefone': '3333-54321'}
```
* {}.items

Para extrair as chaves e os valores do dicionario
```Python

contatos = {"maria@gmail.com": {"nome": "Maria", "telefone": "3333-54321"}}

resultado = contatos.items()  
print(resultado)
>>> dict_items([('maria@gmail.com', {'nome': 'Maria', 'telefone': '3333-54321'})])
```
* {}.keys

Retorna só as chaves do dicionário
```Python

contatos = {"maria@gmail.com": {"nome": "Maria", "telefone": "3333-54321"}}

resultado = contatos.keys()  
print(resultado)
>>> dict_keys(['maria@gmail.com'])
```
* {}.pop

Vai remover um valor do seu dicionário
```Python

contatos = {"maria@gmail.com": {"nome": "Maria", "telefone": "3333-54321"}}

resultado = contatos.pop("maria@gmail.com")  
print(resultado)
>>> {'nome': 'Maria', 'telefone': '3333-54321'}

resultado = contatos.pop("maria@gmail.com", {})
print(resultado)
>>> {} #como ele não encontrou a chave ele voltou utilizando o simbolo que pedimos
```
* {}.popitem

Não especificamos o que queremos tirar e ele vai tirando um por um
```Python

contatos = {"maria@gmail.com": {"nome": "Maria", "telefone": "3333-54321"}}

resultado = contatos.popitem()  
print(resultado)
>>> ('maria@gmail.com', {'nome': 'Maria', 'telefone': '3333-54321'})
```
* {}.setdefault

Pode adicionar informações que não existem, mas se tentar mudar um atributo que já existe, ele não vai mudar
```Python

contato = {"nome": "Maria", "telefone": "3333-54321"}

contato.setdefault("nome", "Marcia")  #como já existe uma chave de nome, ele não muda
print(contato)  
>>> {'nome': 'Maria', 'telefone': '3333-54321'}

contato.setdefault("idade", 20)  
print(contato)
>>> {'nome': 'Maria', 'telefone': '3333-54321', 'idade': 20}
```
* {}.update

Atualiza o dicionário
```Python

contatos = {"maria@gmail.com": {"nome": "Maria", "telefone": "3333-54321"}}

contatos.update({"maria@gmail.com": {"nome": "Ma"}})
print(contatos)
>>> {'maria@gmail.com': {'nome': 'Ma'}}

contatos.update({"marcia@gmail.com": {"nome": "Marcia", "telefone": "54321-8181"}})
print(contatos)
>>> {'maria@gmail.com': {'nome': 'Ma'}, 'marcia@gmail.com': {'nome': 'Marcia', 'telefone': '54321-8181'}}
```
* {}.valus

Retorna todos os valores que estão dentro das chaves
```Python

contatos = {
    "guilherme@gmail.com": {"nome": "Guilherme", "telefone": "3333-2221"},
    "giovanna@gmail.com": {"nome": "Giovanna", "telefone": "3443-2121"},
    "chappie@gmail.com": {"nome": "Chappie", "telefone": "3344-9871"},
    "melaine@gmail.com": {"nome": "Melaine", "telefone": "3333-7766"},
}

resultado = (contatos.values())
print(resultado)
>>> dict_values([{'nome': 'Guilherme', 'telefone': '3333-2221'}, {'nome': 'Giovanna', 'telefone': '3443-2121'}, {'nome': 'Chappie', 'telefone': '3344-9871'}, {'nome': 'Melaine', 'telefone': '3333-7766'}])
```
* In

Verifica se a chave existe no dicionário
```Python

contatos = {
    "guilherme@gmail.com": {"nome": "Guilherme", "telefone": "3333-2221"},
    "giovanna@gmail.com": {"nome": "Giovanna", "telefone": "3443-2121"},
    "chappie@gmail.com": {"nome": "Chappie", "telefone": "3344-9871"},
    "melaine@gmail.com": {"nome": "Melaine", "telefone": "3333-7766"},
}

resultado = "guilherme@gmail.com" in contatos  
print(resultado)
>>> True

resultado = "megui@gmail.com" in contatos  
print(resultado)
>>> False

resultado = "idade" in contatos["guilherme@gmail.com"]  # False
print(resultado)
>>> False

resultado = "telefone" in contatos["giovanna@gmail.com"]  # True
print(resultado)
>>> True
```
* Del

Remove o valor informado
```Python

contatos = {
    "guilherme@gmail.com": {"nome": "Guilherme", "telefone": "3333-2221"},
    "giovanna@gmail.com": {"nome": "Giovanna", "telefone": "3443-2121"},
    "chappie@gmail.com": {"nome": "Chappie", "telefone": "3344-9871"},
    "melaine@gmail.com": {"nome": "Melaine", "telefone": "3333-7766"},
}

del contatos["guilherme@gmail.com"]["telefone"]
del contatos["chappie@gmail.com"]

print(contatos)
>>> {'guilherme@gmail.com': {'nome': 'Guilherme'}, 'giovanna@gmail.com': {'nome': 'Giovanna', 'telefone': '3443-2121'}, 'melaine@gmail.com': {'nome': 'Melaine', 'telefone': '3333-7766'}}
