## Git Commit
  
É usado para confirmar e registrar que determinados arquivos estão agora sendo monitorados pelo Git. Aceita o parâmetro `-m` para inserir uma mensagem de commit.
  
```sh
git commit -m "Commit realizado."
```
  
#### Mudando a mensagem do último commit com o `--amend`
  
Se houver a necessidade de alterar a mensagem do último commit feito faça um novo commit com o parâmetro `--amend`.
  
```sh
git commit -m "Corrigindo a mensagem do último commit." --amend
```
  
> Essa alteração deve ser feita antes de um `push` para o servidor. Se for feita depois do `push` pode causar confusão no repositório.