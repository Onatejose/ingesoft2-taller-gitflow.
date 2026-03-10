# Documento de Pruebas

## 1. Descripcion del Sistema
La Plataforma de Gestión de Eventos Universitarios permite registrar estudiantes, validar su código estudiantil e inscribirlos en eventos. 

El sistema solo acepta estudiantes entre 16 y 65 años. El código estudiantil debe tener 8 caracteres, iniciar con "E" y los 7 restantes ser numéricos. 

Un estudiante solo puede inscribirse a eventos si está registrado, hay cupos disponibles y no está previamente inscrito.

---

## 2. Requerimientos a Evaluar

### RF01 – Edad del estudiante
El sistema debe permitir el registro de estudiantes cuya edad esté entre **16 y 65 años inclusive**.

### RF02 – Código del estudiante
El sistema debe permitir que los estudiantes se registren mediante un código de estudiante que cumpla:

- Debe tener exactamente **8 caracteres**
- El primer carácter debe ser la letra **E**
- Los **7 caracteres restantes deben ser numéricos (0-9)**
- Si el código no cumple las reglas, el sistema debe **rechazar el registro**

### RF03 – Inscripción a Evento

Un estudiante podrá inscribirse a un evento solo si:

- Está registrado.
- El evento tiene cupos disponibles.
- No está previamente inscrito.

Si alguna condición no se cumple, el sistema no debe permitir la inscripción.

---

## 3. Tecnicas de Prueba Aplicadas

### RF01
**Análisis de valores límite**

### RF02
**Partición de equivalencia**

### RF03
**Técnica seleccionada:** Tabla de decisión  

**Justificación:** Esta técnica permite evaluar múltiples condiciones al mismo tiempo y analizar cómo las diferentes combinaciones afectan el resultado de la inscripción al evento.

---

## 4. Casos de Prueba Diseñados

### RF01
| Edad | Resultado |
|-----|------|
| 10 | Fuera del rango |
| 15 | Fuera del rango |
| 16 | Dentro del rango |
| 30 | Dentro del rango |
| 65 | Dentro del rango |
| 66 | Fuera del rango |

### RF02
| Criterio | Clases válidas (V) | Clases inválidas (I) |
|----|------------|----------|
| Longitud | 8 caracteres | menos o más de 8 |
| Inicia con E | Empieza con E | Empieza con otra letra |
| Últimos 7 | Numéricos | No numéricos |

### RF03

| ¿Está registrado? | ¿El evento tiene cupos disponibles? | ¿Está previamente inscrito? | ¿Se registra en el evento? |
|------------------|-----------------------|----------------------|----------------------|
| Sí | Sí | No | Sí |
| No | Sí | Sí | No |

---
## 5. Trazabilidad
| Requerimiento |          Técnica        | Casos asociados |
|---------------|------------------------------------------------------|-----------------|
| RF-01         |  Análisis de valor límite| CP-01, CP-02    |
| RF-02         |  Partición de equivalencia       | CP-03    |
| RF-03         |    Tabla de decisión    | CP-04    |

---

## 6. Gestion de Versiones (GitFlow)

**Ramas creadas:**

- main  
- develop  
- feature/descripcion-del-sistema  
- feature/rf01-registro-estudiantes  
- feature/rf02-codigo-estudiante  
- feature/rf03-inscripcion-evento  
- feature/trazabilidad  
- feature/gestion-de-versiones  
- feature/analisis  

**Flujo seguido:**

Se creó a partir de la rama **main** la rama **develop**, y a partir de **develop** se crearon las ramas **feature** correspondientes a cada ítem del documento. Cada integrante realizó las tareas correspondientes a su feature y las subió a la rama **develop**. Allí se aceptaron los cambios y, una vez estuvieron todas las features integradas y sin conflictos, se subió el documento completo desde **develop** a **main**.

**Cambios integrados:**

Cada cambio se subió desde la **feature** a **develop**. Allí uno de los integrantes verificó que la información fuera correcta respecto a lo solicitado y que no hubiera conflictos. Si aparecían conflictos, esta persona los solucionaba y finalmente permitía la integración.

**Conflictos:**

En algunos intentos de integración hacia **develop** se generaron conflictos. La persona encargada los resolvía revisando ambas versiones y ubicando los textos en la posición correcta dentro del documento.
## 7. Analisis


¿Qué técnica fue más compleja de identificar?
La técnica más compleja de identificar fue la tabla de decisión, ya que requiere analizar múltiples condiciones al mismo tiempo y definir todas las combinaciones posibles de resultados. Esto hace que el diseño de los casos de prueba sea más detallado y requiera mayor análisis lógico.

¿Qué diferencia notaron entre develop y main?
La rama main contiene la versión estable y final del proyecto, mientras que develop es la rama donde se integran los cambios de desarrollo antes de pasar a la versión final. En develop se prueban y revisan los cambios antes de integrarlos en main.

¿Qué pasaría si trabajaran directamente en main?
Si todos trabajaran directamente en main, podrían generarse conflictos constantes entre cambios, errores en la versión principal y pérdida de estabilidad del proyecto. Además, sería más difícil controlar y revisar las modificaciones realizadas.

¿Cómo ayuda GitFlow a controlar el cambio?
GitFlow ayuda a organizar el trabajo mediante ramas específicas para cada funcionalidad, permitiendo desarrollar cambios de forma independiente. Esto facilita la revisión, la integración progresiva y la detección de errores antes de que los cambios lleguen a la versión final del sistema.
