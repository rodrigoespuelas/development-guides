# GIT

## Recursos

https://githowto.com/  
https://lemoncode.net/lemoncode-blog/2017/12/12/git-y-visual-studio-code  

http://rogerdudler.github.io/git-guide/index.es.html   
https://es.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud  
https://git-scm.com/book/es/v1/  
https://code.tutsplus.com/es/tutorials/quick-tip-leveraging-the-power-of-git-stash--cms-22988  
https://es.atlassian.com/git/tutorials/undoing-changes  

### Version de Git
`git --version`

### Repositorio Local  
* Directorio de trabajo  
* Index (stage)  
* HEAD  

### 1. Preparation
`git config --global user.name "Rodrigo Espuelas Garmilla"`  
`git config --global user.email "rodrigoespuelas@yahoo.es"`  
`git config --global core.editor "code --wait"`  

#### Comprobando la configuración  
`git config --list`  
`git config user.name`  

### Clonar GitLab
`git clone https://gitlab.com/rodrigoespuelas/test.git`

### Clonar BitBucket
`git clone https://rodrigoespuelas@bitbucket.org/rodrigoespuelas/test.git`

### Clonar GitHub
`git clone https://github.com/rodrigoespuelas/test.git` 

### Clonar Azure DevOps
`git clone https://rodrigoespuelas.visualstudio.com/test/_git/test` 

### Staging Area
`git status` 


`# On branch master (rama principal)`   
`# Changes not staged for commit:`   
`#   (use "git add <file>..." to update what will be committed)`   
`#   (use "git checkout -- <file>..." to discard changes in working directory)`   
`#`   
`#   modified:   hello.html`   
`#`   
`no changes added to commit (use "git add" and/or "git commit -a")`   

#### Para añadir un solo archivo
`git add nombre_del_archivo` 
 
#### Para añadir todo lo que hay en el directorio actual
`git add --all` 
`git add .` 

#### Para añadir solo los que estan trackeados
`git add -A` 

#### Commit (archivo esta incluído en el HEAD)
`git commit -m 'Primer commit'` 
`git commit -a -m 'Primer commit'` 

#### Rectificar commit: git commit –amend
`git commit --amend -m "Nuevo mensaje corregido para el commit"` 

#### 
`git push origin master` 

####


### 7. Staging and committing  
`git add a.html`  
`git add b.html`  
`git commit -m "Changes for a and b"`  
`git add c.html`  
`git commit -m "Unrelated change to c"`  

### 8. Commiting the changes  

### 9. Changes, not files  

### 10. History  
`git log`   
`git log --pretty=oneline`   
`git log --pretty=oneline --graph`     

`git log --pretty=oneline --max-count=2`   
`git log --pretty=oneline --since='5 minutes ago'`   
`git log --pretty=oneline --until='5 minutes ago'`   
`git log --pretty=oneline --author=<your name>`   
`git log --pretty=oneline --all`   

### 11. Aliases  
`git config --global alias.co checkout`     
`git config --global alias.ci commit`   
`git config --global alias.st status`   
`git config --global alias.br branch`   
`git config --global alias.hist "log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short"`     
`git config --global alias.type 'cat-file -t'`   
`git config --global alias.dump 'cat-file -p'`   

### 12. Getting older versions  
##### Getting hashes for the previous versions
`git hist`   
`git checkout <hash>`   
##### Returning to the latest version in the master branch
`git checkout master`   
`cat hello.html`     
 
### 13. Tagging versions
`git tag`  
`git tag 1.0.0 1b2e1d63ff`  
`git log`  

### 14. Discarding local changes (before staging)
### 15. Cancel Staged changes (before committing)
### 16. Cancelling commits

#### Git Stash  
##### remover los cambios que no se han commiteado.  
`git reset --hard`   

##### 1. Stasheando cambios  
`git stash`   

##### 2. Re-aplicando cambios stasheados
`git stash pop`  

### 20. Moving files  
`mkdir lib`    
`git mv hello.html lib`     
`git status`    
`git commit -m "Moved hello.html to lib"`   

### 24. Creating a Branch
`git checkout -b style`    
`git status`   

