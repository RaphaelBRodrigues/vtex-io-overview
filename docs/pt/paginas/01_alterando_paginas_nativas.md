# Alterando Páginas Nativas
Como já vimos em outras secções a estrutura da maioria das páginas nativas podem ser alteradas através dos arquivos `store/blocks/**/*.jsonc`, agora veremos um pouco mais sobre elas.  

## Páginas Nativas
Podemos identificar os blocos que representam as páginas através do seu nome, todas elas seguem a seguinte nomenclatura `store.*`, e podemos adicionar e remover os blocos que as compôem através das propriedades `blocks` ou `children` dependendo do template, vale ressaltar que esses blocos podem possuir um contexto próprio e que os blocos filhos terão acesso a ele.

### Exemplos de Páginas Nativas
* `store.account` - Template da página Minha Conta
* `store.product` - Template das PDPs
* `store.home` - Template da Home
* `store.search` - Template das páginas de Busca (pode conter variações _#brand_, _#departament_...)
* `store.orderPlaced` - Template da página orderPlaced 
* `store.not-found` - Template de página não encontrade (pode conter variações _#product_, _#category_)


## Links
[Estrutura Básica](docs/pt/setup/03_entendendo_a_estrutura.md)

[Blocos Nativos](docs/pt/blcoos/02_blocos_nativos.md)
