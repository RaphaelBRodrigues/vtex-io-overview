# O Que é um Bloco
Pense em um bloco como um componente React, as páginas (home, pdp, categoria...) são grandes componentes, com vários outros menores (vitrines, banners, newsletters...) dentro deles, todo o front de uma loja IO é baseada nesses componentes, a VTEX disponibiliza vários blocos nativos que podemos utilizar, mas também podemos criar nossos próprios blocos conforme nossa necessidade.

## Utilizando blocos
  No exemplo a seguir vemos o bloco `store.home` que é o bloco nativo responsável pela home do site, dentro desse bloco existe a propiedade `blocks` onde os `childrens` desse bloco são inseridos.

```jsonc
// store/blocks/home/home.jsonc

{
  "store.home": {
    "blocks": [
      "rich-text"
    ]
  }
}
```
  Analisando esse bloco notamos que ele possui apenas um bloco filho, o [rich-text](https://vtex.io/docs/components/all/vtex.rich-text@0.9.1/), que é um bloco nativo da VTEX responsável por exibir textos

  No exemplo apresentado nada será exibido na home do site, pois utilizamos o bloco `rich-text` dentro do template da home o `store.home`, mas não passamos nenhum texto para ele exibir, para corrigirmos isso precisamos passar algumas propiedades para ele, como no exemplo a seguir

  ```jsonc
  // store/blocks/home/home.jsonc

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

Para passarmos o conteúdo para o bloco utilizado, precisamos criar uma chave no json para ele, então na linha `07` estamos configurando o bloco `rich-text` que está sendo usado na linha `04`, as propriedades que os blocos nativos aceitam podem ser encontradas na [documentação](https://developers.vtex.com/vtex-developer-docs/docs/welcome) do VTEX IO

O exemplo acima já funciona, e exibe o texto `Olá, seja bem vindo!` na home de nossa loja, mas e se precisarmos utilizar outro rich-text?

Nós podemos atribuir "ids" aos blocos para os personalizar individualmente, como no exemplo a seguir

  ```jsonc
  // store/blocks/home/home.jsonc
  
{                                       // 01
    "store.home": {                       // 02
      "blocks": [                         // 03
        "rich-text#welcome-message"       // 04
        "rich-text#store-description"     // 05
      ]                                   // 06
    },                                    // 07
    "rich-text#welcome-message": {        // 08
      "props": {                          // 09
        "text": "# Olá, seja bem vindo!"  // 10
      }                                   // 11
    }                                     // 12
    "rich-text#store-description": {      // 13
      "props": {                          // 14
        "text": "Lorem ipsum dolor sit"   // 15
      }                                   // 16
    }                                     // 17
}                                       // 18
```

Note que agora temos dois blocos `rich-text` na home, porém cada um possui um identificador único depois do `#`, então o `rich-text#welcome-message` configurado na linha `08` está sendo utilizado na linha `04` e o `rich-text#store-description` da linha `13` está sendo utilizado na linha `05` do bloco da home

## Links
[Documentação de Componentes Nativos](https://developers.vtex.com/vtex-developer-docs/docs/store-framework-apps)

[Exemplo de Bloco](https://github.com/vtex-apps/store-theme/blob/master/store/blocks/home/home.jsonc)