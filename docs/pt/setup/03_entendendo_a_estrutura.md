# Entendendo a Estrutura
Agora veremos um pouco sobre alguns arquivos e pastas que se encontram dentro de um app do Store Framework.

## Arquivos na Raiz
  * `manifest.json` - Esse arquivo concentra todas as informações relacionadas a VTEX no app, nele coisas como o nome do app, nome da conta, dependências do IO e builders são configurados.

## Pastas 
 As pastas na raiz do projeto estão diretamente ligadas aos `builders` configurados dentro do `manifest.json`, cada builder é responsável por processar e interpretar a pasta que leva o mesmo nome

### Store
  Dentro dessa pasta são configurados os blocos, interfaces e rotas do app
  * Blocos
    * São como peças de lego que compôem o layout de nosso app
    * Path - `store/blocks/**/*.jsonc` 
  * Interfaces 
    * É o a ponte entre um componente React customizado e um bloco
    * Path - `store/interfaces.jsonc`
  * Rotas
    * Arquivo onde são configuradas as rotas
    (urls) customizadas da loja
    * Path - `store/routes.jsonc`

### React
  O desenvolvimento de blocos nativos acontece nessa pasta, na raiz dela os componentes devem ser exportados
  * Exportação do componente
    * A exportação dos componentes deve acontecer estritamente na raiz da pasta react, mas a lógica dele não
    * Path - `react/*.ts`
  * Componentes 
    * A lógica do componente pode ficar em subpastas, é comum que seja criada uma pasta chamada components e dentro dela outras subspastas que correspondem a cada componente, então o arquivo que está na raiz importa o componente de uma dessas pastas e o exporta
    * Path - `react/components/**/**.tsx`

### Styles
  Toda a estilização de blocos externos (blocos que não tenha sido criados dentro da pasta react) deve acontecer dentro desta pasta e no arquivo relacionado ao App do bloco
  * CSS
    * Pasta onde todos os arquivos .css estão localizados
    * Path - `styles/css`

    e.g. Para estilizarmos um `rich-text` precisamos localizar o arquivo que corresponda ao app do `rich-text` que é o mesmo app localizado na propriedade `dependencies` do `manifest.json`, então toda a estilização de um bloco `rich-text` precisa estar dentro do arquivo `store/css/vtex.rich-text.css`.



## Links
[Manifest](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-manifest)

[Builders](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-builders)

[Interfaces](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-interface)

[Blocos](/docs/pt/blocos/01_o_que_e_um_bloco.md)

[Estilização](https://learn.vtex.com/docs/course-styles-course-step01csshandles-lang-en)