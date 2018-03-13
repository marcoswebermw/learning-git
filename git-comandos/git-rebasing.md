## Git rebasing
  

Usa uma abordagem que deixa o histórico mais limpo.

Melhor usado localmente. Se já tiver sido feito push de um commit para o servidor, não use o `rebase` nele.

### Alterando um commit com `rebase`
  
Um determinado commit pode ter sua mensagem alterada pelo modo interativo do rebase, através do parâmetro `-i`.
  
```sh
git rebase -i
```
  
Será aberto um editor de texto com todos os commits feitos no repositório. Localize o commit que quiser fazer a alteração da mensagem. Troque a palavra `pick` que vem antes dele por `reword` ou `r`. Salve o arquivo e feche o editor. 
  
O editor será aberto novamente com a mensagem do commit anterior. Modifique-a e depois salve e feche o editor.
  
> Essa alteração deve ser feita antes de um `push` para o servidor. Se for feita depois do `push` pode causar confusão no repositório.
  
### Referências
  
* [Documentação do Git](https://git-scm.com/book/pt-br/v1/Ramifica%C3%A7%C3%A3o-Branching-no-Git-Rebasing)