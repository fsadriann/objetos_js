# objetos_js

# Objeto window

- El objeto window representa una ventana abierta en un navegador.

Si un documento contiene marcos o etiquetas de tipo:
```Javascript 
<iframe>
```
El navegador crea un objeto de ventana para el documento HTML y un objeto de ventana adicional para cada marco.

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
