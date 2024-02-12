# Formato de los 
#### [Volver al índice](../README.md)

Es necesario utilizar el siguiente formato: `<type>(<scope>): <description>`. Si es necesario, ponga cualquier información extra en la descripción.

## Tipos de commit
Los tipos de commit incluyen (pero no se limitan a):
- docs: Cambios sólo en la documentación
- feat: Una nueva característica
- fix: Una corrección de errores
- testing: Añadir o arreglar pruebas
- chore: Otros cambios que no afectan el código fuente, como por ejemplo añadir contenido al fichero .gitignore, agregar logs.
- revert: Si el commit revierte un commit anterior. Debería indicarse el hash del commit que se revierte.

## Scope
El scope se va a basar en el nombre de la carpeta en la que se encuentra el fichero modificado. Por ejemplo, si se modifica un fichero en la carpeta `apps/client-web`, el scope será `client-web`. Asi mismo con los ficheros de la carpeta `libs`, `principal-api`, etc.
Si son en la raíz del proyecto, el scope será `root`.

## Ejemplos:
- `docs(root): Añadir información sobre el formato de los commits`
- `feat(client-web): Añadir componente de login`