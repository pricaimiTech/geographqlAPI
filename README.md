# Automação de Testes para a API Geograph [![Newman run](https://github.com/pricaimiTech/fakestoreapi/actions/workflows/main.yml/badge.svg?branch=main)](https://github.com/pricaimiTech/fakestoreapi/actions/workflows/main.yml)

Teste de API Rest do manual a CI/CD

## O que é

Este repositório foi criado para mostrar o processo de automação de uma API Rest com upload de massa de testes por arquivo .csv

## Tecnologias utilizadas

- Postman versão web
- node version v18.16.1
- newman v5.3.2
- newman-reporter-html

## Documentações

- Doc da API: [Consulte Documentação](https://geographql.netlify.app/)

## Como instalar o ambiente

- Primeiro: instale o node em seu computador [baixe aqui](https://nodejs.org/en/download)
- Segundo: realize a instalação do newman de forma global [baixe aqui a dependencia](https://www.npmjs.com/package/newman)

```
npm install -g newman
```

- Terceiro: realize a instalação da dependencia dos relatórios (opcional) [newman-reporter-html
  ](https://www.npmjs.com/package/newman-reporter-html)

```
npm install -g newman-reporter-html
```

## Como rodar os testes

### Pelo Postman web ou desktop

- Import a collection e o environment
- Execute os teste de forma manual ou automatizada

### Pelo newman

- Abra o console de preferência
- Execute a seguinte linha de comando para rodar os testes

  ```
    newman run geographql.postman_collection.json -e GeographQL.postman_environment.json -r cli
  ```

- Execute os teste com relatório

```
 newman run geographql.postman_collection.json -e GeographQL.postman_environment.json -r cli,htmlextra --reporter-htmlextra-export testResults/index.html
```

### Report

Se você optou por rodar os teste com o report htmlextra, você gerou um arquivo html com o resultado dos testes e para verificar as validações você pode abrir a pasta **newman** que foi criada no local em que os arquivos de collection e environment se encontram.

## Entre em contato

email: priscila.caimi@hotmail.com

redes socias: https://linktr.ee/priscilacaimi
