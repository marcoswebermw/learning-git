## Git Stash
  
O `stash` existe para aquele momento que já existe um trabalho feito(modificado e rastreado pelo Git) porém inacabado, e existe 
a necessidade de trabalhar com outra parte do projeto. Ou teríamos que comitar o que já foi feito, ou descartar o trabalho feito.  

Para resolver essa situação existe o `stash`. Ele permite que o trabalho feito até o momento seja salvo e logo em seguida o repositório é limpo para trabalharmos com outras coisas. 
  
Podem existir vários stashes feitos na pilha de trabalho inacabado, e é possível acessá-los individualmente.   

Quando adequado, poderemos recuperar o trabalho que ainda não tinhamos terminado na branch atual ou em uma nova branch.  
  
### Salvando o trabalho atual (fazer o stash)
  
`git stash`  
  
### Lista de stash salvas 
  
`git stash list`  
  
### Recuperando o último stash feito
     
`git stash apply`  
  
Nesse caso os arquivos modificados e que estavam prontos para ser commitados terão que ser adicionados 
novamente com `git add nome_arquivo`. Caso queira recuperar da mesma forma que estavam os arquivos 
anteriormente (prontos para serem commitados) use:  
    
`git stash apply --index`  
  
### Recuperando determinado stash
  
`git stash apply stash@{3}`  
  
### Removendo o stash da pilha de stash
  
Mesmo o stash sendo aplicado com o `git stash apply` ele continua na pilha de stash. Para removê-lo use:
      
`git stash drop stash@{2}`  
  
### Removendo todos stash da pilha de stash de uma só vez
  
`git stash clear`  
    
### Recuperando o stash e o apagando logo em seguida da pilha de stash
  
`git stash pop`  
  
`git stash pop stash@{0}`  
   
Talvez seja melhor evitar o `git stash pop` e usar o `git stash apply && git stash drop`.  
  
### Nova branch a partir de uma stash

É possível criar uma stash diretamente em uma nova branch e evitar possíveis conflitos com na branch atual.  
O stash será apagado e as alterações estarão na nova branch.  
  
`git stash branch nova_branch`  
  

### Referências
  
* [Documentação do livro do Git](https://git-scm.com/book/pt-br/v1/Ferramentas-do-Git-Fazendo-Stash);  
* [Documentação do Git](https://git-scm.com/docs/git-stash)
