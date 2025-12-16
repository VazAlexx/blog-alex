# Feedback PR #13 – VazAlexx

¡Hola Alexx! 👋

Revisé tu PR #13 "Agrego diagrama MVC y comentario en clase 3". Excelente iniciativa de agregar un diagrama visual para complementar la teoría de MVC. A continuación te doy un feedback constructivo.

---

## ✅ Aspectos positivos

- **Aporte complementario**: Agregaste contenido a la clase 3 existente con un diagrama visual del patrón MVC.
- **Referencia correcta**: Usaste sintaxis Markdown apropiada para la imagen.
- **Actitud proactiva**: Ya vas en tu segundo PR, lo cual demuestra compromiso con el proyecto.

---

## 📋 Observaciones y mejoras necesarias

### 1) Falta línea en blanco al final del archivo

❌ **Problema**: El archivo `clase-3-principios-patrones-arquitecturas.md` no termina con una línea en blanco (`newline`).

```text
![Diagrama MVC](./img-diagrama-clase3/diagrama-mvc.png)
\ No newline at end of file
```

✅ **Solución**: Agregá una línea vacía al final del archivo.

**Acción**: Editá el archivo y presiona Enter al final para agregar el newline.

---

### 2) Archivo desktop.ini no debería estar en el repositorio

❌ **Problema**: Incluiste un archivo `desktop.ini` que es un archivo de configuración de Windows.

```text
img-diagrama-clase3/desktop.ini
[LocalizedFileNames]
Captura de pantalla 2025-11-07 203526.png=...
```

✅ **Solución**: Este archivo no debe estar en el repositorio Git.

**Acción**:

1. Eliminá el archivo del commit:

   ```bash
   git rm img-diagrama-clase3/desktop.ini
   git commit --amend --no-edit
   git push --force-with-lease
   ```

2. Agregalo al `.gitignore` si no está ya:

   ```text
   # Windows
   desktop.ini
   Thumbs.db
   ```

---

### 3) Falta archivo fuente .drawio

❌ **Problema**: Solo subiste la imagen PNG del diagrama MVC, sin el archivo fuente editable.

✅ **Solución**: **Debés incluir el archivo `.drawio` original** para que pueda ser editado posteriormente:

```text
img-diagrama-clase3/
├── diagrama-mvc.drawio
└── diagrama-mvc.png
```

**Acción**: Subí el archivo `.drawio` que usaste para crear el diagrama.

---

### 4) Convención de nombres de carpetas

⚠️ **Observación**: La carpeta `img-diagrama-clase3` usa guiones pero podrías ser más específico.

✅ **Sugerencia**: Considera renombrar a algo más descriptivo:

```text
clase-3-diagramas/
o
imgs-clase-3/
```

Para mantener consistencia con otras estructuras del repositorio.

**Acción**: Opcional, pero recomendado para mantener uniformidad.

---

### 5) Mensaje de commit

⚠️ **Observación**: Tu mensaje de commit es descriptivo pero no sigue Conventional Commits:

```text
❌ "Agrego diagrama MVC y comentario en clase 3"
```

✅ **Formato correcto:**

```text
✅ "feat(clase-3): agregar diagrama visual del patrón MVC"
o
✅ "docs(clase-3): agregar diagrama MVC y sección de aporte"
```

**Acción**: En futuros commits, usá el formato `tipo(scope): descripción`.

---

### 6) Mejorar la sección "Aporte de Alex"

⚠️ **Observación**: La sección que agregaste es breve y podría ser más descriptiva.

✅ **Sugerencia**: Expandí la explicación del diagrama:

```markdown
### Diagrama MVC - Ejemplo Blog

A continuación se presenta un diagrama visual del patrón MVC aplicado al sistema de blog:

![Diagrama MVC](./img-diagrama-clase3/diagrama-mvc.png)

**Componentes del diagrama:**

- **Modelo**: Gestiona los datos (Artículo, Usuario, Comentario)
- **Vista**: Presenta la información al usuario (templates HTML)
- **Controlador**: Coordina la lógica (ArticuloController, UsuarioController)

Este diagrama complementa la explicación teórica y muestra las relaciones entre componentes.
```

**Acción**: Considerá ampliar la documentación para mayor claridad pedagógica.

---

### 7) Relación con PR #10

📝 **Nota**: Este es tu segundo PR (ya tienes el #10 abierto sobre clase 2). Ambos tienen observaciones similares sobre:

- Archivos `.drawio` faltantes
- Convenciones de nombres
- Conventional Commits

**Sugerencia**: Trabajá primero en completar el PR #10 aplicando todas las correcciones, y luego aplicá las mismas mejoras a este PR #13. Así consolidás el aprendizaje de las convenciones.

---

## 📝 Checklist de acciones requeridas

Para que pueda aprobar este PR, necesito que:

- [ ] Agregues línea en blanco al final de `clase-3-principios-patrones-arquitecturas.md`
- [ ] Elimines el archivo `desktop.ini` del commit
- [ ] Incluyas el archivo `.drawio` fuente del diagrama MVC
- [ ] (Opcional) Renombres la carpeta a `imgs-clase-3/` o similar
- [ ] (Opcional) Expandas la documentación del diagrama con más contexto

---

## 🎯 Nota pedagógica

Notás un patrón en los feedbacks: **documentación completa = código + fuentes + explicación**.

En proyectos de software:

1. **Imágenes PNG**: Para visualización rápida
2. **Archivos .drawio**: Para edición y mantenimiento
3. **Documentación Markdown**: Para contexto y explicación

Los tres elementos trabajan juntos para crear documentación profesional y mantenible.

---

## 🚀 Próximos pasos

1. Aplicá las correcciones de este feedback
2. Revisá el feedback del PR #10 y aplicá las mismas mejoras allí
3. Comentá en ambos PRs cuando estén listos para revisión
4. Continuá con clase 4 (versionado y colaboración)

¡Muy bien por la participación activa! Estás demostrando buen ritmo de trabajo. Solo necesitamos pulir los detalles de formato y documentación. 💪

---

**Recursos útiles:**

- [Guía de uso de IA para aprender](guia-uso-ia-aprender.md)
- [Herramientas esenciales](herramientas-esenciales.md)
- [Política de no self-merge](https://github.com/IES9018/proyecto-modelado-2025/discussions/6)
