## ¿Qué son las Cookies HTTP?

De una forma u otra, todos los días utilizamos internet e interactuamos con cookies HTTP. Las cookies HTTP permiten a las páginas web personalizar la experiencia de usuario que nos entregan. Es una funcionalidad muy útil que algunas veces simplemente se ignora o incluso se malinterpreta.

Desde el otro lado de un sitio o aplicación web, las cookies HTTP permiten a los desarrolladores crear funcionalidades y comportamientos que se ajusten a las preferencias detectadas del usuario.

Más allá de todos estos beneficios es necesario tener en cuenta algunos riesgos de seguridad relacionados con las cookies HTTP, tópico bastante escuchado en los últimos años, sobre todo entre personas que se preocupan por cada detalle en la utilización de la información personal.

En este artículo explicaré cómo funcionan las cookies HTTP.

## ¿Qué son las cookies HTTP?

Las cookies son pequeñas piezas de datos almacenados en el navegador web y que se envían al servidor en cada solicitud. Son utilizadas para almacenar el estado de la sesión de usuario, preferencias y también seguimiento del usuario.

### Gestión de la sesión del usuario

La gestión de la sesión del usuario permite la interacción segura entre el usuario y algún servicio o aplicación. A medida que el usuario continúa interactuando con la aplicación web, se envían datos que especifican si la sesión del usuario continúa activa.

Algunos ejemplos: Logins (sesión iniciada con una cuenta de usuario), autocompletado de formularios, carros de compra.

### Personalizaciones del usuario

Almacena preferencias del usuario especificadas en la configuración, para ser  usadas las próximas veces que el usuario ingrese a la aplicación.

Algunos ejemplos: Preferencias, temas de interfaz (claro u oscuro), idioma.

### Seguimiento

Registra y analiza hábitos y búsquedas del usuario en el navegador web. Los detalles incluyen el tiempo que el usuario permanece en una página determinada dentro de la aplicación o sitio web, y la lista de las páginas visitadas. Debido a la información confidencial detrás del seguimiento, los usuarios deben estar al tanto de las vulnerabilidades al visitar páginas web inseguras.

Ejemplo: seguimiento de anuncios

## ¿Cómo crear cookies HTTP?

Desde la consola de tu navegador web, puedes configurar una cookie con JavaScript escribiendo el siguiente código:


```javascript
document.cookie="example=1"
``` 

Para comprobar si tu cookie está configurada, abre la pestaña "Aplicación" y haz clic en la pestaña "Cookies" para acceder a tu nueva cookie.

## Propiedades de las cookies

- Cookie scope
- Expires y Max-age
- SameSite

## Tipos de cookies HTTP

- Session cookies
- First-Party cookies
- Third-Party cookies
- Secure cookies
- Zombie cookies

## Conclusión

Hemos visto las principales características de las cookies HTML y aunque muchas veces se las presenta como algo muy peligroso a evitar siempre, normalmente son muy útiles y beneficiosas. 

Simplemente hay que evitar proveer datos sensibles a sitios web que no sean de confianza, incluso la mayoría de los sitios web nos muestran un mensaje dándonos la posibilidad de habilitar o no el uso de cookies.