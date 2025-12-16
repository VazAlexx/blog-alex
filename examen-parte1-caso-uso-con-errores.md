# Parte 1 del Examen: Análisis Crítico
**Tiempo:** 20 minutos  
**Puntaje:** 20% del examen final

---

## 📋 Consigna

A continuación se presenta un caso de uso con **7 errores intencionales**. Tu tarea es:

1. **Identificar mínimo 5 errores**
2. **Explicar por qué es un error**
3. **Proponer la corrección apropiada**

**Formato de respuesta:**

```
ERROR #1:
Ubicación: [Sección donde está el error]
Descripción: [Qué está mal]
Corrección: [Cómo debería ser]
```

---

## 📄 Caso de Uso con Errores

### CU-05: Eliminar Artículo

**Actor Principal:** Sistema, Administrador

**Descripción:**  
El sistema permite eliminar artículos del blog cuando el usuario lo solicita.

**Precondiciones:**
- El artículo debe existir en la base de datos
- El artículo debe tener más de 100 comentarios

**Flujo Principal:**
1. El Administrador accede al panel de control
2. El Administrador selecciona la opción "Gestionar Artículos"
3. El sistema muestra la lista de artículos
4. El Administrador hace clic en "Eliminar" junto al artículo deseado
5. El sistema elimina el artículo inmediatamente
6. El sistema muestra mensaje "Artículo eliminado"
7. Fin del caso de uso

**Flujos Alternativos:**
- Ninguno

**Postcondiciones:**
- El artículo ya no existe en la base de datos
- El sistema envía un email al autor
- Todos los comentarios asociados se eliminan
- El Administrador recibe una notificación

**Excepciones:**
- Si el artículo no existe, el sistema muestra un error

---

## 🔍 SOLUCIÓN PARA EL EVALUADOR

### Error #1: Actores Incorrectos
**Ubicación:** Actor Principal  
**Error:** "Sistema" no puede ser un actor principal. Los actores deben ser entidades externas al sistema (personas, otros sistemas, dispositivos).  
**Corrección:** El actor principal debe ser solo "Administrador" o "Autor del Artículo"

**Puntaje:** 2 puntos (1 identificación + 1 corrección)

---

### Error #2: Precondición Incorrecta
**Ubicación:** Precondiciones  
**Error:** "El artículo debe tener más de 100 comentarios" es una regla de negocio arbitraria que no tiene sentido como precondición. Las precondiciones deben ser estados necesarios para ejecutar el caso de uso, no restricciones de negocio sin justificación.  
**Corrección:** 
- "El usuario debe estar autenticado como Administrador o ser el Autor del artículo"
- "El artículo debe existir en el sistema"

**Puntaje:** 2 puntos

---

### Error #3: Falta Confirmación en Flujo Principal
**Ubicación:** Flujo Principal, paso 5  
**Error:** El sistema elimina el artículo inmediatamente sin pedir confirmación. Esto es peligroso para operaciones destructivas.  
**Corrección:** Agregar pasos:
```
5. El sistema muestra un diálogo de confirmación: "¿Está seguro de eliminar este artículo?"
6. El Administrador confirma la eliminación
7. El sistema elimina el artículo
```

**Puntaje:** 2 puntos

---

### Error #4: Flujos Alternativos Vacíos
**Ubicación:** Flujos Alternativos  
**Error:** Dice "Ninguno" pero claramente hay flujos alternativos posibles (ej: el usuario cancela la eliminación en el paso 5).  
**Corrección:** Agregar al menos:
```
FA1: Cancelar eliminación
- En el paso 6, si el Administrador cancela:
  6a. El sistema no elimina el artículo
  6b. El sistema muestra mensaje "Operación cancelada"
  6c. Retorna al paso 3
```

**Puntaje:** 2 puntos

---

### Error #5: Postcondiciones Excesivas
**Ubicación:** Postcondiciones  
**Error:** Hay 4 postcondiciones listadas, pero algunas son demasiado específicas o no son postcondiciones reales:
- "El sistema envía un email al autor" es parte del flujo, no una postcondición
- "El Administrador recibe una notificación" también es parte del flujo

**Corrección:** Las postcondiciones deben ser estados finales del sistema:
```
Postcondiciones:
- El artículo ya no existe en la base de datos
- Todos los comentarios asociados se eliminan
- Se registra la eliminación en el log del sistema
```

**Puntaje:** 2 puntos

---

### Error #6: Falta Actor Secundario
**Ubicación:** Actores  
**Error:** Si el sistema envía un email al autor (postcondición mencionada), entonces "Sistema de Email" o "Servicio de Notificaciones" debería ser un actor secundario.  
**Corrección:** Agregar:
```
Actor Secundario: Sistema de Notificaciones
```

**Puntaje:** 2 puntos

---

