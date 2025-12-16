# Cómo Crear Pull Requests hacia IES9018/proyecto-modelado-2025

Hola Vanesa! 👋

Veo que ya tenés PRs abiertos (#4 y #18), pero te dejo una guía completa para que puedas crear PRs adicionales para las Clases 3 y 4 que están en tu fork.

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
# Ejemplo para Clase 3
git checkout main
git pull upstream main
git checkout -b clase-3-arquitectura

# Trabajar en tus archivos...
git add clase-3-principios-patrones-arquitecturas.md diagramadeflujo.md
git commit -m "feat(clase-3): agregar arquitectura MVC y principios"
git push origin clase-3-arquitectura
```

### 3. Abrir el PR desde GitHub

#### Opción A: Desde tu fork
1. Ir a https://github.com/Anmonte/vane_legui-blog
2. Verás un banner amarillo: **"This branch is X commits ahead..."**
3. Click en **"Contribute"** → **"Open pull request"**
4. Asegurate de que:
   - Base repository: `IES9018/proyecto-modelado-2025`
   - Base: `main`
   - Head repository: `Anmonte/vane_legui-blog`
   - Compare: tu rama (ej: `clase-3-arquitectura`)

#### Opción B: Desde el repositorio upstream
1. Ir a https://github.com/IES9018/proyecto-modelado-2025/pulls
2. Click en **"New pull request"**
3. Click en **"compare across forks"**
4. Seleccionar:
   - Base repository: `IES9018/proyecto-modelado-2025` (main)
   - Head repository: `Anmonte/vane_legui-blog` (tu rama)

### 4. Título y descripción del PR

Usá un formato claro:

**Título**: `Clase X: Descripción breve - Vanesa`

**Ejemplo**: `Clase 3: Arquitectura MVC - Vanesa Legui`

**Descripción**: Incluí:
- Qué clase/contenido entregas
- Qué archivos principales agregaste
- Cualquier duda o comentario

## 📊 Estado actual de tus entregas

### ✅ Clase 1 y 2 (parcialmente en PRs existentes)
- PR #4: Sistema de categorías + algunos diagramas
- PR #18: Feature/comentarios

### 📌 Clase 3 (en tu fork, falta PR)
Veo que tenés:
- `clase-3-principios-patrones-arquitecturas.md` modificado
- `diagramadeflujo.md` con diagramas MVC
- Imágenes de diagramas Mermaid

**Acción**: Crear un PR específico para Clase 3

```powershell
git checkout main
git pull origin main
git checkout -b clase-3-arquitectura-mvc

# Asegurate de incluir solo los archivos de Clase 3
git add clase-3-principios-patrones-arquitecturas.md
git add diagramadeflujo.md
git add image.png mermaid-diagram-*.png
git add scripts/

git commit -m "feat(clase-3): arquitectura MVC y principios de diseño"
git push origin clase-3-arquitectura-mvc

# Luego ir a GitHub y crear el PR
```

### 📌 Clase 4 (ver la otra Issue)
Ya tenés mucho avanzado en tu fork:
- README personalizado ✅
- CHANGELOG.md ✅
- Releases publicados ✅

Solo falta crear un PR para mostrar estos cambios.

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

## 🎯 PRs recomendados para completar

### PR para Clase 3
```powershell
git checkout main
git checkout -b clase-3-arquitectura-mvc
# Incluir archivos de Clase 3
git add clase-3-principios-patrones-arquitecturas.md diagramadeflujo.md
git commit -m "feat(clase-3): arquitectura MVC, principios y patrones"
git push origin clase-3-arquitectura-mvc
```

**Título PR**: `Clase 3: Arquitectura MVC y Principios - Vanesa Legui`

### PR para Clase 4
```powershell
git checkout main
git checkout -b clase-4-version-independiente
# Incluir archivos de identidad
git add README.md CHANGELOG.md LICENSE .gitignore
git add Clase1.drawio  # tus .drawio fuente
git commit -m "docs: vane_legui-blog v1.0.0 versión independiente"
git push origin clase-4-version-independiente
```

**Título PR**: `Clase 4: vane_legui-blog v1.0.0 - Vanesa Legui`

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

¡Tu trabajo está excelente, solo falta organizarlo en PRs! 💪

---
_Issue generada: 2025-11-18_
