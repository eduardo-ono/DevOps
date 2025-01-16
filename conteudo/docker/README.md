<h1 align="center">Docker</h1>
<h3 align="center">Prof. Eduardo Ono</h3>
<h6 align="center">Atualizado em: 21/04/2024</h6>

&nbsp;

## Tópicos

* ### Instalação do Docker

* ### Utilizando o Docker

* ### Principais Comandos

&nbsp;

## Comandos

* Exibir a versão do Docker instalada:

    ```sh
    docker --version
    ```

* Instalar (_pull_) de uma imagem Docker:

    ```sh
    docker pull <nome_da_imagem>
    ```

  * Exemplo

    ```sh
    docker pull nginx
    ```

* Listar todas as imagens instaladas:

    ```sh
    docker images
    ```

* Executar um _container_ baseado em uma imagem Docker, ou seja, uma instância de uma imagem:

  ```sh
  docker run <nome_da_imagem>:<nome_da_tag>
  ```

  Exemplo:

  ```sh
  docker run nginx:latest
  ```

* Verificar quais _containers_ estão em execução:

  ```sh
  docker ps
  ```

* Para executar um _container_ (exemplos):

  ```sh
  docker run -d -p 8080:80 nginx:latest
  docker run -d -p 8080:80 -p 3000:80 nginx:latest
  ```

Obs.: Abrindo o navegador no endereço localhost:8080, o servidor nginx deverá estar sendo executado.

* Remover todos os _containers_:

    ```sh
    docker rm $(docker ps -aq)
    ```

&nbsp

## Dockerfiles (Exemplos)

```sh
FROM nginx:latest
ADD ./usr/share/
```

```sh
docker build --tag servidorweb:latest
```

&nbsp;

## Bibliografia

* MIELL, Ian; SAYERS, Aidan Hobson. [Docker in Practice](https://archive.org/details/DockerInPractice), 2016.

* GUPTA, Arun. [Docker for Java Developers](https://archive.org/details/DockerForJavaDevelopers), 2016.

* STONEMAN, Elton. [Docker Succinctly](https://www.syncfusion.com/ebooks/docker_succinctly).

&nbsp;
