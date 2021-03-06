# Frontend Developer

El **Frontend** es la parte gráfica de una página web. Es la parte por donde el usuario va a interactuar.

**Proyecto de este curso:** [adonyssantos.me/platzi-video/](http://adonyssantos.me/platzi-video/)

## Table of contents

- [Basic Concepts](#basic-concepts)
- [Favicon](#favicon)
  - [Favicon Generator](#favicon-generator)
  - [Dynamic Favicons](#dynamic-favicons)
- [Semantics](#semantics)
- [Types of selectors, pseudo-classes and pseudo-elements](#types-of-selectors-pseudo-classes-and-pseudo-elements)
  - [Pseudo-clases](#pseudo-clases)
  - [Some tools](#some-tools)
- [Box model](#box-model)
- [Colors](#colors)
- [Fonts](#fonts)
- [Imagenes Random (Unsplash API)](#imagenes)
- [Transition](#transition)
- [Animation](#animation)
- [Arquitectura CSS](#arquitectura-css)
  - [¿Qué son y para qué nos sirven las arquitecturas CSS?](#qué-son-y-para-qué-nos-sirven-las-arquitecturas-css)
    - [Los objetivos son](#los-objetivos-son)
    - [Buenas practicas](#buenas-practicas)
  - [OOCSS, BEM, SMACSS, ITCSS y Atomic Design](#oocss-bem-smacss-itcss-y-atomic-design)
    - [OOCSS (Object Oriented CSS)](#oocss-object-oriented-css)
    - [BEM](#bem)
    - [SMACSS](#smacss)
    - [ITCSS (Inverted Triangle CSS)](#itcss-inverted-triangle-css)
    - [Atomic Design](#atomic-design)
  - [Flexbox vs CSS Grid: ¿Cuál es la diferencia?](#flexbox-vs-css-grid-cuál-es-la-diferencia)
  - [CSS Grid](#css-grid)

## Basic Concepts

- Document Object Model (DOM): [developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
- CSS Object Model (CSSOM): [developer.mozilla.org/en-US/docs/Glossary/CSSOM](https://developer.mozilla.org/en-US/docs/Glossary/CSSOM)
- Render-tree Construction: [developers.google.com/web/fundamentals/performance/critical-rendering-path/render-tree-construction](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-tree-construction)

![](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/images/render-tree-construction.png)

## Favicon

### Favicon Generator

[www.favicon-generator.org](https://www.favicon-generator.org/)

### Dynamic Favicons

For dynamic favicons, we will use favicon-switcher.
You'll only need to add the following lines of code to your site:

```html
<head>
  <link
    rel="icon"
    type="image/svg"
    media="(prefers-color-scheme:light)"
    href="/favicon_light.svg"
  />
  <link
    rel="icon"
    type="image/svg"
    media="(prefers-color-scheme:dark)"
    href="/favicon_dark.svg"
  />
  <script
    src="https://unpkg.com/favicon-switcher@latest/dist/index.js"
    crossorigin="anonymous"
    type="application/javascript"
  ></script>
  <title>Example</title>
</head>
```

![Dynamic Favicons](https://res.cloudinary.com/practicaldev/image/fetch/s--LPeNe99V--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/i/gnyp0jrbbj6hoxzpdq53.png)

## Semantics

```html
<header>
  <a href="#">Home</a>
  <a href="#">Blog</a>
  <a href="#">Contact</a>
</header>
<section>
  <h1>This is a title</h1>
  <p>This is a paragraph</p>
  <img src="#" alt="" />
  <em>Emphasis</em>
  <i>Italic</i>
</section>
<aside></aside>
<footer></footer>
```

# Types of selectors, pseudo-classes and pseudo-elements

\*(asterisco): Es el selector universal. Las propiedades se aplicaran a todos los elementos de nuestro HTML.

Tipo: Son selectores que se aplican a cierto elemento HTML en específico. Las propiedades se aplicaran a la etiqueta que queremos, por ejemplo p, body, html, div, etc.

Clase: Si nuestras etiqueta de HTML tienen un atributo de class podemos usar ese valor o identificador para que los cambios en el CSS afecten únicamente a ese elemento.

ID: Es similar al anterior, si la etiqueta HTML tiene un ID podemos afectar solo ese elemento.

Las Pseudo-clases y Pseudo-elementos nos permiten ser aún más específicos con qué elemento o partes de nuestros elementos deben recibir los estilos.

Para usarlas debemos definir el selector base (por ejemplo, p) seguido de dos puntos y la pseudo-clase que queremos estilizar (por ejemplo: p:first-child). En el caso de los pseudo-elementos debemos usar el dos puntos 2 veces (p::first-letter).

```css
/* Asterisco (universal) */
* {
  margin: 0;
}

/* Tipo */
h1 {
  color: red;
}

/* Clase */
.saludo {
  font-size: 2em;
}

/* ID */
#id {
  border-radius: 20px;
}

/* Pseudo-clases */
p:first-child {
  color: white;
}

p:last-child {
  color: purple;
}

p:nth-child(2n) {
  color: red;
}
```

### Pseudo-clases

```css
p {
  color: yellowgreen;
}

p:first-child {
  color: yellow;
}

p:last-child {
  color: violet;
}

p:nth-child(2n) {
  color: turquoise;
}

p:nth-child(2n + 1) {
  color: tomato;
}
```

### Some tools

- [emojikeyboard.org](https://emojikeyboard.org/)
- [developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)
- [https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)

## Box model

Todos los elementos de HTML tienen un modelo de caja y esta compuesto por 5 elementos: contenido, padding, border, outline, margin.

![Box model](https://cms-assets.tutsplus.com/uploads/users/30/posts/24126/image/boxmodel6.svg)

```css
.box {
  background-color: orange;
  width: 40px;
  height: 40px;
  padding: 40px;
  border: 4px solid teal;
  box-sizing: border-box;
  outline: none;
  margin: 40px;
  content: "";
}
```

## Colors

**Some tools:**

- [picular.co](https://picular.co/Video)
- [paletton.com](https://paletton.com/#uid=1000u0kllllaFw0g0qFqFg0w0aF)
- [coolors.co](https://coolors.co/001514-fbfffe-6b0504-a3320b-e6af2e)
- [cssgradient.io](https://cssgradient.io/gradient-backgrounds/)
- [color.adobe.com](https://color.adobe.com/create/color-wheel)

## Fonts

- [fonts.google.com](https://fonts.google.com/)

## Imagenes

Si necesitas poner imágenes sin descargarlas puedes usar Unsplash, documentación de su API y un ejemplo, es muy simple de usar: [Unsplash Source](https://source.unsplash.com/)

```
https://source.unsplash.com/random
```
Ademas puedes pasarle un parametro como término de busqueda:

```
https://source.unsplash.com/random?movie
https://source.unsplash.com/random?people
```

- [**Documentacion de Unsplash**](https://unsplash.com/developers)

## Transition

- [www.w3schools.com/css/css3_transitions.asp](https://www.w3schools.com/css/css3_transitions.asp)

- [developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)

- [css-tricks.com/almanac/properties/t/transition/](https://css-tricks.com/almanac/properties/t/transition/)

## Animation

- [www.w3schools.com/css/css3_animations.asp](https://www.w3schools.com/css/css3_animations.asp)

- [developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations)

- [css-tricks.com/almanac/properties/a/animation](https://css-tricks.com/almanac/properties/a/animation/)

## Arquitectura CSS

### ¿Qué son y para qué nos sirven las arquitecturas CSS?

#### Los objetivos son:

- **Predecible:** Escribir reglas claras.
- **Reutilizable:** No escribir código redundante.
- **Mantenible:** Que sea fácil de leer y adaptarnos a los estandares.
- **Escalable:** Que pueda crecer facilmente pero sin afectar el rendimiento.

#### Buenas practicas

- Establecer reglas para que el equipo se entienda.
- Explicar la estructura base o dar los fundamentos del proyecto a un nuevo integrante.
- Evitar hojas de estilo muy extensas.
- Tener una buena documentación explicando ciertos aspectos del codigo.

### OOCSS, BEM, SMACSS, ITCSS y Atomic Design

#### OOCSS (Object Oriented CSS)

CSS Orientado a Objetos. Separa el diseño del contenido, así podemos reutilizar nuestro código.

```css
// ejemplo, en vez de para cada elemento una clase.
.globalWidth {
  width: 100%;
}
```

**Referencias:** [www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss](https://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/)

#### BEM

Block Element Modifier. Separa los elementos y los modificadores

```css
.header {
} // bloque
.header__button--red {
} // block, element, modifier
```

**Referencias:** [getbem.com/introduction](http://getbem.com/introduction/)

#### SMACSS

Scalable and Modular Arquitecture for CSS. Arquitectura de css escalable y modular. PAra eso se realizan cinco pasos

1. Dividir nuestro CSS en **Componentes Base**.
2. Definir **Layout**: son los elementos que se utilizan solo una vez. ej. Footer, Header.
3. Definir **Modulos**: son los componentes que se usan mas de una vez.
4. Definir **Estados**: estos estados definen los cambios que existen en nuestros elementos/componentes. ej. Cambio de color cuando hacen hover, etc.
5. Definir **Temas**: separar los temas y sus cambios _(no todas las librerias tienen temas)_.

**Rerferencias:** [smacss.com](http://smacss.com/)

#### ITCSS (Inverted Triangle CSS)

**Triangulo Invertido de CSS:** Lo que nos indica esta metodologia es poder dividir todos nuestros archivos de css en ciertas partes para que no se mezclen.

Triangulo invertido, desde arriba hacia abajo:

- Ajustes
- Herramientas
- Generico
- Elementos
- Objetos
- Componentes
- Utilidades

**Rerferencias:** [www.xfive.co/blog/itcss-scalable-maintainable-css-architecture](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/)

#### Atomic Design

Esta basada en la quimica.

![Periodic Table of the Elements](https://bradfrost.com/wp-content/uploads/2012/11/Screen-Shot-2012-11-13-at-5.15.05-PM.png)

Sedivide de la siguiente manera:

_Atomos < Moleculas < Organismos < Templates < Paginas_

**Rerferencias:** [bradfrost.com/blog/post/atomic-web-design](https://bradfrost.com/blog/post/atomic-web-design/)

La eleccion de la metodologia depende del proyecto y del equipo

**Especificidad:** son los elementos o clases con mayor peso que otros.

**Nota**: No es tan buena practica usar `!important`

## Flexbox vs CSS Grid: ¿Cuál es la diferencia?

[platzi.com/blog/flexbox-vs-css-grid-cual-es-la-diferencia](https://platzi.com/blog/flexbox-vs-css-grid-cual-es-la-diferencia/)

## CSS Grid

![](https://static.platzi.com/media/user_upload/Captura%20de%20pantalla%202019-08-17%20a%20las%2021.30.58-b724dd11-7374-4f61-9d0b-5b905aa9b961.jpg)
