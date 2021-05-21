# Frontend Developer

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
