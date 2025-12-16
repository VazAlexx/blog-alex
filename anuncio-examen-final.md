# 📢 Anuncio: Examen Final de Modelado de Software

## 🎓 Información General

¡Hola a todos! Les comparto los detalles del **examen final** de la materia Modelado de Software.

**Fecha:** [A confirmar]  
**Duración:** 2 horas (120 minutos)  
**Modalidad:** Presencial  
**Nota mínima:** 6.0/10

---

## 📋 Estructura del Examen

El examen tiene **3 partes**:

| Parte | Descripción | Tiempo | Puntaje |
|-------|-------------|--------|---------|
| **1** | Análisis Crítico de Caso de Uso | 20 min | 20% |
| **2** | Diseño de Nueva Funcionalidad | 60 min | 50% |
| **3** | Defensa Oral Individual | 10 min | 30% |

---

## 📝 Parte 1: Análisis Crítico (20 min - 20%)

### ¿Qué tengo que hacer?

Te daré un **caso de uso con errores intencionales**. Debes:
- Identificar **mínimo 5 errores** (hay 7 en total)
- Explicar por qué es un error
- Proponer la corrección

### Ejemplo de error típico:

❌ **Error:** "Sistema" aparece como actor principal  
✅ **Corrección:** Los actores deben ser entidades externas. Cambiar a "Administrador" o "Usuario"

### ¿Dónde buscar errores?

- ✅ Actores (¿son externos al sistema?)
- ✅ Precondiciones (¿tienen sentido lógico?)
- ✅ Flujo principal (¿falta confirmación en operaciones destructivas?)
- ✅ Flujos alternativos (¿están todos los caminos?)
- ✅ Postcondiciones (¿son estados finales o acciones?)

---

## 💻 Parte 2: Diseño Práctico (60 min - 50%)

### ¿Qué tengo que hacer?

Te asignaré **un requisito nuevo** para tu proyecto. Debes crear:

1. **Caso de Uso Completo** (20 pts)
   - Con todos los campos: actores, precondiciones, flujo, postcondiciones
   
2. **Diagrama de Clases** (15 pts)
   - Clases nuevas necesarias
   - Relaciones con clases existentes
   
3. **Diagrama de Secuencia** (15 pts)
   - Flujo principal del caso de uso
   - Mínimo 4 objetos interactuando

### Ejemplos de requisitos:

**Nivel Básico:**
> "Agregar funcionalidad de 'Guardar artículo como borrador' antes de publicar"

**Nivel Intermedio:**
> "Implementar sistema de 'Me gusta' en artículos con contador visible"

**Nivel Avanzado:**
> "Agregar sistema de notificaciones: el autor recibe alerta cuando alguien comenta"

**Nota:** El nivel se asignará según tu desempeño en el trabajo práctico.

### ¿Puedo consultar mi proyecto?

✅ **Sí**, puedes ver tu proyecto en GitHub para consultar tu estructura existente.

---

## 🎤 Parte 3: Defensa Oral (10 min - 30%)

### ¿Qué tengo que hacer?

Presentación individual donde debes:

1. **Mostrar tu proyecto** (3 min)
   - Nombre, identidad, feature única
   - Arquitectura MVC aplicada

2. **Explicar una decisión de diseño** (3 min)
   - Te preguntaré sobre tu estructura de clases, patrones aplicados, etc.

3. **Defender tu diseño de Parte 2** (2 min)
   - Explicar el caso de uso y diagramas que creaste

4. **Responder preguntas** (2 min)
   - Conceptos teóricos (SOLID, MVC, patrones)

### Ejemplo de preguntas:

- "¿Por qué elegiste esta estructura de clases?"
- "¿Cómo aplicaste el patrón MVC en tu proyecto?"
- "¿Qué patrones de diseño identificaste?"

---

## 📚 ¿Cómo me Preparo?

### Material de Estudio

1. **Documentos del curso:**
   - `clase-1-introduccion-uml.md` - Casos de uso
   - `clase-2-diagramas-uml.md` - Diagramas
   - `clase-3-principios-patrones-arquitecturas.md` - MVC, patrones
   - `glosario-desarrollo-software.md` - Terminología

2. **Tu propio proyecto:**
   - Revisa tu README, CHANGELOG
   - Repasa tus casos de uso y diagramas
   - Identifica qué patrones aplicaste
   - Prepara explicación de tu feature única

### Conceptos Clave a Repasar

- ✅ Actores primarios vs secundarios
- ✅ Precondiciones vs Postcondiciones
- ✅ Flujos principales vs alternativos
- ✅ Relaciones en diagramas de clases (asociación, composición, herencia)
- ✅ Mensajes en diagramas de secuencia
- ✅ Patrón MVC (Model-View-Controller)
- ✅ Principios SOLID básicos

### Práctica Recomendada

1. **Practica crear casos de uso en 10-15 minutos**
2. **Practica diagramas de clases simples**
3. **Explica tu proyecto en voz alta** (para la defensa oral)
4. **Revisa casos de uso de compañeros** y busca errores

---

## 🎯 Ejemplos de Referencia

He preparado **ejemplos completos** de soluciones esperadas para que te orientes:

### Ejemplo 1: Caso de Uso con Errores

📄 Ver: [`examen-parte1-caso-uso-con-errores.md`](./examen-parte1-caso-uso-con-errores.md)

Este documento muestra:
- Un caso de uso con 7 errores típicos
- Dónde buscar cada tipo de error
- Ejemplos de correcciones apropiadas

