
#### Translation for: **[English](https://github.com/alisonbuss/quickstart-drone-ci/blob/master/README_LANG_EN.md)**.

# Quickstart Drone CI.

Quickstart of a Continuous Delivery service (Drone CI) with Gitea and Traefik(v2. *), using Docker Compose and Swarm.


#### Status do Projeto: *(Desenvolvimento)*.

# Exibir informações gerais do ambiente Docker.
docker image ls && docker network ls && docker volume ls && docker container ls;

# Valide e visualize o arquivo de composição.
docker-compose --file ./docker-compose.yml config;

# Criar ou reconstruir serviços e construa imagens em paralelo.
docker-compose --file ./docker-compose.yml build --parallel;

# Criar ou reconstruir serviços no modo desanexado.
docker-compose --file ./docker-compose.yml up --detach;

# Lista todos os containers do Compose.
docker-compose --file ./docker-compose.yml ps;

# Imprimir a versão do Traefik em atividade.
docker exec <"OBTENHA O ID DO COMANDO ANTERIOR"> traefik version;

# Imprimir o log do Traefik em atividade.
docker exec <"ID DE UM DETERMINADO CONTÊINER"> cat /var/log/traefik/traefik.log;

docker exec <"ID DE UM DETERMINADO CONTÊINER"> ls /var/log/postgresql

docker exec 823 ls /var/log/postgresql

# Testar se a aplicação está funcionando.
curl -H Host:whoami.docker.localhost https://127.0.0.1 --insecure;

# Parar e remover contêineres, redes, imagens e volumes.
docker-compose --file ./docker-compose.yml down;
docker-compose --file ./docker-compose.yml rm -f;

# DANDO UMA LIMPADA NO AMBIENTE:
# Esse comando remove todos os contêineres parados, redes não utilizadas, imagens pendentes e caches de compilação...
# É o satanais!!!
docker system prune -a;

## OU...
docker stop $(docker ps -a -q) && docker rm $(docker ps -a -q) && docker rmi $(docker images -q);

docker container stop
docker container prune
docker volume prune
docker image prune
docker network prune

    

https://developer.okta.com/blog/2017/10/11/developers-guide-to-docker-part-3

https://blog.anoff.io/2019-03-24-self-hosted-gitea-drone/


https://blog.anoff.io/2019-03-24-self-hosted-gitea-drone/

https://www.optimadata.nl/blogs/3/nlm8ci-how-to-run-postgres-on-docker-part-3

https://www.depesz.com/2011/05/06/understanding-postgresql-conf-log/


https://www.reddit.com/r/Traefik/comments/dk1rsj/trying_to_configure_traefic_as_proxy_to_gitea_but/

https://www.pgadmin.org/docs/pgadmin4/latest/container_deployment.html#traefik

### Referências:

* Docker - Official Site, Docker Documentation. ***Docker overview*** <br/>
  Acessado: *Dezembro de 2019* <br/>
  Disponível: *[https://docs.docker.com/engine/docker-overview/](https://docs.docker.com/engine/docker-overview/)*

* Docker Compose - Official Site, Docker Compose Documentation. ***Docker Compose File*** <br/>
  Acessado: *Dezembro de 2019* <br/>
  Disponível: *[https://docs.docker.com/compose/compose-file/](https://docs.docker.com/compose/compose-file/)*

* Traefik - Official Site, Traefik Documentation. ***Configuration Introduction - How the Magic Happens*** <br/>
  Acessado: *Dezembro de 2019* <br/>
  Disponível: *[https://docs.traefik.io/getting-started/configuration-overview/](https://docs.traefik.io/getting-started/configuration-overview/)*




### Licença

[<img width="190" src="https://raw.githubusercontent.com/alisonbuss/my-licenses/master/files/logo-open-source-550x200px.png">](https://opensource.org/licenses)
[<img width="166" src="https://raw.githubusercontent.com/alisonbuss/my-licenses/master/files/icon-license-mit-500px.png">](https://github.com/alisonbuss/quickstart-drone-ci/blob/master/LICENSE)
