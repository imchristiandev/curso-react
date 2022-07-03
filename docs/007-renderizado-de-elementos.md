# Renderizado de elementos
Se puede renderizar una colección de elementos dentro de react recorriendo un array, lo que si debe ser, es que debe producir una key

Se recomienda que se use un identificador único basado en los datos que se presentan, si la api trae un ID usarlo como key automáticamente, en caso de que no sea así usar la llave que traiga el .json a consultar

Aquí un ejemplo en código de cómo se realizar el proceso.

```
export default class RenderizadoElementos extends Component {

constructor(props) {
	super(props);
	this.state = {
		seasons: ["Primavera", "Verano", "Otoño", "Invierno"]
	};
}

render() {
	return (
	<div>
	<h2>Renderizado de elementos</h2>
	<h3>Estaciones del año</h3>
	<ol>
	{
		this.state.seasons.map((season, index) => <li key={season}>{season}</li>)
	}
	</ol>
	<h3>Frameworks Frontend JavaScript</h3>
	<ul>
	{
		data.frameworks.map((el) => <ElementoLista key={el.id} el={el}/>)
	}
	</ul>
	</div>
	)
	}
}
```

```
function ElementoLista (props) {
	return (
		<li>
			<a 
				href={props.el.web} 
				rel="noreferrer" 
				target="_blank"
			>
				{props.el.name}
			</a>
		</li>
	)
}
```