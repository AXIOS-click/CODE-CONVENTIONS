# Convencion de nombres de 

#### [Volver al índice](../README.md)

## Nombres de variables, funciones, clases, y Constantes
### Nombres de variables en camelCase
```typescript
const nombreDeVariable = 'valor';
```

### Nombres de funciones en camelCase
```typescript
function nombreDeFuncion() {
  // ...
}
```

### Nombres de clases en PascalCase
```typescript
class NombreDeClase {
  // ...
}
```

### Nombres de constantes en UPPER_SNAKE_CASE
```typescript
const NOMBRE_DE_CONSTANTE = 'valor';
```

### Nombres de interfaces, types, enums en PascalCase
Para interfaces y types se debe utilizar PascalCase, ya que son tipos de datos y deben in precedidas por la palabra `I`.
Para types se debe utilizar PascalCase, ya que son tipos de datos y deben in precedidas por la palabra `T`.
Para enums se debe utilizar PascalCase, ya que son tipos de datos y deben in precedidas por la palabra `E`.
```typescript
interface INombreDeInterface {
  // ...
}

type TNombreDeType = {
  // ...
}

enum ENombreDeEnum {
  // ...
}
```