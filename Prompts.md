Product Backlog

1. Product Backlog

Resume las descripciones de esto

|**ID**| **DESCRIPCIÓN**|**PRIORIDAD**|**STATUS**|**SPRINT**|
|-|-|-|-|-|
|HU1|**Como** usuario del sistema, **quiero** ver los nombres de las posturas en tres idiomas diferentes (sánscrito, español e inglés), **para** aprender su significado.**Criterio de aceptación:** **Dado** que el usuario ingresa una postura, **cuando** el software muestra la información de la postura, **entonces** el software permitirá la visualización del nombre de la postura en tres idiomas diferentes, con una fuente grande y llamativa, que permita su fácil lectura.|Alta|No Iniciada|0|
|HU2|**Como** usuario del sistema, **quiero** escribir los nombres de las posturas en sánscrito, español o inglés y obtener la traducción en sánscrito, español e inglés, **para** poder comprender su significado y ampliar mi vocabulario. **Criterio de aceptación:** **Dado** que el usuario ingresa un nombre de postura en sánscrito, español o inglés, **cuando** el software procesa el nombre, **entonces** el software devuelve la traducción en sánscrito, español e inglés, con una fuente clara y legible, que permita su fácil comprensión.|Alta|No Iniciada|0|
|HU3|**Como** usuario del sistema, **quiero** recibir una notificación cuando ingrese nombres de posturas inexistentes o con mala escritura de una postura en el sistema, **para** poder corregir la entrada fácilmente. **Criterio de aceptación:** **Dado** que el usuario ingresa un nombre de postura inexistente o con mala escritura de una postura, **cuando** el software procesa el nombre, **entonces** el software muestra una notificación llamativa, en forma de un mensaje de error, con una fuente grande y un color llamativo, indicando que se debe revisar el nombre ingresado.|Alta|No Iniciada|0|
|HU4|**Como** usuario del sistema, **quiero** tener una interfaz de usuario fácil de usar, que considere aspectos de accesibilidad, **para** facilitar mi interacción con el software y mejorar mi experiencia de usuario. **Criterio de aceptación:** **Dado** que el usuario accede al software, **cuando** el software muestra la interfaz de usuario, **entonces** el software muestra una interfaz de usuario intuitiva, simple y atractiva, que sigue las mejores prácticas de diseño de interfaces.|Alta|No Iniciada|0|

2. Sprint 1

a. Sprint Backlog 

Generas tareas para el spring Backlog a partir de estas historias de usuario
|**ID**| **DESCRIPCIÓN**|**PRIORIDAD**|**STATUS**|**SPRINT**|
|-|-|-|-|-|
|HU1|Ver nombres de posturas en tres idiomas con una visualización clara y atractiva para facilitar el aprendizaje de su significado.|Alta|No Iniciada|0|
|HU2|Escribir y obtener traducciones de los nombres de las posturas en los tres idiomas mencionados para comprender su significado y ampliar el vocabulario del usuario.|Alta|No Iniciada|0|
|HU3|Recibir notificaciones sobre errores al ingresar nombres de posturas, ya sea por ser inexistentes o estar mal escritas, para corregir fácilmente la entrada.|Alta|No Iniciada|0|
|HU4|Disponer de una interfaz de usuario fácil de usar y accesible para mejorar la experiencia del usuario y su interacción con el software.|Alta|No Iniciada|0|

3. Estándares de codificación 
Complementa este documento de estandares de programacion <h1 align="center">
    Escuela Politécnica Nacional<br>
    Facultad de Ingeniería en Sistemas<br>
    Metodologías Ágiles<br>
</h1>

# Estándares de Codificación - Empresa Yoghismo

## Convenciones Generales

1. **Indentación:**
   - Utilizar tabulaciones en lugar de espacios.
   - Establecer una indentación de 1 tabulación.

2. **Punto y Coma:**
   - Incluir punto y coma al final de cada declaración.

3. **Longitud de línea:**
   - Limitar la longitud de línea a 80-100 caracteres.

4. **Espacios en Blanco:**
   - Utilizar espacios en blanco de manera consistente para mejorar la legibilidad.

## Nombrado de Variables

5. **Variables:**
   - Utilizar camelCase para nombrar variables (e.g., `miVariable`).

6. **Constantes:**
   - Nombrar constantes en mayúsculas con guiones bajos para separar palabras (e.g., `MI_CONSTANTE`).

## Estructuras de Control

7. **if-else:**
   - Incluir llaves incluso para bloques de código de una sola línea.
```javascript
if (condicion) {
    // código
} else {
    // código
}
```

8. **Switch:**
   - Incluir un comentario `// fall through` cuando se omite un `break` de manera intencional.

```javascript
switch (variable) {
    case 1:
        // código
        break;
    case 2:
        // código
        // fall through
    case 3:
        // código
        break;
    default:
        // código
        break;
}
```


## Funciones

9. **Declaración de Funciones:**
   - Utilizar la declaración de funciones con nombre en lugar de expresiones de función anónimas.

```javascript
function miFuncion(parametro) {
    // código
}
```


10. **Parámetros de Función:**
   - Utilizar camelCase para los nombres de parámetros.

```javascript
function sumaDosNumeros(numeroUno, numeroDos) {
    return numeroUno + numeroDos;
}
```


## Comentarios

11. **Comentarios:**
   - Utilizar comentarios descriptivos y claros. Evitar comentarios obvios o innecesarios.

```javascript
// Buen comentario
function dividirDosNumeros(dividendo, divisor) {
    // Verificar que el divisor no sea cero antes de realizar la división
    if (divisor !== 0) {
        return dividendo / divisor;
    } else {
        console.error("Error: División por cero.");
        return NaN;
    }
}
```