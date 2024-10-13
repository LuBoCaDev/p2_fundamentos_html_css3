# Lucas Borondo Cañizares (@LuBoCaDev) - Desarrollo Web Full Stack XVII
## Práctica 2. Fundamentos HTML5 y CSS 3

### Información a tener en cuenta:
- Se recomienda abrir el Read Me en modo vista previa para facilitar la lectura.
- El objetivo es crear un portafolio personal o de un personaje de ficción usando únicamente HTML5 y CSS3. En mi caso, he decidido hacer un portafolio de los Avengers del Universo Cinematográfico de Marvel y he utilizado la Saga del Infinito como los proyectos de su trayectoria.
- La información ha sido extraída en su mayoría de la wiki del MCU, y las imágenes de múltiples fuentes online.
https://marvelcinematicuniverse.fandom.com/es/wiki/Saga_del_Infinito
- Dado que el proyecto es para un uso exclusivo como práctica de clase, este documento está enfocado a la lectura por parte del profesorado, dividiéndose principalmente en dos secciones que faciliten su comprensión y corrección. Una primera que explica y anota los requisitos punto por punto y en el mismo orden como se solicitan en la práctica incluida en el documento adjunto "Práctica_HTML5yCSS3.pdf". La segunda sección hace una lectura "vertical" de la web explicando paso a paso qué nos podemos encontrar.
- Esta web ha sido desplegada en GitHub Pages, y puede ser visualizada en: https://lubocadev.github.io/p2_fundamentos_html_css3/

---

### Sección primera: Detalles de implementación
---

* #### Header
A la izquierda muestra el logo de los Vengadores. A la derecha encontramos enlaces a los elementos del portafolio, con estado hover suavizado. Algunos se ven en la versión móvil y otros no. El botón de "Recibir más info" va al formulario al final de la página de index y, por tanto, en las otras páginas se ha vinculado con `index.html#formulario`. Tanto estos botones como los del formulario y la página 404 tienen el estado hover suavizado.__*El CSS se puede encontrar en header.css y el de los botones en components.css*__.

* #### Sección con nuestra descripción y barras de habilidades
Se encuentran en el index. La descripción es la parte donde pone "Sobre los Vengadores" y la de las habilidades justo a continuación. Las barras empiezan en color blanco al igual que el color del texto, y a partir del 50% cambian al rojo. __**La animación de las barras se encuentra en spinners.css.**__

* #### Banner con dos imágenes de fondo
En el index. Aunque visualmente el "dibujo" es el mismo, son dos imágenes (archivos) diferentes, que al final es lo que se buscaba. Se ha hecho mediante una media query. __**Se ha estilado en banner.css.**__

* #### Formulario con inputs con tipos correctos y validados
En el index. __**Estilado en form.css y en components.css**__. Los botones usan el mismo estilo que los del header.

* #### Footer
Tiene links externos y, por tanto, se ha tenido en cuenta añadir `target="_blank" rel="noopener noreferrer"`. Esto también se ha tenido en cuenta en el link externo de la página del error 404.  
__**Estilado en footer.css**__.

* #### Video con fade in y auto-play
En total hay dos videos en el proyecto. Uno se encuentra en la sección de Películas (Proyectos) y otro en la página del error 500. El primero no tiene el fade in, solo el auto-play. El segundo lo tiene todo, y además el video empieza más o menos a la mitad.
<p>
Esta decisión la he tomado en base a que personalmente no me parece un efecto muy "elegante" y estéticamente no pegaba con la página de las películas. Sin embargo, en la del error 500, que busca ser más gamberra y mamarracha, sí encajaba más.

* #### Página con grid
El grid se encuentra a la mitad de la página de Películas, en concreto dividiendo las películas entre las 3 fases de la saga. De esta forma, las fases 1 y 2 tienen 6 películas, y la 3 tiene 11, y el grid se adapta bien en ambos casos. Además, las imágenes están animadas para ampliarse al pasar el ratón sobre ellas. __**Tanto el grid como las animaciones se estilan en projects.css.**__
<p>
(Nota: Descargar las 23 portadas, vincular las imágenes en el CSS con su `alt` incluido para que tenga buena semántica, añadirles el `figcaption` y un `p` con el año y director me ha comido mucho tiempo. Tengo intención de añadirles también un link externo a dichas películas en Disney+, pero es algo que también puede llevar mucho tiempo. Por ahora ya he demostrado en otras partes de la web que sé poner links externos, con lo cual, si en el día de entrega siguen sin estar, es que no me ha dado tiempo. Espero que se entienda).

* #### Menú burger
Posiblemente no me dé tiempo, aunque más adelante quiero seguir con este proyecto y reutilizarlo para otros (como por ejemplo, mi portafolio verdadero) y lo aplicaré.

* #### Despliegue en GitHub Pages
¡Por supuesto! Aquí está: https://lubocadev.github.io/p2_fundamentos_html_css3/

* #### Página de error 404
En esta página tenemos centrado y en columna un texto, un link externo con un botón con estilo propio (aunque guardando la estéticaparecida a la de la web), una imagen y otro botón con un estilo nuevo aunque ambos con su hover. __**Estilada en card400.css**__.

* #### Página de error 500
Esta página tiene una imagen de fondo y un texto superpuesto. Además, el video con fade-in y auto-play desciende desde arriba, como se solicita en la práctica, y se va opacando poco a poco, pero no del todo, para que se siga viendo la imagen de fondo. El video empieza más o menos a la mitad, en un momento específico del videoclip. __**Estilada en error500.css**__.

