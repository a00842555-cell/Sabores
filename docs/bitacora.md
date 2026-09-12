Erick Manuel Ureña Matos A00842555
Ejercicio 0

Los endpoints sirven para las siguientes pantallas:

- `GET /restaurants`: muestra la lista de restaurantes.
- `GET /restaurants/3`: muestra el detalle del restaurante con ID 3.
- `GET /reviews?restaurantId=3`: obtiene las reseñas del restaurante con ID 3.
- `POST /reviews`: permite crear una nueva reseña.
- `GET /me/reviews`: muestra las reseñas que ha creado el usuario.
- `DELETE /reviews/12`: elimina la reseña con ID 12.

Ejercicio A2  ¿Quién calcula el promedio ahora?

Los dos lo calculan, pero tienen diferentes propósitos.
El servidor manda ratingAverage ya calculado y este se utiliza en la lista de restaurantes, porque así no es necesario pedir las reseñas de cada restaurante solamente para mostrar su promedio.
Por otro lado, RatingSummary.from(reviews) se utiliza en el detalle del restaurante, donde las reseñas ya están cargadas. 

Ejercicio B1 — ¿Cuántos estados tiene de verdad una pantalla con red?
La pantalla tiene 3 estados principales:
1.	Cargando: se muestra un indicador de progreso mientras se espera la respuesta del servidor. 
2.	Éxito: se muestra la lista de restaurantes. Incluso puede ser una lista vacía, pero eso es diferente a estar cargando. 
3.	Error: se muestra un mensaje indicando que ocurrió un problema y un botón para reintentar
La lista vacía no debería utilizarse para representar el estado de carga, porque no se podría distinguir entre que sí todavía se están obteniendo los datos y que sí realmente no existen restaurantes.

Ejercicio C2 — ¿Por qué el servidor también valida?
El cliente valida los datos para evitar errores y darle una respuesta rápida al usuario, pero el servidor también debe validarlos porque no puede confiar en que todas las peticiones vienen de nuestra aplicación.











