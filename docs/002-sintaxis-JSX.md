# JSX
Es una sintaxis de JavaScript muy parecida al HTML, pero es **azúcar sintáctica** se puede ver la diferencia en el parámetro `className` en vez de `class`, ya que `class` es una palabra reservada, otro ejemplo es `htmlFor` en vez de `for`.

Podemos hacer expresiones, pasar variables y hacer trabajos con JavaScript.

Las etiquetas self closing se deberá cerrar como XML

```
<img src="./img/hello.png" />
```

```
<div className="container" id="hola">
	hola mundo
</div>


React.createElement(
	"div",
	{
		className: "container",
		id: "hola"
	},
	"hola Mundo"
)
```

Recordar que no se permite agregar más de dos o más elementos fuera de un mismo paquete

Se puede utilizar React.Fragment para crear dos elementos adyacentes sin un padre aparente

```
let nombre = "Christian";

<>
	<div className="container" id="hola">
		hola Mundo
	</div>
	<article>{nombre}</article>
</>
```

En caso de no respetar estas leyes, la consola lanzará automáticamente un error y falla la compilación para hacer respetar un desarrollo basado en prácticas limpias.

Es posible aplicar métodos de recorrido de arrays, para generar código tipo lista de forma dinámica al igual que validaciones mediante operadores ternarios:

```
let auth = false;
let estaciones = ['Primavera', 'Verano', 'Otoño', 'Invierno']

<>
	<ul>
		{ estaciones.map((estacion,index) => <li key={index}>{estacion}</li>) }
	</ul>	
	<p>{ auth ? 'El usuario está logeado' : 'El usuario no está logeado' }</p>
</>
```