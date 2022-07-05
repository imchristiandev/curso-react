# Eventos Nativos, Sintéticos & Personalizados
A tus manejadores de eventos se les pasarán instancias de `SyntheticEvent`, un contenedor agnóstico al navegador alrededor del evento nativo del navegador. Tiene la misma interfaz que el evento nativo del navegador, incluyendo `stopPropagation()` y `preventDefault()`, excepto que los eventos funcionan de manera idéntica en todos los navegadores.

Si encuentras que necesitas el evento del navegador subyacente por alguna razón, simplemente use el atributo `nativeEvent` para obtenerlo. Los eventos sintéticos son diferentes y no tienen una correspondencia directa con los eventos nativos del navegador. Por ejemplo en `onMouseLeave` `event.nativeEvent` apuntará al evento `mouseout`. La correspondencia específica no es parte de la API pública y puede cambiar en cualquier momento. Cada objeto `SyntheticEvent` tiene los siguientes atributos:

```
boolean bubbles
boolean cancelable
DOMEventTarget currentTarget
boolean defaultPrevented
number eventPhase
boolean isTrusted
DOMEvent nativeEvent
void preventDefault()
boolean isDefaultPrevented()
void stopPropagation()
boolean isPropagationStopped()
void persist()
DOMEventTarget target
number timeStamp
string type
```

React normaliza los eventos para que tengan propiedades consistentes en diferentes navegadores.

Los controladores de eventos a continuación se activan por un evento en la fase de propagación. Para registrar un controlador de eventos llamado en la fase de captura, agrega `Capture` al nombre del evento; por ejemplo, en lugar de usar `onClick`, usarías`onClickCapture` para manejar el evento de click en la fase de captura.

-   [Eventos del Portapapeles](https://es.reactjs.org/docs/events.html#clipboard-events)
-   [Eventos de Composición](https://es.reactjs.org/docs/events.html#composition-events)
-   [Eventos del Teclado](https://es.reactjs.org/docs/events.html#keyboard-events)
-   [Eventos de Enfoque](https://es.reactjs.org/docs/events.html#focus-events)
-   [Eventos de Formulario](https://es.reactjs.org/docs/events.html#form-events)
-   [Eventos genéricos](https://es.reactjs.org/docs/events.html#generic-events)
-   [Eventos del Ratón](https://es.reactjs.org/docs/events.html#mouse-events)
-   [Eventos del Puntero](https://es.reactjs.org/docs/events.html#pointer-events)
-   [Eventos de Selección](https://es.reactjs.org/docs/events.html#selection-events)
-   [Eventos Táctiles](https://es.reactjs.org/docs/events.html#touch-events)
-   [Eventos de la Interfaz de Usuario](https://es.reactjs.org/docs/events.html#ui-events)
-   [Eventos de la Rueda del Ratón](https://es.reactjs.org/docs/events.html#wheel-events)
-   [Eventos de Medios](https://es.reactjs.org/docs/events.html#media-events)
-   [Eventos de Imagen](https://es.reactjs.org/docs/events.html#image-events)
-   [Eventos de Animación](https://es.reactjs.org/docs/events.html#animation-events)
-   [Eventos de Transición](https://es.reactjs.org/docs/events.html#transition-events)
-   [Otros Eventos](https://es.reactjs.org/docs/events.html#other-events)

