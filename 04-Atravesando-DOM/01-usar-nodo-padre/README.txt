Añadir un botón eliminar con la "clase remove" a cada elemento li de esta forma:   

<li>grapes <button class="remove">Remove</button></li>

Utilizando el mismo principio de eventos en burbuja, cuándo pulsemos en el botón eliminar de cada elemento, borraremos ese elemento de la lista sin ordenar ul (el elemento padre del botón) con el método removeChild.

pista: para saber si se ha pulsado algún botón en la lista dentro de addEventListener, usar la condición event.target.tagName == 'BUTTON'