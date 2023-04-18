Estoy aprendiendo React 2023 con el canal de youtube [midulive](https://www.youtube.com/@midulive)

# [Introduccion](https://www.youtube.com/watch?v=7iobxzd_2wY)

## Definicion de React

- Una biblioteca de JS para construir interfaces de usuario
- Declarativo
- Basado en componentes (Reutilizar el codigo)
- Biblioteca Universa (cliente y servidor)
- FAQs: [Reactjs Wiki](https://www.reactjs.wiki/)
- Es de META (se creo porque era muy dificil armar formularios)

## 7 razones para usar React

- Es el framework mas demandado en el mundo (como minimo igualado con Angular)
- Tambien se puede usar para aplicaciones moviles (React Native)
- Tiene mantenimiento asegurado (se usa constantemente en Meta y tiene un gran comunidad)
- Te va a servir con el resto de framework (conceptos parecidos)
- Futuro prometedor (No para de ir para arriba)
- Tiene su API estable (biblioteca medianamente estable, casi no cambia la sintaxis)
- Tiene una comunidad gigante (todos los dias hay hackatones, siempre hay soporte)

## ¿Por qué React? Creando un botón sin React

### Vanilla

- Recuperamos el boton
- Al hacerle click, tenemos que ejecutar una funcion
    - Recuperar el id del atributo del HTML
    - Llamar a un servivio para actualizar el MG (toggleLike(id))
El codigo es imperativo, le estamos diciendo que tiene que hacer (como hacerlo).
Si tenemo varios botones, hay que recuperar todos los botones. 
Poco reutilizable, poco escalable.

### React Base

El codigo es declarativo, facil de reutilizar. En React todo es un componente
- import ReactDOM from 'https://esm.sh/react-dom@18.2.0/client'
- import React from 'https://esm.sh/react-dom@18.2.0'
- Obtener el div de la app (document.getElementById('app'))
- Crear el root (ReactDOM.createRoot(appDom))
- Para renderizar algo es necesario crear un elemento (React.createElement('button', { "data-id": 123 }, 'Button 1'))
- Para renderizar varios elementos tenemos el Fragment (React.createElement(React.Frgment, null, [button, button2, button3]))
- root.render(app)

### React JSX (La posta)

<React.Fragment>
    <button data-id='123'>Button 1</button>
    <button data-id='234'>Button 2</button>
    <button data-id='567'>Button 2</button>
</React.Fragment>

Se pueden poner expresiones: <p> Hola {name} </p>

## Crea tu primera aplicación con React

- Usaremos [Vite](https://vitejs.dev/)
- Un componente es un funcion que devuelve un elemento
- Los componentes tienen que ser PascalCase para que no se confunda con futuros HTML
- La base de la reutilizacion son las PROPS (deberian ser inmutables)
- La expresion solo se evalua cuando estan entre {}
- Tratar de no utilizar mb (usar el estilo de separacion en un contenedor)
- El children es todo lo que se envuelve con el componente (nunca usar como props)
- {... midudev} pasa sus campos como prop (es medio mala practica)

### Componente vs Elemento

- Componentes: Una factoria de elementos (funcion que devuelve elementos)
- Elemento: Es lo que renderiza React

### Estado

- React hace una foto de lo renderizado y compara con los cambios de estado (solo hace los minimos)
- Cuando hay un cambio de estado se renderizan sus hijos si o si (por eso conviene hacer los cambios de estado donde se debe)
- Si la prop se usa para inicializar el estado usamos -> initialIsFollowing (no se reinicializa cada vez que cambio el estado)
- Siempre que renderizamos una lista de elementos debemos renderizar la key (identificador unico para ese elemento). Utilizar algo que es unico del elemento
