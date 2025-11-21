# Pruebas de Comandos de Git

Objetivo: practicar los comandos esenciales de Git con ejemplos rápidos.


## Inicialización
- Crear repo: `git init`
- Ver estado: `git status`
- Ignorar archivos: crea `.gitignore` y añade patrones (por ejemplo: `node_modules/`, `.env`).

## Flujo básico de trabajo
- Añadir archivos: `git add .`
- Confirmar cambios: `git commit -m "Mensaje claro del cambio"`
- Ver historial: `git log --oneline`
- Ver diferencias: `git diff`

## Ramas
- Renombrar rama principal: `git branch -M main`
- Crear y cambiar: `git checkout -b feature/mi-cambio`
- Listar ramas: `git branch`
- Volver a `main`: `git checkout main`
- Fusionar una rama: `git merge feature/mi-cambio`

## Remoto
- Añadir remoto: `git remote add origin https://github.com/usuario/repositorio.git`
- Ver remotos: `git remote -v`
- Subir rama por primera vez: `git push -u origin main`
- Traer cambios: `git pull`

## Revisar y comparar
- Ver un commit específico: `git show <hash>`
- Log bonito: `git log --graph --decorate --oneline --all`
- Quién cambió cada línea: `git blame <archivo>`

## Deshacer y arreglar (usar con cuidado)
- Quitar del área de staging: `git restore --staged <archivo>`
- Restaurar archivo al último commit: `git restore <archivo>`
- Revertir un commit (crea uno nuevo): `git revert <hash>`
- Reset suave al commit anterior: `git reset --soft HEAD^`
- Reset duro al commit anterior: `git reset --hard HEAD^`  (¡cuidado, pierde cambios!)

## Stash y cherry-pick
- Guardar cambios temporales: `git stash push -m "WIP"`
- Listar stashes: `git stash list`
- Recuperar último stash: `git stash pop`
- Aplicar un commit específico a otra rama: `git cherry-pick <hash>`

## Buenas prácticas
- Mensajes de commit descriptivos y en imperativo.
- Una rama por feature/bugfix.
- Pull requests pequeños y frecuentes.
- Mantén `main` siempre estable.

## Cheatsheet rápido
- Inicializar: `git init`
- Estado: `git status`
- Añadir: `git add .`
- Commit: `git commit -m "mensaje"`
- Ramas: `git checkout -b rama`; `git merge rama`
- Remoto: `git remote add origin URL`; `git push -u origin main`
- Historial: `git log --oneline`
- Diferencias: `git diff`
- Revertir: `git revert <hash>`
- Stash: `git stash push`; `git stash pop`

## Ejercicios rápidos
1) Crea un archivo `hola.txt`, añade texto, `git add .`, `git commit -m "Agregar hola"`.
2) Crea `feature/saludo`, edita `hola.txt`, confirma, vuelve a `main` y fusiona.
3) Añade remoto (si usas GitHub), sube `main` y luego `feature/saludo`.

Consejo: en PowerShell/Windows, usa rutas con `\` y evita caracteres especiales en mensajes sin comillas.