# Criando e Gerenciando Workspaces
Quando logamos na conta da VTEX utilizando o comando `vtex login` nós automaticamente estamos usando o workspace master (o que está em produção) da conta.

## Criando uma workspace para o desenvolvimento
Para começarmos a desenvolver algo precisamos criar uma workspace de desenvolvimento, para isso precisamos rodar os seguintes comandos

```bash
  vtex use {{workspaceName}}
```

```bash
  vtex link
```

```bash
  vtex browse
```

## Criando uma workspace de produção
Não é possível linkar um app em uma workspace de produção, mas o processo de criação e utilização de uma é bem parecido a de desenvolvimento.
```bash
  vtex use -p {{workspaceName}} 
``` 
```bash
  vtex install {{vendor}}.{{appName}}@{{version}}
```
```bash
  vtex browse
```
Note que o comando `vtex link` foi substituido pelo `vtex install`, pois vimos que não é possivel linkar apps nesse tipo de workspace, mas podemos instalar apps nela

Lembre-se de rodar o comando `vtex whoami` para confirmar em qual conta e workspace vocÊ está logado

## Links
* [Comandos básicos](../docs/pt/cli/02_comandos.md)