# Configurações básicas
Já baixamos os arquivos necessarios para o começo do desenvolvimento, agora precisamos fazer algumas configurações no `manifest.json`

## Ajustando o manifest
Abra o arquivo `manifest.json` e faça as seguintes alterações
* Coloque o nome da conta da VTEX que está sendo utilizada na chave `vendor`, e.g. `"vendor": "corebiz"`

* Altere o `name` do app para `{{accountName}}-theme`, e.g. `"vendor": "corebiz-theme"`, p.s. não e obrigatório que o nome do app seja esse

* Dentro da chave [`builders`](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-builders) adicione `"react": "3.x"`, é necessário que esse builder seja adicionado para que o React funcione

  e.g.
  ```jsonc
    // manifest.json 
    
    "builders": {
      "styles": "2.x",
      "assets": "0.x",
      "store": "0.x",
      "sitemap": "0.x",
      "docs": "0.x",
      "messages": "1.x",
      "react": "3.x"
    }
  ```

* Feito isso rode o comando
  ```bash
    vtex setup
  ```

E pronto, o repositório está pronto para ser utilizado!

## Links
[Comandos Básicos](/docs/pt/cli/02_comandos.md)

[Builders](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-builders)