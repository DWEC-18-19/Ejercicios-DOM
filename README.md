 
## 1 Empezando a manejar DOM

### 1.1 Ejemplo sencillo

Añadir un evento al encabezado para que al hacer clic sobre el cambie a otro color.

### 1.2 Seleccionar elementos por id

Añadir un input con un id y un botón con otro id, al poner un color, por ejemplo red, y pulsar el botón, cambiará el encabezado que tiene otro id

### 1.3 Seleccionar elementos por tipo

1. Eliminar el input y el botón.
1. Añadir un lista no ordenada de cosas que tengan un color. 
1. Añadir en el fichero javascript un bucle que cambie a ese color todos los elementos li de la página.

### 1.4 Seleccionar elementos por clase

1. Añadir de forma desordenada elementos que no tengan ese color a la lista sin ordenar.
1. Poner a estos elementos una clase, por ejemplo, error-no-verde.
1. Añadir al fichero javascript otro bucle que cambie de color todos los elementos que tengan esa clase.

### 1.5 Consultas de selección css

Añadir un tercer bucle que seleccione todos los elementos li impares de la lista y ponerles como fondo gris claro.

## 2 Construyendo la aplicación

### 2.1 Text content e inner html

Añadir un input y un botón que cambie el texto del elemento párrafo con la clase description de la página  por la que hayas introducido en el input.

### 2.2 Cambiando los atributos elemento

Modificar el elemento con la clase description para que aparezca el texto todo en mayúsculas.

### 2.3 Dando estilo a los elementos

1. Añadir un botón que ponga ocultar lista.
1. Al pulsar sobre el botón oculta la clase lista cambiando la propiedad css display a none.
1. El botón mostrará ahora mostrar lista y al pulsarlo volverá a mostrar la lista poniendo la propiedad css display a block

### 2.4 Creando y agregando elementos DOM

1. Añadir un input y un botón añadir elemento al final de la página
1. Al escribir un elemento y pulsar el botón añadirá ese elemento a la lista, antes del input y botón añadir.

### 2.5 Eliminando nodos

1. Añadir otro botón elemental último elemento
1. Al pulsarlo eliminará el último elemento de la lista.

## 3 Respondiendo a la interacción del usuario

### 3.1 Escuchando eventos

Añadir un escuchador de eventos a cada elemento li con addEventListener para que al pasar el ratón por un elemento (mouseover) ponga el texto el mayúsculas y al salir del elemento (mouseout) lo vuelva a dejar en minúsculas

### 3.2 Burbujas de eventos y delegación

El principio de los eventos burbuja (bubbling) es sencilla, al generarse un evento en un elemento, primero ejecuta los maneadores en ese elemento, luego en su padre, y así continuamente hasta pasarlo a todos sus antecesores.

Vamos a utilizar estar propiedad para añadir el manejado en vez de en cada elemento ``li``, solo en la lista completa (seleccionar la clase list) con ``addEventListener`` para hacer el mismo comportamiento.

Para saber qué elemento ``li`` ha generado el evento y modificarlo, utilizaremos ``event.target ``


## 4 Atravesando DOM

### 4.1 Usar nodo padre

1. Añadir un botón eliminar con la "clase remove" a cada elemento li de esta forma: 
``<li>grapes <button class="remove">Remove</button></li>``
2. Utilizando el mismo principio de eventos en burbuja, cuándo pulsemos en el botón eliminar de cada elemento, borraremos ese elemento de la lista sin ordenar ul (el elemento padre del botón) con el método ``removeChild``. 
- **Pista**: para saber si se ha pulsado algún botón en la lista dentro de addEventListener, usar la condición ``event.target.tagName == 'BUTTON'``

### 4.2 Usar elementos hermanos previos

1. Añadir otro botón arriba con clase "up" a cada elemento li de esta forma:   
```
<li>grapes 
          <button class="up">Arriba</button>          
          <button class="remove">Eliminar</button>
</li>
```
2. Intercambiar el elemento superior por el pulsado para que suba un nivel. 

- **Pista**, usar la propiedad ``reviousElementSibling`` del elemento ``li`` pulsado y el método ``insertBefore`` del elemento ``ul`` para intercambiarlos.

### 4.3 Acceder al siguiente elemento hermano

1. Añadir otro botón abajo con clase "down" a cada elemento li de esta forma:   
```
<li>grapes 
          <button class="up">Arriba</button>   
     <button class="down">Down</button>            
          <button class="remove">Eliminar</button>
</li>
```
2. Hacer lo mismo que en el anterior, pero esta vez bajando el elemento.

### 4.4 Obtener todos los elementos hijos

Modificar el código de añadir para que añade también al elemento li los botones para subir, bajar y eliminar, todo mediante DOM (sin usar ``innerhtml``)

### 4.5 Obtener el primer y el ultimo elemento hijo

1. Mediante los métodos ``firstElementChild`` y ``lastElementChild``, cambiar el color del primer elemento de la lista a lightskyblue y del último elemento de la lista a lightsteelblue.

2. Como reto puedes crear una función para actualizarlo para que según se añadan, eliminen o cambien de orden los elementos, se actualice.

