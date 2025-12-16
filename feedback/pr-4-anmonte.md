# Instrucciones para continuar – PR #4 (Anmonte)

¡Hola! 👋 Gracias por tu aporte en el PR #4.

Te dejo dos caminos posibles para subir los cambios que estás trabajando en tu fork: 1) continuar en el mismo PR, o 2) abrir un PR nuevo consolidado. Elegí el que te quede más cómodo.

---

## Opción A: Seguir en el mismo PR (recomendado)

Esto mantiene toda la discusión y el historial en un solo lugar.

1) Verificá (y si falta, agregá) el remoto `upstream` al repo del IES9018:

```bash
git remote -v
# Si no aparece "upstream" apuntando a IES9018, agregalo:
git remote add upstream https://github.com/IES9018/proyecto-modelado-2025.git
```

2) Traé los últimos cambios y actualizá tu rama del PR (reemplazá `tu-rama-del-PR` por el nombre de la rama que usaste para abrir el PR; podés verlo en la página del PR):

```bash
git fetch origin
git fetch upstream

git checkout tu-rama-del-PR
# Opcional simple (merge):
git merge upstream/main
# Alternativa más prolija (rebase):
# git rebase upstream/main
```

3) Aplicá tus cambios pendientes (por ejemplo: subir `.drawio`, renombrar archivos a kebab-case, ajustar Markdown) y commiteá usando Conventional Commits:

```bash
# Ejemplos
# docs(clase-1): mejorar descripción y estructura del caso de uso
# feat(clase-1): agregar archivo fuente .drawio del diagrama de casos de uso

git add -A
git commit -m "feat(clase-1): agregar fuente .drawio y referenciar imagen"
git push origin tu-rama-del-PR
```

Listo: el PR #4 se actualizará automáticamente con estos nuevos commits.

---

## Opción B: Abrir un PR nuevo consolidado

Si preferís partir de un estado limpio y dejar este PR como referencia, podés crear un PR nuevo. En ese caso:

1) Asegurate de tener el `upstream` y actualizá tu `main` local con la `main` del IES9018:

```bash
git checkout main
git fetch origin
git fetch upstream

git merge upstream/main
# o, si usás rebase:
# git rebase upstream/main

git push origin main
```

2) Creá una nueva rama de trabajo y aplicá los cambios mejorados allí:

```bash
git checkout -b feat/clase-1-ajustes
# Copiá/ajustá tus archivos: .drawio + .png, Markdown con secciones, nombres en kebab-case

git add -A
git commit -m "feat(clase-1): consolidar caso de uso y diagramas con .drawio"
git push origin feat/clase-1-ajustes
```

3) Abrí el PR desde tu fork hacia `IES9018/proyecto-modelado-2025:main` con un título estilo Conventional Commits, por ejemplo:

```text
docs(clase-1): mejorar caso de uso "Leer Artículo" y referenciar diagrama
```

---

## Recordatorios de calidad (aplican a cualquiera de las dos opciones)

- Archivos fuente: incluí los `.drawio` junto a las imágenes `.png`.
- Nombres: usá minúsculas con guiones (kebab-case), sin espacios.
- Markdown: encabezados con línea en blanco, listas numeradas, newline al final.
- Mensajes: Conventional Commits (tipo(scope): descripción).

Cuando lo tengas, avisá con un comentario y lo reviso de nuevo. ¡Gracias! 🚀
