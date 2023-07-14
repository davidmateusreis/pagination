# Paginação com Spring Data  

O projeto foi elaborado [nesse vídeo](https://youtu.be/Jrhb5YJK5II) que mostra como criar um serviço web com paginação usando Spring Data.

## Tecnologias

- [Spring Boot](https://spring.io/projects/spring-boot)
- [Spring Data JDBC](https://spring.io/projects/spring-data-jdbc)

## O que foi criado

Um serviço web de consulta com suporte a paginação usando Spring Data. O serviço lista os posts dos usuários de forma paginada.

## Como executar

- Clonar repositório
- Construir o projeto
```
$ ./mvnw clean package
```
- Executar a aplicação
```
$ java -jar target/pagination-0.0.1-SNAPSHOT.jar
```
## API Endpoint

A requisição HTTP abaixo foi feita usando o [httpie](https://httpie.io)

- Listar posts
```
http GET ":8080/posts?page=0&size=2"

HTTP/1.1 200
Connection: keep-alive
Content-Type: application/json
Date: Fri, 14 Jul 2023 18:40:24 GMT
Keep-Alive: timeout=60
Transfer-Encoding: chunked

[
    {
        "author": "David",
        "content": "Lorem ipsum dolor sit.",
        "id": 1
    },
    {
        "author": "David",
        "content": "Lorem ipsum dolor sit.",
        "id": 2
    }
]
```