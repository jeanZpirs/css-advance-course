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

## ¿Como funciona CSS?

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

1. ¿Cómo hacer el proceso de cascada para resolver los conflictos?

Toma en cuenta la importancia, luego la especificidad y al final el orden del código escrito.

![How work css cascade](imgs_readme/cascade-work.png)

2. ¿Cómo procesa los valores CSS?

Unidades:

- <strong>%</strong> en tamaño de elemento: los porcentajes lo calcula teniendo en cuenta al ancho del elemento padre.
- <strong>%</strong> en tamaño de fuente: los porcentajes se calculan teniendo en cuenta el tamaño de fuente del elemento padre.
- <strong>em</strong> en tamaño de fuente: Se calcula teniendo en cuenta al elemento padre inmediato.

- <strong>rem</strong>: se calcula teniendo en cuenta el elemento raíz (<hml>).

![How css parsed values](imgs_readme/css-parsed-values.png)

3. Herencia en CSS

Existe propiedades que se heredan en css del elemento padre al elemento hijo, como las propiedades de tipografía. La herencia es bastante intuitiva en CSS por la que no es realmente compleja.

![inheritcence](imgs_readme/herencia.png)

### ¿Cómo CSS renderiza una web?

Después de los de los procesos de CSS viene lo que es el modelo de formato visual CSS, que es un algoritmo que calcula las cajas y determina el diseño de las cajas para cada elemento en el árbol de representación con el fin de determinar el diseño final de la página.

El algoritmo tiene en cuenta los siguientes factores:

- Tamaño de cajas: el modelo de caja
- Tipo de caja: En linea, bloque, en linea y bloque.
- Esquema posicional: flotantes y posicionamientos.
- Apilado de contextos
- Otros elementos del árbol.
- Tamaño del viewport, dimensiones de imágenes, etc.

### Arquitectura CSS, componentes y metodología BEM

¿Cómo debemos pensar en los diseños y como debemos pensar en nuestro código?

Una buena mentalidad a la hora de crear proyectos, es <strong>pensar</strong>, <strong>construir</strong>, <strong>arquitectura</strong>.

Pensar: Antes de construir la página debemos pensar en el diseño.

Para eso podemos usar el principio <strong>component-drive design</strong>, basado en:

- Separar en bloques cada parte de la web.
- Colección de componente unidos para el diseño general de la página.
- Reutilizabas para el proyecto y diferentes proyectos.
- Deben ser independientes.

Construir: Necesitamos una buena estrategia y estructura consistentes para nombrar nuestras clases. Uno de las mejores es el metodo BEM:

- Block Element Modifier
- Block: Componente independiente que es significativo por sí mismo.
- Element: Parte del bloque que no tiene significado por sí mismo.
- Modifier: Una versión diferente del elemento.

Arquitectura:

También debemos tener una buena estructura de carpetas donde estarán nuestros archivos CSS.

Una buena solución sería el patrón 7-1, siete diferentes carpetas y un solo archivo principal.

## Introducción a SASS

SASS es un pre-procesador de CSS, una extensión de CSS que añade funciones y características al lenguaje.

Características que SASS nos da:

- Variables: valores reutilizables como colores, tamaños y espaciados, etc.
- Nesting: Anidamiento de selectores, permitiendo escribir menos código.
- Operadores: Podemos hacer cálculos matemáticos en CSS.
- Imports: Podemos escribir CSS en diferentes archivos y unir todos en un solo archivo.
- Mixins: Podemos escribir código CSS reutilizable.
- Funciones: Similar a los mixins pero este produce un valor que podemos usar.
- Extends: Se pueden usar para hacer que diferentes selectores hereden declaraciones que son comunes a ellos.
- Control de directivas: para escribir codigo complejo usando condicionales y bucles.

### Implementando patron 7 - 1 en SASS

Ayuda muchísimo organizando nuestros archivos SCSS, lo hace mantenible, escalable y mucho mas fácil de leer.

![patron-7-1](imgs_readme/patron7-1.png)

### Color de texto tipo background - background-clip

El fondo se aplica al área de contenido del texto, permitiendo que el fondo se recorte en las formas del texto.

![Background-Clip](imgs_readme/background-clip.png)

### Hover, Not:Hover y Outline

Un truco que podemos hacer para darle reacción a otros elementos cuando pasamos el mouse por encima haciendo `hover`, es aplicar en los demás la pseudoclase `:not(:hover)`.

![trick-hover](imgs_readme/trick-hover.png)

Podemos usar la propiedad `outline-offset` para agregar un espaciado entre el elemento y su `outline`.

