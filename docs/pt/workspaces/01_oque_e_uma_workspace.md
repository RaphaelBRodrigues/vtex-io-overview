# O Que é Workspace
Uma workspace é uma versão da loja em que você está logado, porém isolada do ambiente de produção, ela serve como um clone da loja onde você podera desenvolver e testar suas alterações sem afetar o ambiente principal (master).

Pense em uma workspace como uma branch do git, onde a branch principal (master) corresponde a versão que está em produção e as demais branchs à features e correções que estão sendo 
feitas.

## Tipos de Workspace
* Master - É a workspace principal da conta, ou seja, a workspace que está sendo usada em produção

* Desenvolvimento - São workspaces onde o desenvolvimento acontece, nela é possível rodar comandos como o `vtex link` para testar as alterações em tempo real que estão sendo feitas no código fonte

* Produção - São workspaces que podem substituir a workspace master, utilizando o comando `vtex promote`, não é possivel linkar apps nesta workspace com o comando `vtex link`
  * e.g. Foi criado um novo layout para a black friday algumas semanas antes, está tudo certo com a workspace, mas ainda não é a hora da virada do layout, então no momento correto essa workspace irá substituir a de produção, aplicando o novo layout a loja.


## Links
[Docs](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-2-basicsetuptodevelopinvtexio)

[Workspaces de Produção](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-creating-a-production-workspace?_ga=2.140637746.1411386765.1641603712-1420314383.1630247374)