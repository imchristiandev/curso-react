# Estado
Es el conjunto de variables que va a tener tus componentes y que intervienen en la modificación de dicho componente.

Tiene tres características importantes
- Es inmutable
- No se puede modificar directamente
- Es asíncrono

Para hacer cambios hay que hacer uso del método ***setState()***

Antes de los hooks se debía hacer un componente tipo clase, pero ya no es de esta forma.

```
import React, { Component } from 'react';

function EstadoAHijo(props) {
	return (
		<div>
			<h3>{props.contadorHijo}</h3>
		</div>
	)
}

export default class Estado extends Component {

	constructor(props) {
	super(props);
	this.state = {
		contador: 0,
	}

	setInterval(() => {
		this.setState({
			contador: this.state.contador + 1}
		)
	}, 1000)
}
  
render () {
	return(
		<div>
			<h2>El state</h2>
			<p>{this.state.contador}</p>
			<EstadoAHijo contadorHijo={this.state.contador} />
		</div>
	)
	}
}
```