# [Learn CSS](https://web.dev/learn/css/)
<a name="indice"></a>

**NOTA** Estoy son mis apuntes, o mis notas del curso, algo asi como "spreadsheet" para buscar cuando olvide algo.Quizas te sirven de algo y eso me alegraria, pero recuerda que la fuente es (https://web.dev/).

1. [Box Model.](#box_model) Todo lo mostrado por CSS es una caja o box. Entender como funciona el modelo de caja de CSS (Box Model) es la base fundamental de CSS.
2. [Selectors.](#selectors)
3. [The Cascade.](#cascade)
4. [Specificity.](#specificity)
5. [Inherintance.](#inherintance)
6. [Color.](#color)
7. [Sizing Units.](#sizing_units)
8. [Layout.](#layout)
9. [Flexbox.](#flexbox)
10. [Grid.](#grid)
11. [Logical Properties.](#logical_properties)
12. [Spacing.](#spacing)
13. [Pseudo-elements.](#pseudo-elements)
14. [Pseudo-clases.](#pseudo-clases)
15. [Borders.](#borders)
16. [Shadows.](#shadows)
17. [Focus.](#focus)
18. [Z-index and stacking contexts.](#zindex_stacking_contexts)
19. [Functions.](#functions)
20. [Gradients.](#gradients)
21. [Filters.](#filters)
22. [Blend Modes.](#blend_modes)
23. [Conclusion and next Steps.](#conclusion-next-steps)
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>



<a name="box_model"></a>
## Box Model.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>

Lo realmente importante a recordar que todo escrito en CSS, o trabajando con un web como un todo, ***TODO*** lo mostrado es una caja. Sin importar si es una foto o solo un texto: La clave es recordar que todos son cajas.

### Contenido y Tamaños.

Las cajas tienen diferentes comportamientos segun el valor ```display```. El contenido podrian ser mas cajas, imagenes o simplemente texto. De cualquier forma, el contenido se vera afectado por el tamaño de la caja (by default) de forma predeterminada.

* Tamaño Extrinsico (extrinsic sizing). Nosotros controlamos el tamaño.
* Tamaño Intrinsico (intrinsic sizing). El Navegador toma las desiciones basadas en el contenido.

**NOTA: Estan utilizan [code pen](https://codepen.io/) que es una excelente herramienta para probar y mostrar codigos. En las configuraciones utilizarn una importacion a unas clases de CSS de ellos. El codigo funciona sin este enlace, pero se ve mejor usandolo.El enlace los puedes encontrar en "Settings", pero te lo dejo aqui para que lo veas ```<link rel="stylesheet" href="https://codepen.io/web-dot-dev/pen/abpoXGZ.css">```**


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://codepen.io/web-dot-dev/pen/abpoXGZ.css">
</head>
<body>
    <main>
        <div class="wrapper">
          <article class="flow">
            <h1>Extrinsic sizing vs intrinsic sizing</h1>
            <figure class="callout">
              <p>
                Notice that when the box is using <strong>extrinsic sizing</strong>, there’s
                a limit of how much content you can add before it overflows out of the box’s
                bounds. This makes the word, “awesome”, overflow.
              </p>
            </figure>
            <label class="toggle" for="intrinsic-switch">
              <span class="toggle__label">Turn on intrinsic sizing</span>
              <input type="checkbox" role="switch" class="toggle__element" id="intrinsic-switch" />
              <div class="toggle__decor" aria-hidden="true">
                <div class="toggle__thumb"></div>
              </div>
            </label>
            <p class="awesome" data-element="awesome">CSS is awesome</p>
          </article>
        </div>
      </main>
      <script src="scritp.js"></script>
</body>
</html>
```

```css
.awesome {
    text-transform: uppercase;
    font-size: 5rem;
    font-weight: 700;
    line-height: 1;
    border: 5px solid;
    padding: 2rem;
  
    /* The important extrinsic width */
    width: 320px;
  }
  
  .awesome[data-sizing="intrinsic"] {
    width: min-content;
  }
  
  /*
  
  
  Presentational styles 
  */
  .awesome {
    --flow-space: 2rem;
  }
```

```js
const awesome = document.querySelector('[data-element="awesome"]');
const intrinsicSwitch = document.querySelector("#intrinsic-switch");

// Set sizing attribute based on switch
intrinsicSwitch.addEventListener("change", () => {
  awesome.setAttribute(
    "data-sizing",
    intrinsicSwitch.checked ? "intrinsic" : "extrinsic"
  );
});
```

**Explicacion:** Este ejemplo es un poco complejo para demostrar algo sencillo, pues utilizan JS para cambiar un atributo definido por el usuario ```data-sizing="intrinsic"``` para cambiar la propiedad ```width``` al valor ```min-content```,y al darle esta propiedad la caja se comporta de forma intrinsica, es decir, se va el ancho "widht" se va a ajustar minimo al contenido que tenga.


En este ejemplo esta el parrafo ```<p>``` "CSS is awesome" en una caja con dimensiones fijas y definidas. La caja tiene la propiedad ```width``` es decir, tamaño extrinsico, el problema es que la palabra "awesome" es muy grande para las dimensiones que le asignamos.


**NOTA: Cuando el contenido es muy grande para la caja, se llama <u>"overflow"</u> o desbordamiento. Se puede manejar el overflow usando la propiedad ```overflow```.**


### Las areas del modelo de caja.

Las cajas estan compuestas de diferentes areas, y cada una de estas areas tiene una funcion especifica.

![Box Model Areas](https://web-dev.imgix.net/image/VbAJIREinuYvovrBzzvEyZOpw5w1/ECuEOJEGnudhXW5JEFih.svg)  

<a name="selectors"></a>
## Selectors.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="cascade"></a>
## The Cascade.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="specificity"></a>
## Specificity.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="inherintance"></a>
## Inherintance.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="color"></a>
## Color.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="sizing_units"></a>
## Sizing Units.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="layout"></a>
## Layout.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="flexbox"></a>
## Flexbox.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="grid"></a>
## Grid.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="logical_properties"></a>
## Logical Properties.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="spacing"></a>
## Spacing.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="pseudo-elements"></a>
## Pseudo-elements.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="pseudo-clases"></a>
## Pseudo-clases.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="borders"></a>
## Borders.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="shadows"></a>
## Shadows.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="focus"></a>
## Focus.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="zindex_stacking_contexts"></a>
## Z-index and stacking contexts.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="functions"></a>
## Functions.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="gradients"></a>
## Gradients.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="filters"></a>
## Filters.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="blend_modes"></a>
## Blend Modes.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>
<a name="conclusion-next-steps"></a>
## Conclusion and next Steps.<sub><sup><sub><sup>[indice](#indice)</sub></sup></sub></sup>

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

