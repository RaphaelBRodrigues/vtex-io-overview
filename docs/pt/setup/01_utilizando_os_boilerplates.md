# Utilizando os boilerplates
A VTEX disponibiliza alguns repositórios que podem ser utilizados como template para a criação de novas lojas.

## Criando a estrutura básica
Podemos criar a estrutura de um app automaticamente utilizando o seguinte comando
```bash
  vtex init
```
Ao rodar o comando selecione a opção `store`, ao fazer isso o template será criado, agora rode o comando para acessar a estrutura básica do app
```bash
  cd minimum-boilerplate-theme
```
Feito isso precisamos configurar o React no boilerplate, para isso execute os seguintes comandos
```bash
  mkdir react && cd $_;
```
Agora vamos fazer o download do arquivos package.json do boilerplate da VTEX
```bash
curl -O https://raw.githubusercontent.com/vtex-apps/react-app-template/master/react/package.json && code package.json;
```
Altere as chaves `name` e `version` para `react` e `1.0.0` e rode o comando
```bash
  npm install
```

## Links
[Comandos Básicos](/docs/pt/cli/02_comandos.md)

[React App Template](https://github.com/vtex-apps/react-app-template/) 