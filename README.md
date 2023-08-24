# CRUD-SpringAngular
# Desenvolvimento Backend com Spring Boot

Este repositório contém a implementação do backend de uma aplicação Spring Boot para gerenciamento de dados de clientes. A aplicação oferece operações CRUD (Criar, Ler, Atualizar, Excluir) para a entidade "Cliente".

## Tecnologias Utilizadas

- Spring Boot
- Spring Data JPA
- Banco de Dados MySQL

## Pré-requisitos

- Java JDK (versão 17 ou superior)
- Banco de Dados MySQL
- Maven (para construir e executar o projeto)

## Começando

1. **Clonar o Repositório:**

   ```bash
   git clone https://github.com/your-username/your-project.git
   cd your-project

2. **Configuração do Banco de Dados:**

- Crie um banco de dados MySQL com o nome `projeto_angular_spring`.
- Atualize o `spring.datasource.username` e `spring.datasource.password` no arquivo `application.properties` com suas credenciais de banco de dados.

3. **Construir e Executar:**

Você pode usar o Maven para construir e executar a aplicação.

    ```bash
    mvn spring-boot:run
    A aplicação será iniciada em http://localhost:8080.

## Endpoints da API

- **POST /:**
  Cria um novo Cliente.

- **GET /:**
  Recupera uma lista de todos os clientes.

- **PUT /:**
  Atualiza um Cliente existente.

- **DELETE /{codigo}:**
  Exclui um Cliente pelo seu código único.

## Entidade: Cliente

A entidade Cliente representa dados de clientes com os seguintes campos:

- `codigo` (gerado automaticamente)
- `nome`
- `idade`
- `email`
- `cidade`

## Arquivos Importantes

1. `Controle.java`:
   Este arquivo contém a classe de controle principal que lida com as requisições HTTP e as mapeia para os métodos correspondentes para operações CRUD.

2. `Cliente.java`:
   Este arquivo define a classe de entidade Cliente usando anotações JPA.

3. `Repositorio.java`:
   Este arquivo define a interface do repositório para operações CRUD na entidade Cliente.

4. `ApiApplication.java`:
   Este arquivo contém o ponto de entrada principal da aplicação Spring Boot.

5. `application.properties`:
   Arquivo de configuração do Spring Boot, incluindo configurações de conexão com banco de dados e comportamento do Hibernate DDL.

## Gerenciamento de Banco de Dados

A propriedade `spring.jpa.hibernate.ddl-auto` no arquivo `application.properties` está configurada como `update`, o que significa que o Hibernate criará ou atualizará automaticamente o esquema do banco de dados com base nas classes de entidade. Certifique-se de alterar esse comportamento para uma abordagem mais controlada em um ambiente de produção.

## Compartilhamento de Recursos de Origem Cruzada (CORS)

A anotação `@CrossOrigin` é usada para permitir solicitações de origens cruzadas de qualquer fonte. Em um ambiente de produção, você deve restringir as origens permitidas por motivos de segurança.

## Contribuição

Sinta-se à vontade para contribuir para este projeto, abrindo problemas ou solicitações de pull. Suas contribuições são bem-vindas!
