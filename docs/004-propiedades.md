# Propiedades
Son valores que recibe un componente hijo desde su componente padre. Se agrupan en un objeto llamado **props**. El cual puede recibir diferentes tipos de datos como:

- Strings
- Numbers
- Booleans
- Arays
- Objects
- Functions
- React Elements
- React Components

Las **props** soin inmutables, es decir son valores netamente de **lectura**

App.js
```
<Componente
	message="Hola, soy un Componente funcional expresado desde una prop"
/>
```

Componente.js
```
const Componente = (props) => <h2>{props.message}</h2>
```

Es posible cargar propiedades por defecto internamente, de la siguiente forma:

```
Propiedades.defaultProps = {
	porDefecto: "Las props"
}
```

Si se desea validar el tipo de propiedades, se puede instalar el módulo de prop-types

```
npm i -s prop-types
```

Y se declara de la siguiente forma en el componente

```
import PropTypes from 'prop-types';

Propiedades.propTypes = {
	cadena: PropTypes.string,
	numero: PropTypes.number.isRequired,
	booleano: PropTypes.bool,
	arreglo: PropTypes.array,
	objeto: PropTypes.object,
	elementoReact: PropTypes.element,
	componenteReact: PropTypes.element
};
```