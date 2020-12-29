[Curso de JAVASCRIPT - Nivel MID LEVEL](https://youtu.be/xOinGb2MZSk)

- [Introduccion a windown](#windown): [ver más informacion](https://developer.mozilla.org/en-US/docs/Web/API/Window)
    




<a name="windown"></a>## Introduccion a windown:
El objeto window representa la ventana que contiene un documento DOM; la propiedad document apunta al DOM document.[ver más informacion](https://developer.mozilla.org/en-US/docs/Web/API/Window)

* Open(): Abre la ventana indicada.
* Close(): Cierra la ventana.
* Close: Pregunta si la ventana abierta o no.
Un ejemplo del uso de los metodos de apertura y cierre:

Html:
```html
<div>
        <label>Abrir ventana de https://</label>
        <input type="text" value="youtube.com" id="ventanaTexto">
        <input type="submit" value="Abrir Ventana" id="abrir" onClick="abrir()"><br>
    </div>
    <div>
        <label>Abrir ventana abierta</label>
        <input type="submit" value="Cerrar Ventana" id="cerrar" onClick="cerrar()"><br>
    </div>
    
    <script src="codigo.js"></script>
```

JS
```js

var ventanaAbierta;
var ventanaActual;

function abrir (){
    const elementoTexto = document.getElementById("ventanaTexto").value;
    paguina = 'https://'+ elementoTexto;
    ventanaAbierta = window.open(paguina);
}

function cerrar() {
    ventanaAbierta.close();
}
```

* Stop(): Detiene la ejecución de carga.
* Alert(): Muestra un ventana emergente con el mensaje.
* Print(): Imprime la paguina.
* Prompt(): Ventana emergente para ingresar datos el usuario. Y devuelve un string.
* Confirm(): Ventana emergente para confirmar, o no, una acción.
* Screen: Es un objeto y podemos acceder a las propiedades.
* ScreenLeft: Devuelve la distancia horizontal entre el borde izquierdo del navegador y el borde del monitor.
* ScreenTop: Igual que screenleft pero con el tope.
* <a name="Scrolllx"></a>Scrollx:
* <a name="Scrolly"></a>Scrolly](#)
* <a name="Scroll"></a>Scroll():
* <a name="Minimize"></a>Minimize():
* <a name="Risize"></a>ResizeBy():
* <a name="MoveBy"></a>MoveBy():
* <a name="MoveTo"></a>MoveTo():
* <a name="Ojetos"></a>Objetos barprpop:](#)
    * <a name="LocationBar"></a>Locationbar:
    * <a name="MenuBar"></a>MenuBar:
    * <a name="PersonalBar"></a>PersonalBar:
    * <a name="ScrolBar"></a>ScrolBars:
    * <a name="StatusBar"></a>StatusBar:
    * <a name="ToolBar"></a>ToolBar:
* <a name="Hereda"></a>Hereda las proppiedades de EventTarget:



















a
a
a
a
a
a
a
<a name="prueba"></a>