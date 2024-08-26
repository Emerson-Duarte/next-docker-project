# Projeto Web em React com Docker

Este projeto é uma aplicação frontend construída com React e configurada para ser executada em um ambiente Docker. A aplicação consome uma API backend (também em Docker) e exibe os dados retornados.

## Estrutura do Projeto

- **React**: Biblioteca utilizada para construção do frontend.
- **Docker**: Utilizado para criar um ambiente isolado e reproduzível para o desenvolvimento e execução da aplicação.
- **Docker Compose**: Orquestra os containers Docker, permitindo o gerenciamento simultâneo da aplicação frontend e do backend.

## Pré-requisitos

Certifique-se de ter as seguintes ferramentas instaladas em sua máquina:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Configuração do Projeto

### 1. Clonar o Repositório

Primeiro, clone o repositório para o seu ambiente local:

```bash
git clone https://github.com/seu-usuario/seu-projeto-web.git
cd seu-projeto-web
```

### 2. Configurar as Variáveis de Ambiente
Certifique-se de configurar as variáveis de ambiente necessárias para o projeto. Crie um arquivo .env na raiz do projeto e defina as variáveis como:

```
NEXT_PUBLIC_API_URL=http://localhost:3002
```

### 3. Construir e Rodar os Containers
Use o Docker Compose para construir e rodar os containers:

```
docker-compose up --build
```

Isso irá construir as imagens Docker necessárias e rodar os containers da aplicação e da API.

### 4. Acessar a Aplicação
Após subir os containers, a aplicação React estará disponível em:

```
http://localhost:3003
```

Certifique-se de que a API também esteja rodando e acessível na porta 3002.




#### Desenvolvimento Local
Durante o desenvolvimento, você pode usar o comando abaixo para subir o ambiente de desenvolvimento:

```
docker-compose up
```


#### Debugging
- Erro de CORS: Certifique-se de que a API está configurada para permitir requisições do frontend (veja a configuração do CORS na API).
- Problemas de Rede: Verifique se os containers estão conectados à mesma rede Docker.
- Erros de Construção: Caso tenha problemas ao construir as imagens Docker, verifique se todas as dependências estão corretamente instaladas e configuradas.


#### Contribuição
Sinta-se à vontade para contribuir com melhorias para este projeto. Para isso, siga os passos abaixo:

- Faça um fork do projeto.
- Crie uma nova branch (git checkout -b feature/nome-da-feature).
- Faça commit das suas alterações (git commit -m 'Adiciona nova feature').
- Envie para o repositório (git push origin feature/nome-da-feature).
- Abra um Pull Request.