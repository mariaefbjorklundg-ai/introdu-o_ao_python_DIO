## Funções de Entrada e Saída

#### Função Input
Essa função builtin **input** é utilizada quando queremos ler padrões de entrada padrão (o teclado). E ela recebe um argumento do tipo string, que é exibido para o usuário na saída padrão (a tela). A função lê a entrada, converte para string e retorna o valor.

Essa função já esta na biblioteca padrão do python.

Exemplo:

```Python
nome = input("Informe o seu nome:  ")
>>> Informe o seu nome: | # ele vai ficar esperando a pessoa responder o nome e depois vai substituir por uma variavel
```

#### Função Print
Esta função builtin **print** é utilizada quando queremos exibir dados na saída padrão (a tela). Ela recebe um argumento obrigatório tipo varargs de objetos e 4 argumentos opcionais (seo, end, file e flush). Todos os objetos são convertidos para string, separados por sep e terminados por end. A string final é exibida para o usuário.

Exemplo:
```Python
nome = "Maria"
sobrenome = "Silva"

print(nome, sobrenome)
>>> Maria Silva

print(nome, sobrenome, end="...\n")#para acabar com esses caracteres
>>> Maria Silva...

print(nome, sobrenome, sep="#")#para separar as variáveis e colocar aquele caracter no meio
>>> Maria#Silva

print(nome, sobrenome, sep="#", end="...\n")
>>> Maria#Silva...
