# Feedback PR #9 - Lautaro Lopez (@LL1121)

**Fecha:** 2025-11-19  
**PR:** [#9 - Creación de los casos de uso del programa](https://github.com/IES9018/proyecto-modelado-2025/pull/9)  
**Fork:** [LautaroBlog](https://github.com/LL1121/LautaroBlog)  
**Estado:** OPEN (7 commits, última actualización: 2025-11-19 01:54:46Z)

---

## ✅ Excelentes Avances

### 1. Identidad de Proyecto Establecida ⭐
- ✅ **README personalizado** con identidad clara: "LautaroBlog v1.0.0"
- ✅ **CHANGELOG estructurado** siguiendo Keep a Changelog
- ✅ **Roadmap definido** con versiones planificadas (v1.0.0 → v2.0.0)
- ✅ **Commits convencionales**: `feat:`, `docs:`, `fix:` correctamente aplicados

### 2. Casos de Uso Completos (Clase 1) ⭐
Has creado **3 casos de uso** bien documentados:

#### CU01: Publicar Artículo
- ✅ Actor, resumen, flujos principal y alternativo claros
- ✅ Validación de datos incluida en flujo alternativo

#### CU02: Leer Artículo
- ✅ **Flujo complejo** con múltiples interacciones: filtros, favoritos, opiniones
- ✅ **4 flujos alternativos** bien documentados (artículo no encontrado, sesión, contenido prohibido, BD)
- ⚠️ Este CU combina múltiples responsabilidades (ver mejora recomendada)

#### CU03: Moderar Comentarios (¡Nuevo!)
- ✅ **Excelente adición** - caso de uso único no presente en proyecto base
- ✅ Precondiciones claramente establecidas
- ✅ Flujos de aprobación y rechazo bien diferenciados
- ✅ Manejo de errores de conexión incluido

### 3. Diagramas UML (Clase 2) ⭐
Has incluido **5 diagramas PNG**:
- `DiagramaDeClases.png`
- `DiagramaDeSecuencia.png`
- `DiagramaDeActividad.png`
- `DiagramaDeFrecuencia.png`
- `DiagramaMVC.png` (Clase 3)

### 4. Actividad Reciente
- ✅ Último commit hace **menos de 2 horas**: `feat: agregar sistema de moderación de comentarios v1.1.0`
- ✅ **8 archivos modificados** en último commit
- ✅ Trabajo constante con múltiples commits convencionales

---

## 📋 Pendientes Críticos para Completar Entrega

### 1. 🚨 FALTA: Archivos Fuente `.drawio`
**Urgente:** Los diagramas **DEBEN** tener sus archivos fuente editables.

**Qué hacer:**
```bash
# En tu fork LautaroBlog
# 1. Abre cada diagrama PNG en diagrams.net
# 2. Guarda como .drawio en la misma carpeta
# 3. Nombra coherentemente:

diagramas/diagrama-clases.drawio
diagramas/diagrama-clases.png
diagramas/diagrama-secuencia.drawio
diagramas/diagrama-secuencia.png
diagramas/diagrama-actividad.drawio
diagramas/diagrama-actividad.png
diagramas/diagrama-frecuencia.drawio  # ¿Es diagrama de secuencia o de estados?
diagramas/diagrama-frecuencia.png
diagramas/diagrama-mvc.drawio
diagramas/diagrama-mvc.png
```

### 2. 🗂️ FALTA: Organización en Carpetas
Actualmente todos los archivos están en la raíz. **Estructura esperada:**

```
LautaroBlog/
├── casos_de_uso/
│   ├── cu01-publicar-articulo.md
│   ├── cu02-leer-articulo.md
│   └── cu03-moderar-comentario.md
├── diagramas/
│   ├── diagrama-clases.drawio
│   ├── diagrama-clases.png
│   ├── diagrama-secuencia.drawio
│   ├── diagrama-secuencia.png
│   ├── diagrama-actividad.drawio
│   ├── diagrama-actividad.png
│   ├── diagrama-mvc.drawio
│   └── diagrama-mvc.png
├── CHANGELOG.md
├── README.md
├── LICENSE          ← FALTA
└── .gitignore       ← YA TIENES ✅
```

**Comandos para reorganizar:**
```bash
# Crear carpetas
mkdir casos_de_uso diagramas

# Mover casos de uso
git mv CU01PublicarArticulo.md casos_de_uso/cu01-publicar-articulo.md
git mv CU02LeerArticulo.md casos_de_uso/cu02-leer-articulo.md
git mv CU03ModerarComentario.md casos_de_uso/cu03-moderar-comentario.md

# Mover diagramas (y renombrar a kebab-case)
git mv DiagramaDeClases.png diagramas/diagrama-clases.png
git mv DiagramaDeSecuencia.png diagramas/diagrama-secuencia.png
git mv DiagramaDeActividad.png diagramas/diagrama-actividad.png
git mv DiagramaDeFrecuencia.png diagramas/diagrama-frecuencia.png
git mv DiagramaMVC.png diagramas/diagrama-mvc.png

# Commit
git commit -m "refactor: reorganizar estructura de archivos en carpetas"
```

### 3. 📄 FALTA: Archivo LICENSE
Debes agregar una licencia para tu proyecto.

**Opción recomendada:** MIT License (permisiva y sencilla)

```bash
# Crear LICENSE desde GitHub
# O usa este contenido:
```

**Contenido sugerido para `LICENSE`:**
```
MIT License

Copyright (c) 2025 Lautaro Lopez

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

```bash
# Después de crear el archivo
git add LICENSE
git commit -m "docs: agregar licencia MIT"
```

### 4. 🔧 Mejora Sugerida: Separar CU02
El caso de uso `CU02LeerArticulo.md` mezcla **tres responsabilidades**:
1. **Leer artículo** (pasos 1-5)
2. **Marcar como favorito** (pasos 6-7)
3. **Opinar/Calificar** (pasos 8-13)

**Recomendación:** Dividir en tres CU independientes:
- `cu02-leer-articulo.md`: Solo lectura con filtros
- `cu04-marcar-favorito.md`: Agregar/quitar favoritos
- `cu05-opinar-articulo.md`: Sistema de opiniones y calificación

Esto sigue el principio de **responsabilidad única** de casos de uso.

### 5. 📝 Newlines al Final de Archivos
Asegúrate de que todos los archivos `.md` terminen con una línea en blanco (newline).

---

## 🎯 Checklist Final - Completar Antes de Solicitar Revisión

- [ ] **Archivos `.drawio`** para todos los diagramas PNG
- [ ] **Organizar en carpetas**: `casos_de_uso/` y `diagramas/`
- [ ] **Renombrar a kebab-case**: `cu01-publicar-articulo.md`, `diagrama-clases.png`, etc.
- [ ] **Agregar LICENSE** (MIT recomendado)
- [ ] **Actualizar README** con enlaces a nueva estructura de carpetas
- [ ] **Verificar newlines** al final de todos los archivos `.md`
- [ ] **Opcional:** Separar CU02 en casos de uso más específicos
- [ ] **Push final** con commit convencional: `refactor: estructura final para revisión`

---

## 📚 Referencias de las Issues en tu Fork

Ya tienes **6 Issues abiertas** con guías detalladas:

1. [Issue #1: Clase 1 - Casos de Uso](https://github.com/LL1121/LautaroBlog/issues/1)
2. [Issue #2-4: Clase 2 - Diagramas UML](https://github.com/LL1121/LautaroBlog/issues/2)
3. [Issue #5: Clase 3 - Patrón MVC](https://github.com/LL1121/LautaroBlog/issues/5)
4. [Issue #6: Clase 4 - Versión Independiente](https://github.com/LL1121/LautaroBlog/issues/6)

**Puedes cerrar las Issues a medida que completas cada checklist.**

---

## 💡 Resumen de tu Progreso

| Clase | Estado | Observaciones |
|-------|--------|---------------|
| **Clase 1** | 🟡 80% | Casos de uso completos, falta organización/formato |
| **Clase 2** | 🟡 60% | Diagramas presentes, **faltan .drawio** |
| **Clase 3** | 🟢 90% | DiagramaMVC.png incluido, verificar anotaciones |
| **Clase 4** | 🟢 95% | README/CHANGELOG/Roadmap excelentes, falta LICENSE |

**Estado General:** 🟡 **Muy buen avance - Requiere normalización final**

---

## 🚀 Próximos Pasos

1. **HOY:** Completar checklist de pendientes críticos (1-3 horas de trabajo)
2. **Crear nuevo PR** desde tu fork consolidando todos los cambios
3. **Cerrar Issues** del fork a medida que completas cada punto
4. **Solicitar revisión final** cuando todo esté verde ✅

---

**Excelente trabajo, Lautaro. Tu proyecto muestra progreso consistente y uso correcto de Git. Completa los pendientes de normalización y estarás listo para la evaluación final.** 🎓

**Cualquier duda, comenta en este PR o en las Issues de tu fork.**
