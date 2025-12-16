# Cómo Crear Pull Requests hacia IES9018/proyecto-modelado-2025

Hola Agustina! 👋

Veo que ya tenés PRs abiertos (#8 y #25), pero te dejo una guía completa para asegurarte de que el proceso funcione correctamente.

## 📋 Pasos para crear un PR correctamente

### 1. Verificar que tu fork esté actualizado

Primero, asegurate de tener el upstream configurado:

```powershell
# Agregar el upstream (solo una vez)
git remote add upstream https://github.com/IES9018/proyecto-modelado-2025.git

# Verificar remotes
git remote -v
```

### 2. Crear una rama para tu trabajo

**Importante**: Nunca trabajes directamente en `main`. Creá ramas por cada clase o feature:

```powershell
# Ejemplo para Clase 2
git checkout main
git pull upstream main
git checkout -b clase-2-diagramas-uml

# Trabajar en tus archivos...
git add .
git commit -m "feat(clase-2): agregar diagramas de clases, secuencia y actividad"
git push origin clase-2-diagramas-uml
```

### 3. Abrir el PR desde GitHub

#### Opción A: Desde tu fork
1. Ir a https://github.com/Agustinagnz/proyecto-modelado-2025
2. Verás un banner amarillo: **"This branch is X commits ahead..."**
3. Click en **"Contribute"** → **"Open pull request"**
4. Asegurate de que:
   - Base repository: `IES9018/proyecto-modelado-2025`
   - Base: `main`
   - Head repository: `Agustinagnz/proyecto-modelado-2025`
   - Compare: tu rama (ej: `clase-2-diagramas-uml`)

#### Opción B: Desde el repositorio upstream
1. Ir a https://github.com/IES9018/proyecto-modelado-2025/pulls
2. Click en **"New pull request"**
3. Click en **"compare across forks"**
4. Seleccionar:
   - Base repository: `IES9018/proyecto-modelado-2025` (main)
   - Head repository: `Agustinagnz/proyecto-modelado-2025` (tu rama)

### 4. Título y descripción del PR

Usá un formato claro:

**Título**: `Clase X: Descripción breve - Tu Nombre`

**Ejemplo**: `Clase 2: Diagramas UML - Agustina`

**Descripción**: Incluí:
- Qué clase/contenido entregas
- Qué archivos principales agregaste
- Cualquier duda o comentario

## ⚠️ Problemas comunes y soluciones

### ❌ "No se puede crear el PR"
**Causa**: Tu rama está desactualizada o no tiene cambios respecto a upstream/main

**Solución**:
```powershell
git checkout tu-rama
git fetch upstream
git rebase upstream/main
git push origin tu-rama --force-with-lease
```

### ❌ "El PR no aparece"
**Causa**: Puede haber demora en notificaciones

**Solución**:
- Verificá en https://github.com/IES9018/proyecto-modelado-2025/pulls (debe aparecer)
- Si no aparece, revisá que hayas hecho push de tu rama: `git push origin tu-rama`

### ❌ "Dice que no tengo permisos"
**Causa**: Posible problema de autenticación

**Solución**:
```powershell
# Verificar autenticación
gh auth status

# Si no está autenticado
gh auth login
```

## 🎯 Estructura recomendada de entregas

### Clase 1 (ya tenés PR #8 ✅)
- Casos de uso con `.drawio` fuente

### Clase 2 (pendiente)
```
clase-2/
├── README.md
├── diagrama-clases.drawio
├── diagrama-clases.png
├── diagrama-secuencia.drawio
├── diagrama-secuencia.png
├── diagrama-actividad.drawio
└── diagrama-actividad.png
```

### Clase 3 (veo que tenés cambios recientes)
```
clase-3/
├── README.md
├── diagrama-arquitectura-mvc.drawio
├── diagrama-arquitectura-mvc.png
└── explicacion-principios.md
```

### Clase 4 (ver la otra Issue)
- README personalizado de tu proyecto
- CHANGELOG, LICENSE, .gitignore
- Feature única

## 📝 Workflow recomendado

```powershell
# Por cada clase:
git checkout main
git pull upstream main
git checkout -b clase-X-nombre-descriptivo

# Trabajar...
git add .
git commit -m "feat(clase-X): descripción"
git push origin clase-X-nombre-descriptivo

# Ir a GitHub y crear el PR
```

## ✅ Checklist antes de crear cada PR

- [ ] Trabajaste en una rama separada (no en `main`)
- [ ] Todos los archivos `.drawio` están incluidos
- [ ] Los nombres de archivos usan `kebab-case`
- [ ] Incluiste README o documentación explicativa
- [ ] Hiciste `git push origin tu-rama`
- [ ] Revisaste que el PR apunte a `IES9018/proyecto-modelado-2025:main`

## 🆘 Si seguís con problemas

1. **Capturá un screenshot** del error que te muestra GitHub
2. **Comentá en esta Issue** con el screenshot y yo te ayudo
3. O contactame en clase para revisar juntos

¡Cualquier duda, preguntá acá! 💪

---
_Issue generada: 2025-11-18_
