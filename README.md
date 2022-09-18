***Projeto kube-news***
*Sobre o projeto*
O projeto conversão de temperatura é um projeto desenvolvido em NodeJS e um banco Postgres.

*Observações do projeto*
A aplicação é exposta usando a porta 8080

**srv/Dockerfile**
```
FROM node:16.15.0
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node", "server.js"]
```

**Docker Hub - [giozandonai/kube-news](https://hub.docker.com/u/giozandonai/kube-news)**

**Github - [giozandonai/kube-news](https://github.com/giozandonai/kube-news)**

**Rodando compose:**
`$ docker-compose --env-file .env up -d`

**Acessando a aplicação:**
`http://localhost:8080`

**Acessando pgadmin:**
`http://localhost:8090`
