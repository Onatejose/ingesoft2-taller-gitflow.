# Documento de Pruebas

## 1. Descripcion del Sistema
rf02
- el sistema debe permitir que los estudiantes se pueda registrar mediante un codigo del estudiante que minimo deba tener 8 caracteres, siguiendo algunas condiciones, como por ejemplo el primer caracter deba tener la letra E


## 2. Requerimientos a Evaluar
 RF02
-Debe tener exactamente 8 caracteres.
-El primer carácter debe ser la letra “E”.
-Los 7 caracteres restantes deben ser numéricos (0-9).
-El sistema debe aceptar el registro únicamente si el código cumple todas las condiciones.
-Si el código no cumple alguna de las reglas, el sistema debe rechazar el registro y mostrar un mensaje de error indicando que el código es inválido.




## 3. Tecnicas de Prueba Aplicadas
RF02
Tecnica- Particion de equivalencia
-se usa particion de equivalencia, por que hace que el sistema implemente nuevas reglas como en este caso, son 8 caracteres que necesita como minimo se acopla muy bien al requerimiento

---


## 4. Casos de Prueba Diseñados
RF02
| Criterio |clases validas(V) | Clases invalidas(I) |
|----|------------|----------|
| longitud de caracter | solamente 8 caracteres | menos o mas de 8 caracteres |
|iniciar con la lera E|debe iniciar con la letra E|inicia con cualquier letra menos E|
|7 caracter restantes numericos|los ultimos 7  son numericos|los ultimos no son numericos|








## 5. Trazabilidad


## 5. Trazabilidad
## 6. Gestion de Versiones (GitFlow)
