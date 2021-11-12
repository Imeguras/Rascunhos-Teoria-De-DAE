## Identity Map

### Unit of work

basicamente ele vai guardando alterações em vez de o fazer diretamente, quando se faz commit(); elas sao executadas (por exemplo um carrinho de compras)

### Caller registration

O client app e que tem a responsabilidade de registar

### Object registration

O objeto e que faz a registação, ou seja quando se faz load o objeto torna-se limpo

### Unit Of Work Controller

E basicamente faz um diff, faz um clone e deixa tudo acontecer ao se fazer commit diff sao executados e conflicts sao resolvidos

## Gateways

### Active Record
