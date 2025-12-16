### 🏫 **Institución:** IES 9-018 "Gobernador Celso Jaque"
### 📚 **Carrera:** Tecnicatura Superior en Desarrollo de Software
### 📖 **Materia:** Modelado de Software
### 👨‍🏫 **Profesor:** Paulo Alvarez
---
# Proyecto de Aprendizaje: Modelado de Software - Institución Digital

## ¡Bienvenido/a!

Este repositorio contiene todo el material de clase para la materia "Modelado de Software". Nuestro objetivo es aprender los fundamentos del diseño y la arquitectura de software de una manera práctica y aplicada. Para ello, no solo estudiaremos teoría, sino que construiremos, paso a paso, el modelo de un proyecto real: un Sistema de Gestión de Contenidos (CMS) llamado **"Institución Digital"**.

---

## ¿Cómo Usar este Repositorio?

Sigue estos pasos para sacar el máximo provecho del material.

### Paso 1: Clona el Repositorio

Para tener una copia completa del proyecto en tu computadora, necesitarás clonar este repositorio. Abre una terminal o línea de comandos y ejecuta el siguiente comando (reemplaza la URL con la URL real de tu repositorio de GitHub):

```bash
# Clona el proyecto a tu máquina local
git clone https://github.com/IES9018/proyecto-modelado-2025.git

# Entra en la carpeta del proyecto
cd tu-repositorio
```

### Paso 2: Sigue las Clases en Orden

El aprendizaje está diseñado para ser progresivo. Los archivos más importantes son los tutoriales de cada clase. Debes seguirlos en orden:

1.  **[`clase-1-introduccion-uml.md`](./clase-1-introduccion-uml.md)**: Aprenderás los conceptos básicos, a definir los requisitos de un sistema con Casos de Uso y tus primeros comandos de Git.
2.  **[`clase-2-diagramas-uml.md`](./clase-2-diagramas-uml.md)**: Diseñarás la estructura interna del sistema con Diagramas de Clases y modelarás sus flujos con Diagramas de Secuencia y Actividad.
3.  **[`clase-3-principios-patrones-arquitecturas.md`](./clase-3-principios-patrones-arquitecturas.md)**: Aprenderás a refinar tu diseño con principios profesionales, patrones y la arquitectura MVC para que tu software sea de alta calidad.

### Paso 3: Consulta el Glosario

¿Encuentras un término que no entiendes? ¡No hay problema! El archivo [`glosario-desarrollo-software.md`](./glosario-desarrollo-software.md) es tu diccionario personal. Contiene explicaciones sencillas, analogías y ejemplos de todos los conceptos técnicos que veremos.

### Paso 4: Explora el Historial (Para los Curiosos)

Una de las herramientas más poderosas para aprender es ver cómo se construyó el proyecto. Puedes usar el comando `git log` en tu terminal para ver el historial de todos los "puntos de guardado" (commits). Prueba este comando para una vista gráfica y resumida:

```bash
git log --oneline --graph --all
```

Esto te mostrará las ramas y cómo se fueron fusionando, permitiéndote entender el flujo de trabajo real de un desarrollador.

---

## Estructura de Archivos

