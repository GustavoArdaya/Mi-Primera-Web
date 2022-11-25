# Mi-Primera-Web
<h1>el documento HTML</h1>
Para mi primera web, elegí el tema (redundante) de una nueva presentación literalmente. A riesgo de parecer ególatra o cosas por el estilo escogí esto por ser un tema que se esperaría que domine de alguna manera, y asi me quitaba de encima tiempo de planificación para dedicarme a aprender a solucionar los problemas inherentes a la creación de mi primera pagina web. Como sospechaba habian varios problemas a solucionar. He aqui mi triste historia:<br>
<br>
Este es el código HTML final del proyecto (parte del texto de los párrafos no se visualizan del todo en la pantalla):
![MPP1](https://user-images.githubusercontent.com/118914949/203929670-67cfc4cc-df7b-4fda-9dff-9f2d208dc670.jpg)<br>
<h2>La sección Head</h2>
La verdad que las formulas para inicializar un Html incorporadas en Visual Studio Code ahorran mucho tiempo. Talvez el código (al menos de momento, y en lo personal) mas "abstracto" se encuentra en este apartado: 

![MPP2](https://user-images.githubusercontent.com/118914949/203930379-073862a2-4adb-49bf-bf76-8fcd08294575.jpg)<br>
El atributo HTML lang se puso a "es" que es el equivalente a español. Aparentemente existen ciertos convenios de como definir los lenguajes (por ejemplo "en" para el inglés, o "fr" para el francés). De momento desconozco si esto tiene alguna función aparte de ayuda al usuario que vaya a leer el código.<br>
Bajo la seccion de title se pone el título que figurará en la pestaña superior del navegador. Elegí el apropiado "Mi Primera Web". Para el link de estilo CSS puse el nombre de "styles.css" como Sergi hizo en la demostración.<br>
<h2>La sección Body</h2>

![MPP3](https://user-images.githubusercontent.com/118914949/203933061-8cbb0fe0-5c9e-45a9-8fb8-46b56534f05b.jpg)<br>
Aqui no hay demasiado a destacar. Utilicé un header 1 y uno 2 para dos titulos de tamaño ligeramente diferente.<br>

<h3>Peleándose con el Flex</h3>
Algo que si resulto un poco más complicado fue utilizar el Flex, para poner dos elementos lado a lado (en este caso una foto de su servidor a la izquierda, y el texto biográfico a la derecha). Naturalmente fui a buscar alguna especie de tutorial online y encontré una guia aquí:(https://css-tricks.com/snippets/css/a-guide-to-flexbox/)<br>
<br>El primer paso fue dividir el Body en una Section a la que le puse de id "bio" a la que luego dividiría en dos Divs identificadas a su vez como "Foto" y "texto". 

![MPP4](https://user-images.githubusercontent.com/118914949/203935898-1b9aed4e-6864-4b60-b5bd-6ad4f9fe5731.jpg)<br>
Es importante notar que debí agrupar todo el texto (h3 y p) en la seccion de texto de manera que el Flex entienda que los elementos a dividir son 2 (Foto y texto) y no todos estos elementos independientes.<br>
<br>La foto la inserte con <img> usando los parametros src, en el que especificaba la dirección donde el código debía buscar la foto que era la raiz de MiPrimeraWeb (donde previamente habia copiado la imagen que quería utilizar); el parametro alt, donde puse una pequeña descripción; y finalmente elementos de estilo.<br>
Nótese tambien que ciertos elementos de estilo de la foto los puse directamente en el documento HTML y no en el documento CSS, al ser un elemento único que no compartia características con otros de la página. No sé si esto sera una buena práctica.<br>
De todas formas ajuste el padding, tanto superior como derecho, para "despegar" la foto del texto de la columna derecha. Visualmente el resultado me fué satisfactorio:

![MPP6](https://user-images.githubusercontent.com/118914949/203937068-33f08b73-c179-4a47-86f8-c6c8bdb55bca.jpg)<br>

El formato de los párrafos y del header 3 que utilicé a la derecha si fue especificado en el documento CSS y lo comentaré brevemente cuando toquemos ese parte, asi como los parametros del Flex (que adelanto que son los por defecto, jaja).<br>

<h2>La sección Footer</h2>
Esta parte tambien tenia un poco de complicación y creo que es la que talvez tiene mas código ineficiente y redundante.<br>
En esta sección debia poner una imagen con un enlace a alguna página web, y a la cual decidí poner un pequeño texto explicativo (o mas bien apologético):

![MPP7](https://user-images.githubusercontent.com/118914949/203938475-7d250fbc-90d3-4a44-b5f5-491749acae73.jpg)<br>

En esta parte creé una sección llamada "Spotify" que contiene dos eleméntos, uno de texto y otro una imagen, que a la vez es un enlace. Para que esten lado a lado utilicé el flex nuevamente, aunque creo que de una manera menos eficiente.<br>
Para la imagen con un enlace, el eleménto talvez mas interesante de la página, busqué de internet una imagen png, de fondo transparente, para acomodar la imagen de una manera un poco más estética. La añadí a la pagina utilizando el elemento anchor (a) con el atributo href, donde especifiqué la dirección del enlace, y entre la apertura y cierre del anchor incluí una imagen con img, siguiendo los pasos antes descritos en la sección de Body.<br><br>
Hasta ahi lo "fácil"...<br><br>
Poner los elementos en el orden específico fue un poco complicado y creo que me desordené un poco en esta parte, ya que incluí elementos de estilo tanto en el HTML como en el CSS. Utilicé el atributo float para llevar los elementos hacia la derecha de la página, y estuve experimentando un poco, aunque el resultado final no llegó nunca a ser satisfactorio. Intentaré solucionarlo ahora, pero veremos si me da el tiempo ya que la entrega se acerca y estoy demorando un poco en este README, intentando ser lo mas explicativo posible.<br>
Vamos ahora con el CSS. (Advertencia: este si es bastante más caótico y creo que tiene mas código "innecesario").<br>

<h1>El documento CSS</h1>
Aqui una pequeña visión global de mi codigo CSS:

![MPP8](https://user-images.githubusercontent.com/118914949/203942777-d424fcec-64fc-4ada-b619-2394cd713eee.jpg)<br>

Los comentarios serán un poco menos específicos que en la primera parte HTML. Aunque el resultado de mi primera página fue "satisfactorio" me da la impresión que aun no se bien como aprovechar todas las posibilidades de CSS. Además, aclaro que deje bastante codigo talvez inservible, en parte a manera de aprendizaje (como los colores que fueron "comentados", y en otra parte por dudas respecto a si su presencia hacía que la página funcione, aunque de forma rudimentaria.<br>

![MPP9](https://user-images.githubusercontent.com/118914949/203943765-6fa5f599-02ae-4935-866a-9bdd36079211.jpg)<br>
La parte mas larga del CSS es la de body. A destacar aqui el color del fondo (me gustó por que permitia un buen contraste de lectura y el fondo de la foto), el tamaño de 22px que me parecio que era el "justo" para el resultado que buscaba, aunque me preocupa un poco su compatibilidad con otras plataformas. Un texto blanco a secas.<br>
A destacar, pero de manera mas negativa: el overflow lo puse ahi, con la intención de solucionar un problema de la superposicion del texto por encima del footer al reducir la ventana, problema que no logré solucionar de momento. Tendré que revisar el capitulo de Codecademy que habla al respecto, ya que al haber hecho un curso tan rápido siento que algunos de los conceptos se me fueron (y admito que CSS es mi punto débil, de momento).<br>
Otra cosa que me pregunto es si no estoy usando demasiado el padding en lugar de otros elementos del box, como el margin, etc. De momento me funciona a nivel visual, pero me pregunto si no habran formas mas eficientes de lograr lo que estoy buscando y si esto no causará algun otro tipo de problema, o si no es práctica estandar.


![MPPA](https://user-images.githubusercontent.com/118914949/203945174-80e4e615-3eaf-444e-9b63-864786eb9406.jpg)<br>

En las etiquetas de texto y bio puse los parámetros de max-height y margin-bottom intentando solucionar el tema antes mencionado. No logró ningun cambio visible, pero lo dejo a manera de aprendizaje.<br>
<br>Aqui la anunciada utilización de Flex: usé el atributo display al que asigne Flex y ya está... Utilicé parametros por defecto utilizando solamente la posición y agrupación de los elementos para acomodarlos de forma correcta: de izquierda a derecha, y de arriba a abajo.<br>
<br><br>
![MPPB](https://user-images.githubusercontent.com/118914949/203946848-7cc21acd-c78b-4765-b7b8-86e721a99882.jpg)<br>
 
En la sección de footer, volvi a poner el atributo floater, como lo había hecho ya en el HTML. El resultado visual es el deseado, pero solamente un una ventana de dimensiones "estandares" para una pantalla de ordenador. Ahora terminando éste README me pongo a investigar una solución, y si lo consigo actualizaré este documento. (como añadido y EDIT, para que quede constancia de las dificultades que tuve durante el aprendizaje. <br>
<br>
Pues eso es todo de momento.<br>
<br>Peace out.<br>
<br>Gustavo


