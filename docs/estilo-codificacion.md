# Estilo de codificación

#### [Volver al índice](../README.md)

Para maximizar la legibilidad y la corrección de nuestro código, requerimos que los nuevos envíos sigan el estilo estándar de JavaScript/Typescript.

Algunas (pero no todas) de las cosas a tener en cuenta:

- Siga la indentación del código: Utilice siempre 4 espacios para la sangría de los bloques de código (esta validado con prettier).
- Asegurese de que su código no contenga espacios en blanco innecesarios.
- No olvide que toda declaración debe terminar con un punto y coma.
- Siempre use los types de TypeScript para las variables y funciones. No utilice `any` o `unknow` a menos que sea absolutamente necesario.
```typescript
function sumOfArray(arrayOfNumbers: number[]): number {
  let suma: number = 0

  for (let i: numver = 0; i < arrayOfNumbers.length; i++) {
    suma += arrayOfNumbers[i]
  }
  return suma
```
- Evite el uso de variables globales y evite `==` en favor de `===`.
- Utiliza `let` en lugar de `var`.
- Por favor, absténgase de utilizar `console.log` o cualquier otro método de consola cuando envies tu PR (Si los usas para debuggear eliminalos antes de realizar tu PR o se rechazará).
- No utilices en absoluto `alert`.
- Recomendamos encarecidamente el uso de ECMAScript 6.
- Evite importar bibliotecas externas para afunciones basicas. Sólo utilice esas bibliotecas que ya tengamos implementadas en caso de ser asi.