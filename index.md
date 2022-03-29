# Introducción

El proposito es crear una plataforma para la gestión de la colección de videojuegos (así como de sus elementos relacionados) y su ciclo de vida y actividad (videojuegos terminados, jugando, parados, etc.).

La plataforma por lo tanto estará dividida en tres grandes sectores relacionados entre si:

- Base de datos: Todos los elementos tendrán que poder ser registrados en el nivel de detalle deseado.
- Colección: Un usuario dispondrá de 3 grandes listas para gestionar:
  - Colección: Se incluyen aqui todos los elementos que se poseen.
  - Reservas: Se incluyen aqui los elementos que aún no se dispone de ellos pero se ha realizado una reserva para tenerlos en un futuro.
  - Lista de deseos: Se incluyen aqui todos los elementos que ni tenemos ni hemos reservado pero nos gustaría tener en algún momento.
- Actividad: Sistema de eventos donde se registrarán entradas relacionadas con la actividad en la plataforma o en los juegos. Por ejemplo, se ha añadido un juego a alguna lista de la colección, o se ha empezado a jugar a un juego/terminado un juego/etc.

# Entidades de la Base de Datos

## Videojuego (Game)

Un videojuego es la entidad básica para nuestra plataforma. Representa un videojuego en si mismo, independientemente de sus añadidos, la edición publicada o en que versiones/plataformas ha sido publicado.

## Complemento (Extra)

Un complemento representa un elemento coleccionable que acompaña o complementa a un videojuego. Estos pueden ser añadidos para ser utilizados en el juego (items, mapas, etc.) o complementos externos al videojuego que acompañan al juego (tanto físicos como digitales), como por ejemplo libros de arte, posters, bandas sonoras, etc.

## Publicación (Release)

Una publicación es cuando un videojuego esta disponible para una plataforma/formato/región concreta.

Ejemplo: Resident Evil se ha publicado el 22 de marzo de 1996 en Japón para PlayStation y el 17 de septiembre de 1997 en Europa para PC.

## Edición (Edition)

Una edición es como un juego se pone a la venta, puede ser la edición estandar que incluye únicamente el juego o ser una edición especial/coleccionista que incluya complementos de manera adicional.

Ejemplo: Elden Ring esta disponible en 5 ediciones diferentes.
- Standard: Incluye el juego y sólo esta disponible en formato digital.
- Deluxe Edition: Incluye el juego, banda sonora y libro de arte digitales, sólo esta disponible en formato digital.
- Launch Edition: Incluye el juego, poster, 3 postales, un parche de ropa, sólo esta disponible en formato físico.
- Collector's Edition: Incluye todo el contenido de la Launch Edition, asi como un código de descarga de la banda sonora digital, una caja metalica para el juego, libro de arte de 40 páginas, una figura de Malenia de 22 cm y una caja especial para la edición coleccionista.
- Premium Collector's Edition: Incluye todo el contenido de la Collector's Edition, así como una Replica escala 1:1 del casco de Malenia.

## Paquete (Bundle)

Un paquete es una compilación que puede incluir 1 o más juegos/ediciones y/o 1 o más complementos.

Ejemplo: El [Lote Triple de EA STAR WARS](https://store.playstation.com/es-es/product/EP0006-CUSA15089_00-STARWARSTRIPBUND) para PS4/PS5 incluye 3 juegos:
- STAR WARS: Squadrons
- Edición Deluxe de STAR WARS Jedi: Fallen Order
- Edición Celebration de STAR WARS: Battlefront II

# Entidades de la Colección

## Colección (Owned)

Aqui se registran todos los elementos que el usuario posee en su colección. Los elementos serán principalmente tres, Ediciones, Paquetes o Complementos. Se registrará además detalles como la fecha de compra, publicación especifica que se posee, origen de la compra, precio pagado, etc.

## Reservas (Preorder)

Aqui se registran los elementos reservados que en un momento concreto del futuro pasarán a ser parte de la colección. Los detalles a registrar serán similares a los de la Colección. Habrá una cierta automatización (automática o semiautomática) para trasladar los juegos de esta lista a la Colección.

## Lista de Deseos (Wishlist)

Aqui se registran los elementos que nos gustaría tener en algún momento. Los detalles en este caso serán más escasos ya que no sabes el precio pagado o cuando vas a comprarlo. Habrá una cierta automatización (sólo semiautomática) para trasladar los juegos de esta lista a cualquiera de las otras dos (Reservas o Colección) tras solicitar al usuario los detalles faltantes (fecha de compra/reserva, precio pagado, etc.).

# Entidades de la Actividad

TBD
