Git Commands and Terminal / Comandos de GIT y Terminal
============

_A list of commonly used Git and Terminal commands_
### Terminal Commands / Comandos de la Terminal

| Command | Description | Descripción |
| ------- | ----------- | ------------ |
| `cd [rute]` | To change directory | Cambia el directorio |
| `mkdir [name]` | Make directory | Crea una nueva carpeta |
| `ls -a` | List information about the files | Lista los archivos del directorio |
| `clear` | clear the terminal screen | Limpia la Terminal |
| `Touch [name.txt]` | create a empty file | Crea un archivo vacio |
| `rm [file]` | remove files | Elimina un archivo |
| `rm -rf [dir]` | remove directories | Elimina una carpeta |
| `pwd` | Print name of current/working directory | Muestra el directorio donde nos encontramos |
| `mv` | move (rename) files | Mueve o renombra archivos |
| `cat [name.txt]` | Concatenate files and print on the standard output | Vista previa del contenido del archivo |
| `sudo` | execute a command as another user | Ejecuta un commando como administrador |

### Config Git / Configuracion de Git

| Command | Description | Descripción |
| ------- | ----------- | ------------ |
| `git config --global user.name "name-example"` | Add a user name | Añade un nombre de usuario |
| `git config --global user.email user@example.com` | Add a email for user | Añade un correo del usuario |
| `git config --list` | List all setings | Muestra todas las configuraciones |
| `git [command] --help` | Show the Manual Page | Muestra el manual de ayuda |

### Config SSH Keys / Configuracion de Credenciales SSH

| Command | Description | Descripción |
| ------- | ----------- | ------------ |
| `ssh-keygen -t rsa -b 4096 -C "Email"` | Generate SSH key | Generar credencial SSH |
| `eval $(ssh-agent -s)` | Verify ssh agent | Verifica la existencia del servidor de credenciales SSH |
| `ssh-add [rute]` | Add SSH key to your workspace | Agrega la credencial SSH al entorno de trabajo |

### Creating Projects / Creacion de proyectos

| Command | Description | Descripción |
| ------- | ----------- | ------------ |
| `git init` | Initialize a local Git repository | Inicia un repositorio local de Git |
| `git clone [url]` | Create a local copy of a remote repository | Crea una copia local de un repositorio remoto |

### Basic Snapshotting / Snapshooting Basico

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| `git status` | Check status | Verifica el estatus del repositorio |
| `git add [file-name.txt]` | Add a file to the staging area | Añade un archivo al area de preparación |
| `git add .` | Add all new and changed files to the staging area | Añade todos los archivos al area de preparación |
| `git commit -m "[commit message]"` | Commit changes | Añade los archivos al repositorio |
| `git commit -am "[commit message]"` |Add changed files and commit | Añande los cambios y hace commit |
| `git rm -r [file-name.txt]` | Remove a file (or folder) | Elimina archivos o carpetas |
| `git rm --cached [file-name.txt]` | Unstage and remove paths only from the index. | Elimina archivos o carpetas del add |
| `git clean --dry-run` | Just show untracked files | Muestra los archivos no trackeados |
| `git clean` | Remove untracked files from the working tree. | Elimina archivos no trackeados |
| `git commit --ammend` | Ammend the last commit | Agrega los cambios al ultimo commit en caso de error |

### Branching & Merging / Ramas y fusionar

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) | Lista todas las ramas |
| `git branch -a` | List all branches (local and remote) | Lista todas las ramas locales y remotas |
| `git branch [branch name]` | Create a new branch | Crea una nueva rama |
| `git branch -d [branch name]` | Delete a branch | Elimina una rama |
| `git branch -D [branch name]` | Allow deleting the branch irrespective of its merged status | Elimina una rama sin importar su status|
| `git show-branch --all` | List all branches local | Lista todas las ramas en local |
| `git push origin --delete [branch name]` | Delete a remote branch | Elimina una rama remota |
| `git checkout -b [branch name]` | Create a new branch and switch to it | Crea una nueva rama y cambia a ella |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it | Clona una rama remota y cambia a ella |
| `git checkout [branch name]` | Switch to a branch | Cambiar a una rama determinada |
| `git checkout -` | Switch to the branch last checked out | Cambia a la ultima rama seleccionada |
| `git checkout -- [file-name.txt]` | Discard changes to a file | Descarta los cambios de un archivo |
| `git checkout [ref]` | Move to [ref] (git reflog). Restore working tree files| Te mueve a un commit en el tiempo (git reflog) y restaura los archivos a ese momento |
| `git merge [branch name]` | Merge a branch into the active branch | Fusiona una rama a la rama activa
| `git merge [source branch] [target branch]` | Merge a branch into a target branch | Fusiona una rama a una rama determinada |
| `git stash` | Saves your local modifications away and reverts the working directory to match the HEAD commit | Guarda las modificaciones en un stash y revierte el branch al estado del último commit
| `git stash list` | List the stash entries that you currently have | Lista los stash actuales
| `git stash branch [branch name]` | Creates and checks out a new branch named with the stsh | Crea una nueva branch con el stash
| `git stash pop` | Remove a single stashed state from the stash list and apply it on top of the current working tree state | Revierte el stash 
| `git stash clear` | Remove all stashed entries |Elimina los Stash

