## Estruturas Condicionais
Ela permite o desvio de fluxo de controle, quando determinadas expressões lógicas são atendidas.

#### If
Utilizamos o **If** para criar uma estrutura condicional simples, composta por um unico desvio.
O comando irá testar a expressão lógica, e em casod e retorno verdadeiro as ações presentes no bloco de código do if serão executadas.

Exemplo:
```Python
saldo = 2000.0
saque = float(input("Informe o valor do saque:  "))

if saldo >= saque:
    print("Realizando saque!")

if saldo < saque:
    print("Saldo insuficiente!")
```
#### If/Else
Com dois desvios criamos uma estrutura condicional que podemos utilizar as palavras reservadas **if e else**. Se a expressão lógica testada no if for verdadeira, o código do if será testado. Caso contrário o bloco de código do else será executado.

Exemplo:
```Python
saldo = 2000.0
saque = float(input("Informe o valor do saque:  "))

if saldo >= saque:
    print("Realizando saque!")
else:
     print("Saldo insuficiente!")
```
#### If/Elif/Else
Algumas vezes queremos mais do que dois desvios, para isso podemos utilizar a palavra **elif**. O elif é composto por uma nova expressão lógica, que será testada e caso retorne verdadeiro o bloco de código doelif será executado.
Não tem um número máximo de elifs que podemos usar.  

Criando grandes estruturas condicionais, elas aumentam a complexidade do código.

Exemplo:
```Python
opcao = int(input("Informe uma opção: [1] Sacar /n[2] Extrato: "))

if opcao ==1:
    valor = float(input("Informe a quantia para o saque: "))
elif opcao == 2: #se não for a opção 1 pode ser a 2
     print("Exibindo p extrato...")
else:
     sys.exit("Opção inválida")

# exemplo 2
MAIOR_IDADE = 18
IDADE_ESPECIAL = 17

idade = int(input("Informe a sua idade: "))

if idade >= MAIOR_IDADE:
    print("Maior de idade, pode tirar CNH.")

if idade < MAIOR_IDADE:
    print("Ainda não pode tirar a CNH.")


if idade >= MAIOR_IDADE:
    print("Maior de idade, pode tirar CNH.")
else:
    print("Ainda não pode tirar a CNH.")


if idade >= MAIOR_IDADE:
    print("Maior de idade, pode tirar CNH.")
elif idade ==IDADE_ESPECIAL:
    print("Pode fazer aulas teóricas,mas não pode fazer aulas práticas")
else:
    print("Ainda não pode tirar a CNH.")
```
### If Aninhado
Para criar estruturas condicionais aninhadas, temos que adicionar if/elif/else dentro do bloco de código de estrutura if/elif/else.

Exemplo:
```Python
saldo = 500
conta_normal = 400
cheque_especial = 300
conta_universitaria = 100

print("Selecione o tipo de conta.")
print("1 - Conta Normal")
print("2 - Conta Universitaria")
opcao_conta = int(input("Digite a opção (1 ou 2): "))
saque = int(input("Informe o valor que deseja sacar: "))

if conta_normal == 1:
    if saldo >= saque:
        print("Saque realizado com sucesso!")
    elif saque <= (saldo + cheque_especial):
        print("Saque realizado com uso de cheque especial!")
    else:
        print("Saldo insuficiente!")
elif conta_universitaria == 2:
     if saldo >= saque:
            print("Saque realizado com sucesso!")
else:
            print("Saldo insuficiente!")
```

### If Ternário
Ele permite escrever uma condição em uma única linha.
Ele é composto por três partes, a primeira é o retorno caso a expressão retorne verdadeiro, a segunda é a expressão lógica e a terceira é o retorno caso a expressão não seja atendida.

Exemplo:
```Python
saldo = 2000
saque = 500

status = "Sucesso" if saldo >= saque else "Falha"        

print(f"{status} ao realizar o saque!")
>>> Sucesso ao realizar o saque!
