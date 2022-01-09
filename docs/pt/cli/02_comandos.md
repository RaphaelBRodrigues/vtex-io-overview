# Principais Comandos
A seguir veremos os principais comandos do CLI durante o desenvolvimento de um app.

## Comandos
* `vtex help` - Exibe todos os comandos disponíveis do CLI
* `vtex whoami` - Mostra a conta da VTEX, email e workspace atual
* `vtex init` - Cria algumas pastas e arquivos básicos para o início do desenvolvimento
* `vtex setup` - Configura o ambiente de desenvolvimento (eslint, prettier, typescript...)
* `vtex login {{accountName}}` - Loga em alguma conta da VTEX; e.g. `vtex login corebiz`
  * accountName - Nome da conta da VTEX
* `vtex use {{workspace}}` - Muda a workspace atual; e.g. `vtex use raphaeldev`
  * workspace - Nome da workspace já existente ou que será criado
* `vtex link` - Sincroniza o app da pasta atual com a workspace em uso
* `vtex browse` - Abre a workspace atual no navegador
* `vtex install {{vendor}}.{{app}}@{{version}}` - Instala um app na workspace atual; e.g. `vtex install vtex.service-example@0.x`
  * vendor - A conta que mantém o app, pode ser a mesma conta do projeto que esta sendo desenvolvido ou uma terceira como a própia VTEX, no caso de apps nativos
  * app - Nome do app que será instalado
  * version - A versão do app que será instalado, caso a versão não seja passada a mais recente será instalada.
  
## Links
[Comandos CLI](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-vtex-io-cli-command-reference)