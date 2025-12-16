# Examen Final - Modelado de Software
**Materia:** Modelado de Software  
**Profesor:** Paulo Alvarez  
**Institución:** IES 9-018 "Gobernador Celso Jaque"  
**Duración Total:** 2 horas (120 minutos)

---

## 📋 Estructura del Examen

El examen consta de 3 partes:

| Parte | Descripción | Tiempo | Puntaje |
|-------|-------------|--------|---------|
| **Parte 1** | Análisis Crítico de Caso de Uso | 20 min | 20% |
| **Parte 2** | Diseño Práctico de Nueva Funcionalidad | 60 min | 50% |
| **Parte 3** | Defensa Oral Individual | 10 min | 30% |

**Nota mínima para aprobar:** 6.0/10

---

## 📝 Parte 1: Análisis Crítico (20 min - 20%)

### Objetivo
Evaluar tu capacidad de identificar errores y proponer correcciones en un caso de uso mal diseñado.

### Consigna
Se te presentará un caso de uso con **7 errores intencionales**. Debes:

1. **Identificar mínimo 5 errores** (1 punto c/u)
2. **Proponer la corrección** para cada error identificado

### Criterios de Evaluación
- **Identificación correcta del error:** 0.5 puntos
- **Corrección apropiada:** 0.5 puntos
- **Total:** 5 errores × 2 puntos = 10 puntos (20% del examen)

### Ejemplo de Respuesta Esperada

**Error identificado:**
> "El actor 'Sistema' no debería ser un actor primario, ya que los actores deben ser externos al sistema."

**Corrección propuesta:**
> "Cambiar el actor a 'Administrador' o 'Usuario Autenticado' según corresponda."

---

## 💻 Parte 2: Diseño Práctico (60 min - 50%)

### Objetivo
Diseñar una nueva funcionalidad para tu proyecto con documentación completa.

### Consigna
Se te asignará **uno de los siguientes requisitos** para implementar en tu proyecto:

#### Opción A (Nivel Básico)
"Agregar funcionalidad de 'Guardar artículo como borrador' antes de publicar"

#### Opción B (Nivel Intermedio)
"Implementar sistema de 'Me gusta' en artículos con contador visible"

#### Opción C (Nivel Avanzado)
"Agregar sistema de notificaciones: el autor recibe alerta cuando alguien comenta su artículo"

### Entregables Requeridos

#### 1. Caso de Uso Completo (20 puntos)
Usar la plantilla estándar:
- **ID y Nombre**
- **Actores**
- **Descripción**
- **Precondiciones**
- **Flujo Principal**
- **Flujos Alternativos**
- **Postcondiciones**

#### 2. Diagrama de Clases (15 puntos)
- Clases nuevas necesarias
- Atributos y métodos principales
- Relaciones con clases existentes
- Cardinalidad correcta

#### 3. Diagrama de Secuencia (15 puntos)
- Flujo principal del caso de uso
- Mínimo 4 objetos interactuando
- Mensajes y respuestas claros
- Orden temporal correcto

### Criterios de Evaluación

**Caso de Uso (20 puntos):**
- Completitud (todos los campos): 5 pts
- Claridad del flujo principal: 5 pts
- Precondiciones/Postcondiciones correctas: 5 pts
- Flujos alternativos relevantes: 5 pts

**Diagrama de Clases (15 puntos):**
- Clases apropiadas: 5 pts
- Atributos y métodos correctos: 5 pts
- Relaciones bien definidas: 5 pts

**Diagrama de Secuencia (15 puntos):**
- Objetos correctos: 5 pts
- Mensajes apropiados: 5 pts
- Flujo lógico: 5 pts

---

## 🎤 Parte 3: Defensa Oral (10 min - 30%)

### Objetivo
Evaluar tu comprensión profunda del proyecto y capacidad de comunicación técnica.

### Estructura de la Defensa

#### 1. Presentación de tu Proyecto (3 min)
- Nombre e identidad del proyecto
- Feature única implementada
- Arquitectura general (MVC)

#### 2. Explicación de Decisión de Diseño (3 min)
El profesor elegirá UNA de estas preguntas:
- "¿Por qué elegiste esta estructura de clases?"
- "¿Cómo aplicaste el patrón MVC en tu proyecto?"
- "¿Qué patrones de diseño identificaste y por qué?"

#### 3. Defensa del Diseño de Parte 2 (2 min)
- Explicar caso de uso creado
- Justificar decisiones en diagramas

#### 4. Preguntas del Profesor (2 min)
Preguntas conceptuales sobre:
- Principios SOLID
- Diferencias entre diagramas UML
- Buenas prácticas aplicadas

