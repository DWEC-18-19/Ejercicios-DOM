El principio de los eventos burbuja (bubbling) es sencilla, al generarse un evento en un elemento, primero ejecuta los maneadores en ese elemento, luego en su padre, y así continuamente hasta pasarlo a todos sus antecesores.

Vamos a utilizar estar propiedad para añadir el manejado en vez de en cada elemento li, solo en la lista completa (seleccionar la clase list) con addEventListener para hacer el mismo comportamiento.

Para saber qué elemento li ha generado el evento y modificarlo, utilizaremos event.target 
