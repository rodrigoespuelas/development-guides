# GIT

## Recursos

https://githowto.com/
http://rogerdudler.github.io/git-guide/index.es.html
https://lemoncode.net/lemoncode-blog/2017/12/12/git-y-visual-studio-code  

http://rogerdudler.github.io/git-guide/index.es.html   
https://es.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud  
https://git-scm.com/book/es/v1/  
https://code.tutsplus.com/es/tutorials/quick-tip-leveraging-the-power-of-git-stash--cms-22988  
https://es.atlassian.com/git/tutorials/undoing-changes  
https://www.hostinger.es/tutoriales/comandos-de-git
https://frontendlabs.io/940--la-importancia-del-comando-git-stash-en-un-proyecto

### Version de Git
`git --version`

### Repositorio Local  
* Directorio de trabajo  
* Index (stage)  
* HEAD  

### 1. Preparation
global gitconfig file is located in C:\Users\MyLogin\.gitconfig  
`git config --global user.name "Rodrigo Espuelas Garmilla"`  
`git config --global user.email "rodrigoespuelas@yahoo.es"`  

###### Eliminar el valor de la configuración en el repositorio local
`git config --unset core.autocrlf`  

###### Visual Studio Code 
`git config --global core.editor "code --wait"`  

###### Meld (Diff & Merge)
`git config --global merge.tool meld`   
git config --global diff.tool meld`    
git config --global mergetool.meld.path "C:\Program Files (x86)\Meld\Meld.exe"`    

###### Meld

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

###### Agregar archivos de forma interactiva  
`git add -i`  

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

##### Git Stash  
###### remover los cambios que no se han commiteado.  
`git reset --hard`   

###### Stasheando cambios  
`git stash`   
###### Re-aplicando los ultimos cambios stasheados
`git stash pop`  
`git stash apply stash@{1}`  
###### Listar la pila de stash  
`git stash list`  
###### Aplicar un stash
`git stash apply stash@{1}`  
###### Borrar un stash
`git stash drop stash@{1}`  

##### 20. Moving files  
`mkdir lib`    
`git mv hello.html lib`     
`git status`    
`git commit -m "Moved hello.html to lib"`   

##### 24. Creating a Branch
`git checkout -b feature_x`   
###### Volver a la rama principal
`git checkout master`   
###### Borra la rama
`git branch -d feature_x`   

### 25. Navigating Branches  
`git hist --all`    

### 28. Merging ?
`git checkout style`         
`git merge master`         
`git hist --all`        

##### 35. Merging to the Master branch
`git checkout master`        
`git merge style`       

##### 37. Cloning repositories (Copia 'test_copy' local apuntando a 'test')  
`git clone test test_copy`        
`git remote`        

##### 39. What is origin?  
`git remote show origin`        

###### Optimizar el repositorio
`git gc`        

##### Comandos básicos
* git add [archivo] Agrega el archivo al Stage
* git rm --cached [archivo] Quita el archivo del Stage
* git add -A Agrega todos los archivos al Stage
* git rm -f [archivo] Quita los archivos del Stage y borrarlos
* git commit -m "[mensaje]" Realiza commit al archivo y envia un mensaje para saber que se hizo ejm. ‘Iniciar nuestro landing’
* git log Muestra el historial de todos los commit que hemos realizado
* git log --oneline Version resumida del historial
* git log -[numero] Muestra la cantidad de commits segun el numero que indiques
* git commit --amend Anexa al ultimo commit, un cambio que hayamos olvidado hacer.
* git tag -a [version] -m "[mensaje]" Crea un tag (etiqueta) a el último commit realizado
* git tag [version] [hash1] Crear un tag a un hash especifico
* git tag -l Muestra todos los tag
* git tag -d [version] Elimina el tag
* git branch [nombre] Crea una nueva rama (Master también se considera una rama)
* git branch -l Lista todas las ramas que tienes
* git branch -d Borra la rama si esta esta vacía.
* git branch -D Borra la rama aún asi esta contenga información.
* git branch -m [NombreActual][NombreNuevo] Cambia de nombre a una rama
* git config --list Muestras todas las propiedades que git a configurado
* git diff [hash1] Muestra las diferencias entre el hash que has puesto con el ultimo que tenemos
* git reset --soft Quita un cambio, pero lo mantiene en el Stage.
* git reset --mixed Quita un cambio, lo quita del stage. Los mantiene en el working directory
* git reset --hard Quita un cambio, los borra totalmente, pero si tienes guardado el hash1, lo puedes recuperar
* git checkout [branch] Nos permite pasearnos entre los branchs (ramas), tambien crearlas.




