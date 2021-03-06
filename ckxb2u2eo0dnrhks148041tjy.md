## Desestructurando - JavaScript PRO Tips

Ahora veamos algunas cosas que podemos aplicar a nuestro c贸digo para que sea m谩s conciso y eficiente.

Imaginemos que tenemos un objeto con datos de un animal:

```javascript
const turtle = {
    name: 'Bob 馃悽',
    legs: 4,
    shell: true, 
    type: 'amphibious',
    meal: 10,
    diet: 'berries'
}
``` 

Y necesitamos una funci贸n que nos diga c贸mo alimentar a este animal.

```javascript
// Mal c贸digo 馃挬

function feed(animal) {
    return `Feed ${animal.name} ${animal.meal} kilos of ${animal.diet}`;
}

console.log(feed(turtle))
``` 

Esto es solamente una funci贸n que retorna un *string*, y ese *string* se crea interpolando las propiedades del objeto animal.

Esto luce mal porque estamos repitiendo la palabra `animal` muchas veces.

Existe una t茅cnica llamada "Desestructurar objetos", que podemos utilizar para eliminar las repeticiones.

En este ejemplo tenemos una funci贸n que recibe un objeto, pero nosotros solo necesitamos las propiedades de ese objeto, entonces para desestructurar este objeto, reemplacemos el par谩metro de entrada de la funci贸n de `animal` a `{ name, meal, diet }`. Ahora en el bloque de la funci贸n podemos utilizar las propiedades directamente como variables: 

```javascript
// Buen c贸digo 鉁?

function feed({ name, meal, diet }) {
    return `Feed ${name} ${meal} kilos of ${diet}`;
}

console.log(feed(turtle))
``` 

Para analizar esta t茅cnica con m谩s detalle, agreguemos un paso extra colocando la desestructuraci贸n del objeto dentro del cuerpo de la funci贸n:

```javascript
// Buen c贸digo 鉁?

function feed(animal) {
    const { name, meal, diet } = animal;
    return `Feed ${name} ${meal} kilos of ${diet}`;
}

console.log(feed(turtle))
``` 

En la l铆nea `const { name, meal, diet } = animal;` se crean tres constantes individuales, cada una de ellas con el nombre y el valor de una de las propiedades del objeto. Los nombres de las constantes deben coincidir con los nombres de las propiedades del objeto, aunque no es necesario utilizar todas las propiedades.

**Fuentes:**
- [JavaScript Pro Tips - Code This, NOT That](https://www.youtube.com/watch?v=Mus_vwhTCq0)
- [Do THIS to Write Clean Code! | JavaScript Pro Tips (2021)](https://www.youtube.com/watch?v=ZI3q-_vjSZE)
- [Junior Vs Senior Code - How To Write Better Code](https://www.youtube.com/watch?v=g2nMKzhkvxw)