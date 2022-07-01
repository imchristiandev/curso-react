# Renderizado condicional
Es cuando un valor del estado o de las propiedades del componente cambian y obliga a repintar la interface, es por esto que podemos utilizar un operador ternario que sea manipulado por el estado, como el siguiente ejemplo:

```
import React, { Component } from 'react';

function Login() {
	return(
		<div>
			<h3>Login</h3>
		</div>
	)
}

function Logout() {
	return(
		<div>
			<h3>Logout</h3>
		</div>
	)
}

export default class RenderizadoCondicional extends Component {

	constructor(props) {
		super(props);
		this.state = {
			session: true
		}
	}

	render() {
		return (
			<div>
				<h2>Renderizado condicional</h2>
				{ this.state.session ? <Login /> : <Logout /> }
			</div>
		)
	}
}
```