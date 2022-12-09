# Cloud-Parking

Projeto desenvolvido como desafio durante o bootcamp da Digital Innovation One, com o objetivo de gerenciar a entrada e saída de carros em um estacionamento.

### 🚀 Começando

Para executar e testar o projeto será necessário baixar as dependencias listadas/contidas no arquivo [pom.xml](https://github.com/leobrunno/bet-api/blob/main/pom.xml), ter instalado o Java 11 e utilizar um API Client como o [Postman](https://www.postman.com/) ou [Insomnia](https://insomnia.rest/) para gerar requisições.
Na pasta raiz do projeto, há o arquivo [docker-compose.yml](https://github.com/leobrunno/cloud-parking/blob/main/docker-compose.yml).

Utilizando o comando: 
```
$ docker-compose up
```
Será iniciado um container com a imagem do PostgreSQL:11-alpine e o PGAdmin. Sendo o postgresql disponivel na porta 5432 e o PGAdmin na porta 15432
a partir das credenciais listadas no arquivo [docker-compose.yml](https://github.com/leobrunno/cloud-parking/blob/main/docker-compose.yml).

Ao iniciar a aplicação, é possível acessar as rotas disponiveis e documentadas com Swagger a partir do endereço http://localhost:8080/swagger-ui.html . Para realizar requisições, será pedido as credenciais de acesso, listadas no arquivo [application.properties](https://github.com/leobrunno/cloud-parking/blob/main/src/main/resources/application.properties), sendo elas:
```
spring.security.user.password=crf@574
spring.security.user.roles="USER"
```

### 🔧 Testes
Na implementação dos testes foi utilizada a dependencia Test Containers, para que caso haja indisponibilidade do banco utilizado para desenvolvimento, um container com a imagem definida na classe de configuração seja levantado e os testes ainda possam ser executados.
Foi criada a classe de configuração [AbstractContainerBase.java](https://github.com/leobrunno/cloud-parking/blob/main/src/test/java/one/digitalinnovation/parking/controller/AbstractContainerBase.java),
nesse arquivo é definido qual imagem iremos utilizar para o container e redefinida as propriedades de conexão durante a execução dos testes.


### 🛠️ Construído com

Para a construção do projeto foi utilizado as seguintes tecnologias:

* [Java 11](https://www.oracle.com/br/java/)
* [Springboot 2.6.13](https://spring.io/)
* [PostgreSQL](https://www.postgresql.org/)

### 📋 Dependências

As dependências do projeto estão no arquivo [pom.xml](https://github.com/leobrunno/cloud-parking/blob/main/pom.xml) sendo compostas por:

* [Spring Boot Starter Data JPA](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-data-jpa)
* [Spring Boot Starter Web](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-web)
* [Spring Boot Starter Test](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-test)
* [ModelMapper](https://mvnrepository.com/artifact/org.modelmapper/modelmapper)
* [Springfox Swagger Ui](https://mvnrepository.com/artifact/io.springfox/springfox-swagger-ui/2.9.2)
* [Springfox Swagger2](https://mvnrepository.com/artifact/io.springfox/springfox-swagger2/2.9.2)
* [PostgreSQL](https://mvnrepository.com/artifact/org.postgresql/postgresql)
* [Test Containers](https://mvnrepository.com/artifact/org.testcontainers/postgresql/1.17.6)
* [Rest Assured](https://mvnrepository.com/artifact/io.rest-assured/rest-assured)
* [Spring Security](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-security)

### 📄 Licença

Este projeto está sob a licença  MIT.
