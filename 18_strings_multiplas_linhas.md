## Strings de Múltiplas Linhas
Definidas informando 3 aspas simples ou duplas durante a atribuição. 

Elas podem ocupar várias linhas de código, e todos os espaços em branco são incluídos na string final.

* Stringds Triplas
```Python
nome = "Maria"

mensagem = f''' 
   Oie meu nome é {nome},
Eu estou aprendendo Python.
    Essa mensagem tem diferentes recuos
'''

print(mensagem)
>>>   Oie meu nome é Maria,
   Eu estou aprendendo Python.
    Essa mensagem tem diferentes recuos

print(
    """
    ========== MENU =========
    
    1 - Depositar
    2 - Sacar
    0 - Sair
    
    ========================
    
            Obrigada pelo teste
"""
)
>>> 
    ========== MENU =========
    
    1 - Depositar
    2 - Sacar
    0 - Sair
    
    ========================
    
            Obrigada pelo teste

```
