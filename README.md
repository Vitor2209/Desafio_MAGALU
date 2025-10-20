🗓️ Agendador de Notificações

Este projeto foi desenvolvido como parte de um desafio técnico com o objetivo de demonstrar habilidades de desenvolvimento Java Backend.
O sistema tem como propósito cadastrar e gerenciar notificações que serão enviadas posteriormente com base em um agendamento definido.

🚀 Tecnologias Utilizadas

Java 17+

Spring Boot

Maven

Docker & Docker Compose

Banco de Dados (por exemplo, PostgreSQL ou H2)

JUnit / Mockito para testes automatizados

⚙️ Executando o Projeto Localmente
1️⃣ Clone o repositório
git clone https://link-para-o-projeto

2️⃣ Acesse o diretório do projeto
cd agendador-notificacoes

3️⃣ Suba os containers com Docker
docker-compose up --build


O serviço será iniciado e estará disponível em:

http://localhost:8080

📚 Documentação da API
📌 Cadastrar nova notificação

Endpoint:
POST /agendamento

Body (JSON):

Campo	Tipo	Obrigatório	Descrição
emailDestinatario	string	✅	Email do destinatário da notificação
telefoneDestinatario	string	✅	Telefone do destinatário da notificação
mensagem	string	✅	Conteúdo da notificação
dataHoraEvento	LocalDateTime	✅	Data e hora do evento no formato dd-MM-yyyy HH:mm:ss

Exemplo de requisição:

{
  "emailDestinatario": "usuario@teste.com",
  "telefoneDestinatario": "11999999999",
  "mensagem": "Seu evento está próximo!",
  "dataHoraEvento": "20-10-2025 14:30:00"
}

🔍 Buscar notificação por ID

Endpoint:
GET /agendamento/{id}

Parâmetros:

Parâmetro	Tipo	Obrigatório	Descrição
id	string	✅	ID da notificação a ser consultada

Exemplo:

GET /agendamento/123

❌ Cancelar notificação por ID

Endpoint:
DELETE /agendamento/{id}

Parâmetros:

Parâmetro	Tipo	Obrigatório	Descrição
id	string	✅	ID da notificação a ser cancelada

Exemplo:

DELETE /agendamento/123

🧪 Executando os Testes

Para rodar os testes automatizados, execute o comando abaixo:

mvn test


Os testes cobrem camadas de serviço, repositório e controladores, garantindo o bom funcionamento do sistema.

🧰 Estrutura do Projeto
agendador-notificacoes/
│
├── src/
│   ├── main/
│   │   ├── java/com/exemplo/agendador/
│   │   │   ├── controller/
│   │   │   ├── service/
│   │   │   ├── model/
│   │   │   └── repository/
│   │   └── resources/
│   │       ├── application.yml
│   │       └── data.sql
│   └── test/
│       └── java/com/exemplo/agendador/
│
├── docker-compose.yml
├── pom.xml
└── README.md

📄 Licença

Este projeto é distribuído sob a licença MIT.
Sinta-se à vontade para usá-lo e modificá-lo conforme necessário.

✨ Autor

Seu Nome
💼 Vitor2209
📧 vitordutra1125@gmail.com