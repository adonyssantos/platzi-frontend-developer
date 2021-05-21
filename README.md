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
