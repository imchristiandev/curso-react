# Eventos & Binding
El manejo de eventos en React es muy similar a manejar eventos en el DOM. Sin embargo existen algunas diferencias en la sintáxis.

- Los eventos de React se nombran usando un camelCase, en vez de minúsculas
- Con JSX se pasa una función como el manejador del evento, en vez de un string.

Ejemplo. en HTML

```
<button onclick="cambiarIdioma()">Cambiar Idioma</button>
```

Ejemplo en React

```
<button onClick={cambiarIdioma}>Cambiar Idioma</button>
```

Otra diferencia es que en *React* no puedes retornar ***false*** para prevenir el comportamiento por defecto. Se debe retornar explicitamente ***preventDefault***

En componentes de tipo clase, es necesario hacer el binding de métodos, de la siguiente forma:

```
import React, { Component } from 'react';

export default class Eventos extends Component {
	constructor(props) {
		super(props);
		this.state = {
			contador: 0
		};
		this.sumar = this.sumar.bind(this);
		this.restar = this.restar.bind(this);
	}

	sumar(e) {
		this.setState({
			contador: this.state.contador + 1
		});
	}



	restar(e) {
		this.setState({
			contador: this.state.contador - 1
		})
	}

	render() {
		return(
		<div>
		<h2>Eventos en Componentes de clase</h2>
		<nav>
		<button onClick={this.restar}>-</button>
		<button onClick={this.sumar}>+</button>
		</nav>
		<h3>{this.state.contador}</h3>
		</div>
		)
	}
}
```