> **Nota sobre Diagramas:** Este repositorio utiliza [Mermaid](https://mermaid-js.github.io/mermaid/#/) para la creación de diagramas directamente en Markdown. Puedes copiar el código de cualquier diagrama Mermaid y pegarlo en [mermaid.live](https://mermaid.live/) para visualizarlo y experimentar con él.

*   `README.md`: Esta guía que estás leyendo.

**Documentos de Apoyo y Flujo de Trabajo:**

*   [`herramientas-esenciales.md`](./herramientas-esenciales.md): **(Leer primero)** Guía de instalación y uso de Git, GitHub, diagrams.net y VS Code.
*   [`flujo-trabajo-colaborativo.md`](./flujo-trabajo-colaborativo.md): **(Muy importante)** Explica cómo usar Forks y Pull Requests, el método que usaremos para las entregas.
*   [`CHANGELOG.md`](./CHANGELOG.md): Documenta todos los cambios significativos en el material del curso, ideal para entender la evolución del proyecto.
*   [`guia-uso-ia-aprender.md`](./guia-uso-ia-aprender.md): **(Recomendado)** Enseña cómo usar una IA como Gemini de forma efectiva y ética para potenciar tu aprendizaje.
*   [`fundamentos-arquitectura-software.md`](./fundamentos-arquitectura-software.md): Lectura recomendada para entender los conceptos de alto nivel detrás de nuestras decisiones de diseño.
*   [`glosario-desarrollo-software.md`](./glosario-desarrollo-software.md): Tu diccionario de consulta para todos los términos técnicos.

**Documentos del Proyecto y Tarea:**

*   [`tarea-proyecto-final.md`](./tarea-proyecto-final.md): **(Importante)** Contiene las instrucciones detalladas de la tarea final del curso.
*   [`rubrica-evaluacion.md`](./rubrica-evaluacion.md): Describe cómo será evaluado tu trabajo.
*   [`LISTA_ESTUDIANTES.md`](./LISTA_ESTUDIANTES.md): Directorio con los enlaces a los repositorios de todos los compañeros para la revisión por pares.

**Tutoriales del Proyecto:**

*   [`clase-1-introduccion-uml.md`](./clase-1-introduccion-uml.md): **(Empezar aquí)** Tutorial de la Clase 1.
*   [`clase-2-diagramas-uml.md`](./clase-2-diagramas-uml.md): Tutorial de la Clase 2.
*   [`clase-3-principios-patrones-arquitecturas.md`](./clase-3-principios-patrones-arquitecturas.md): Tutorial de la Clase 3.
*   [`clase-4-fork-independiente.md`](./clase-4-fork-independiente.md): Crea tu propia versión independiente (tipo Cursor/VSCode). Incluye Versionado Semántico (SemVer), tags, releases y CHANGELOG.

**Documentos del Curso:**

*   [`propuesta-pedagogica-modelado-software.md`](./propuesta-pedagogica-modelado-software.md): Documento con la estrategia pedagógica general del curso.

**Diagramas del Sistema (Mermaid):**

*   [`diagrama-sistema-completo.md`](./diagrama-sistema-completo.md): Visión general y evolutiva del sistema "Institución Digital" a través de diagramas Mermaid.

---

## Versionado y Releases del Repositorio

Este repositorio usa **Versionado Semántico (SemVer)** con el formato `vMAJOR.MINOR.PATCH`.

Principios aplicados:
* Cada incorporación de una nueva clase principal incrementa MINOR.
* Correcciones y ajustes no disruptivos incrementan PATCH.
* Cambios estructurales mayores (reorganización profunda del contenido) incrementarán MAJOR.

Recursos y evidencias:
* Historial de cambios en [`CHANGELOG.md`](./CHANGELOG.md)
* Tags publicados en la sección Releases de GitHub
* Ejemplo real de fork independiente en la Clase 4

Ejemplo de comandos (documentación):
```powershell
# Crear un tag anotado para la nueva versión
git tag -a v1.4.0 -m "Release 1.4.0: Clase 4 - Forks independientes y versión propia"

# Ver los tags existentes
git tag --list

# Subir el tag al repositorio remoto
git push origin v1.4.0
```

Después de crear el tag se genera un Release en GitHub copiando la sección correspondiente del CHANGELOG.

## Tarea del Proyecto Final

La evaluación principal de este curso se basa en la construcción de tu propio proyecto "Institución Digital". Todos los detalles, instrucciones de entrega y expectativas están en los siguientes documentos:

*   **[Instrucciones de la Tarea](./tarea-proyecto-final.md):** Lee este documento cuidadosamente para saber qué tienes que hacer.
*   **[Rúbrica de Evaluación](./rubrica-evaluacion.md):** Consulta este documento para entender cómo será evaluado tu trabajo.
