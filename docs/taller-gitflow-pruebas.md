# Documento de Pruebas

## 1. Descripcion del Sistema

## 2. Requerimientos a Evaluar

---
## RF-03 Inscripción a Evento

Un estudiante podrá inscribirse a un evento solo si:

- Está registrado.
- El evento tiene cupos disponibles.
- No está previamente inscrito.

Si alguna condición no se cumple, el sistema no debe permitir la inscripción.

---

## 3. Tecnicas de Prueba Aplicadas

---
## RF-03 Inscripción a Evento

**Tecnica seleccionada:** Tabla de decisión

**Justificación:** Este tipo de tecnica es la mejor ya que nos permite comparar varias condiciones y acciones para analizar como estas diferentes combinaciones nos pueden llevar a varios resultados y asi ayudandonos para el caso de prueba.

---

## 4. Casos de Prueba Diseñados

---
## RF-03 Inscripción a Evento

**Diseño de casos de prueba:**

- **CP-05:** En este caso de prueba se asume que la persona está registrado, el evento tiene cupos disponibles y la persona esta previamente inscrita, por ende el resultado es que se registra exitosamente en el evento. 


| ¿Está registrado? | ¿El evento tiene cupos disponibles? | ¿Está previamente inscrito? | ¿Se registra en el evento? |
|------------------|-----------------------|----------------------|----------------------|
| Sí               | Sí                    | No                   | Sí                   |


- **CP-06:** En este caso de prueba se asume que la persona NO está registrado, el evento tiene cupos disponibles y la persona esta previamente inscrita, por ende el resultado es que se NO registra en el evento. 


| ¿Está registrado? | ¿El evento tiene cupos disponibles? | ¿Está previamente inscrito? | ¿Se registra en el evento? |
|------------------|-----------------------|----------------------|----------------------|
| No               | Si                   | Si                   | No                   |


---

## 5. Trazabilidad

## 6. Gestion de Versiones (GitFlow)