### Criterios de Evaluación (30 puntos)

**Claridad de Comunicación (10 pts):**
- Explicación clara y estructurada
- Uso correcto de terminología técnica
- Capacidad de síntesis

**Comprensión del Proyecto (10 pts):**
- Demuestra conocimiento profundo
- Explica decisiones de diseño
- Identifica fortalezas y debilidades

**Respuestas a Preguntas (10 pts):**
- Respuestas correctas y fundamentadas
- Capacidad de relacionar teoría con práctica
- Pensamiento crítico

---

## 📚 Material de Estudio Recomendado

### Documentos del Curso
- `clase-1-introduccion-uml.md` - Casos de uso
- `clase-2-diagramas-uml.md` - Diagramas de clases, secuencia, actividad
- `clase-3-principios-patrones-arquitecturas.md` - MVC, patrones, SOLID
- `glosario-desarrollo-software.md` - Terminología técnica

### Tu Propio Proyecto
- Revisa tu README, CHANGELOG
- Repasa tus casos de uso y diagramas
- Identifica qué patrones aplicaste
- Prepara explicación de tu feature única

### Conceptos Clave a Repasar
- Diferencia entre actores primarios y secundarios
- Precondiciones vs Postcondiciones
- Tipos de relaciones en diagramas de clases
- Orden de mensajes en diagramas de secuencia
- Principios SOLID básicos
- Patrón MVC (Model-View-Controller)

---

## 🎯 Consejos para el Examen

### Antes del Examen
1. ✅ Revisa tu proyecto completo
2. ✅ Practica crear casos de uso en 10-15 minutos
3. ✅ Practica diagramas de clases simples
4. ✅ Prepara explicación de tu arquitectura MVC
5. ✅ Repasa terminología técnica

### Durante el Examen
1. ⏰ Administra bien tu tiempo (20-60-10 min)
2. 📝 Lee todas las consignas antes de empezar
3. 🎯 En Parte 1: busca errores obvios primero
4. 💡 En Parte 2: empieza por el caso de uso, luego diagramas
5. 🗣️ En Parte 3: respira, habla claro, no te apures

### Herramientas Permitidas
- ✅ draw.io / diagrams.net
- ✅ Mermaid Live Editor
- ✅ Tu proyecto en GitHub (consulta)
- ✅ Documentación del curso
- ❌ ChatGPT u otras IAs
- ❌ Comunicación con compañeros

---

## 📅 Información Logística

**Fecha:** [A confirmar]  
**Hora:** [A confirmar]  
**Modalidad:** Presencial  
**Lugar:** [A confirmar]

### Qué Traer
- Laptop con batería cargada
- Acceso a internet
- Tu proyecto en GitHub accesible
- Herramientas de diagramado instaladas

---

## ❓ Preguntas Frecuentes

**P: ¿Puedo consultar mi proyecto durante el examen?**  
R: Sí, en la Parte 2 puedes consultar tu proyecto para ver tu estructura existente.

**P: ¿Qué pasa si no termino la Parte 2 en 60 minutos?**  
R: Entrega lo que tengas. Es mejor un caso de uso completo y un diagrama parcial, que todo incompleto.

**P: ¿Puedo elegir el nivel de dificultad en Parte 2?**  
R: El profesor asignará el requisito según tu desempeño en el trabajo práctico.

**P: ¿La defensa oral es obligatoria?**  
R: Sí, representa el 30% de la nota. Sin defensa oral no se puede aprobar.

**P: ¿Qué pasa si me pongo nervioso en la defensa?**  
R: Es normal. Respira, tómate tu tiempo. El profesor hará preguntas de apoyo si es necesario.

---

## 📊 Ejemplo de Distribución de Puntaje

| Parte | Puntaje Máximo | Nota Equivalente |
|-------|----------------|------------------|
| Parte 1 | 10 puntos | 2.0/10 |
| Parte 2 | 50 puntos | 5.0/10 |
| Parte 3 | 30 puntos | 3.0/10 |
| **TOTAL** | **100 puntos** | **10/10** |

**Escala de Aprobación:**
- 90-100 pts: 9.0-10 (Sobresaliente)
- 80-89 pts: 8.0-8.9 (Muy Bueno)
- 70-79 pts: 7.0-7.9 (Bueno)
- 60-69 pts: 6.0-6.9 (Aprobado)
- 0-59 pts: 0-5.9 (Desaprobado)

---

**¡Éxito en tu examen!** 🚀

Si tienes dudas, consulta en las issues del repositorio o contacta al profesor.
