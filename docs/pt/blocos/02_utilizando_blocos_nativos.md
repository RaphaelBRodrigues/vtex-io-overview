# Utilizando blocos nativos
Como já vimos, o front de uma loja IO é composto por blocos, e a VTEX já disponibiliza diversos destes nativamente no Store Framework, agora veremos como importar esses apps em nossa aplicação para que tenhamos acesso a esses blocos

## Importando Apps Nativos
  Antes de utilizarmos os blocos nativos, precisamos importar os Apps responsáveis por ele, por exemplo, para utilizarmos o `rich-text` dentro de algum outro bloco precisamos importar o App `vtex.rich-text` em nosso `manifest.json`

  e.g.
  ```jsonc
  {
    "dependencies": {
      "vtex.rich-text": "0.x"
    }
  }
```
 E só então utilizar o bloco `rich-text`
  ```jsonc
{                                       // 01
    "store.home": {                       // 02
      "blocks": [                         // 03
        "rich-text"                       // 04
      ]                                   // 05
    },                                    // 06
    "rich-text": {                        // 07
      "props": {                          // 08
        "text": "# Olá, seja bem vindo!"  // 09
      }                                   // 10
    }                                     // 11
}                                       // 12
```
O mesmo se aplica a todos os outros blocos, nativos ou customizados que não estejam presentes no App atual, que serão utilizados na loja
e.g.
```jsonc
  "dependencies": {
    "vtex.store": "2.x",
    "vtex.store-header": "2.x",
    "vtex.product-highlights": "2.x",
    "corebiz.custom-login": "4.x"
  }
```

## Links
[Documentação de Blocos Nativos](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-dependencies)
