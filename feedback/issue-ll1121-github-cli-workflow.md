# 🛠️ Guía: GitHub CLI y Gestión de Issues - LautaroBlog

**Para:** Lautaro Lopez (@LL1121)  
**Fecha:** 2025-11-19  
**Objetivo:** Optimizar tu workflow de desarrollo con GitHub CLI y gestión efectiva de Issues

---

## 📥 Instalación de GitHub CLI

### Opción 1: winget (Recomendado para Windows 11)
```powershell
winget install --id GitHub.cli
```

### Opción 2: Chocolatey
```powershell
# Si tienes Chocolatey instalado
choco install gh
```

### Opción 3: Scoop
```powershell
# Si usas Scoop
scoop install gh
```

### Verificar Instalación
```powershell
gh --version
# Debe mostrar: gh version X.X.X (fecha)
```

---

## 🔐 Autenticación

```powershell
# Iniciar sesión interactiva
gh auth login

# Seguir los pasos:
# 1. GitHub.com
# 2. HTTPS
# 3. Yes (autenticar con credenciales)
# 4. Login with a web browser (más fácil)
# 5. Copiar el código que te muestra
# 6. Pegar en el navegador y autorizar
```

---

## 📋 Comandos Útiles para tu Proyecto

### Ver Estado de tu Fork
```powershell
# En tu carpeta LautaroBlog
cd C:\ruta\a\tu\LautaroBlog

# Ver Issues abiertas en TU fork
gh issue list

# Ver Issues con más detalles
gh issue list --json number,title,state,updatedAt
```

### Cerrar Issues Verificando Checklist

**Ejemplo práctico:**

```powershell
# Ver Issue #1 (Clase 1) completa
gh issue view 1

# Revisar checklist vs tu código:
# ✅ ¿Tienes casos de uso en carpeta casos_de_uso/?
# ✅ ¿Archivos nombrados en kebab-case?
# ✅ ¿Incluyes .drawio además de PNG?

# Si TODO está completo, cerrar Issue:
gh issue close 1 --comment "✅ Completado: casos de uso organizados en carpeta, archivos .drawio incluidos, nombres en kebab-case"

# Si FALTA algo, comentar qué está pendiente:
gh issue comment 1 --body "⚠️ Pendiente: falta agregar archivos .drawio para diagramas"
```

### Flujo Completo para Cada Issue

#### Issue #1 - Clase 1: Casos de Uso

```powershell
# 1. Ver requisitos
gh issue view 1

# 2. Verificar tu código
ls casos_de_uso/  # ¿Existen los archivos?
cat casos_de_uso/cu01-publicar-articulo.md  # ¿Formato correcto?

# 3. Checklist mental:
# [ ] Carpeta casos_de_uso/ creada
# [ ] Archivos en kebab-case (cu01-..., cu02-...)
# [ ] Flujos principales y alternativos documentados
# [ ] Newline al final de archivos
# [ ] .drawio del diagrama de casos de uso

# 4. Cerrar cuando TODO esté verde:
gh issue close 1 --comment "✅ Clase 1 completada:
- 3 casos de uso documentados
- Organizados en casos_de_uso/
- Nombres en kebab-case
- Diagrama .drawio incluido"
```

#### Issue #4 - Clase 2: Diagramas UML

```powershell
# 1. Ver requisitos
gh issue view 4

# 2. Verificar tu estructura
ls diagramas/  # ¿Existen .drawio Y .png?

# Checklist:
# [ ] Carpeta diagramas/ creada
# [ ] diagrama-clases.drawio + .png
# [ ] diagrama-secuencia.drawio + .png
# [ ] diagrama-actividad.drawio + .png
# [ ] Todos en kebab-case

# 3. Si TODO está completo:
gh issue close 4 --comment "✅ Clase 2 completada:
- 3 diagramas con archivos .drawio y .png
- Organizados en carpeta diagramas/
- Nomenclatura kebab-case aplicada"
```

#### Issue #5 - Clase 3: Patrón MVC

```powershell
# Ver Issue
gh issue view 5

# Verificar:
# [ ] diagrama-mvc.drawio + .png en carpeta diagramas/
# [ ] Documento explicando arquitectura (opcional: docs/arquitectura.md)
# [ ] Anotaciones claras en diagrama

# Cerrar:
gh issue close 5 --comment "✅ Clase 3 completada: diagrama MVC documentado con arquitectura clara"
```

#### Issue #6 - Clase 4: Versión Independiente

```powershell
gh issue view 6

# Checklist crítico:
# [ ] README.md personalizado con identidad LautaroBlog
# [ ] CHANGELOG.md con historial de versiones
# [ ] LICENSE agregado (MIT, GPL, etc.)
# [ ] .gitignore configurado
# [ ] Roadmap de features únicas documentado

# Cerrar:
gh issue close 6 --comment "✅ Clase 4 completada:
- README/CHANGELOG personalizados
- LICENSE MIT agregado
- Roadmap v1.0.0 → v2.0.0 documentado"
```

---

## 🎯 Workflow Recomendado

### 1. Antes de Empezar
```powershell
# Ver todas las Issues pendientes
gh issue list --state open

# Elegir una Issue para trabajar (ej: Issue #4)
gh issue view 4 > checklist-clase2.txt
# Ahora tienes la checklist en un archivo local
```

### 2. Durante el Desarrollo
```powershell
# Trabajas en tu código...
mkdir diagramas
git mv DiagramaDeClases.png diagramas/diagrama-clases.png

# Cada vez que completas un item de la checklist:
gh issue comment 4 --body "✅ Movidos diagramas a carpeta diagramas/"
```

