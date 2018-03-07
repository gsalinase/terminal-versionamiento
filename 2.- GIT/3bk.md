## Introducción a GIT

Hola, bienvenido, en esta experiencia vamos a conocer más en profundidad GIT y cómo utilizarlo.

Para entender como funciona GIT vamos a trabajar sobre la metáfora de una mudanza.

En una mundaza lo primero que hacemos es introducir nuestras cosas en una caja, de la misma forma lo haremos con GIT, que agregamos nuestros archivos y cambios utilizando `git add`

El segundo paso consiste en confirmar los cambios, esto quiere decir que verificamos que la caja esté completa y le asignamos un nombre, esto se logra con `git commit`

El tercer paso es enviar la caja a destino, esto se hace via `git push`

Los dos primeros pasos suceden completamente dentro de nuesto computador, el tercer paso consiste en enviar los cambios a un punto remoto, para el cual utilizaremos github.
 
En este capítulo nos enfocaremos en los dos primeros pasos que consisten en el add y el push.

# Setup del proyecto
Ya sabemos inicializar GIT, ahora lo haremos dentro de un proyecto nuevo, para eso crearemos una carpeta, y dentro de ella realizaremos git init.

Pasos a seguir:

```
mkdir proyecto_git
cd proyecto_git
git init
```

deberíamos obtener un mensaje de que se inicializó GIT.

<pre>
Initialized empty Git repository in /ruta/al/archivo
</pre>


# Añadiendo a la caja
El primer concepto que aprenderemos será agregar nuestros cambios a una caja.

Para eso necesitamos algo que agregar a la caja, nuestro proyecto está vacío, por ahora simplemente crearemos un archivo llamado `index.html` 

git nos ayuda a saber que tenemos dentro de cajas y que no, para eso podemos escribir `git status`

y veremos un mensaje del tipo:

```
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	index.html

nothing added to commit but untracked files present (use "git add" to track)
```



luego, debemos indicarle que archivos tiene que tener en su índice, esta etapa se llama stage ( git add) .  Y por último, cuando confirmamos que guarde los cambios estamos pasando la información a HEAD (git commit).


Veámoslo con un ejemplo práctico , vamos a indicarle a nuestro computador que un proyecto o archivos  serán controlados por GIT.

Esto lo realizamos con git init, con esto se añade una carpeta .git a nuestra carpeta de proyecto, con los archivos para su funcionamiento, es decir la etapa donde se define el Working directory”.

A continuación  debemos indicar qué archivos necesitan ser añadidos a la lista de versionamiento. Esto lo realizamos con git add .  el punto indica añadir todos los archivos , también podemos añadirlos uno a uno.  esta etapa es la creación del stage [No es la creación, es añadir al stage que es la etapa de preparación]

[git status es muy importante y no está explicado]
Si necesitamos saber que archivos se han añadido, o en que estado estan los archivos ya indicados, lo podemos realizar con git status.

Una vez que los archivos ya están añadidos, Podemos decir que guarde el punto donde están los documentos. y guarde su estado.  Esto lo realizamos con un git commit ,
“git commit -m “ADD: First Commit”, Detengámonos a analizar este comando.  Primero le indicamos a git que realizaremos un commit ( es decir, guardar [confirmar los cambios] los cambios) , -m indica que el commit llevará un mensaje y  Lo que está dentro de las comillas es el mensaje que verán las personas que revisen este commit.  Este tercer paso se conoce como crear el Head [Realmente no es crear a menos que el branch esté vacío], es decir git guarda el estado de nuestros archivos  y añade un cálculo para identificar estos cambios.

[explicar que el git init solo se hace una vez ]

Devemos recalcar que solo realizaremos git init una vez.

[agregar un diagrama de flujo con las opciones ]

Diapòsitiva añadida.

[realizar ejercicio desde cero]

Ejemplo practico por consola.


[crear ejercicio básico que pueda seguir el alumno]

	Falta añadir un ejericio simple. 
	
[después de confirmar los cambios hay que explicar git log]
	una vez subidos nuestros cambios, podemos utilizar git log  para ver los commit ya realizados y quien los realizo, podemos explicar el numero que aparece en el commit (CHECKSUM) y que se calcula con SHA 1.

Debemos resaltar que nuestro control de versiones está registrando los cambios que le indiquemos.  por lo tanto si añadimos nuevos archivos, debemos nuevamente realizar un git add. y volver a hacer commit.


Quiero recordarles que estamos usando git de forma local, por lo cual nuestros cambios y registros solo estarán disponibles en nuestra máquina. [git de forma local podría ser el nombre del capítulo]

Crea ahora un pequeño proyecto con tu editor de texto y añade git a la carpeta del proyecto. añade tus archivos y crea tu primer commit. [El ejercicio tiene que ser mas pauteado]
