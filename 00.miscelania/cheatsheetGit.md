# 🚀 Guía rápida (Cheatsheet) de Git y GitHub

## 1. Configuración inicial
Establece la identidad de usuario antes de realizar cualquier confirmación en la máquina local.

* `git config --global user.name "Tu Nombre"`: Define el nombre del autor de manera global.
* `git config --global user.email "tu@email.com"`: Asocia el correo electrónico a los commits realizados.
* `git config --list`: Lista los parámetros de configuración activos.

---

## 2. Creación e inicialización de proyectos

* `git init`: Inicializa un repositorio Git local en la carpeta actual creando el directorio oculto `.git` y activando el área de preparación (*Staging Area*).
* `git clone <URL>`: Copia y descarga un repositorio remoto existente en tu computadora local junto con todo su historial.

---

## 3. Ciclo de trabajo local

* `git status`: Consulta el estado actual de los archivos (rastreados, sin rastrear, modificados o en el área de preparación).
* `git add <archivo>`: Añade los cambios de un archivo al área de preparación (*Staging Area*).
* `git add .`: Agrega todos los archivos modificados o nuevos del directorio al *Staging Area*.
* `git commit -m "tipo: mensaje"`: Guarda una instantánea permanente de los cambios agregados al *Staging Area* con un mensaje explicativo.
* `git commit -am "mensaje"`: Prepara e incluye de forma directa todos los archivos rastreados que han sido modificados sin requerir `git add` previo.
* `git log`: Visualiza el historial de confirmaciones (*commits*) realizadas en el proyecto.
* `git diff`: Muestra las diferencias de los archivos modificados en el directorio de trabajo que aún no se han añadido al *Staging Area*.

---

## 4. Trabajo con repositorios remotos (GitHub)

* `git remote add origin <URL>`: Vincula un repositorio local previamente creado con un repositorio remoto en GitHub asignándole el alias `origin`.
* `git push origin <rama>`: Envía los commits locales al repositorio remoto en GitHub.
* `git fetch`: Descarga las novedades del repositorio remoto hacia el repositorio local sin integrarlas en el código activo.
* `git pull`: Descarga e integra automáticamente los cambios del repositorio remoto en tu copia de trabajo local (combina `git fetch` y `git merge`).

---

## 5. Corrección de errores y deshacer cambios

* `git checkout -- <archivo>`: Descarta las modificaciones de la copia de trabajo y restaura el archivo a su último estado confirmado.
* `git reset HEAD <archivo>`: Saca un archivo del *Staging Area* conservando sus cambios en el directorio de trabajo.
* `git rm --cached <archivo>`: Elimina un archivo del seguimiento de Git sin borrarlo físicamente del disco.
* `git commit --amend`: Modifica la última confirmación realizada para agregar cambios olvidados o corregir el mensaje del commit.

---

## 💡 Buenas prácticas clave
* **Archivo `.gitignore`**: Incluye patrones de archivos que no deben rastrearse (como claves, archivos temporales o dependencias).
* **Frecuencia de actualización**: Ejecuta `git pull` siempre al iniciar la jornada de trabajo para mantener el código sincronizado con el repositorio remoto.
