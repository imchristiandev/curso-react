# Comunicación etnre componentes
React utiliza el **one way data binding** flujo de datos de padre a hijo.

Tenemos 3 casos de comunicación entre los componentes de *React*

1.  Comunicación entre un componente padre a uno hijo
2. Comunicación entre un componente hijo y su padre
3. Comunicación entre componentes no relacionados

## Comunicación entre un componente padre a uno hijo
Se deberá pasar mediante propiedades.

## Comunicación entre un componente hijo a uno padre
Cuando tenemos la necesidad de que un componente hijo mande datos a su padre los podemos hacer a traves de los **eventos**, simplemente pasamos una función como _**prop**_ del componente padre al componente hijo, y éste ejecutará la función .

En este ejemplo, cambiaremos el estado del componente padre pasando una función al componente hijo e invocando esa función dentro del componente hijo.

## Comunicación entre componentes no relacionados

Si los componentes no tienen una relación padre-hijo o están relacionados, pero están demasiado lejos, como por ejemplo, un bisnieto o tataranieto, tenemos que crear un mecanismo de observación y/o suscripción para la comunicación entre dichos componentes.

Al menos existen 3 patrones para hacer esto.

1.  Patrón **Emisor de eventos / Destino / Despachador** : los oyentes deben hacer referencia a la fuente para suscribirse.
2.  Patrón **Publicación / Suscripción**: no necesita una referencia específica a la fuente que desencadena el evento, hay un objeto global accesible en todas partes que maneja todos los eventos.
3.  Patrón **Señales**: similar al Emisor de Eventos, pero aquí no usa cadenas aleatorias. Cada objeto que podría emitir eventos debe tener una propiedad específica con ese nombre. De esta manera, se sabe exactamente qué eventos puede emitir un objeto.
4.  [**Portales**](https://es.reactjs.org/docs/portals.html): proporcionan una opción de primera clase para renderizar hijos en un nodo _DOM_ que existe por fuera de la jerarquía del _DOM_ del componente padre.

Puedes encontrar más información al respecto en este [enlace](https://github.com/millermedeiros/js-signals/wiki/Comparison-between-different-Observer-Pattern-implementations).

Otra manera de compartir datos entre componentes sin que tengan una relación padre-hijo es compartiendo un **estado global** accesible para todos los componentes de nuestra aplicación, para ello podríamos usar 2 opciones:

1.  _**Redux**_: librería externa a _React_ para el manejo del estado.
2.  _**Context**_: un _API_ interna de _React_ que provee una forma de pasar datos a través del árbol de componentes sin tener que pasar _props_ manualmente en cada nivel. Esta _API_ la retomaremos cuando veamos el tema de _Hooks_.