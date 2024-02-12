# Documentación para Ramas y PRs 

#### [Volver al índice](../README.md)

## Nomenclatura de Ramas
Para nombrar las ramas, se debe seguir la siguiente convención:

- Tipo de Rama: Este identifica la naturaleza de la rama. 
    - Ejemplos: feature/, release/, hotfix/, etc.
- Nombre de la Funcionalidad: Es el nombre de la tarea, se debe usar kebab-case (ej. nuevo-cambio).
- Dependencias de Ramas: Si una rama depende de otra rama, esta dependencia se indica con un guion bajo _ (ej. feature/nuevo-cambio-rama_adyacente).

## Gráfico de Tipos de Ramas
```mermaid
graph TD
    A[main] -->|Generada por defecto| B[develop]
    B -->|Nuevo Feature| C[feature/nombre-feature]
    B -->|Preparar nueva versión| D[release/vX.X.X]
    A -->|Corregir error crítico| E[hotfix/descripcion-error]
    C -->|Al completar desarrollo| B
    D -->|Tras pruebas finales| A
    E -->|Tras corregir el error| A
```

## Grafico ejemplo de git:
```mermaid
gitGraph
    commit
    branch develop
    checkout develop
    commit
    commit
    branch feature/nombre-feature
    checkout feature/nombre-feature
    commit
    commit
    branch feature/nombre-feature_adyacente
    checkout feature/nombre-feature_adyacente
    commit
    checkout feature/nombre-feature
    merge feature/nombre-feature_adyacente
    commit
    checkout develop
    merge feature/nombre-feature
    commit
    checkout main
    merge develop tag:"v1.0.0"
    commit
    branch hotfix/descripcion-error
    checkout hotfix/descripcion-error
    commit
    checkout main
    merge hotfix/descripcion-error tag:"v1.1.0"
    commit
```

## Pull Requests (PRs)
Al hacer un Pull Request:

1. **Título**: Colocar el nombre de la rama. Si es la primera vez que se hace un PR de esa rama, sólo poner el nombre. Si no es la primera vez, separar con un guion medio `-` y agregar el motivo por el cual se hace nuevamente el PR (ej. `feature/ventana-consulta-usuarios - correcciones QA`).

```mermaid
sequenceDiagram
    participant D as Desarrollador
    participant R as Revisor
    participant B as Rama Base (ej. develop)
    participant F as Rama Feature
    D->>F: Commit cambios en rama feature
    D->>R: Solicita PR (Pasa a la columna de revision)
    R->>F: Revisa cambios en rama feature
    R->>D: Da feedback (Si hay error se regresa a InPrgoress)
    D->>F: Hace cambios necesarios
    R->>B: Acepta PR y mergea cambios a rama base (Pasa a la columna por desplegar)
```