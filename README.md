## Udemy - Docker: Ferramenta essencial para Desenvolvedores

### Overview
Projeto para Envio de E-mails com Workers.

### Arquitetura
![alt text](https://github.com/Rafael-Pieri/docker-udemy/blob/master/images/arquitetura.png)

### Como subir a aplicação
Execute o comando abaixo para subir os componentes da aplicação:
```docker-compose up```

Caso queira escalar os workers, execute o comando abaixo informando a quantidade de instâncias:
```docker-compose up -d --scale worker=3```

Com a aplicação inicializada, acesse-a em:
```localhost```

Será apresentada a página abaixo:
![alt text](https://github.com/Rafael-Pieri/docker-udemy/blob/master/images/pagina-enviador-email.png)

Ao informar o assunto e a mensagem, clique em 'Enviar'. A página abaixo será apresentada:
![alt text](https://github.com/Rafael-Pieri/docker-udemy/blob/master/images/mensagem-enviada.png)

Para consultar a mensagem salva no banco de dados, execute o seguinte comando:
```docker-compose exec db psql -U postgres email_sender -c 'select * from emails'```

![alt text](https://github.com/Rafael-Pieri/docker-udemy/blob/master/images/mensagem-salva-db.png)
