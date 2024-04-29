# AtividadesM10

# O que é o backstage

Backstage é uma plataforma open-source criada pelo Spotify para gerenciar a infraestrutura de desenvolvimento de software, simplificando o acesso a ferramentas e serviços para os desenvolvedores. Ele é muito util para a gestao de pipelines CI/CD.

# Tecnologias envolvidas

- Github
- Docker / Docker Compose
- SQL

# Conceitos aprendidos

- Controle de versão com git
- Construção Docker de multiestágio
- Configuração de contêineres Docker


# Guia passo a passo para a execução, vou separar em etapas

1 - Instalação das dependencias, vou apenas configurar o diretório e instalar as dependências necessarias


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

``` docker run -it -p 7007:7007 backstage ```


![atividadecertam10](https://github.com/MrSchipRozen/-AtividadesM10/assets/99350292/806b2925-40f8-4e46-b7e3-03ae5373d931)

5 - Backstage, para acessar basta por no navrgador http://localhost:8009 e tera acesso ao backstage

Prints em execução

<img width="1553" alt="Screenshot 2024-04-28 at 22 52 17" src="https://github.com/MrSchipRozen/-AtividadesM10/assets/99350292/ce35ece1-b818-44b0-8ee9-17491f606f4b">

<img width="1800" alt="atividadem10" src="https://github.com/MrSchipRozen/-AtividadesM10/assets/99350292/f2ecf9eb-87ab-49bd-a5bf-6e55c46a89d3">


