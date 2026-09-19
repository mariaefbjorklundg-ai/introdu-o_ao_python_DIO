## Estética
Identar o código mantém o código fonte mais legível e manutenível. Em Python, através da identação o interpretador consegue determinar onde um bloco de comando inici e onde ele termina.

#### Bloco de Comando
Linguagens de Programação costumam utilizar caracteres ou palavras reservadas para terminar o inicio e fim do bloco.

* Bloco em Java: utiliza {}
```Java
void sacar(double valor) {  // inicio do bloco do metodo
     if(this.saldo >= valor) { // inicio do bloco if
        this.saldo -= valor;

     } // fim do bloco do if
} // fim do bloco do metodo

// Bloco em Java sem formatar: fica pior de ler
void sacar(double valor) { // inicio do bloco do metodo
if(this.saldo >= valor) { // inicio do bloco if
this.saldo -= valor;
}  // fim do bloco do if
} // fim do bloco do metodo
```
#### Utilizando Espaços em Python
Há uma convenção em Python, onde define as boas práticas para escrita de código na linguagem. É indicado utilizar 4 espaços em branco por nível de indentação, a cada novo bloco adicionamos 4 novos espaços em branco.
* Bloco em Python
```Python
#essa seria a versão mais fácil de ler
def sacar(self, valor: float) None: #inicio do bloco do metodo
    if self.saldo >= valor: #inicio do bloco if
       self.saldo -= valor
    #fim do bloco do if
#fim do bloco do metodo

# Isso não funciona em Python
def sacar(self, valor: float) None: #inicio do bloco do metodo
if self.saldo >= valor: #inicio do bloco if
self.saldo -= valor
#fim do bloco do if
#fim do bloco do metodo
