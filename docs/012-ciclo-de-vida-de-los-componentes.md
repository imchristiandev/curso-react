# Ciclo de vida
Son métodos especiales que se ejecutan automáticamente en un **Componente de clase**. ocurren en 3 fases:

1. Montaje.
2. Actualización.
3. Desmontaje.

## Montaje
Estos métodos se ejecutan cuando se crea un componente y se inserta en el árbol del DOM.

- **constructor()** Cuando se genera la instancia del componente
- **render()** Es el único método requerido, cuando se ejecuta, examina el estado y las propiedades, dibujando el componente del árbol del DOM
- **componentDidMount()** Se invoca inmediatamente despues de que un componente se ha insertado al arbol del DOM.

## Actualización
Estos métodos son ejecutados por cambios en el estado o las propiedades o componente.

- **render()** redibuja el componente cuando detecta cambios en el estado o las propiedades del componente.
- **componentDidUpdate()** Se ejecuta inmediatamente después de la actualización del estado o las propiedades.

## Desmontaje.
- **componentWillUnmount()** Se ejecuta antes de destruir el componente del arbol del DOM. Es un método útil para una tarea de limpieza.