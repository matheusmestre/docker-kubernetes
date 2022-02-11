# Docker Cheat Sheet

## Arquivo de Help
```
docker --help
```
## Versão
```
docker --version
```

# Imagens
## Criar Imagem
### Criar imagem a partir do Dockerfile no diretório atual.
```sh    
docker build .
```
### Criar imagem com nome customizado.
```
docker build -t <name> .
```
### Criar imagem com nome/tag customizados.
```
docker build -t <name>:<tag> .
```
## Remover Imagem
### Remove uma imagem que não tem vinculo com um container.
```
docker rmi <image>
```
### Remove todas imagens que não tem vinculo com um container.
```
docker image prune
```
### Remove todas as imagens (All).
```
docker image prune -a
```
### Remove todas as imagens sem pedir confirmação (Force).
```
docker image prune -f
```
### Informações sobre a imagem
```
docker image inspect <image>
```

# Containers
## Listar Containers
### Lista os containers em execução.
```
docker ps
```
### Lista todos os containers (All).
```
docker ps -a
```
## Criar Containers
### Cria e Executa um container a partir de uma imagem
```
docker run -p <external>:<internal> <image>
```
#### As variações abaixo podem ser utilizadas em conjunto:
### Modo Detached (-d)
```
docker run -d -p <external>:<internal> <image>
```
### Modo interativo (-i)
```
docker run -i -p <external>:<internal> <image>
```
### Remove container ao finalizar execução (--rm)
```
docker run --rm -p <external>:<internal> <image>
```
### Criar container com nome customizado (--name)
```
docker run --name <name> -p <external>:<internal> <image>
```

## Iniciar Container
### Inicia um container criado anteriormente.
```
docker start <container>
```
### Inicia um container em modo Attached.
```
docker start -a <container>
```
## Reiniciar Container
```
docker restart <container>
```
## Finalizar Container
```
docker stop <container>
```

## Excluir Container
### Exclui um Container
```
docker rm <container>
```
### Remove todos containers que estão parados
```
docker container prune
```

## Logs de Container
### Lista os logs feitos pelo container
```
docker logs <container>
```
### Fica "escutando" a saída dos logs do container (Follow)
```
docker logs -f <container>
```

## Outras Operações
### Altera um container iniciado em Detached Mode para Attached Mode
```
docker container attach <container>
```
### Cria uma imagem a partir de outra com novo nome fornecido
```
docker tag <image> <new-image>
```

# Docker Hub
### Realiza login no Docker Hub
```
docker login
```
### Faz o upload da imagem para docker hub
```
docker push <image>
```




    