* #### Detalles de implementación
He intentado revisar la semántica y creo que en general no me he dejado nada. En los heads, he tenido en cuenta meter los `meta name="description" content`, el title, y open graphs (que son diferentes en cada caso). He procurado rellenar los `alt` en todos los casos posibles y creo que de manera suficientemente descriptiva. Creo que, en general, las etiquetas header, main, section, footer, h1, etc. no están mal implementadas, al igual que las etiquetas label o `aria-labelledby` en el caso del formulario. Así con todo, seguramente se me escapen algunas cosillas, pero poco a poco me voy dando cuenta cada vez que repaso una y otra vez.
<p>
No hay uso de librerías externas.
<p>
En todo momento he realizado el proyecto con la página abierta con Live Server, inspeccionando con resolución para Mobile L - 425px, para asegurarme de que todo se mostrara de la forma deseada y añadiendo media queries cuando fuera necesario.

* #### Otras consideraciones y apuntes personales
Por ahora nada.
---

### Sección segunda: Descripción de la web
1. Index
2. Películas (proyectos)
3. What if...?
4. Error 404
5. Error 500
6. Elementos comunes
---

* #### Index
En nuestra página principal, lo primero que encontramos es un banner con una imagen de fondo que cambia si la resolución de pantalla es diferente. La imagen (visualmente) es la misma, pero en realidad son dos archivos diferentes. La finalidad es que la imagen se recorte en torno al centro de la armadura de Iron Man, como centro de la esfera exterior que enmarca a los protagonistas principales. La imagen tiene superpuesto un título principal seguido de un texto en cursiva.
<p>
Seguidamente, nos encontramos un apartado con su propio título que nos cuenta sobre quiénes son los Vengadores. En pantallas con resolución grande, se expande lateralmente más que el resto de elementos de la página, pero solo hasta cierto punto.
<p>
El siguiente bloque empieza con un título menor que el anterior (h2) que nos muestra unas animaciones con las principales habilidades de nuestros héroes.
<p>
Las animaciones consisten en unas barras crecientes que, a mitad de su progreso, muestran a qué hacen referencia.
<p>
Finalmente, nos encontramos con un formulario con diferentes inputs y sus validaciones, finalizando con un botón de enviar y otro de reset que limpia todo el contenido escrito por el usuario.

* #### Películas (proyectos)
El primer bloque de esta web se visualiza de manera diferente según la resolución de pantalla, ya que en resoluciones pequeñas primero vemos el texto y debajo el video, mientras que en resoluciones mayores, el texto se posiciona a la derecha del video tal y como aprendimos en clase.
<p>
El texto es una breve descripción de las películas que veremos más abajo. El video no tiene animación de entrada y se reproduce automáticamente aunque silenciado. (Nota: El video empieza con la pantalla en negro y puede parecer que no se está reproduciendo, pero sí lo hace).
<p>
La siguiente parte de esta página consiste en un grid que se ajusta según la resolución de la pantalla. Nos muestra las diferentes portadas de las películas con su título, año y director al pie de cada imagen. Las imágenes se amplían ligeramente al pasar el ratón por encima. (Nota: Admito que las imágenes no tienen link a las películas porque es un trabajo absurdamente largo y repetitivo, y en la siguiente página ya demuestro que sí sé cómo hacerlo).

* #### What if...?
Esta página no había sido solicitada en la práctica. Dado que se nos proponía opcionalmente la creación de una página de error 404 y otra de 500 pero que, por su naturaleza, no deberían tener link de acceso natural en la web, he decidido crear esta página como antesala a las mismas.
<p>
Aquí encontramos un texto centrado y de un ancho similar a la imagen inferior.
<p>
La imagen inferior en realidad son dos imágenes animadas con links a las páginas 404 y 500. (Nota: aquí sí hay imágenes con links).
<p>
Al pasar el ratón por encima, las imágenes se amplían y se superponen a la otra, aumentando su contraste y su tamaño, pero todo dentro del mismo rectángulo.

* #### Error 404
En el centro total de esta página, Deadpool (quién si no) nos da el error 404. Entre el mensaje de error y la imagen, hay un botón con un link a una web externa que se abre en ventana separada.
<p>
Debajo de Deadpool, hay un botón intencionalmente muy pequeñito y disimulado para volver a la página principal. Es así de pequeño porque Deadpool es así de gamberro y quiere que nos quedemos con él. Aunque, al pasar el ratón por encima, el color del botón cambia para que se visualice ligeramente mejor (tan mal chaval no es).

* #### Error 500
En esta página, Deadpool vuelve a hacer de las suyas. En este caso, la imagen está de fondo y el texto se superpone. Además, nos encontramos con un video con animación fade in de entrada entrando desde abajo y haciéndose más opaco gradualmente, pero no del todo, para que sigamos viendo la maravillosa pose de Deadpool.
<p>
El video se reproduce automáticamente y en silencio, empezando a la mitad, que es el mejor momento del videoclip y en el que lo da todo.

* #### Elementos comunes
Nuestra web tiene dos elementos comunes en la mayoría de sus páginas: la barra de navegación y el footer.
La barra de navegación muestra el logo de los Avengers a la izquierda y los botones de navegación a la derecha. Los botones nos llevan, respectivamente, a la página principal, a la de los proyectos, a la de What if...? y a la sección inferior de la página principal que contiene el formulario.
<p>
Estos dos últimos botones se ocultan en pantallas más pequeñas.
<p>
Por otro lado, el footer es una franja sencilla que ocupa todo el ancho de la página y que no llega a tocar la parte inferior de la pantalla. En el centro, nos encontramos imágenes con links a webs externas que se abren en ventanas separadas.
---