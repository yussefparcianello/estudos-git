# Estudos GitHub

## Limpando o commit history

Sabe aquela situação em que seu repositório está com o project history repleto de registros desinteressantes de commits? Poie é, se vocẽ quiser zerar o seu project history mantendo intacto o estado dos arquivos do repositório, faça o seguinte:
```
#crie uma branch órfa, ou seja, uma cópia da branch atual, mas sem os registros do project history
git checkout --orphan latest_branch

Adiciona todos os arquivos e suas modificações
git add -A

Efetua o commit
git commit -am "Meu primeiro commit"

Deleta a 'não mais desejada' branch master
git branch -D master

Renomeia a branch atual
git branch -m master

Sobe tudo para o github
git push -f origin master
```