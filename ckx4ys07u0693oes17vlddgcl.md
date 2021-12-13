## Cómo crear tu primer programa en Go (Golang)

El clásico programa "¡Hola Mundo!" es una tradición en programación. Es un simple pero completo programa para principiantes, y también es una buena manera de estar seguros de que el entorno de desarrollo está correctamente configurado.

Este artículo te llevará a través de la creación de ese primer programa en Go. Sin embargo, para hacer ese programa más interesante, modificaremos el tradicional "¡Hola Mundo!" de tal manera que este pregunte tu nombre y luego imprima un saludo.

Cuando finalices este artículo, tendrás un programa que lucirá así al ejecutarse:

```bash
go run hello.go
Por favor ingresa tu nombre:
Sammy
¡Hola Sammy!, yo soy Go.
```

## Prerrequisitos

Antes de iniciar este tutorial, necesitarás tener configurado tu entorno local de desarrollo en Go. Puedes consultar las siguientes guías si necesitas ayuda con esto:

-  [Cómo instalar Go en macOS](https://www.digitalocean.com/community/tutorials/how-to-install-go-and-set-up-a-local-programming-environment-on-macos) 
-  [Cómo instalar Go en Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-install-go-and-set-up-a-local-programming-environment-on-ubuntu-18-04) 
-  [Cómo instalar Go en Windows](https://www.digitalocean.com/community/tutorials/how-to-install-go-and-set-up-a-local-programming-environment-on-windows-10)

## Paso 1: Escribir el programa "¡Hola Mundo!" básico

Para escribir el programa "¡Hola Mundo!", abre un editor de línea de comandos, como por ejemplo `nano`, creando un nuevo archivo `hello.go`, así:

```bash
nano hello.go
```

Esto también se puede hacer en editores de interfaz gráfica, como el popular Visual Studio Code.

Ya con el editor abierto, escribe el siguiente código:

```go
package main

import "fmt"

func main() {
	fmt.Println("¡Hola Mundo!")
}
```

Analicemos cada parte de este código.

La palabra clave `package` define a qué paquete de código pertenece este archivo. Puede haber solo un paquete por carpeta y cada archivo `.go` debe declarar el mismo paquete en la parte superior de su contenido. En este ejemplo el código pertenece al paquete `main`.

La palabra clave `import` le dice al compilador de Go qué otros paquetes vas a usar en este archivo. Aquí estamos importando el paquete `fmt` que pertenece a la biblioteca estándar de Go. El paquete `fmt` provee funcionalidades para dar formato e imprimir contenido, lo cual es muy útil para el desarrollo.

La función `Println`, perteneciente al paquete `fmt`, que dice a la computadora que imprima el texto especificado en pantalla. El texto es `"¡Hola Mundo"`, el cual se encuentra entre comillas porque se trata de un `string`, el tipo de dato que representas los textos. La función `fmt.Println` imprimirá este `string` en la pantalla donde el programa se ejecute.

Para finalizar este paso, guarda el contenido y cierra el editor nano presionando las teclas `CTRL + X`, y luego la tecla `Y` para aceptar que los cambios se guarden.

En el siguiente paso probaremos este programa.

## Paso 2: Ejecutar el programa en Go

Con el programa "¡Hola Mundo!" escrito, ahora estás listo para ejecutarlo. Para esto, utilizarás el comando `go run` seguido del nombre del archivo que acabas de crear, de esta forma:

```bash
go run hello.go
```

La salida que verás en la misma consola debe ser:

```bash
¡Hola Mundo!
```

Analicemos qué es lo que ha pasado.

El programa necesita ser compilado antes de ejecutarse. Cuando ejecutas el comando `go run` seguido del nombre del archivo, en este caso `hello.go`, el comando `go` compila el código y luego ejecuta el binario resultante.

Para los programas escritos en lenguajes de programación compilados, el compilador toma el código del programa y genera otro tipo de código de bajo nivel (el código de máquina) que es el ejecutable final del programa.

Los programas de Go requieren un paquete `main` y exactamente una función `main()` que funciona como punto de entrada para la aplicación. La función `main` no recibe argumentos ni devuelve valores, pero le dice al compilador de Go que este paquete debe ser compilado como un ejecutable, ya que existen otros casos en los que un paquete está destinado a ser utilizado por otros paquetes y no a generar un archivo ejecutable.

Una vez compilado, el binario internamente ejecuta la instrucción correspondiente a la línea `fmt.Println("¡Hola Mundo!")`, lo cual envía este texto a ser impreso en pantalla.

Las comillas alrededor del texto `¡Hola Mundo!` no se imprimen, ya que estas son parte de la definición del `string`.

En este paso has compilado y ejecutado un programa "¡Hola Mundo!" completo.