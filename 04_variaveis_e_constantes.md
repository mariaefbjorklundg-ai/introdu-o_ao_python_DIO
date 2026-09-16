## Variáveis e Constantes 

### Variáveis 
Nas linguagens de programação podemos definir valores que podem sofrer alterações no decorrer da execução do programa. Esses valores se chamam Variáveis, porque eles nascem com um valor e não precisam necessariamente permanecer com ele durante a execução do programa.

Exemplo:
```Python

age = 21
name = 'Maria'
print(f'Meu nome é {name} e eu tenho {age} ano(s) de idade.')
>>> Meu nome é Maria e eu tenho 21 ano(s) de idade.

age, name = (21, 'Maria')
print(f'Meu nome é {name} e eu tenho {age} ano(s) de idade.')
>>> Meu nome é Maria e eu tenho 21 ano(s) de idade
```

* Alternando os Valores:

Não precisamos definir o tipo de dados da variável, o Python faz isso sozinho. Por isso não podemos criar uma variável sem atribuir um valor. Para alterar o valor da variável basta fazer uma atribuição de um novo valor.

Isso faz dela um valor Mutável

Exemplo:
```Python

age = 21
name = 'Maria'
print(f'Meu nome é {name} e eu tenho {age} ano(s) de idade.')
>>> Meu nome é Maria e eu tenho 21 ano(s) de idade.

age = 30
name = 'Sergio'
print(f'Meu nome é {name} e eu tenho {age} ano(s) de idade.')
>>> Meu nome é Sergio e eu tenho 30 ano(s) de idade. #como mexemos nos valores isso mudou o resultado!
```

### Constantes
Constantes são utilizadas para armazenar valores. 

Uma constante não pode mudar de valor, quando é determinado um valor pra ela, ela permanece com esse valor até o final da execução do programa, tornando ela um valor imutável.

Em python não existe uma palavra fixa para informar ao programador que o valor é constante. Por isso utilizamos a convenção que diz ao programador que a variável é uma constante. Para fazer isso, devemos criar uma variávelcom o nome todo em letrar maiúsculas.

 Ele é mais utilizado para valores que não mudam, como em um site os estados de envio do produto.

Exemplo parecido com a Variável;
```Python

AGE = 21
NAME = 'Maria'
print(f'Meu nome é {name} e eu tenho {age} ano(s) de idade.')
>>> Meu nome é Maria e eu tenho 21 ano(s) de idade.

age = 30
name = 'Sergio'
>>> Meu nome é Maria e eu tenho 21 ano(s) de idade.

BRAZILIAN_STATES = ["SP", "SC", "RS"]
>>> ['SP', 'SC', 'RS']
```

### Padrões no Pythons
* O padrão de nomes deve ser em snake case (que seria o  _ , Produto_1)
* Escolher nomes sugestivos (para você não esquecer os nomes que você criou, e para ajudar a não criar varios codigos sendo que poderia ter um só. E é preferivel não abreviar os nomes pois é provavel que esqueça mais rapido)
* Nome da constante todo em Maiúsculo
