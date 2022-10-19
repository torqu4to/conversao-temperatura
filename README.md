# Projeto conversão de temperatura

### Sobre o projeto
O projeto conversão de temperatura é um projeto desenvolvido em NodeJS. O projeto tem como objetivo ser um exemplo para a criação de ambiente com containers usando NodeJS.

### Observações do projeto
A aplicação é exposta usando a porta 8080

##


## Etapas para executar o projeto em um container Docker

Faça o download do projeto para a sua máquina:

```bash
git clone https://github.com/torqu4to/conversao-temperatura.git
```

Agora vamos construir a imagem do nosso container:

```bash
docker build -t torqu4to/conversao-temperatura:v1 .
```

Vamos verificar se a imagem de fato foi criada:

```bash
docker image ls
```

### Esse é o resultado esperado, listando suas imagens:
<img src="https://cdn.discordapp.com/attachments/906609410472804415/1032054956678725702/unknown.png">

<br>
Vamos então executar o container utilizando os parâmetros -d para a aplicação rodar em background e -p 8080:8080 que faz a conexão entre as portas da aplicação e da sua máquina:

```bash
docker container run -d -p 8080:8080 torqu4to/conversao-temperatura:v1
```

Com isso, se tudo der certo a sua aplicação ja estará "no ar".Podemos conferir acessando a seguinte URL no navegador:

```bash
localhost:8080
```

### E voilà, aplicação rodando como esperado
<img src="https://cdn.discordapp.com/attachments/906609410472804415/1032061832946520095/unknown.png">


<br>

Pra finalizar vamos subir nossa imagem para o DockerHub:

```bash
docker push torqu4to/conversao-temperatura:v1
```