![hover-outline](imgs_readme/hover-outline.png)

### Skew en el elemento padre sin afectar los demás

Simplemente podemos aplicar `skew` al elemento padre y darle `skew` contrario a los elementos hijos.

![parent-skew](imgs_readme/parent-skew.png)

### Rotación de 180º a los elementos

Podemos aplicar el siguiente codigo para rotar un elemento.

```
transform: rotateY(180deg);
```

Para eliminar la cara posterior del elemento o dejarlo invisible usamos

```
backface-visibility: hidden
```

Para una rotación con una visualización correcta se le agrega la propiedad `perspective` con una unidad de tamaño grande.

```
perspective: 150rem;
```

### Agregado de efectos o filtro a las imagenes.

Para agregar efectos como cambiado de color, colores negativos, mas contraste, etc, tenemos una propiedad que nos da efectos predefinidos `background-blend-mode`, tiene una buena variedad de efectos y filtros.

### Igualando cajas divididas

A veces tenemos un titulo que se divide en dos linea por poco espacio, este titulo tenia un padding en donde solo se aplica al inicio y al final del texto.

![alt text](imgs_readme/box-break-ex1.png)

Entonces podemos aplicar `box-decoration-break: clone` para que ambos cuadros tomen el padding.

![alt text](imgs_readme/box-break-ex2.png)

### Texto o elemento rodeando otros elementos

Para tener elemento rodeando a otros podemos utilizar las siguientes propiedades:

```
    float: left;
    -webkit-shape-outside: circle(50% at 50% 50%);
    shape-outside: circle(50% at 50% 50%);
```

`float`: para que los elementos alrededor se junten.
`shape-outside` : para darle forma de circulo al contorno o caja del elemento.

### Filtros en las imagenes

Podemos usar la propiedad `filter` para agregar filtro como brillo, blur, opacidad, etc.

### Linear gradient solo a mitad del elemento.

Con el siguiente código podemos agregar un `linear-gradient` que solo se vea por la mitad y ademas de que podemos rotarlo con `deg`.

```
    background-image: linear-gradient(
      105deg,
      rgba($color-white, 0.8) 0%,
      rgba($color-white, 0.8) 50%,
      transparent 50%
    ),
    url("../img/nat-10.jpg");

```

![alt text](imgs_readme/mitad-color.png)

### Formularios

Podemos editar los `inputs` de tipo texto con las propiedades y pseudo clase `placeholder` y `focus`.

Es por el momento dar estilos a los elementos tipo radio, check y select.

Podemos combinarlo con el label que se empareja con los inputs y creando un pseudo-elemento darle la forma que queramos.

### Selector de hermano

Hasta ahora solo vimos seleccionar hijos desde el elemento padre.

Pero ahora con el selector `+` y `~` podemos seleccionar elemento hermanos.

![alt text](imgs_readme/siblings-select.png)

### Cubic Biezer

Podemos agregarla a la propiedad `transition` para poder agregar animaciones de retroceso o aceleración.

![cubic-bezier](imgs_readme/cubic-bezier.png)

### Transform-origin

Es una propiedad que no permite elegir desde que lado del elemento aplicar los efectos del `transform`.

### Media Queries

Existen dos prácticas a la hora de desarrollar una web y hacerla receptiva a cambios de tamaño de pantalla.

- Desktop First - Hacer la página empezando para pc de escritorio.
- Mobile First - Hacer la página empezando para teléfonos.

Con desktop-first aplicamos media queries preguntando si el ancho es `<= 600px?`, menor o igual que el ancho de 600px, entonces sí es verdadero los estilos se pueden aplicar.

Y con mobile-first aplicamos media queries preguntando si el ancho es `>= 600px?`, es mayor o igual que el ancho de 600px, entonces sí es verdadero se aplicaron los estilos.

Podemos preguntarnos que pasa cuando el ancho de pantalla es de 800px, dando como verdadera dos media queries de 600px y 900px, entonces creando conflictos entre estilos pero esto se arregla mediante el orden en el que está escrito el código.

Tenemos que saber en que anchos de pantalla aplicar los media queries, la mejor manera es tomar un ancho que cubra el mayor porcentaje de anchos de pantalla o podemos ver nuestro diseño y a medida que se vaya reduciendo la pantalla ir arreglando los estilos.

### SASS y Media Queries

Gracias a SASS podemos aplicar algunas prácticas para que la codificación sean más sencilla, podemos crear mixins y usar directivas de sass. (@if, @content)

![sass_mediaqueries](imgs_readme/sass_mediaqueries.png)
