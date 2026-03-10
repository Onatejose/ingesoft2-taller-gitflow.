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

---

## 3. Tecnicas de Prueba Aplicadas

### RF01
**Análisis de valores límite**

### RF02
**Partición de equivalencia**

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

---

## 5. Trazabilidad

## 6. Gestion de Versiones (GitFlow)