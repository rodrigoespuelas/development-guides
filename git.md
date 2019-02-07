# GIT

## Recursos

http://rogerdudler.github.io/git-guide/index.es.html   
https://es.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud  
https://githowto.com/  

### Version de Git
`git --version`

### Repositorio Local  
* Directorio de trabajo  
* Index (stage)  
* HEAD  

### 1. Preparation
`git config --global user.name "Rodrigo Espuelas Garmilla"`  
`git config --global user.email "rodrigoespuelas@yahoo.es"`  

### Clonar GitLab
`git clone https://gitlab.com/rodrigoespuelas/aspnet_mvc5_full_version.git`

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

#### o bien
`git add .` 

#### Commit (archivo esta incluído en el HEAD)
`git commit -m 'Primer commit'` 

#### 
`git push origin master` 

### 10. History  
`git log --pretty=oneline` 

### 13. Tagging versions
`git tag`  
`git tag 1.0.0 1b2e1d63ff`  
`git log`  

### 14. Discarding local changes (before staging)
### 15. Cancel Staged changes (before committing)
### 16. Cancelling commits