### Error #7: Excepción Redundante
**Ubicación:** Excepciones  
**Error:** "Si el artículo no existe, el sistema muestra un error" es redundante porque ya está en las precondiciones que el artículo debe existir. Si la precondición no se cumple, el caso de uso no debería ejecutarse.  
**Corrección:** Eliminar esta excepción o moverla a un flujo alternativo:
```
FA2: Artículo no encontrado
- En el paso 4, si el artículo ya no existe:
  4a. El sistema muestra mensaje "El artículo no existe o ya fue eliminado"
  4b. Retorna al paso 3
```

**Puntaje:** 2 puntos

---

## 📊 Rúbrica de Evaluación

### Puntaje Total: 10 puntos (20% del examen)

**Por cada error correctamente identificado y corregido:**
- Identificación del error: 1 punto
- Corrección apropiada: 1 punto
- **Total por error:** 2 puntos

**Mínimo requerido:** 5 errores (10 puntos)

### Criterios de Calidad

**Identificación (1 punto):**
- ✅ Identifica correctamente la ubicación del error
- ✅ Explica claramente por qué es un error
- ✅ Demuestra comprensión del concepto

**Corrección (1 punto):**
- ✅ Propone una solución viable
- ✅ La corrección sigue las buenas prácticas
- ✅ Es específica y aplicable

### Puntaje Parcial

Si el estudiante:
- Identifica el error pero la corrección es incompleta: 1.5 puntos
- Identifica el error pero la corrección es incorrecta: 1 punto
- Identifica algo que no es un error: 0 puntos

---

## 📝 Ejemplo de Respuesta Excelente

```
ERROR #1:
Ubicación: Actor Principal
Descripción: "Sistema" está listado como actor principal, pero los actores 
deben ser entidades externas al sistema. El sistema no puede ser actor de 
sí mismo.
Corrección: Eliminar "Sistema" de los actores. El único actor principal 
debe ser "Administrador" (o "Autor del Artículo" si se permite que los 
autores eliminen sus propios artículos).

ERROR #2:
Ubicación: Precondiciones - "El artículo debe tener más de 100 comentarios"
Descripción: Esta precondición no tiene sentido lógico. ¿Por qué un artículo 
necesitaría 100 comentarios para poder ser eliminado? Las precondiciones deben 
ser condiciones necesarias para ejecutar el caso de uso, no restricciones 
arbitrarias.
Corrección: Reemplazar con precondiciones relevantes:
- "El usuario debe estar autenticado como Administrador"
- "El artículo debe existir en el sistema"
```

---

## 🎯 Consejos para Estudiantes

### Dónde Buscar Errores Comunes

1. **Actores:**
   - ¿Son entidades externas?
   - ¿El "Sistema" está como actor?
   - ¿Faltan actores secundarios?

2. **Precondiciones:**
   - ¿Son realmente necesarias?
   - ¿Tienen sentido lógico?
   - ¿Faltan precondiciones importantes?

3. **Flujo Principal:**
   - ¿Falta confirmación en operaciones destructivas?
   - ¿Los pasos son claros y secuenciales?
   - ¿Hay saltos lógicos?

4. **Flujos Alternativos:**
   - ¿Están todos los caminos alternativos?
   - ¿Qué pasa si el usuario cancela?
   - ¿Qué pasa si hay errores?

5. **Postcondiciones:**
   - ¿Son estados finales del sistema?
   - ¿O son acciones que deberían estar en el flujo?
   - ¿Son verificables?

6. **Excepciones:**
   - ¿Son realmente excepciones o flujos alternativos?
   - ¿Son redundantes con las precondiciones?

---

## ⏰ Gestión del Tiempo

**Tiempo total: 20 minutos**

- **5 min:** Lectura completa del caso de uso
- **10 min:** Identificación de errores (busca 7, necesitas 5)
- **5 min:** Escribir correcciones claras

**Estrategia:**
1. Lee todo el caso de uso primero
2. Marca los errores obvios
3. Revisa sección por sección
4. Escribe las correcciones de los 5 más claros
5. Si te sobra tiempo, busca los 2 restantes

---

## 📚 Recursos de Estudio

Para prepararte para esta parte:

1. Revisa `clase-1-introduccion-uml.md` - Sección de Casos de Uso
2. Mira la plantilla de casos de uso del curso
3. Revisa tus propios casos de uso del proyecto
4. Practica identificar qué hace a un buen caso de uso

**Conceptos clave:**
- Actores primarios vs secundarios
- Precondiciones vs Postcondiciones
- Flujo principal vs Flujos alternativos
- Excepciones vs Flujos alternativos

---

**Nota para el Profesor:**  
Este documento contiene tanto el caso de uso con errores como la solución completa. 
Entregar solo la primera sección a los estudiantes durante el examen.
