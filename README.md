# API TodoList

Este repositório contém a documentação da API TodoList, uma API RESTful de lista de tarefas que permite ao usuário inserir suas tarefas e ter a garantia que somente ele as veja.

## Menu

* [Objetivo](#objetivo)
* [Tecnologias](#tecnologias)
* [Como utilizar](#como-utilizar)
* [Autor](#autor)

## Objetivo

O objetivo desta API é fornecer uma maneira segura e fácil para os usuários criarem e gerenciarem suas listas de tarefas. A API é baseada no protocolo REST e usa o padrão de autenticação Basic Auth para garantir a segurança das informações dos usuários.

## Tecnologias

A API TodoList foi desenvolvida usando as seguintes tecnologias:

* Java 17
* Spring Framework
* Render (deploy)
* Basic Auth
* H2 Database

## Como utilizar

Para utilizar a API TodoList, é necessário primeiramente criar um usuário. Para isso, faça uma requisição do tipo `POST` para a URL `https://todolist-5k4j.onrender.com/users/`, com o seguinte corpo:
```json
{
    "name": "Nome desejado",
    "username": "userDesejado",
    "password": "senha"
}
```

Após criar um usuário, você pode começar a criar tarefas. Para isso, faça uma requisição do tipo `POST` para a URL `https://todolist-5k4j.onrender.com/tasks/`, com o seguinte corpo:

```json
{
    "description": "Assistir a aula da Rocketseat referente a REST",
    "title": "Assistir a aula",
    "priority": "ALTA",
    "startAt": "2023-10-20T10:15:00",
    "endAt": "2023-10-30T13:15:00"
}
```

Para consultar todas as tarefas do usuário logado, faça uma requisição do tipo `GET` para a URL `https://todolist-5k4j.onrender.com/tasks/`.

Para editar informações de uma tarefa, faça uma requisição do tipo `PUT` para a URL `https://todolist-5k4j.onrender.com/tasks/` e adicionando o id da tarefa no corpo da requisição.
Exemplo:
```json
    {
        "title": "Aula de Tasks",
        "description": "aqui vai a descrição da tarefa"
    }
```

## Autor

Este projeto foi desenvolvido por Felipe Feyh.
