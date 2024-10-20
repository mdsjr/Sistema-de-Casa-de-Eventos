# Sistema-de-Casa-de-Eventos
Projeto: Conteinerização do "Sistema de Casa de Eventos" para Implantação Global

## Tecnologias Utilizadas

- React
- Vite
- Node
- Docker

## Dependências Utilizadas

- React Router
- Styled Components
- Axios
- React Toastify

## Instruções de Instalação

Clonar o projeto com o comando abaixo:

```sh
git clone 
```

Entrar na pasta do projeto

```sh
cd casa-de-eventos-react
```

Instalar as dependencias

```sh
npm install
```

## Instruções para rodar o projeto

Digitar o comando para criar a imagem do docker baseado nos requisitos do Dockerfile

```sh
docker buildx build -t casa-de-eventos-react .
```
Digitar o comando para rodar a imagem do docker em uma porta especifica


```sh
docker run -d -p 5173:5173 casa-de-eventos-react
```

```sh
docker ps
```

```sh
CONTAINER ID   IMAGE                   COMMAND                  CREATED         STATUS         PORTS                    NAMES
392f8e2e4404   casa-de-eventos-react   "docker-entrypoint.s…"   2 minutes ago   Up 2 minutes   0.0.0.0:5173->5173/tcp   wonderful_raman

```



### Guardar imagem Docker no Docker Hub

```sh
docker login
```
Depois

```sh
docker tag <tag do nome da imagem> <tag do usuario do docker hub>/<tag do nome da imagem>:<tag da versão>
Exemplo: docker tag casa-de-eventos-react mdsjr/casa-de-eventos-react:v.10
```

Publicação no Docker Hub

```sh
docker push <tag do usuario do docker hub>/<tag do nome da imagem>:<tag da versão>
docker push mdsjr/casa-de-eventos-react:v.10
```

### Docker Hub

https://hub.docker.com/r/mdsjr/casa-de-eventos-react


