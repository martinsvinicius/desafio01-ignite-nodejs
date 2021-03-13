<p align="center">


</p>
<h1 align="center">
  NODEJS - DESAFIO 01
</h1>

<h4 align="center"> 
	<p>Resolução do primeiro desafio da trilha nodejs do bootcamp Ignite 🚀</p>
</h4>

<p align="center">
 <a href="#sobre">Sobre</a> •
 <a href="#features">Features</a> •
 <a href="#rotas">Rotas</a> •
 <a href="#autor">Autor</a>
</p>

## 💻 Sobre

Esta aplicação gerencia tarefas (em inglês *todos*). É permitido a criação de usuários com ```name``` e ```username```, bem como o CRUD de *todos*.

---

## 🚀 Features

Recursos disponíveis:
- Criar um novo *todo*;
- Listar todos os *todos*;
- Alterar o `title` e `deadline` de um *todo* existente;
- Marcar um *todo* com feito;
- Excluir um *todo*.

## 🚨 Rotas

### POST `/users`

A rota recebe `name`, e `username` dentro do corpo da requisição. Ao cadastrar um novo usuário, ela armazena os dados dentro de um objeto no seguinte formato:

```js
{ 
	id: 'uuid', // precisa ser um uuid
	name: 'Danilo Vieira', 
	username: 'danilo', 
	todos: []
} 
```

### GET `/todos`

A rota recebe, pelo header da requisição, uma propriedade `username` contendo o username do usuário e retornar uma lista com todas as tarefas desse usuário.

### POST `/todos`

A rota recebe `title` e `deadline` dentro do corpo da requisição e, uma propriedade `username` contendo o username do usuário dentro do header da requisição. Ao criar um novo *todo*, ele é armazenado na lista `todos` do usuário que está criando essa tarefa. Cada tarefa tem o seguinte formato:

```js
{ 
	id: 'uuid', // precisa ser um uuid
	title: 'Nome da tarefa',
	done: false, 
	deadline: '2021-02-27T00:00:00.000Z', 
	created_at: '2021-02-22T00:00:00.000Z'
}
``` 
**OBS**: Ao fazer a requisição, preencha a data de `deadline` com o formato `ANO-MÊS-DIA`.

### PUT `/todos/:id`

A rota recebe, pelo header da requisição, uma propriedade `username` contendo o username do usuário e recebe as propriedades `title` e `deadline` dentro do corpo. É alterado **apenas** o `title` e o `deadline` da tarefa que possua o `id` igual ao `id` presente nos parâmetros da rota.

### PATCH `/todos/:id/done`

A rota recebe, pelo header da requisição, uma propriedade `username` contendo o username do usuário e alterar a propriedade `done` para `true` no *todo* que possuir um `id` igual ao `id` presente nos parâmetros da rota.

### DELETE `/todos/:id`

A rota recebe, pelo header da requisição, uma propriedade `username` contendo o username do usuário e exclui o *todo* que possuir um `id` igual ao `id` presente nos parâmetros da rota.

---

## 🦸 Autor

<a href="https://instagram.com/martnght">
 <img style="border-radius: 50%;" src="https://media-exp1.licdn.com/dms/image/C4D03AQFhuoTOAycSKw/profile-displayphoto-shrink_200_200/0/1609172591651?e=1615420800&v=beta&t=woKzi7EwtBMQ01ARYyi9cZGYKKY03D4t85xXP1EsFSM" width="100px;" alt=""/>
 <b>Vinicius Victor</b></a> 
 <br />
 <br />


<a href="https://www.twitter.com/martnght/">
  <img alt="Siga no Twitter" src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white">
</a>

<a href="mailto:vinicius.victor.sm@gmail.com">
  <img alt="GitHub last commit" src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white">
</a>

<a href="https://www.linkedin.com/in/vinicius5g">
  <img alt="Perfil Linkedin" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white">
</a>