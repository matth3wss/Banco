## Universidade Federal da Fronteira Sul

# Exercício sobre herança

```
Implementar um conjunto de classes que representem os tipos de conta de um banco. O
diagrama UML abaixo representa as classes do sistema.
```
## Descrição das classes

## Conta

```
O atributo saldo indica quanto o cliente possui na conta.
O método depositar() adiciona um valor ao saldo da conta.
O método sacar() retira valor da conta do cliente, se houver saldo disponível; o método
retorna true se conseguiu sacar ou false se não conseguiu.
O método resumoExtrato() mostra o nome do cliente e o saldo atual da conta.
O método fazManutencao() não executa ação alguma nessa classe, devendo ser sobrescrito
nas subclasses.
A classe deve ter também um construtor.
```
## ContaEspecial

```
O atributo limite indica um crédito extra que o cliente pode utilizar no momento do saque.
Portanto, o método sacar() deve ser sobrescrito a fim de incorporar esta característica.
```

## Universidade Federal da Fronteira Sul

## Ciência da Computação

```
Programação I
```
O atributo **taxaManutencao** é um valor em R$ que o banco cobra do cliente durante cada
manutenção. O método **fazManutencao()** da classe **ContaEspecial** deve descontar do saldo
do cliente o valor estipulado na propriedade **taxaManutencao**.
O método **resumoExtrato()** da classe **ContaEspecial** deve imprimir, além do nome do
cliente e saldo atual, o saldo extra disponibilizado pela propriedade limite e o valor da taxa
de manutenção.
A classe deve ter um construtor, conforme o diagrama.

## Investimento

O atributo **taxaRendimento** indica uma porcentagem que o cliente irá ganhar sobre seu saldo
durante cada manutenção.
O método **fazManutenção()** da classe **Investimento** deve aplicar o rendimento ao saldo da
conta.
O método **resumoExtrato()** da classe **Investimento** deve imprimir, além do saldo atual e
nome do cliente, qual é a porcentagem de rendimento.
A classe deve ter um construtor, conforme diagrama.

## Classe de Teste

Crie uma classe para instanciar e manipular 1 exemplo de objeto do tipo Conta, um do tipo
ContaEspecial e um do tipo Investimento.

* Crie os gets e sets que forem necessários em seus testes.

# Exercício sobre herança - Continuação

```
Com base no exercício anterior, realizar as seguintes alterações:
```
- Tornar a classe **Conta** abstrata.
- Tornar o método **fazManutencao** abstrato.
- Criar uma classe **Cliente** (atributos nome e CPF) e realizar uma associação bidirecional
    entre **Cliente** e **Conta**.
- Criar uma classe **CarteiraPrime** , a qual será uma agregação de **Clientes** (pode
    utilizar ArrayList). A classe deve conter um método **adicionar()** e um **listar()** que
    mostra todos os clientes prime.
- Criar uma Classe **Movimentacao** que registra a data (string), o valor e o tipo de
    operação (crédito ou débito). Cada conta deve conter uma composição de
    Movimentações (pode utilizar ArrayList). A cada operação de depósito, saque ou
    manutenção, um novo objeto **Movimentacao** deve ser adicionado a esta lista.
- Adicionar um método **extrato()** à classe **Conta** , o qual apresenta a lista de todas as
    movimentações
    
## Classe de Teste

Instanciar 2 **Clientes**.

Criar uma **ContaEspecial** e uma conta de **Investimento** e associar ao mesmo cliente.
Realizar algumas operações para testar os métodos. Chamar o método **extrato()** para
visualizar a lista de movimentações.

Adicionar os clientes à **CarteiraPrime** e listá-los.




