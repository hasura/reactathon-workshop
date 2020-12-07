# reactathon-workshop

What we'll be building: https://learn-hasura-todo-app.netlify.com/

## Prerequisites

- Install the [hasura CLI](https://hasura.io/docs/1.0/graphql/core/hasura-cli/install-hasura-cli.html)

## 1. Backend setup with Hasura

### 1.1 Deploy Hasura + Postgres

Deploy Hasura to [Hasura Cloud](https://cloud.hasura.io) and choose Postgres instance from Heroku

```bash
#Clone this repo
git clone https://github.com/hasura/reactathon-workshop

cd reactathon-workshop/hasura

hasura migrate apply
```

### 1.2 Setup Auth

- Add admin secret to your project via `HASURA_GRAPHQL_ADMIN_SECRET` env.
- Head to [https://hasura.io/jwt-config/](Hasura JWT Config) and enter the Auth0 domain as `graphql-tutorials.auth0.com`
- Configure this JWT config via `HASURA_GRAPHQL_JWT_SECRET` env.

### 1.3 Try out the GraphQL API

- Use Mutations to insert users & todos
- Use Queries to try fetching combinations of users and todos

## 2. Integrating a GraphQL API into your app

[React GraphQL Tutorial](https://hasura.io/learn/graphql/react/introduction/)

### 2.1 Setup app-boilerplate

```bash
cd app-boilerplate
npm install
npm start
```