### 3. Al Finalizar
```powershell
# Verificar TODOS los items de la Issue
gh issue view 4

# Hacer último commit
git add .
git commit -m "refactor(clase-2): estructura final diagramas con .drawio"
git push

# Cerrar Issue con resumen
gh issue close 4 --comment "✅ Clase 2 completada - ver commit $(git rev-parse --short HEAD)"
```

---

## 📊 Comandos de Monitoreo

### Ver Progreso General
```powershell
# Issues abiertas vs cerradas
gh issue list --state all --json number,title,state | ConvertFrom-Json | Group-Object state

# Resultado esperado:
# OPEN: 6 → 0 (cuando termines todo)
# CLOSED: 0 → 6
```

### Ver Historial de Comentarios en Issue
```powershell
gh issue view 1 --comments
```

### Ver todas tus Issues cerradas (¡para celebrar!)
```powershell
gh issue list --state closed
```

---

## 🚀 Comandos Avanzados (Opcional)

### Crear Nueva Issue desde CLI
```powershell
# Si detectas algo nuevo que falta
gh issue create --title "Agregar tests unitarios" --body "Pendiente: crear tests para casos de uso"
```

### Reabrir Issue si Olvidaste Algo
```powershell
gh issue reopen 4 --comment "⚠️ Olvidé agregar .drawio de diagrama de actividad"
```

### Ver Issues del Repo Upstream (IES9018)
```powershell
gh issue list --repo IES9018/proyecto-modelado-2025
```

---

## ✅ Checklist de Validación Antes de Cerrar Issue

Para **CADA Issue**, verifica:

### Issue #1 (Clase 1)
```powershell
# Comandos de verificación:
ls casos_de_uso/*.md     # ¿3 archivos en kebab-case?
ls casos_de_uso/*.drawio # ¿Existe diagrama .drawio?
```

### Issue #4 (Clase 2)
```powershell
ls diagramas/*.drawio    # ¿3+ archivos .drawio?
ls diagramas/*.png       # ¿3+ archivos .png?
# Contar: deben ser pares (1 .drawio + 1 .png por diagrama)
```

### Issue #5 (Clase 3)
```powershell
ls diagramas/*mvc*       # ¿Existe diagrama MVC con .drawio y .png?
```

### Issue #6 (Clase 4)
```powershell
cat README.md | Select-String "LautaroBlog"  # ¿Personalizado?
cat CHANGELOG.md | Select-String "\[1.0.0\]" # ¿Versión documentada?
ls LICENSE               # ¿Existe archivo?
```

---

## 💡 Tips de Productividad

### Crear Aliases en PowerShell
```powershell
# Agregar a tu perfil: notepad $PROFILE

# Aliases útiles:
function ghil { gh issue list }
function ghiv { gh issue view $args[0] }
function ghic { gh issue close $args[0] --comment $args[1] }

# Uso:
ghil           # Ver Issues rápido
ghiv 1         # Ver Issue #1
ghic 1 "Done"  # Cerrar Issue #1
```

### Script para Verificar Todo de una Vez
```powershell
# Crear archivo: Check-AllIssues.ps1

Write-Host "Verificando Clase 1..." -ForegroundColor Yellow
if (Test-Path casos_de_uso/) { Write-Host "✅ Carpeta existe" -ForegroundColor Green } else { Write-Host "❌ Falta carpeta" -ForegroundColor Red }

Write-Host "Verificando Clase 2..." -ForegroundColor Yellow
if (Test-Path diagramas/*.drawio) { Write-Host "✅ Archivos .drawio encontrados" -ForegroundColor Green } else { Write-Host "❌ Faltan .drawio" -ForegroundColor Red }

Write-Host "Verificando Clase 4..." -ForegroundColor Yellow
if (Test-Path LICENSE) { Write-Host "✅ LICENSE existe" -ForegroundColor Green } else { Write-Host "❌ Falta LICENSE" -ForegroundColor Red }

# Ejecutar: .\Check-AllIssues.ps1
```

---

## 📝 Resumen de Comandos Esenciales

```powershell
# Ver Issues
gh issue list

# Ver detalle de Issue
gh issue view [número]

# Comentar en Issue
gh issue comment [número] --body "Tu comentario"

# Cerrar Issue
gh issue close [número] --comment "Motivo de cierre"

# Verificar autenticación
gh auth status

# Ver PRs (cuando crees nuevo PR consolidado)
gh pr list
gh pr view [número]
```

---

## 🎯 Meta Final

Cuando hayas completado **TODO**:

```powershell
# Ver resumen final
gh issue list --state all

# Resultado esperado:
# 6 CLOSED Issues
# 0 OPEN Issues

# Crear PR final consolidado
git checkout -b consolidacion-final
# ... hacer cambios finales ...
git push -u origin consolidacion-final
gh pr create --title "feat: entrega final LautaroBlog v1.0.0" --body "Clases 1-4 completas. Todas las Issues cerradas."
```

---

## 📚 Recursos Adicionales

- **Documentación oficial:** https://cli.github.com/manual/
- **Cheat sheet:** https://github.com/github/gh-cli/blob/trunk/docs/command-line-syntax.md
- **Issues del curso:** Las 6 Issues (#1-6) en tu fork tienen checklists detalladas

---

**¡Éxito con tu proyecto, Lautaro! Usa esta guía como referencia constante. Recuerda: cierra cada Issue solo cuando TODOS los items de su checklist estén ✅.**

Si tienes dudas sobre algún comando, usa:
```powershell
gh issue --help
gh pr --help
```
