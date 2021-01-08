# CSS
[Curso Dalto de CSS](https://youtu.be/OWKXEJN67FE)

## Index:
### Basicos:

1. [Estructura.](#Estructura)
2. [Selectores.](#Selectores)
3. [Especificidad.](#Especificidad)
4. [Metodología BEM.](#BEM)
5. [Unidades.](#Unidades)
6. [Propiedades de Texto.](#PropiedadesTexto)
7. [Tipografías externas.](#Tipografias)
8. [Normalize.](#Normalize)
9. [Cajas.](#Cajas)
10. [Padding.](#Padding)
11. [Widht y Height.](#WyH)
12. [Box Sizing.](#BoxSizing)
13. [Margin.](#Margin)
14. [Bordes.](#Bordes)
15. [Box Model.](#BoxModel)
16. [Sombras.](#Sombras)
17. [Outline.](#OutLine)
18. [Position.](#Position)
19. [Position Static.](#PositionStatic)
20. [Position Relative.](#PositionRelative)
21. [Z Index.](#ZIndex)
21. [Position Absolute.](#potitionAboslute)
22. [Position Fixed.](#positionFixed)
23. [Position Sticky.](#positionSticky)

### CSS Intermedio:


25. [Display.](#Display)
26. [Overflow.](#Overflow)
27. [Float.](#Float)
28. [Pseudoelementos.](#pseudoElementos)
29. [Pseudoclases.](#pseudoClases)
30. [Objet Fit.](#objetFit)
31. [Objet Position.](#objetPosition)
32. [Cursor.](#Cursor)
33. [Colorización \(ColorName,Hex, RGB/A\).](#colorizacion)
34. [Conceptos Básicos de Responsive.](#conceptoResponsive)
35. [Menu Responsive.](#menuResponsive)
36. [Introducción a Flexbox.](#flexbox)
37. [Conceptos de Flexbox.](#conceptoFlex)
38. [Display Flex.](#displayFlex)
39. [Flex direction.](#flexDirection)
40. [Flex wrap.](#flexwrap)
41. [Alineación en Flex.](#alineacionFlex)
42. [Flow Grow.](#flowGrow)
43. [Flex Basis.](#flexBasis)
44. [FLex Shrink.](#flexShrink)
45. [Order.](#oder)
46. [Formulario con Flex.](#formularioFlex)
47. [Conceptos de Grid.](#conceptosGrid)
48. [Display Grid.](#displayGrid)
49. [Grid Templates.](#gridTemplates)
50. [Medidas especiales de Grid.](#medidasGrid)
51. [Grid Gap.](#gridGap)
52. [Asignación de espacios.](#asigancionEspacios)
53. [Repeat\(\).](#Repeat)
54. [Grid Implícito y Explícito.](#gridImplicito)
55. [Grid Auto.](#gridAuto)[Grid Dinámico.](#gridDinamico)
56. [Galería en Grid.](#galeriaGrid)
57. [Grid Areas.](#gridAreas)
58. [Nombrar Grid Lines.](#nombrarGridLines)
59. [Grid Shorthands.](#gridShortHands)
60. [Responsive Design.](#responsiveDesign)
61. [Estructura Responsive Básica.](#estructuraResponsiveBasica)  

### CSS Avanzado:  

62. [Transition.](#Transition)
63. [Animaciones.](#Animaciones)
64. [Cubic Bezier.](#cubicBezier)
65. [Transform.](#Transform)
66. [Clip Path.](#clipPath)
67. [Background.](#Bacground)
68. [Variables.](#Variables)
69. [Filtros.](#Filtros)
70. [Práctica con Filter.](#practicaConFilter)
71. [Direction.](#Dierction)
72. [Letter Spacing.](#letterSpacing)
73. [Scroll Behavior.](#scrollBehavior)
74. [User Selected.](#userSelected)
   
***   
    
## Basicos:

<a name="Estructura"></a>   
### 1. [Estructura.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=1075s)
```css
selector{
	propiedad: valor;
	}
```
<a name="Selectores"></a>   
### 2. [Selectores.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=1226s)  
```html
<h1>Mi primer titulo editado en CSS</h1>
<h2 class="titulo-h2">Mi primer h2 con CSS</h2>
<h2 id="id-h2">Otro titulo h2</h2>
<p>Lorem ipsum dolor, sit amet consectetur adipisicing </p>
<div>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing </p>
</div>
```
```css
/* Selector Universal */
* {
    color: blue;
}

/* Selector de tipo (h1, parrafos, botones, inputs, etc */

h1 {
    color: red;
}
p {
    color:aqua;
}
/* Selector por clases */
.titulo-h2{
    color:bisque;
}
/* Selector por ID */
#id-h2{
    background-color: red;
}
/* Selector por atributo, en este caso el atributo es creado */
[rancio="siRancio"]{
    color: white;
    background-color: blue;
}
/* Por descendiente*/ 
/* en este ejemplo seleccionamos a los elementos
p que estan dentro de un div */
div p{
    color:brown;
}
/*en este ejemplo seleccionamos a los p que estan dentro de un div
pero son de la clase=parrafoEspecial
Nota: para las clases se pone el elemento que contien a la clase y luego 
la clase, o simplemente la clase*/
div p.parrafoEspecial{ 
    color:black;
}
/* Selector por pseudoClases, como active, hover. Eventos de las selecciones */
p:hover{
    background-color:red;
    color: black;
}	
```
<a name="Especificidad"></a>   
### 3. [Especificidad.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=2397s)
* La especificidad es la manera mediante la cual los navegadores deciden qué valores de una propiedad CSS son más relevantes para un elemento y, por lo tanto, serán aplicados. La especificidad está basada en las reglas de coincidencia que están compuestas por diferentes tipos de selectores CSS.[más info](https://developer.mozilla.org/es/docs/Web/CSS/Especificidad). El orden de mayor a menor importancia:
	1. !Importat
	2. Estilo en linea.
	3. Identificadores.
	4. Clases, pseudo-clases y los atributos.
	5. elementos y los pseudo-elementos.  
	 **Nota: los pseudo elementos se reconocen porque van precedidos de dos(2) :: y las pseudo-clases solo de uno (1) :**   
	 
	 ```css
	 /* Ejemplo de como usar el !important 	*/
	.titulo-h2{
    color: black;
    background-color:red;
	}
	h2 {
    color:yellow;
    background-color:aqua !important;
	}
	/* El estilo de clase tiene mayor rango 	que la de
	elemento, pero al usar el !important, 	el estilo que
	domina es este. */
	 ```

<a name="BEM"></a>   
### 4. [Metodología BEM.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=3153s)
 Modificador de Bloques de Elementos (del ingles Block Element Modifier BEM).**BEM** es una metodología que usaremos para nombrar y clasificar selectores CSS de manera estricta, transparente e informativa.
[más info](https://blog.interactius.com/metodolog%C3%ADa-css-block-element-modifier-bem-f26e69d1de3)
<a name="Unidades"></a>   
### 5. [Unidades.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=3545s)
Más informacion en mozilla developer: [más info](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/Valores_y_unidades_CSS#Longitudes)

* Fijas o absolutas:
	No son relativas a nada más, generalmente son del mismo tamaño:   
	
| Unidad  | Nombre  				| Equivale a.        |
|---      |---						|---	              |
| cm 		| Centímetros				| 1cm = 96px/2,54    |
| mm 		| Milímetros				| 1mm = 1/10 de 1cm  |
| Q  		| Cuartos de milímetros	| 1Q = 1/40 de 1cm   |
| in 		| Pulgada 				| 1in = 2,54cm = 96px|
| pc 		| Picas					| 1pc = 1/16 de 1in  |
| pt 		| Puntos					| 1pt = 1/72 de 1in  |
| px 		| Píxeles					| 1px = 1/96 de 1in  |
	
* Relativas.  

1 em por defecto es 16px
 
| Unidad | Relativa a                                                                                                                                                                        |
|:------:|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   em   | Tamaño de letra del elemento padre, en el caso de propiedades tipográficas como font-size, y tamaño de la fuente del propio elemento en el caso de otras propiedades, como width. |
|   ex   | Altura x de la fuente del elemento.                                                                                                                                               |
|   ch   | La medida de avance (ancho) del glifo "0" de la letra del elemento.                                                                                                               |
|   rem  | Tamaño de la letra del elemento raíz.                                                                                                                                             |
|   lh   | Altura de la línea del elemento.                                                                                                                                                  |
|   vw   | 1% del ancho de la ventana gráfica.                                                                                                                                               |
|   vh   | 1% de la altura de la ventana gráfica.                                                                                                                                            |
|  vmin  | 1% de la dimensión más pequeña de la ventana gráfica.                                                                                                                             |
|  vmax  | 1% de la dimensión más grande de la ventana gráfica.                                                                                                                              |

<a name="PropiedadesTexto"></a>   
### 6. [Propiedades de Texto.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=4140s)   

```css
.contact-form__h1 {
    /* aqui 1 em es de 20px que es
    el tamaño que viene de la caja contenedora */

    /* tamaño */
    font-size: 2em;
    /* Tipo de letras */
    font-family: Georgia;
    /* Lo que ocupa la caja que contiene la letra, a lo alto */
    line-height: 1.5;
    /* El grosor de cada letra */
    font-weight: 400;
    
}
``` 

Para más detalle u otras opciones en [más info](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals)

<a name="Tipografias"></a>   
### 7. [Tipografías externas.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=4460s)
Para incluir tipografia diferentes se puede usar las de [google](https://fonts.google.com/). En la cabecera del HTML se incluye la tipografia y en CSS se llama a la seleccionada.
   
```html
<link rel="preconnect" href="https://fonts.gstatic.com">
<link href="https://fonts.googleapis.com/css2?family=Redressed&display=swap" rel="stylesheet">
```   

```css
font-family: 'Redressed', cursive;
```   

<a name="Normalize"></a>   
### 8. [Normalize.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=4698s)  
* Se utiliza el normalize para unificar todos los navegadores, entre ellos existen diferencias en el padding y otras propiedades.
[aqui descarga](https://necolas.github.io/normalize.css/) el archivo normalize.   

<a name="Cajas"></a>   
### 9. [Cajas.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=5110s)   
* Bloques: Siempre se ajustan al tamaño, a lo ancho, de la caja que la contiene.
* Linea: Se ajustan al tamaño del contenido del elemento.   

**Nota:** Utilizando la propiedad display se utiliza para cambiar el comportamiento, por ejemplo:   

```css
h2 {
	display: inline;
	height: 400px; /* A los elementos en linea no se aplica height */
```
<a name="Padding"></a>   
### 10. [Padding.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=5597s)
   
   Es la distancia entre el texto y el borde de la caja, es una propiedad resumida, es decir, puedo resumir:
   
   ```css
   padding: 10px 20px 30px 40px;
   /* top=10px derecha=20px 
   	abajo= 30px e izquierda= 40px */
   ```
 


<a name="WyH"></a>   
### 11. [Widht y Height.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=5947s) 
* El ancho y largo de las cajas.   

<a name="BoxSizing"></a>   
### 12. [Box Sizing.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=5966s)  
* box-sizing: content-box;   
Aqui el tamaño de la caja se ve afectado por el padding, margin y border. 
   
   ```css 
   h3 {
	    background-color:red;
	    display:inline-block; /* Inline, pero acepta las propiedades block */
	    padding: 10px 50px;
	    height:100px;
	    width:100px;
	    box-sizing:content-box;
	    /* aqui el ancho de la caja son 100px del widht + 50px de padding 
	    derecha + 50px padding izquierda => total de 200px*/
}
   ``` 
* box-sizing: border-box;    
Del ejemplo anterio si utilizamos la opcion de border-box, la caja va a mantener el valor del width y no le suma los padding.  

<a name="Margin"></a>   
### 13. [Margin.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=6113s)
* Es la distancia entre las cajas, es el borde exterior.

<a name="Bordes"></a>   
### 14. [Bordes.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=6250s)  

Más información [aqui](https://www.w3schools.com/css/css_border.asp) 

<a name="BoxModel"></a>   
### 15. [Box Model.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=6423s)   
![Drag Racing](assets/box.png)  

<a name="Sombras"></a>   
### 16. [Sombras.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=6581s)
* Box-shadow: [más info](https://developer.mozilla.org/es/docs/Web/CSS/box-shadow)   

```css
/* Sintaxis:
/* Keyword values */
box-shadow: none;

/* offset-x | offset-y | color */
box-shadow: 60px -16px teal;

/* offset-x | offset-y | blur-radius | color */
box-shadow: 10px 5px 5px black;

/* offset-x | offset-y | blur-radius | spread-radius | color */
box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);

/* inset | offset-x | offset-y | color */
box-shadow: inset 5em 1em gold;

/* Any number of shadows, separated by commas */
box-shadow: 3px 3px red, -1em 0 0.4em olive;

/* Global keywords */
box-shadow: inherit;
box-shadow: initial;
box-shadow: unset;
```
* text-shadow: [más info](https://developer.mozilla.org/en-US/docs/Web/CSS/text-shadow)

<a name="OutLine"></a>   
### 17. [Outline.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=6932s)
Es igual que el border, pero no es real, no ocupa espacio en el DOM. Es un shorthand, [aqui más info](https://developer.mozilla.org/en-US/docs/Web/CSS/outline).   

```css
/* style */
outline: solid;

/* color | style */
outline: #f66 dashed;

/* style | width */
outline: inset thick;

/* color | style | width */
outline: green solid 3px;
```

<a name="Position"></a>   
### 18. [Position.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=7528s)
Se utiliza para posicionar objetos en el DOM, y al posicionar el objeto adquiere cuatro (4) propiedades: Top, Right, left, botton y el Z-Index. [más info](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Positioning)   

<a name="PositionStatic"></a>   
### 19. [Position Static.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=7616s)   
Es el valor por defecto y se considera que no esta posicionada.   

<a name="PositionRelative"></a>   
### 20. [Position Relative.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=7699s)

Se posiciona pero conserva su espacio en el DOM. **Nota:** Las propiedades TOP y LEFT son las más importantes y dominan a las otras dos (2)
<a name="ZIndex"></a>   
### 21. [Z Index.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=8036s)   
Ordena los elementos en el eje Z, que es el eje  de profundidad de la pantalla. A mayor el número mas adelante se muestra.   

**Nota:** La recomendación es colocar los Z-Index es de 50 en 50 para poder ajustar elementos en medio, es decir, dar espacio para ajustar luego de crearlos.

####Conflicto de hijos y padres del Z-Index:
La unica forma del que el hijo este abajo del padre, es que tenga z-index:-1 y el padre no tener z-index.

```css
.contenedor{
    width:300px;
    height:300px;
    background:blue;
    margin: 80px;
    position: relative; 
}
.hijo {
    background:orange;
    width:120px;
    height:120px;
    position: relative;
    top: -20px;
    left: -20px;
    z-index: -1;
}
```

<a name="potitionAboslute"></a>   
### 21. [Position Absolute.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=8590s) 

Con el position absolute no reserva el espacio y el punto de referencia que se mueve es el contenedor o el viewport...En el relative, era desde su posicion inicial.

**Nota:** Al tener el absolute, el tamaño de la caja se ajusta al contenido, aunque el elemento sea block.

Toma de referencia el view port, a menos que el contenedor este posicionado y ahi, si se puede hacer referencia absoluta respecto al contenedor.

  
<a name="positionFixed"></a>   
### 22. [Position Fixed.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=9577s)   

Igual que el absolute, pero se queda fijado. Utilizado para la publicidad, que queda fija pero lo demas cambia.   

<a name="positionSticky"></a>   
### 23. [Position Sticky.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=9868s)   

Es una mezcla entre relative y el fixed. Se reserva el espacio en el DOM y se define en que momento va ha estar fijo
   
   
## CSS Intermedio:


<a name="Display"></a>   
### 25. [Display.](#)   
* Block.
* Inline.
* InlineBlock.
* Flex.
* Grid.
* InlineFlex.
* InlineGrid.  


<a name="Overflow"></a>   
### 26. [Overflow.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=10530s)   
 Cuando un texto sobrepasa al contenedor, el overflow es la propiedad para tratar estos casos.
 
 Esta propiedad es un shorthand, para [más info](https://developer.mozilla.org/es/docs/Web/CSS/overflow) de los valores, ejemplos y propiedades CSS relacionadas.
 
 

<a name="Float"></a>   
### 27. [Float.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=10926s)   
Es una propiedad de CSS que ubica un elemento al lado izquierdo o derecho de su contenedor, permitiendo a los elementos de texto y en linea aparecer a su costado. El elemento es removido del normal flujo de la pagina, aunque aún sigue siendo parte del flujo.

En la actualidad se utiliza para colocar texto de envuelva a la imagen, utilizado para articulos y blogs, para [más info](https://developer.mozilla.org/es/docs/Web/CSS/float)   

<a name="pseudoElementos"></a>   
### 28. [Pseudoelementos.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=11419s)  
Son elementos que no forman parre del DOM, pero si se ven los resultados, igual que el outline. Para [más info](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements) y son elementos inline:   

* ::first-line.
* ::first-letter.
* ::placeholder.
* ::selctor.
* ::after.(Hijos y necesitan content y son inline)
* ::before.(Hijos y necesitan content y son inline)

**NOTA:** Los pseudo-elementos que tienen la propiedad ***content*** no forman parte del DOM, como por ejemplo ::after y ::before, entonces no pueden ser seleccionadas.


<a name="pseudoClases"></a>   
### 29. [Pseudoclases.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=12245s)   

Una pseudoclase CSS es una palabra clave que se añade a los selectores y que especifica un estado especial del elemento seleccionado. Por ejemplo,  :hover aplicará un estilo cuando el usuario haga hover sobre el elemento especificado por el selector. Para [más info](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes) y algunas pseudo-clases son:   
* :hover.  
* :link. Cambia las propiedades de un link que no hemos visitado.
* :visited. Cambia las propiedades de un link que ya hemos visitado.
* :lang()


<a name="objetFit"></a>   
### 30. [Objet Fit.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=13422s) 
  
La propiedad object-fit indoca como el contenido de un elemento externo, por ejemplo una imagen o un video, deberia redimensionarse para ajustarse a su contenedor...[más info](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit) de los posibles valores:   
* Contain.  
* Cover.  
* Fill.  
* one.  
* Scale-down.

<a name="objetPosition"></a>   
### 31. [Objet Position.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=13955s)  
La propiedad object-position determina el alineamiento del elemento dentro de la caja.<position>, este es un valor de cuatro que representa una posición en 2D con respecto a los bordes de la caja.   

```css
/* left - Right - Top - Button */
object-position: 10px;

/* Puede ser px - em - % - etc */
```

<a name="Cursor"></a>   
### 32. [Cursor.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=14038s)   

La propiedad CSS:cursor especifica el tipo de cursor que se mostrara cuando este se encuentre sobre un elemento. Para ver los posibles valores [más info.](https://developer.mozilla.org/es/docs/Web/CSS/cursor#values) 

<a name="colorizacion"></a>   
### 33. [Colorización \(ColorName,Hex, RGB/A\).](https://www.youtube.com/watch?v=OWKXEJN67FE&t=14191s)

Hay varias formas de indicar los colores:   
* Por el nombre. El navegador interpreta el color y coloca el color, pero hay diferencias entre navegadores.
* RGB (Red-Rojo, Green-Verde, Blue-Azul). Las medidas van del cero(0) al 255, cero(0) es nada y 255 lo maximo.   

```css
/* Negro */
background: rgb(0,0,0);
/* Blanco */
background: rgb(255,255,255);
/* Rojo + Verde  = Amarillo una excepsion */
background: rgb(255,255,0);

```
* RGBA. Es una variacion de RGB y el A es alfa o % de opacidad.    

```css
/* Negro */
background: rgb(0,0,0,.2);
/* Blanco */
background: rgb(255,255,255,.3);
/* Rojo + Verde  = Amarillo una excepsion */
background: rgb(255,255,0,.5);

```
* Hexadecimal. Es la misma base que el RGB pero son en base a 16, es decir, del cero(0) al f.   

Puede estar en base a 3 digitos, por ejemplo: #000 seria el minimo o negro y #fff seria el blanco.    
Puede estar en base a 6 digitos, por ejmplo:
\#000000 seria negro y \#ffffff blanco y \#ff0000 rojo puro.


<a name="conceptoResponsive"></a>   
### 34. [Conceptos Básicos de Responsive.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=14993s)  

Es adaptar la paguina a diferentes resoluciones, lo recomendado es hacer las paguinas Firts Mobile, es decir, diseñar primero para moviles y luego para mayores tamaños.

<a name="menuResponsive"></a>   
### 35. [Menu Responsive.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=15505s)
<a name="flexbox"></a>   
### 36. [Introducción a Flexbox.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=17204s)  

El Módulo de Caja Flexible, comúnmente llamado flexbox, fue diseñado como un modelo unidimensional de layout, y como un método que pueda ayudar a distribuir el espacio entre los ítems de una interfaz y mejorar las capacidades de alineación


<a name="conceptoFlex"></a>   
### 37. [Conceptos de Flexbox.](#)
  
**El flexbox tiene dos ejes:**   

1. Main Axis (Eje Principal). Esta controlado por la propiedad flex-direction.  
2. Cross Axis(Eje Cruzado). Va perpendicular al main axis.
   
<a name="displayFlex"></a> 
### 38. [Display Flex.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=17603s)   

**El contenedor flex:** Un área del documento que contiene un flexbox es llamada contendedor flex. Para crear un contenedor flex, establecemos la propiedad del área del contenedor display como flex o inline-flex. Tan pronto como hacemos esto, los hijos directos de este contenedor se vuelven ítems flex. Las propiedades del contenedor flex son:   
* **flex-direction.**   
* **flex-wrap.**   
* **flex-flow.** Es un shorthand de flex-direction y flex-wrap.   
   
       
<a name="flexDirection"></a>   
### 39. [Flex direction.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=17834s)   

La propiedad CSS flex-direction especifica cómo colocar los objetos flexibles en el contenedor flexible definiendo el eje principal y la dirección (normal o al revés). Valores:   
* **row.** Valor por defecto y muestra los elementos en fila, comenzando de izquierda a derecha.   
* **row-reverse.** Muestra los elementos en fila, pero empezando de derecha a izquierda.   
* **column.** Muestra los elementos en columna de arriba hacia abajo.   
* **column-recerse.** La dirección es de abajo hacia arriba.

<a name="flexwrap"></a>   
### 40. [Flex wrap.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=18115s)   

La propiedad flex-wrap de CSS  especifica si los elementos "hijos" son obligados a permanecer en una misma línea o pueden fluir en varias líneas. Si la cobertura (wrap) está permitida, esta propiedad también te permite controlar la dirección en la cual serán apilados los elementos. Valores:   
* **nowrap.** Valor por defecto.   
* **wrap.**  
* **wrap-reverse.**
   
   
   **Nota:** Si le doy un widht:100%, los elementos se comportan como bloque.   
   **Nota:** Utlizando la propiedad min-width controlo el ancho minimo del contenedor.   
   
   <a name="alineacionFlex"></a>   
### 41. [Alineación en Flex.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=18380s)  

Los flex-box tienen propiedades que controlan la alineación de las cajas y sus contenidos, y estas son:   

* **justify-content.** Controla la alineación de todos los elementos en el eje principal.. Valores:   
	- flex-start:   
	- flex-end:   
	- center:   
	- space-between:   
	- space-around: Deja el mayor espacio posible.   
	- space-evenly: Deja el mismo espacio entre las cajas y el contenedor.   
	
	
*  **align-items**. Controla la alineación de todos los elementos en el eje transversal. Posibles valores:   
	- Normal.
	- flex-start.
	- flex-end.
	- center.
	- start.
	- end.
	- baseline.
	- stretch. Valor por defecto.      
    
*  **align-content**. Descrito en la especificación como para "empaquetar líneas flexibles"; Controla el espacio entre las líneas de flexión en el eje transversal.   

La propiedad **flex** es un [shorthand](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties) y son propiedades de los item flexibles. Hasta ahora hemos visto las propiedades del contenedor: [más info](https://developer.mozilla.org/en-US/docs/Web/CSS/flex)  
    
   * **align-self**. Controla la alineación de un elemento flexible individual en el eje transversal.    
   * **flex-grow.**   
   * **flex-shrink.**   
   * **flex-basis.**

<a name="flowGrow"></a>   
### 42. [Flow Grow.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=19270s)   

Reparte el espacio que sobra del contenedor y los reparte entre los los flex items si se lo asignamos a todos los item o podemos asignarle esta propiedad a un solo elemento.

<a name="flexBasis"></a>   
### 43. [Flex Basis.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=19547s)  

Es como la propiedad width, pero es más importante, le da prioridad al flex-basis.

<a name="FLexShrink"></a>   
### 44. [FLex Shrink.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=19649s)   

La propiedad CSS flex-shrink especifica el factor de contracción de un flex item.

<a name="oder"></a>   
### 45. [Order.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=20175s)   

Es como el Z-index, pero en el eje que apunta el main axis.

<a name="formularioFlex"></a>   
### 46. [Formulario con Flex.](https://www.youtube.com/watch?v=OWKXEJN67FE&t=20422s)   

Lucas hace una practica de crear un formulario utilizando flex-box. En esta guía, [más Info](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Flexible_Box_Layout/Casos_de_uso_tipicos_de_Flexbox.) , se muestran algunos de los casos de uso comunes de flexbox, en aquellos lugares donde tiene más sentido que otro método de diseño.

<a name="conceptosGrid"></a>   
### 47. [Conceptos de Grid.](#)
<a name="displayGrid"></a>   
### 48. [Display Grid.](#)
<a name="gridTemplates"></a>   
### 49. [Grid Templates.](#)
<a name="medidasGrid"></a>   
### 50. [Medidas especiales de Grid.](#)
<a name="gridGap"></a>   
### 51. [Grid Gap.](#)
<a name="asigancionEspacios"></a>   
### 52. [Asignación de espacios.](#)
<a name="Repeat"></a>   
### 53. [Repeat\(\).](#)
<a name="gridImplicito"></a>   
### 54. [Grid Implícito y Explícito.](#)
<a name="gridDinamico"></a>   
### 55. [Grid Auto.](#gridAuto)[Grid Dinámico.](#)
<a name="galeriaGrid"></a>   
### 56. [Galería en Grid.](#)
<a name="gridAreas"></a>   
### 57. [Grid Areas.](#)
<a name="nombrarGridLines"></a>   
### 58. [Nombrar Grid Lines.](#)
<a name="gridShortHands"></a>   
### 59. [Grid Shorthands.](#)
<a name="responsiveDesign"></a>   
### 60. [Responsive Design.](#)
<a name="estructuraResponsiveBasica"></a>   
### 61. [Estructura Responsive Básica.](#)  

## CSS Avanzado:  

<a name="Transition"></a>   
### 62. [Transition.](#)
<a name="Animaciones"></a>   
### 63. [Animaciones.](#)
<a name="cubicBezier"></a>   
### 64. [Cubic Bezier.](#)
<a name="Transform"></a>   
### 65. [Transform.](#)
<a name="clipPath"></a>   
### 66. [Clip Path.](#)
<a name="Bacground"></a>   
### 67. [Background.](#)
<a name="Variables"></a>   
### 68. [Variables.](#)
<a name="Filtros"></a>   
### 69. [Filtros.](#)
<a name="practicaConFilter"></a>   
### 70. [Práctica con Filter.](#)
<a name="Dierction"></a>   
### 71. [Direction.](#)
<a name="letterSpacing"></a>   
### 72. [Letter Spacing.](#)
<a name="scrollBehavior"></a>   
### 73. [Scroll Behavior.](#)
<a name="userSelected"></a>   
### 74. [User Selected.](#)






