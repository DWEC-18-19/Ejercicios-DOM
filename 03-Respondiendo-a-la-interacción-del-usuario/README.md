

## 3 Respondiendo a la interacción del usuario

### 3.1 Escuchando eventos

Añadir un escuchador de eventos a cada elemento li con addEventListener para que al pasar el ratón por un elemento (mouseover) ponga el texto el mayúsculas y al salir del elemento (mouseout) lo vuelva a dejar en minúsculas

### 3.2 Burbujas de eventos y delegación

El principio de los eventos burbuja (bubbling) es sencilla, al generarse un evento en un elemento, primero ejecuta los maneadores en ese elemento, luego en su padre, y así continuamente hasta pasarlo a todos sus antecesores.

Vamos a utilizar estar propiedad para añadir el manejado en vez de en cada elemento ``li``, solo en la lista completa (seleccionar la clase list) con ``addEventListener`` para hacer el mismo comportamiento.

Para saber qué elemento ``li`` ha generado el evento y modificarlo, utilizaremos ``event.target ``
