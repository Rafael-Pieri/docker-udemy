## Udemy - Docker: Ferramenta essencial para Desenvolvedores

### Overview
Projeto para Envio de E-mails com Workers.

### Arquitetura
![alt text](https://github.com/Rafael-Pieri/docker-udemy/blob/master/images/worker-architecture.png)

### Como subir a aplicação
Execute o comando abaixo para inicializá-la:

```docker-compose up```


```docker-compose up -d --scale worker=3```

Acessar a aplicação
```localhost```

```docker-compose exec db psql -U postgres email_sender -c 'select * from emails'```
