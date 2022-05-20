## Monorepo with React and Graphql

Criar pasta do projeto

Entrar na pasta

yarn init -y

adicionar no arquivo pacjage.json 

```
"private": true,
"workspaces": {
  "packages": [
    "packages/*"
  ]
}
```

private - flag necessária para inidicar que ele não é um projeto publico.

packages/* - Dentro da pasta package todas são parte do meu monorepo. 

Criar a pasta package

Criar arquivo .gitignore com:

node_modules
dist
yarn-error.log

Entrar na pasta package

Criar pasta server

Criar pasta web

Criar pasta src dentro de server

Entrar em server e executar: yarn init -y

Trocar nome no package.json do server para: @monorepo/server

Instalar o express: yarn add express

Instalar o cors: yarn add cors

Instalar o axios: yarn add @monorepo/axios-config

Instalar typescript do express como dependencia de desenvolvimento: yarn add @types/express -D

Ir para a pasta Web

yarn init -y

yarn add react react-dom

yarn add @types/react -D

// Alguns pacotes para facilitar o desenvolvimento
// Que serve para criar uma aplicação React do Zero 
yarn add webpack webpack-cli webpack-dev-server html-webpack-plugin @pmmmwh/react-refresh-webpack-plugin @babel/core @babel/preset-env @babel/preset-react @babel/preset-typescript @types/react @types/react-dom babel-loader react-refresh -D 

Criar script de start do react adicionando 

```
"scripts": {
	"start": "webpack-dev-server --mode development"
},

```