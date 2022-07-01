# Componentes
Permiten separar el código y los elementos de la interfaz en pequeñas piezas independientes y reutilizables que estarán aisladas unas de otras.

Los componentes pueden o no tener un estado que son variables internas que lo controlen y pueden o no tener propiedades que sirven para recibir valroes.

En react el flujo de los datos funcionan de forma unidireccional, o sea de padres e hijos.

React permite hacer componentes tipo clase y funcional.

Anteriormente sólo se podían usar componentes lógicos dentro de clases, ahora con los Hooks, es posible generar componentes smart.

Se puede generar de tres formas distintas un componente:

Componente de clase (No muy usado en la actualidad):

```
class Componente extends Component {
	render() {
		return <h2>{this.props.message}</h2>
	}
}
```

Componente funcional declarativo

```
function Componente(props) {
	return <h2>{props.message}</h2>
}
```

Componente funcional expresivo

```
const Componente = (props) => <h2>{props.message}</h2>
```