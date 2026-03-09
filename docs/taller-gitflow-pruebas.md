# Documento de Pruebas

## 1. Descripcion del Sistema
La Plataforma de Gestión de Eventos Universitarios permite registrar estudiantes, validar su código estudiantil e inscribirlos en eventos. El sistema solo acepta estudiantes entre 16 y 65 años. El código estudiantil debe tener 8 caracteres, iniciar con "E" y los 7 restantes ser numéricos. Un estudiante solo puede inscribirse a eventos si está registrado, hay cupos disponibles y no está previamente inscrito. Si alguna condición no se cumple, la inscripción no se permite.
## 2. Requerimientos a Evaluar
RF-O1. El sistema debe permitir el registro de estudiantes cuya edad esté entre **16 y 65 años inclusive**.

Interpretación:

- Edad mínima permitida: **16**
- Edad máxima permitida: **65**
- Edades menores a 16 → **no permitidas**
- Edades mayores a 65 → **no permitidas**

---

## 3. Tecnicas de Prueba Aplicadas
- Análisis de valores límite
- El requerimiento establece un **rango numérico válido**, por lo que lo mas recomendable es Valores límite para probar los extremos del rango donde suelen ocurrir errores.

## 4. Casos de Prueba Diseñados
| Edad | Rango |
|-----|------|
| 10 | Fuera del rango |
| 15 | Fuera del rango |
| 16 | Dentro del rango |
| 30 | Dentro del rango |
| 65 | Dentro del rango |
| 66 | Fuera del rango |


## 5. Trazabilidad

## 6. Gestion de Versiones (GitFlow)
