# Feedback PR #15 – Milasch23 (Camila)

¡Hola Camila! 👋

Revisé tu PR #15 "Clase 2 Diagramas". ¡Buen avance! Te dejo sugerencias para alinearlo al estándar del repositorio.

---

## ✅ Fortalezas

- Sumaste contenido específico de la Clase 2 en un archivo dedicado.
- Muestra intención de estructurar y documentar los diagramas.

---

## 📋 Observaciones y mejoras

### 1) Nombre de archivo y ubicación

- Archivo actual: `clase2Diagramas.md` (camelCase).
- Sugerencia: renombrar a `clase-2-diagramas-uml.md` o integrar tu contenido al archivo existente con ese nombre.
- Evitá duplicar materiales de clase. Si elegís mantener archivo propio, ubicá imágenes y fuentes en una carpeta `clase-2/`.

### 2) Estructura por secciones

Asegurate de incluir secciones claras con encabezados y una línea en blanco entre secciones:

```markdown
## Diagrama de Clases
- Objetivo del diagrama
- Nomenclatura de clases, atributos y métodos
- Imagen: ![Diagrama de Clases](./clase-2/diagrama-clases.png)

## Diagrama de Secuencia
- Escenario modelado (qué caso de uso representa)
- Participantes (lifelines) y mensajes
- Imagen: ![Diagrama de Secuencia](./clase-2/diagrama-secuencia.png)

## Diagrama de Actividad
- Flujo principal y decisiones
- Notas sobre concurrencia o ramificaciones
- Imagen: ![Diagrama de Actividad](./clase-2/diagrama-actividad.png)
```

### 3) Archivos fuente `.drawio`

- Si el PR incluye diagramas exportados, subí también los archivos fuente `.drawio` junto a los `.png`:

```text
clase-2/
├── diagrama-clases.drawio
├── diagrama-clases.png
├── diagrama-secuencia.drawio
├── diagrama-secuencia.png
├── diagrama-actividad.drawio
└── diagrama-actividad.png
```

### 4) Convenciones y formato

- Nombres: minúsculas con guiones (kebab-case) para archivos y carpetas.
- Formato Markdown: encabezados con línea en blanco antes y después; listas bien formadas; `newline` al final del archivo.
- Mensajes de commit: usá Conventional Commits, por ejemplo:

```text
docs(clase-2): agregar explicación y secciones de diagramas UML
feat(clase-2): subir diagramas de clases, secuencia y actividad
refactor(estructura): mover imágenes a carpeta clase-2/
```

---

## 📝 Checklist

- [ ] Renombrar o integrar en `clase-2-diagramas-uml.md`
- [ ] Agregar/adjuntar archivos `.drawio` si corresponde
- [ ] Reorganizar estructura de carpetas (`clase-2/`)
- [ ] Verificar formato Markdown y `newline` final
- [ ] Ajustar mensajes de commit (Conventional Commits)

---

Cualquier duda, preguntá por acá y lo vemos. ¡Buen trabajo y a seguir! 🚀
