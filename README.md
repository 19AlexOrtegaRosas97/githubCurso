Comandos Chidos  y necesarios de GIT

Log
git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"

Status
git config --global alias.s status --short

Alternativa útil de status
git config --global alias.s status -sb

📌 Configuración Inicial
git config --global user.name "Tu Nombre" → Configura el nombre de usuario.
git config --global user.email "tu@email.com" → Configura el correo electrónico.
git config --list → Muestra la configuración actual de Git.

📌 Iniciar y Clonar Repositorios
git init → Inicializa un nuevo repositorio en la carpeta actual.
git clone <URL> → Clona un repositorio remoto en tu máquina local.

📌 Seguimiento de Cambios
git status → Muestra el estado actual del repositorio.
git add <archivo> → Agrega un archivo al área de preparación (staging).
git add . → Agrega todos los archivos modificados al área de preparación.
git commit -m "Mensaje" → Guarda los cambios en el repositorio con un mensaje.

📌 Historial y Diferencias
git log → Muestra el historial de commits.
git log --oneline → Muestra el historial de commits en una línea cada uno.
git diff → Muestra diferencias entre archivos modificados y el último commit.

📌 Ramas (Branches)
git branch → Lista las ramas disponibles.
git branch <nombre_rama> → Crea una nueva rama.
git checkout <nombre_rama> → Cambia a otra rama.
git checkout -b <nombre_rama> → Crea y cambia a una nueva rama.
git merge <rama> → Fusiona una rama en la actual.

📌 Ramas (Branches) - Continuación
git switch <nombre_rama> → Cambia a otra rama (más recomendado que checkout).
git switch -c <nombre_rama> → Crea y cambia a una nueva rama.
git merge <rama> → Fusiona una rama con la actual.
git rebase <rama> → Reaplica commits de una rama sobre otra, manteniendo un historial más limpio.
git branch -d <nombre_rama> → Elimina una rama local.
git push origin --delete <nombre_rama> → Elimina una rama remota.

📌 Trabajando con Remotos
git remote -v → Muestra los remotos configurados.
git remote add origin <URL> → Agrega un repositorio remoto.
git fetch origin → Descarga cambios sin fusionarlos en la rama actual.
git pull origin <rama> → Descarga y fusiona los cambios remotos en la rama actual.
git push origin <rama> → Sube los cambios de la rama actual al repositorio remoto.

📌 Restaurar y Revertir Cambios
git restore <archivo> → Revierte cambios no confirmados en un archivo.
git restore --staged <archivo> → Quita un archivo del área de preparación sin perder cambios.
git reset --soft HEAD~1 → Deshace el último commit pero mantiene los cambios en staging.
git reset --mixed HEAD~1 → Deshace el último commit y los cambios vuelven a archivos sin seguimiento.
git reset --hard HEAD~1 → Deshace el último commit y borra los cambios definitivamente.
git revert <commit> → Crea un commit inverso para deshacer un commit específico sin modificar el historial.

📌 Etiquetas (Tags)
git tag → Lista todas las etiquetas en el repositorio.
git tag <nombre_etiqueta> → Crea una nueva etiqueta ligera.
git tag -a <nombre_etiqueta> -m "Mensaje" → Crea una etiqueta con anotación.
git push origin <nombre_etiqueta> → Sube una etiqueta al repositorio remoto.
git push --tags → Sube todas las etiquetas al repositorio remoto.
git tag -d <nombre_etiqueta> → Elimina una etiqueta local.
git push origin --delete <nombre_etiqueta> → Elimina una etiqueta en el repositorio remoto.

📌 Búsquedas y Filtrado
git grep "texto" → Busca una cadena en los archivos del repositorio.
git log --grep="mensaje" → Busca commits con un mensaje específico.
git log --author="Nombre" → Filtra commits por autor.
git shortlog -sn → Muestra un resumen de commits por autor.

📌 Stash (Guardar Cambios Temporalmente)
git stash → Guarda temporalmente los cambios no confirmados.
git stash list → Muestra la lista de cambios guardados.
git stash apply → Aplica los cambios guardados sin eliminarlos del stash.
git stash pop → Aplica los cambios guardados y los elimina del stash.
git stash drop → Elimina un stash específico.
git stash clear → Borra todos los stashes.

📌 Submódulos (Repositorios dentro de otro repositorio)
git submodule add <URL> → Agrega un submódulo.
git submodule update --init --recursive → Clona y actualiza todos los submódulos.
git submodule foreach git pull → Actualiza todos los submódulos a su última versión.

📌 Otros Comandos Útiles
git blame <archivo> → Muestra quién modificó cada línea de un archivo.
git show <commit> → Muestra detalles de un commit específico.
git reflog → Muestra un historial de referencias recientes, útil para recuperar commits eliminados.
git bisect start → Inicia una búsqueda binaria para encontrar un commit que introdujo un error.
git cherry-pick <commit> → Aplica un commit específico a la rama actual.