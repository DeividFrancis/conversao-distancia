# Desafio 1 - Docker - Desafio DevOps & Cloud by @fabricioveronez

Este repositório é parte do treinamento Desafio DevOps & Cloud, conduzido por @fabricioveronez. Aqui você encontrará a solução para o Desafio 1, que aborda conceitos fundamentais e práticas essenciais no uso do Docker.

O objetivo deste repositório é demonstrar a aplicação prática dos conceitos aprendidos no treinamento, com foco na criação e gerenciamento de containers Docker.

### Comandos que utilizei durante a aula

```bash
# -i (interativo) -t (tty)
$ docker run -it ubuntu /bin/bash

# -f nome do dockerfile (pode ser omitido caso o nome seja Dockerfile)
$ docker build -t conversao-distancia -f Dockerfile .

# -p <externo>:<interno>
$ docker run -d -p 5000:5000 conversao-distancia

# tag (Cria uma copia da imagem com nome diferente, interessante que mantem o msm ID)
$ docker tag conversao-distancia deividoliver/conversao-distancia:v1

# existe uma nomeclatura para poder fazer o upload da imagem no dockerhub
$ docker push deividoliver/conversao-distancia:v1

# -qa lista somente os ids dos container
$ docker container rm $(docker container ls -qa)
```