### Sharing & Updating Projects / Compartiendo y Repositorios Remotos

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository | Envia el repositorio local a remoto |
| `git push origin --delete [branch name]` | Delete a remote branch | Elimina un repositorio remoto |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository | Hace un feth y fusiona
| `git pull origin [branch name] --allow-unrelated-histories` | Allow to merge histories that do not share a common ancestor | Hace un feth y fusiona aunque no tengan historia en común
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository | Crea un repositorio remoto |
| `git remote add upstream [project URL]` | Fork | Copia un repositorio externo a un branch upstream |
| `git remote -v` | list remote connections | Lista las conexiones remotas |
| `git remote set-url [branch name] [url]` | Change the url | Cambia la url del repositorio |
| `git remote rm [branch name]` | Remove a remote repository | Elimina un repositorio remoto |
| `git remote prune` | Delete the refs to branches that don't exist on the remote | Elimina la copia local de un branch eliminado en remoto |
| `git rebase [branch name]` | Reapply commits on top of another base tip | Trae los commit de un branch mas avanzado y los aplica a este branch |
| `git rebase --continue` | Restart the rebasing process after having resolved a merge conflict. | Continúa el rebase una vez solucionado los conflictos |
| `git rebase --abort` | Abort the rebase operation. | Cancela el rebase |
| `git blame -c [file name]` | Show what revision and author last modified each line of a file | Muestra quién y que modificó de un archivo |
| `git shortlog -sn --all --no-merge` | Summarize 'git log' output | Muestra cuántos commit ha hecho cada miembro, quitando los eliminados y sin los merges. |

### Inspection & Comparison / Inspeccion y Comparacion

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| `git log` | View changes | Muestra los cambios en el repositorio |
| `git log --summary` | View changes (detailed) | Muestra los cambios en el repositorio detalladamente |
| `git log -all --graph --decorate --oneline` | View changes (Max-detailed) | Muestra todos los cambios del repositorio detallada y graficamente |
| `git diff [source branch] [target branch]` | Preview changes before merging | Compara los diferentes cambios |
| `git reflog` | Shows the log of the reference provided in the command-line (or HEAD, by default) | Muestra toda la historia con su referencia |

### Others / Otros

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| `alias [name=] "command"` | Create a shorcut for a command | Crea un alias para llamar a un comando |
| `git tag -a [name] -m "message" [id/hashtag]` | Create a tag for a commit | Crea un tag de un commit en especifico |
| `git show-ref --tags` | List all tags | Lista los tags existentes |
| `git push --tags` | Push tags to your repository | Envia los tags al repositorio remoto |
| `git tag -d [name]` | Delete a tag | Elimina un tag en especifico |
| `git push origin :refs/tags/[name]` | Delete a tag from GitHub | Elimina un tag dentro de GitHub |
| `gitk` | Open GUI | Abre una interfaz grafica |
| `git cherry.pick [id]` | Take commit from other branches | Trae un commit especifico desde otra rama |
| `git grep -n [word]` | Search words in the proyect | Busca la palabra especificada en todo el proyecto |
| `git reset --soft [ref]` | Reset current HEAD to the specified state. Does not touch the index file or the working tree at all (but resets the head to commit). This leaves all your changed files "Changes to be committed" | Vuelve al commit especificado, no toca archivos y deja todo pendiente de commit |
| `git reset --hard [ref]` | Reset current HEAD to the specified state. Resets the index and working tree. Any changes to tracked files in the working tree since commit are discarded. | Vuelve al commit especificado, revierte los archivos y nada queda pendiente. Todo despues de ese commit es descartado. |
| `git commit --amend` | Replace the tip of the current branch by creating a new commit with more changes (to be forced first with git add [filename]). | Reemplaza el último commit con uno nuevo con más cambios (que hay que forzar con git add [archivo]) previamente. |

### Notes  / Notas
**Evitar que Git suba ciertos archivos**
Crear un fichero con una lista de los archivos, extensiones o carpetas a ignorar y guardarlo en el directorio del proyecto como ".gitignore” Ej.
```html
*.jpg
*.log
*.key
/images/*
```
**Salir del editor de texto de la consola**
ESC --> SHIFT+Z+Z


