# Curso de CSS Avanzado y Sass - Flex-blox, Grid, Animaciones - Inicio: 25/06/2024

## Natours

### Reset correcto de CSS para los navegadores

Los navegadores suelen tener sus propias reglas css y esto genera un inconveniente de no poder crear una web igual para todos los navegadores, entonces se aplica un reset de css para hacer que la web se vea igual en todos los navegadores.

Se usa la siguiente regla css:

![Reset css](/imgs_readme/reset-css.png)

### Definiendo la tipografía para todo el proyecto

Desde un inicio podemos elegir la tipografía, color de texto, tamaño de fuente, grosor de fuente y separación entre lineas desde el selector `body`.

![Init font](./imgs_readme/init-font.png)

### Clip-path

Podemos utilizar esta propiedad CSS para recortar imágenes o dar forma geométrica a nuestro elementos html.

![Clip-path](imgs_readme/clip-path.png)

### Position Absolute

Con esta propiedad css podemos posicionar elementos dentro de un contenedor de forma libre. El elemento que es posicionado sale del flujo apilado de elementos.

![Position Absolute](imgs_readme/position-absolute.png)

### Key-Frames

Podemos añadir animaciones complejas con esta función de CSS. Permiten especificar estados intermedios de una animación a lo largo de su duración.

![keyframes](imgs_readme/keyframes.png)

Forma de aplicar a un elemento dicha animación.

![Animation css property](imgs_readme/animation.png)

`animation-backwards` hace que desde un comienzo el elemento tenga el css del 0% respetando el `animation-delay` para comenzar la animación.

### Pseudo Elementos - Pseudo Clases

Las pseudo-clases son un estado especial de un selector, actuando como condicional.

![Pseudo clases](imgs_readme/pseudo-clases.png)

Los pseudo-elementos son elementos virtuales creados desde css que se posicionan después del elemento al que se le crea, se les puede personalizar como cualquier elemento.

![Pseudo elementos](imgs_readme/pseudo-elementos.png)

### Propiedad transition

Podemos usar transition para que los cambios de css se hagan de forma animada y suave.

### Tres pilares para escribir buen código CSS y HTML.

1. Responsive Design:

Diseños fluidos, media queries, imágenes responsivas, uso de unidades responsivas, practicar desktop first vs mobile first.

2. Código mantenible y escalable:

Código limpio, fácil de entender, escalable, reusable, archivos organizados, nombramientos de clases y buen estructurado del HTML.

3. Rendimiento de una web:

Minimizar la peticiones http, el código, comprimir el código, usar pre-procesadores de css (SASS), minimizar imágenes, comprimir imágenes.

### ¿Cómo funciona CSS detrás de escena?

¿Qué pasa cuando con el código de css cuando carga la página web?

![css-load](imgs_readme/css-load.png)

Cuando el CSS es cargado pasa por 2 procesos o 2 pasos, el procesa de resolver conflictos de declaraciones css y el procesamiento de valores finales en CSS.

Cuando resolvemos conflictos usamos un proceso llamado "Cascada", este proceso se encarga de combinar diferentes estilos resolviendo conflictos entre diferentes reglas CSS que son aplicas a cierto elemento.

¿Cómo hacer el proceso de cascada para resolver los conflictos?

Toma en cuenta la importancia, luego la especificidad y al final el orden del código escrito.

![How work css cascade](imgs_readme/cascade-work.png)
