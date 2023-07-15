# Catálogo de Games - DSlist

Este é o README do projeto de backend desenvolvido durante o intensivo de Java Spring Boot do "DevSuperior". O projeto consiste em um catálogo de games, onde é possível listar, criar e gerenciar listas de jogos.

## Tecnologias Utilizadas

- Java 17
- Spring Boot
- PostgreSQL
- Banco de dados H2

A seguir estão listados os endpoints disponíveis neste projeto:

## GET /games
```
https://localhost:8080/games
```
Retorna a lista de todos os jogos cadastrados.

## GET /games/{id}
```
https://localhost:8080/games/2
```
Retorna as informações de um jogo específico com base no ID.

## GET /lists
```
https://localhost:8080/lists
```
Retorna a lista de todas as listas de jogos cadastradas.

GET /lists/{id}/games
```
https://localhost:8080/lists/1/games
```
Retorna a lista de jogos pertencentes a uma lista específica com base no ID da lista.

## POST /lists/{id}/replacement
```
https://localhost:8080/lists/1/replacement
```
Substitui a posição de dois jogos em uma lista específica com base no ID da lista.

Body (raw, JSON):
```json
{
    "sourceIndex": 3,
    "destinationIndex": 1
}
```

## Executando o Projeto

Para executar o projeto, siga as instruções abaixo:

1. Certifique-se de ter o Java 17 instalado em sua máquina.
2. Configure as informações de conexão com o banco de dados H2 no arquivo `application.properties`.
3. Compile e execute o projeto usando sua IDE de preferência ou execute o comando `mvn spring-boot:run` na raiz do projeto.

Após a execução bem-sucedida, os endpoints estarão disponíveis no `localhost` na porta `8080`.
