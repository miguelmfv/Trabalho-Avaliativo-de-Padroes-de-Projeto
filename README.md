# Trabalho de Padrões de Projeto
Este projeto é uma aplicação Java desenvolvida com o objetivo de simular um sistema de compras, com suporte para registro de usuários, login, cadastro de produtos, realização de pedidos e notificação de administradores. A aplicação é executada em modo console e utiliza o JPA (Java Persistence API) para comunicação com o banco de dados.

## 📌 Funcionalidades

- Cadastro e login de usuários.
- Registro de produtos.
- Realização de pedidos com escolha de quantidade e produto.
- Adição opcional de embalagem para presente.
- Notificação de administradores sobre novos pedidos.
- Uso de um menu interativo no console.

## 💡 Padrões de Projeto Utilizados

Este projeto aplica diversos padrões de design para promover organização, escalabilidade e reutilização de código:

### ✅ **DAO (Data Access Object)**
Utilizado indiretamente com JPA para abstrair a persistência dos dados via `EntityManager`.

### ✅ **Service Layer**
Todas as regras de negócio estão concentradas nas classes `*Service`, separando a lógica de negócio da camada de apresentação.

### ✅ **Observer**
O padrão Observer foi usado para notificar automaticamente todos os administradores quando um novo pedido é criado. 

### ✅ **Decorator**
Utilizado para adicionar funcionalidades extras ao pedido sem alterar a classe original. 

### ✅ **Adapter**
Adaptador que conecta a entidade `Pedido` à interface `PedidoComponent`, usada pelo Decorator.

