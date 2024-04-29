# -AtividadesM10

##Guia passo a passo para a execução, vou separar em etapas

1 - Instalação das dependencias, vou apenas configurar o diretório e instalar as dependências necessarias

Execução dos comandos

```
npm intall --global yarn
yarn install
```

2 - Build

```
yarn install --frozen-lokfile
yarn tsc
yarn build
```

3 - Build docker

```
docker image build . -f packages/backend/Dockerfile --tag backstage --no-cache

```

4 - Docker Compose, vai ser ele que vai orquerstar toca a aplicação do backstage

```
version: '3.8'
services:
  backstage:
    image: backstage
    environment:
      POSTGRES_HOST: db
      POSTGRES_USER: postgres
      POSTGRES_PASSWORD: example
    ports:
      - '8009:7007'
  db:
    image: postgres
    environment:
      POSTGRES_USER: postgres
      POSTGRES_PASSWORD: example
      POSTGRES_DB: backstage
    volumes:
      - postgres-data:/var/lib/postgresql/data

volumes:
  postgres-data:
```


