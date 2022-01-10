# Blocos Customizados
Podemos criar blocos customizados utilizando componentes React com o Store Framework conforme nossa necessidade, é possível passar argumentos para o componente através dos blocos nos json ou pelo Site Editor tornando o bloco customizado personalizável para o cliente.

## Configurando o builder do React
Antes de começaramos a desenvolver o bloco, precisamos adicionar o builder responsável por processar o react, para isso iremos adicionar a seguinte propriedade dentro do `manifest.json`
```jsonc
// manifest.json

"builders": {
  "react": "3.x"
}
```

## Criando o Componente React
Agora podemos criar o componente react, para isso devemos criar os seguintes arquivos e pastas
```
react
│   HelloWorld.ts
│
└───components
    │
    └───HelloWorld
        │   index.tsx
```
É necessário que exista um arquivo na raiz da pasta react exportando o componente react, e uma subpasta dentro da pasta `components` com a lógica do componente.
```tsx
// react/components/HelloWorld/index.tsx

import React from 'react'

const HelloWorld: React.FC = () => {
  return <h1>Hello World</h1>
}

export default HelloWorld;
```

```ts
// react/HelloWorld.ts

export { default as HelloWorld } from './components/HelloWorld'
```

Note que a lógica do componente se encontra dentro da pasta `react/components/HelloWorld`, e o arquivo `HelloWorld.ts` que está na raiz faz apenas a exportação desse componente para o builder da VTEX

## Criando e Utilizando o Bloco Customizado
Agora que estamos exportando o componente na raiz da pasta react, podemos criar um bloco apartir desse componente, para isso iremos adicionar a seguinte estrutura dentro do arquivo `store/interfaces.jsonc`

```jsonc
// store/interfaces.jsonc

{
  "hello-world": {
    "component": "HelloWorld"
  }
}
```

Com isso criamos um bloco apartir de um componente react, o nome da propriedade `hello-world` será usado para a chamada do bloco dentro de outro bloco ou para fazer sua personalização, já a propriedade `component` recebe o nome do componente que está sendo exportado no arquivo `react/HelloWorld.ts

Agora podemos utilizar o nosso novo bloco customizado dentro de outro bloco, como no exemplo a seguir
```jsonc
// store/blocks/home/home.jsonc

{
  "store.home": {
    "blocks": [
      "hello-world"
    ]
}

```

## Links
[Entendendo a Estrutura](/docs/pt/setup/03_entendendo_a_estrutura.md)
