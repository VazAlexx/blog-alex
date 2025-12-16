# Feedback PR #5 – ClaudioMPerez

¡Hola Claudio! 👋

Revisé tu PR #5 "Carpeta de caso de uso" con los diagramas de las clases 1, 2 y 3. Te felicito por el esfuerzo y por tener trabajo de varias clases. A continuación te doy un feedback constructivo para que puedas mejorar tu entrega.

---

## ✅ Aspectos positivos

- **Completitud**: Incluiste diagramas de las tres primeras clases (casos de uso, diagramas UML clase 2, y arquitectura MVC clase 3).
- **Organización inicial**: Creaste una estructura de carpetas para organizar tus imágenes.
- **Uso de drawio**: Veo que al menos un archivo tiene `.drawio.png` en el nombre, lo cual es positivo.

---

## 📋 Observaciones y mejoras necesarias

### 1) Convención de nombres de archivos

❌ **Problema**: Los nombres de tus archivos tienen espacios y mayúsculas.

```text
imgs_claudio/casos_de_uso/casos de uso autor y visitante.drawio.png
imgs_claudio/clase 3/diagrama mvc.png
imgs_claudio/diagramas/diagrama de actividad.png
```

✅ **Solución**: Usá nombres en minúsculas con guiones (kebab-case), sin espacios:

```text
imgs-claudio/casos-de-uso/casos-uso-autor-visitante.drawio.png
imgs-claudio/clase-3/diagrama-mvc.png
imgs-claudio/diagramas/diagrama-actividad.png
```

**Acción**: Renombrá todos los archivos y carpetas para seguir esta convención.

---

### 2) Falta documentación Markdown

❌ **Problema**: Solo subiste imágenes sin ningún archivo `.md` que las explique o contextualice.

✅ **Solución**: Debés crear archivos markdown que:

- Expliquen el contexto de cada diagrama
- Describan las decisiones de diseño
- Referencien las imágenes con sintaxis Markdown

**Ejemplo para clase 1:**

```markdown
## Casos de Uso - Sistema de Blogs

### Actores
- **Autor**: Usuario que publica y gestiona artículos
- **Visitante**: Usuario que lee artículos

### Casos de uso principales
1. Publicar artículo
2. Leer artículo
3. Comentar artículo

![Diagrama de casos de uso](../imgs-claudio/casos-de-uso/casos-uso-autor-visitante.drawio.png)
```

**Acción**: Creá archivos como `clase-1-casos-uso.md`, `clase-2-diagramas.md`, `clase-3-arquitectura.md` en la raíz o en carpetas organizadas.

---

### 3) Archivos fuente .drawio obligatorios

❌ **Problema**: Solo veo imágenes PNG. No están los archivos fuente `.drawio` editables (excepto quizás el de casos de uso).

✅ **Solución**: **Debés incluir los archivos `.drawio` originales** además de las imágenes exportadas:

```text
imgs-claudio/
├── casos-de-uso/
│   ├── casos-uso-autor-visitante.drawio
│   └── casos-uso-autor-visitante.png
├── clase-2/
│   ├── diagrama-clases.drawio
│   ├── diagrama-clases.png
│   ├── diagrama-secuencia.drawio
│   ├── diagrama-secuencia.png
│   ├── diagrama-actividad.drawio
│   └── diagrama-actividad.png
└── clase-3/
    ├── diagrama-mvc.drawio
    └── diagrama-mvc.png
```

**Acción**: Subí los archivos `.drawio` para que puedan ser editados posteriormente.

---

### 4) Estructura del repositorio

❌ **Problema**: Creaste una carpeta personal `imgs_claudio/` que no sigue la estructura común del repositorio.

✅ **Solución**: Dos opciones válidas:

**Opción A) Integrar con archivos de clase existentes:**
Editá los archivos de las clases (`clase-1-introduccion-uml.md`, `clase-2-diagramas-uml.md`, etc.) agregando secciones con tus diagramas.

**Opción B) Carpeta temática organizada:**

```text
diagramas-claudio/
├── clase-1-casos-uso.md
├── clase-2-diagramas-uml.md
├── clase-3-arquitectura-mvc.md
└── imgs/
    ├── casos-uso-autor-visitante.drawio
    ├── casos-uso-autor-visitante.png
    ├── diagrama-clases.drawio
    ├── diagrama-clases.png
    └── ...
```

**Acción**: Elegí una opción y reestructurá tu contenido.

---

### 5) Mensajes de commit

⚠️ **Observación**: Tus mensajes de commit son descriptivos pero no siguen Conventional Commits:

```text
❌ "Agregar caso de uso"
❌ "diagramas"
❌ "ordenando archivos"
```

✅ **Usar formato:**

```text
✅ "feat(clase-1): agregar diagrama casos de uso autor y visitante"
✅ "feat(clase-2): agregar diagramas de clases, secuencia y actividad"
✅ "refactor(estructura): reorganizar imágenes en carpeta diagramas-claudio"
```

**Acción**: En futuros commits, usá el formato `tipo(scope): descripción`.

---

### 6) Política de no self-merge

🔒 **Recordatorio**: **NO mergees tu propio PR**. Esperá la revisión y aprobación del docente.

Revisá la política oficial: [Política de no self-merge](https://github.com/IES9018/proyecto-modelado-2025/discussions/6)

---

## 📝 Checklist de acciones requeridas

Antes de que pueda aprobar este PR, necesito que:

- [ ] Renombres todos los archivos y carpetas a kebab-case (minúsculas con guiones)
- [ ] Incluyas archivos `.drawio` fuente para todos los diagramas
- [ ] Crees archivos Markdown (`.md`) que expliquen y referencien tus diagramas
- [ ] Reorganices la estructura siguiendo las opciones A o B sugeridas
- [ ] Agregues una línea en blanco al final de cada archivo
- [ ] Uses Conventional Commits en futuros commits

---

## 🎯 Nota pedagógica

El objetivo de este proyecto no es solo **crear diagramas**, sino también **documentar y comunicar** tus decisiones de diseño. Los archivos Markdown son tan importantes como las imágenes porque:

1. Explican el **contexto** y **justificación** de tus decisiones
2. Facilitan la **revisión** y **comprensión** del proyecto
3. Demuestran tu capacidad de **comunicación técnica**

Los archivos `.drawio` son esenciales porque permiten:

1. **Edición futura** sin tener que recrear todo desde cero
2. **Colaboración** con otros desarrolladores
3. **Control de versiones** efectivo (Git puede trackear cambios en XML)

---

## 🚀 Próximos pasos

Una vez que hayas realizado estos ajustes, comentá en este PR indicando que está listo para una nueva revisión. Mientras tanto, podés continuar avanzando con la clase 4 (versionado y colaboración).

¡Seguí así! El esfuerzo es evidente, solo necesitamos pulir la forma de presentar el trabajo. 💪

---

**Recursos útiles:**

- [Guía de uso de IA para aprender](guia-uso-ia-aprender.md)
- [Herramientas esenciales](herramientas-esenciales.md)
- [Clase 4: Versionado y colaboración](clase-4-versionado-colaboracion.md)
