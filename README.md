# Cardápio Digital

![Java](https://img.shields.io/badge/Java-17-blue)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2.4-brightgreen)
![MySQL](https://img.shields.io/badge/MySQL-8.0-orange)
![PRs](https://img.shields.io/badge/PRs-welcome-brightgreen)

## Descrição

O **Cardápio Digital** é uma aplicação backend desenvolvida em Java utilizando o framework Spring Boot. Esta aplicação serve como base para um cardápio digital, permitindo a gestão de alimentos (Food) com funcionalidades de criação e listagem de itens do cardápio. 

A aplicação utiliza o banco de dados MySQL para persistência dos dados e segue a arquitetura RESTful para comunicação.

## Tecnologias Utilizadas

- **Linguagem:** Java 17
- **Framework:** Spring Boot 3.2.4
- **Banco de Dados:** MySQL 8.0
- **Gerenciamento de Dependências:** Maven

## Pré-requisitos

Antes de iniciar a instalação, certifique-se de que você possui os seguintes itens instalados em sua máquina:

- Java 17
- Maven
- MySQL

## Instalação

Siga os passos abaixo para configurar o projeto em sua máquina local:

1. Clone o repositório:
    ```bash
    git clone https://github.com/seu-usuario/cardapio-digital.git
    cd cardapio-digital
    ```

2. Configure o banco de dados MySQL:
    ```sql
    CREATE DATABASE food;
    CREATE USER 'root'@'localhost' IDENTIFIED BY 'root';
    GRANT ALL PRIVILEGES ON food.* TO 'root'@'localhost';
    ```

3. Configure as credenciais do banco de dados no arquivo `application.properties`:
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/food
    spring.datasource.username=root
    spring.datasource.password=root
    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
    ```

4. Compile e execute a aplicação:
    ```bash
    mvn spring-boot:run
    ```

## Como Utilizar

### Adicionar um novo alimento

Para adicionar um novo item ao cardápio, envie uma requisição POST para o endpoint `/food` com o seguinte payload:
```json
{
  "title": "Pizza Margherita",
  "image": "url_da_imagem",
  "price": 3500
}
```

## Listar todos os alimentos
Para listar todos os itens do cardápio, envie uma requisição GET para o endpoint /food. A resposta será uma lista de itens:
```bash
[
  {
    "id": 1,
    "title": "Pizza Margherita",
    "image": "url_da_imagem",
    "price": 3500
  },
  {
    "id": 2,
    "title": "Lasanha",
    "image": "url_da_imagem",
    "price": 4500
  }
]
```

## Contribuição
Contribuições são bem-vindas! Siga os passos abaixo para contribuir com o projeto:<br>
Fork este repositório.<br>
Crie uma branch com a sua feature: git checkout -b minha-feature<br>
Commit suas mudanças: git commit -m 'Adiciona nova feature'<br>
Faça um push para a branch: git push origin minha-feature<br>
Abra um Pull Request.<br>

### Link do repositório(front-end) 




