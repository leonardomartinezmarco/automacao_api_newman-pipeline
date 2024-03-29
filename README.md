# Automação de testes de API com Postman e criação de Pipeline
Este é o conjunto de testes da API ServeRest do site https://serverest.dev/, executado utilizando o Postman e Newman, e integrado em uma pipeline de integração contínua (CI).

## Tecnologias
- Postman versão web
- Node version v16.13.2
- Newman 5.3.2
- Newman-reporter-htmlextra
- Git actions

## Documentações
- Análise Técnica: Analise/
- Doc da API: [Consultar Swagger da API serverRest](https://serverest.dev/)


## Como instalar o ambiente
- Primeiro: Instalar o node em seu computador [Baixe o Node](https://nodejs.org/en/download/current)
- Segundo: Instalar o Newman de forma global ou linha de comando  abaixo: [Baixe as dependências do newman](https://www.npmjs.com/package/newman)

```
npm install -g newman
```

- Terceiro: Instalar as depedênbcias de relatórios (Opcional) [newman-reporter-html](https://www.npmjs.com/package/newman-reporter-html)
```
npm -g newman-reporter-html
```
ou também pode usar o newman-reporter-htmlextra. Com opções mais estilizadas [newman-repórter-htmlextra](https://www.npmjs.com/package/newman-reporter-htmlextra)
```
npm install -g newman-reporter-htmlextra
```
## Como rodar os testes
- No Postman importa a collection e o environment
<img src="https://github.com/leonardomartinezmarco/automacao_api_newman-pipeline/assets/55605892/02bcd848-38b9-46f9-8467-6cb0a3ab3dcc)" width="500" height="250">

- Execute os testes de forma manual ou automatizado

### Pelo Newman (Via console)
- Abra a IDE e console de sua preferência
- Execute a seguinte linha de comando para rodar os testes, e visualizar a ação no console
```
newman run servRest.postman_collection.json -e servRest_test.postman_environment.json -r cli
```
<img src="https://github.com/leonardomartinezmarco/automacao_api_newman-pipeline/assets/55605892/65beb3f8-f575-4602-bbbd-e1eb99a9a6ca)" width="500" height="250">


### Report

Ao rodar os testes com htmlextra, será gerado arquivo em HTML com o resultado dos testes. O arquivo encontra-se na pasta de **newman** que foi criado no local em que os arquivos de collection e environment se encontram, abra para visualizar a página web.
```
newman run servRest.postman_collection.json -e servRest_test.postman_environment.json -r htmlextra
```
<img src="https://github.com/leonardomartinezmarco/automacao_api_newman-pipeline/assets/55605892/1639e4ad-6824-45e3-9140-4dbf6d4c41fa)" width="500" height="250">