**Úsalo para practicar** identificar errores antes del examen.

### Ejemplo 2: Soluciones Completas Parte 2

📄 Ver: [`examen-parte2-ejemplos-soluciones.md`](./examen-parte2-ejemplos-soluciones.md)

Este documento muestra soluciones completas para los 3 niveles:
- **Nivel Básico:** Guardar como borrador
- **Nivel Intermedio:** Sistema de "me gusta"
- **Nivel Avanzado:** Sistema de notificaciones

Cada ejemplo incluye:
- ✅ Caso de uso completo con todos los campos
- ✅ Diagrama de clases con relaciones
- ✅ Diagrama de secuencia con flujo completo

**Úsalos como referencia** del nivel de detalle esperado.

---

## ⏰ Gestión del Tiempo

### Distribución Recomendada

**Parte 1 (20 min):**
- 5 min: Lectura completa
- 10 min: Identificar errores
- 5 min: Escribir correcciones

**Parte 2 (60 min):**
- 20 min: Caso de uso completo
- 20 min: Diagrama de clases
- 20 min: Diagrama de secuencia

**Parte 3 (10 min):**
- Presentación individual
- Responder con calma, sin apuro

### Estrategia

1. **Lee todo antes de empezar**
2. **Prioriza completitud sobre perfección**
3. **Es mejor un caso de uso completo que tres diagramas incompletos**
4. **Deja tiempo para revisar al final**

---

## 🛠️ Herramientas Permitidas

### ✅ Permitido:
- draw.io / diagrams.net
- Mermaid Live Editor
- Tu proyecto en GitHub (consulta)
- Documentación del curso
- Tus propios apuntes

### ❌ NO Permitido:
- ChatGPT u otras IAs generativas
- Comunicación con compañeros durante el examen
- Copiar casos de uso de internet

---

## 💡 Consejos Finales

### Antes del Examen

1. ✅ **Revisa tu proyecto completo** - Conoce tu código
2. ✅ **Practica casos de uso** - Hazlos en tiempo limitado
3. ✅ **Repasa terminología** - Usa el glosario
4. ✅ **Prepara tu defensa** - Explica tu proyecto en voz alta
5. ✅ **Descansa bien** - Llega fresco al examen

### Durante el Examen

1. ⏰ **Administra tu tiempo** - No te quedes atascado en una parte
2. 📝 **Lee todas las consignas** - Antes de empezar a escribir
3. 🎯 **Prioriza completitud** - Mejor completo que perfecto
4. 💡 **Usa los ejemplos** - Como referencia de formato
5. 🗣️ **En la defensa: respira** - Habla claro, sin apuro

### Qué Traer

- 💻 Laptop con batería cargada
- 🌐 Acceso a internet
- 📁 Tu proyecto accesible en GitHub
- 🎨 Herramientas de diagramado instaladas

---

## ❓ Preguntas Frecuentes

**P: ¿Puedo elegir el nivel de dificultad en Parte 2?**  
R: No, el profesor asignará el requisito según tu desempeño en el trabajo práctico.

**P: ¿Qué pasa si no termino en 60 minutos?**  
R: Entrega lo que tengas. Es mejor un caso de uso completo y un diagrama parcial.

**P: ¿Puedo usar Mermaid en lugar de draw.io?**  
R: Sí, puedes usar cualquier herramienta que genere diagramas claros.

**P: ¿La defensa oral es obligatoria?**  
R: Sí, representa el 30% de la nota. Sin defensa no se puede aprobar.

**P: ¿Qué pasa si me pongo nervioso?**  
R: Es normal. Respira, tómate tu tiempo. El profesor hará preguntas de apoyo.

---

## 📊 Escala de Calificación

| Puntaje | Nota | Estado |
|---------|------|--------|
| 90-100 pts | 9.0-10 | Sobresaliente |
| 80-89 pts | 8.0-8.9 | Muy Bueno |
| 70-79 pts | 7.0-7.9 | Bueno |
| 60-69 pts | 6.0-6.9 | Aprobado |
| 0-59 pts | 0-5.9 | Desaprobado |

---

## 📅 Próximos Pasos

1. **Lee el documento completo del examen:** [`examen-final-modelado-software.md`](./examen-final-modelado-software.md)
2. **Estudia los ejemplos de referencia** (enlaces arriba)
3. **Practica con los ejemplos** de casos de uso con errores
4. **Revisa tu proyecto** y prepara tu defensa
5. **Consulta dudas** en las issues o con el profesor

---

## 💬 ¿Dudas?

Si tienes preguntas sobre el examen:
- 📝 Abre un issue en este repositorio
- 📧 Contacta al profesor: Paulo Alvarez
- 👥 Consulta con tus compañeros (antes del examen)

---

## 🎯 Mensaje Final

Este examen evalúa todo lo que aprendiste en el curso:
- ✅ Análisis crítico de diseño
- ✅ Habilidad práctica de modelado
- ✅ Comunicación técnica

**Has trabajado duro en tu proyecto.** Ahora solo necesitas demostrar que comprendes los conceptos y puedes aplicarlos.

**Confía en tu preparación.** Tienes todas las herramientas y el conocimiento necesario.

**¡Éxito en tu examen!** 🚀

---

**Profesor:** Paulo Alvarez  
**Materia:** Modelado de Software  
**Institución:** IES 9-018 "Gobernador Celso Jaque"
