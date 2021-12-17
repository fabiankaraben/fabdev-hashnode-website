## Depurando con console.log - JavaScript PRO Tips

Hoy en día JavaScript ya no es solo un lenguaje de programación para hacer cositas en el navegador web, encontramos a JavaScript en desarrollo de backend (API), herramientas de consola de comandos, funciones en la nube (Cloud functions), y en muchos otros lugares.

## Analizando `console.log`

Lo primero que debes saber es cómo depurar tu código JavaScript como un profesional, y la manera de hacer esto es utilizando la función `console.log`. Pero existen buenas maneras de utilizar `console.log` y malas maneras de utilizar `console.log`. 

Imaginemos que tenemos tres objetos diferentes, cada uno asignado a su propia variable:

```javascript
const foo    = { name: 'juan',   age: 30, nervous: false };
const bar    = { name: 'pedro',  age: 40, nervous: false };
const baz    = { name: 'fabian', age: 50, nervous: true };
``` 

La manera más obvia de registrar esto es una llamada a cada objeto:

```javascript
// Mal código

console.log(foo);
console.log(bar);
console.log(baz);
``` 

Sin embargo, el problema principal es que de esta manera no podemos conocer el nombre de la variable al analizar los datos impresos en la consola del navegador web (o la salida de REPL o la consola de comandos, si estamos trabajando con Node.js).

![console-log-bad.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1639696665149/1BmgW50Kx.jpeg)

Existe un truco que podemos utilizar aquí llamado "nombre de las propiedades", donde agregamos las variables a un objeto. Esto no solo reduce la cantidad de líneas del código, sino que también nos dice exactamente qué variable almacena estos datos:

```javascript
// Buen código

console.log({ foo, bar, baz });
``` 

Ahora la consola se ve así:

![console-log-good.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1639696693152/y85kqlkTl.jpeg)

## Analizando `console.table`

Algo que tal vez notaste es que todos los objetos comparten propiedades, entonces esto es ideal para visualizarlo como una tabla:

```javascript
// Buen código

console.table([foo, bar, baz]);
``` 

La salida será la siguiente:

![console-log-good-table.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1639700059073/uIQoxC58r.jpeg)

Esto es algo muy útil cuando tienes un array de objetos, o como en el ejemplo, solo hay que definir un array que contenga los objetos individuales.

Realmente existen muchas posibilidades para el registro en consola, sin embargo, veamos solamente un par de esas posibilidades.

## Analizando `console.time`

Podemos obtener el tiempo de ejecución de un fragmento de código de la siguiente manera:

```javascript
console.time('looper')

let i = 0;
while (i < 1000000) { i ++ }

console.timeEnd('looper')
``` 

El fragmento de código a contabilizar es:

```javascript
let i = 0;
while (i < 1000000) { i ++ }
``` 

La cuenta inicia con la línea:

```javascript
console.time('looper')
```

Y finaliza con la línea:

```javascript
console.timeEnd('looper')
```

Momento en el que se imprime el tiempo de ejecución en la consola:

![console-time.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1639701086273/r0pkRzUkk.jpeg)

Para cada ejecución el tiempo registrado será diferente.

## Analizando `console.trace`

Pero qué sucede si necesitamos conocer cuál es el archivo desde donde se lanzó la función de registro. En estos casos podemos utilizar `console.trace`, de esta manera:

```javascript
const deleteMe = () => console.trace('hola, es aquí')

deleteMe()
deleteMe()
```

Al ejecutar esto, en la consola veremos:

![console-trace.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1639701456983/eCPHz6Afx.jpeg)

## Conclusión

La función `console.log` es muy útil pero muchas veces no aprovechamos todo su potencial y lamentablemente mucha gente directamente desconoce la existencia de otras funciones interesantes como `console.table`, `console.time` y `console.trace` con las que podemos ahorrar bastante tiempo de trabajo.
