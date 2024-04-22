# objetos_js

# Objeto window

El objeto `window` representa la ventana que contiene un documento DOM; la propiedad document apunta al DOM `document` cargado en esa ventana. El objeto window al que pertenece un documento puede ser obtenido usando la propiedad `document.defaultView.`

Esta sección proporciona una pequeña referencia a todos los métodos, propiedades y eventos disponibles a través del objeto DOM `window`. El objeto `window` implementa la interfaz `Window` , que a su vez hereda de la interfaz `AbstractView`. Algunas funciones como globales adicionales, espacios de nombres, interfaces, y constructores no típicamente asociados con el objeto window pero disponibles en éste, están listados en las Referencia de JavaScript y en el Referencia DOM de Gecko.

En un navegador con pestañas, como Firefox, cada pestaña contine su propio `window` object (y si está escribiendo una extensión, la ventana del navegador es una ventana separada también - para más información vea Trabajar con ventanas desde el código chrome). Esto significa que el objeto `window` no se comparte entre diferentes pestañas de la misma ventana del navegador. Algunos métodos, como `window.resizeTo` (en-US) y `window.resizeBy` (en-US) se aplican sobre toda la ventana del navegador y no sobre una pestaña específica a la que pertenece el objeto `window`. Generalmente, cualquier cosa que razonablemente no pueda pertenecer a una pestaña, pertenece a la ventana.

## Propiedades del objeto window

| Propiedad | Descripción |
| --------- | ----------- |
| closed    | Devuelve un valor booleano verdadero si se cierra una ventana. |
| console   | Devuelve el objeto de consola para la ventana. |
| defaultStatus| Obsoleto. |
| document  | Devuelve el objeto Documento para la ventana. |
| frameElement|  Devuelve el marco en el que se ejecuta la ventana.  |
| frames    | Devuelve todos los objetos de ventana que se ejecutan en la ventana. |
| history   | Devuelve el objeto Historial de la ventana. |
| innerHeight| Devuelve la altura del área de contenido de la ventana (ventana gráfica), incluidas las barras de desplazamiento. |
| innerWidth | Devuelve el ancho del área de contenido de una ventana (ventana gráfica), incluidas las barras de desplazamiento. |
| length    | Devuelve el número de elementos iframe en la ventana actual |
| closed    | Permite guardar pares clave/valor en un navegador web. |
| localStorage|  Almacena los datos sin fecha de caducidad.  |
| location  | Devuelve el objeto Ubicación de la ventana. |
| name      | Establece o devuelve el nombre de una ventana. |
| navigator | Devuelve el objeto Navigator para la ventana. |
| opener    | Devuelve una referencia a la ventana que creó la ventana. |
| outerHeight| Devuelve la altura de la ventana del navegador, incluidas las barras de herramientas/barras de desplazamiento. |
| outerWidth| Devuelve el ancho de la ventana del navegador, incluidas las barras de herramientas/barras de desplazamiento. |
| pageXOffset |  Devuelve los píxeles en los que se ha desplazado el documento actual (horizontalmente) desde la esquina superior izquierda de la ventana.  |
| pageYOffset |  Devuelve los píxeles en los que se ha desplazado el documento actual (verticalmente) desde la esquina superior izquierda de la ventana.  |
| parent |Devuelve la ventana principal de la ventana actual. |
| screenLeft | Devuelve el objeto Pantalla para la ventana. |
| screenTop | Devuelve la coordenada horizontal de la ventana relativa a la pantalla. |
| screenX |  Devuelve la coordenada vertical de la ventana relativa a la pantalla.  |
| screenY |  Devuelve la coordenada horizontal de la ventana relativa a la pantalla.  |
| sessionStorage | Permite guardar pares clave/valor en un navegador web. Almacena los datos de una sesión.|
| scrollX |  Un alias de pageXOffset  |
| scrollY |  Un alias de pageYOffset  |
| self   | Devuelve la ventana actual |
| status   |  Obsoleto. Evite usarlo. |
| top   | Devuelve la ventana superior del navegador. |

## Ejemplo

```Javascript
    // Obtener información de la ventana y mostrarla en el párrafo
    const informacion = document.getElementById('informacion');
    informacion.innerHTML = `
      <ul>
        <li>URL actual: ${window.location.href}</li>
        <li>Título de la página: ${document.title}</li>
        <li>Ancho de la ventana: ${window.innerWidth} px</li>
        <li>Alto de la ventana: ${window.innerHeight} px</li>
        <li>URL del navegador: ${window.navigator.userAgent}</li>
      </ul>
    `;

    // Abrir una nueva ventana emergente
    function abrirNuevaVentana() {
      window.open('https://www.google.com/', 'Nueva ventana', 'width=400,height=300');
    }

    // Cambiar el título de la página
    function cambiarTitulo() {
      window.document.title = 'Nuevo título';
    }
```
# Explicación

1. Obtener info de la ventana:
    - Se utiliza el objeto `window` para acceder a propiedades como `location.href` (URL actual), `document.title` (título de la página), `innerWidth` (ancho de la ventana) y `innerHeight` (alto de la ventana).
La información obtenida se agrega al contenido HTML del párrafo con ID `informacion`.

2. Abrir una nueva ventana emergente:

- La función abrir`NuevaVentana()` utiliza el método `window.open()` para abrir una nueva ventana.
- Se pasan tres argumentos a `window.open()`:
    - La URL de la página que se abrirá en la nueva ventana.
    - El nombre de la nueva ventana.
    - Las dimensiones de la nueva ventana (ancho y alto).

3. Cambiar el título de la página:

- La función `cambiarTitulo()` utiliza la propiedad `document.title` para cambiar el título de la página actual.

## Ejecución:

1. Abra el archivo HTML en un navegador web.

2. Se mostrará una lista con información sobre la ventana actual (URL, título, dimensiones, etc.).

3. Haga clic en el botón "Abrir nueva ventana" para abrir una nueva ventana emergente con [se quitó una URL no válida].

4. Haga clic en el botón "Cambiar título" para cambiar el título de la página actual a "Nuevo título".

Este es solo un ejemplo básico del uso del objeto window en JavaScript. Hay muchas otras propiedades y métodos disponibles que se pueden utilizar para controlar y obtener información sobre la ventana del navegador.