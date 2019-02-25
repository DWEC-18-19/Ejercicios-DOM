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

