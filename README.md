# 🚀 Microsserviços com RabbitMQ + PostgreSQL

Este projeto apresenta a implementação prática de microsserviços desacoplados utilizando RabbitMQ como mensageria e PostgreSQL como base de dados. O objetivo é demonstrar a comunicação entre serviços independentes através do padrão Producer/Consumer.

### 📌 Estrutura do Projeto

🔹 Banco de Dados

Configuração de um PostgreSQL para persistência de dados do microsserviço de pedidos.

🔹 Microsserviço de Pedidos (Producer)

Desenvolvimento do primeiro microsserviço responsável por criar pedidos.

Integração com o RabbitMQ para publicar mensagens.

🔹 RabbitMQ

Configuração do broker e conexão com o CloudAMQP.

Integração do microsserviço de pedidos com o RabbitMQ.

🔹 Microsserviço de Processos (Consumer)

Criação do segundo microsserviço responsável por processar pedidos.

Subida da queue e consumo das mensagens enviadas pelo Producer.

### ⚙️ Fluxo de Comunicação

O Producer (serviço de pedidos) recebe uma requisição e grava os dados no PostgreSQL.

O Producer envia uma mensagem ao RabbitMQ com os dados do pedido.

O Consumer (serviço de processos) escuta a fila, consome a mensagem e processa a requisição.

### 🧪 Testes Realizados

Testes de comunicação entre o Producer e o Consumer.

Validação do envio e consumo de mensagens pelo RabbitMQ.

Testes de persistência no PostgreSQL.

### ✅ Conclusão

O projeto demonstra, na prática, como configurar um ambiente de microsserviços integrados com RabbitMQ e PostgreSQL, explorando a comunicação assíncrona e a escalabilidade da arquitetura distribuída.
