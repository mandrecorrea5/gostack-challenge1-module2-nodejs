# GoStack - Desafio 1 | Módulo 2 - Backend com Node JS
> Primeiro desafio de NodeJS do módulo 2.

    Esse desafio teve por objetivo fazer entradas e saídas de valores, uma conta corrente, mas pra isso algumas regras precisariam ser implementadas, segue:
    
    1 - Implementar método para entrada e saída de dados
    2 - Não permitir retirar um valor que seja maior que o total do balanço
    3 - recuperar um extrato com todas as transações e com o balanço por tipo
    

## Methods and Rules

    POST /transactions: A rota é responsável por fazer fazer as entradas e saídas de valores.
    > body: {title, value, type}
    > type: income ou outcome
    > rule: não pode permitir que um outcome seja efetuado se o valor for maior que o total do balance
    
    GET /transactions: A rota deve retornar todas as transações como balanço
```
{
  "transactions": [
    {
      id 
      title 
      value 
      type 
    },    
  ],
  "balance": {
    income 
    outcome
    total
  }
}
```

## Tests

`should be able to create a new transaction`: Teste verifica se todas as regras para criar uma transaction estão ok
`should be able to list the transactions`: Teste verifica se o retorno das transactions está correto
`should not be able to create outcome transaction without a valid balance`: Teste verifica se foi implementada a regra de verificação do saque ser maior que o total

## Setup Project

### Project struture
    src
    src/__tests__
    src/__tests__/Transaction.spec.ts
    src/models/Transaction.ts
    src/repositories/TransactionRepository.ts
    src/routes/index.ts
    src/routes/transaction.routes.ts
    src/services/CreateTransactionService.ts
    src/app.ts
    src/server.ts
    
### Require instalations

- __[Node](https://nodejs.org/en/)__
- __[Yarn](https://yarnpkg.com)__

### Libs require

- __[Typescript](https://www.typescriptlang.org)__
- __[Express](https://expressjs.com)__
- __[Uuidv4](https://www.npmjs.com/package/uuidv4)__
- __[Jest](https://jestjs.io)__
- __[TSNode](https://www.npmjs.com/package/ts-node)__

### Instalation

```yarn install```
    
### Run Project

```yarn dev:server```

### Run Tests

```yarn tests```

  
    
