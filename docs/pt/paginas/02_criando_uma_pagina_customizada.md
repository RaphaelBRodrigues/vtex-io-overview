# Alterando Páginas Nativas
O Store Framework também nos permite criar páginas customizadas, criando o template através do bloco `store.custom`

## Criando o Template
Para criarmos um novo template precisamos usar o bloco nativo `store.custom` e passar um nome para esse template como um identificador, como no exemplo abaixo:

  ```jsonc
  // store/blocks/about-us.jsonc

  {                                       // 01
    "store.custom#about-us": {            // 02
      "blocks": []                        // 03
    }                                     // 04
  }                                       // 05
```

## Criando a Rota
Com o template definido, podemos criar uma rota a partir dele, para isso iremos criar o arquivo `store/routes.json`, que será responsável por criar algumas das páginas customizadas de nosso site, nele devemos inserir as seguintes propriedes:

  ```jsonc
  // store/routes.jsonc

  {                                       // 01
    "store.custom#about-us": {            // 02
      "path": "/about-us"                 // 03
    }                                     // 04
  }                                       // 05
```

Esse trecho que inserimos é responsável por criar a rota `/about-us` e utilizar o template `store.custom#about-us`, para acessarmos essa nova página precisamos acessar a seguinte url `{{workspace}}--{accountName}.myvtex.com/about-us`

Com a página criada, podemos alterar a propriedade `blocks` do template `store/blocks/about-us.jsonc:03`, e inserir blocos nativos e customizados nela


## Links
[Estrutura Básica](docs/pt/setup/03_entendendo_a_estrutura.md)

[Blocos Nativos](docs/pt/blocos/02_blocos_nativos.md)
