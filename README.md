#Imersão-FullStack-FullCycle

# Repositório do Kafka e Kafka Connect

## Configuração

```
$ sudo nano /etc/hosts
```

Adicionar: 
```
127.0.0.1   host.docker.internal
```

## Subir a aplicação

```
docker-compose up
```

Espere um pouco antes de testar o Control Center no endereço: http://localhost:9021. Configure um client no painel de developers do Twitter: https://developer.twitter.com/en, antes de criar um connector do Twitter no painel do Kafka Connect.

Crie o connector do Twitter, depois o do MongoDB (necessário iniciar o serviço do MongoDB do [docker-compose.yaml](https://github.com/wr2net/nest-api-fullcycle6/blob/master/docker-compose.yml) do Nest.js).

Verifique se o tópico tweets foi criado com os novos tweets capturados (lembre-se de não deixar ativo muito tempo para testar, senão o Twitter pode bloquear).

Toda vez que parar os containers do Kafka, é necessário executar o comando docker-compose down antes.