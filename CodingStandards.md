<h1 align="center">
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

Para complementar el documento de estándares de programación, se pueden incluir secciones adicionales que aborden otros aspectos importantes del desarrollo de software, tales como los estándares para el manejo de errores, pruebas unitarias, versionado de código, y documentación de código. A continuación, se presentan algunas propuestas para estas secciones:

## Manejo de Errores

12. **Manejo de Excepciones:**
   - Capturar excepciones específicas en lugar de usar capturas genéricas.
   - Proporcionar mensajes de error claros y detallados que ayuden en la depuración.

```javascript
try {
    // código que puede lanzar una excepción
} catch (errorEspecifico) {
    console.error("Error específico ocurrido:", errorEspecifico);
} catch (error) {
    console.error("Error genérico:", error);
}
```

13. **Promesas y Async/Await:**
   - Utilizar `async/await` para manejar promesas, mejorando la legibilidad del código.
   - Manejar errores con bloques `try/catch` en funciones asíncronas.

```javascript
async function obtenerDatos() {
    try {
        const datos = await fetch('url');
        return datos.json();
    } catch (error) {
        console.error("Error al obtener datos:", error);
    }
}
```

## Pruebas Unitarias

14. **Escribir Pruebas:**
   - Escribir pruebas unitarias para cada nueva funcionalidad o corrección de errores.
   - Nombrar las pruebas de manera descriptiva, reflejando claramente lo que se está probando.

```javascript
describe('Pruebas para sumaDosNumeros', () => {
    it('debería retornar la suma de dos números', () => {
        expect(sumaDosNumeros(2, 3)).toEqual(5);
    });
});
```

## Versionado de Código

15. **Uso de Git:**
   - Utilizar mensajes de commit claros y descriptivos.
   - Seguir un modelo de ramificación establecido, como Git Flow o GitHub Flow.

```plaintext
Mensaje de Commit:
- Corrige: Descripción breve del problema resuelto.
- Añade: Nueva funcionalidad o archivo añadido.
- Mejora: Mejoras en el código existente sin cambiar su funcionalidad.
```

## Documentación de Código

16. **Documentar Código:**
   - Documentar clases, métodos, y funciones utilizando comentarios de documentación que describan su propósito, parámetros y valor de retorno.
   - Incluir ejemplos de uso cuando sea apropiado.

```javascript
/**
 * Divide dos números.
 * @param {number} dividendo - El número a dividir.
 * @param {number} divisor - El número con el que dividir.
 * @return {number} El resultado de la división.
 * @throws {Error} Lanza un error si el divisor es cero.
 */
function dividirDosNumeros(dividendo, divisor) {
    if (divisor === 0) {
        throw new Error("División por cero.");
    }
    return dividendo / divisor;
}
```

---

Estas secciones adicionales ayudan a abarcar un espectro más amplio de prácticas recomendadas en el desarrollo de software, asegurando que el código no solo sea legible y consistente, sino también robusto, fácilmente mantenible y bien documentado.