# Curso Práctico de JavaScript

Profesor: Juan David

Fecha de Inicio: 07/07/2023

Fecha de Terminacion: 

Horas

---

### Test de JavaScript

**Responde las siguientes preguntas en la sección de comentarios:**
**¿Qué es una variable y para qué sirve?**

Una variable es un espacio en la memoria RAM de la computadora que sirve para guardar un valor

**¿Cuál es la diferencia entre declarar e inicializar una variable?**

Declarar solo crea la referencia en la memoria para ser utilizada por la variable y le asigna un nombre a la variable. Inicializar normalmente hace una declaracion y tambien le asigna el valor al espacio en memoria.

```jsx
//Declarar una variable
let nombre;
//Inicializar la variable
nombre = "Camilo Pascual"
//Podemos generar este proceso en una sola linea.
let nombre = "Camilo Pascual";
```

**¿Cuál es la diferencia entre sumar números y concatenar strings?**

Sumar numeros es una operacion matematica, mientras que concatenar string es una operacion de union de union de cadenas de caracteres.

**¿Cuál operador me permite sumar o concatenar?**

El operador es el signo: +

**Determina el nombre y tipo de dato para almacenar en variables la siguiente información:**

Nombre: String
Apellido: String
Nombre de usuario en Platzi: String
Edad: number
Correo electrónico: string
Mayor de edad: boleano
Dinero ahorrado: number
Deudas: number

**Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.**

```jsx
let nombre = "Camilo Pascual";
let apellido = "Camacho Ruiz";
let nombre_user_platzi = "rocando";
let edad = 25;
let email = "yomismosoy@elquemandayvoy.com";
let mayoria_de_edad = true;
let dinero_ahorrado = 250.000;
let deudas = 20.000;
```

Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

Nombre completo (nombre y apellido)
Dinero real (dinero ahorrado menos deudas)

```jsx
let nombre = "Camilo Pascual";
let apellido = "Camacho Ruiz";
console.log(nombre + " " + apellido);

let dinero_ahorrado = 250.000;
let deudas = 20.000;
console.log(dinero_ahorrado - deudas);
```

## **Funciones**

**Responde las siguientes preguntas en la sección de comentarios:**

**¿Qué es una función?**

Es un bloque de codigo disenado para realizar una tarea especifica. La funcion se ejecuta cuando se llama por su nombre.

**¿Cuándo me sirve usar una función en mi código?**

Cuando se necesita que una misma tarea se ejecutada varias veces en el mismo programa. 

**¿Cuál es la diferencia entre parámetros y argumentos de una función?**

Los parametros son las variables que se definen en la declaracion de la funcion.

Un argumento es el valor real que se le pasa a la funcion cuando se invoca o se llama.

## **Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:**

```jsx
//Codigo Original //
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");

//Codigo Modificado //

function imprimirNombre(name, lastname, nickname):
	 return console.log('Mi nombre es ${name} ${lastname}, pero prefiero que me digas ${nickname}.');

let name = "Juan David";
let lastname = "Castro Gallego";
let nickname = "juandc";

imprimirNombre(name, lastname, nickname);

```

## Condicionales

**Responde las siguientes preguntas en la sección de comentarios:**

**¿Qué es un condicional?**

Las condicionales son instrucciones especiales que permiten controlar el flujo de ejecucion del programa con base al cumplimiento de las condiciones establecidas.

**¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?**

Los tipos de condiciones de javascript son:

**Ciclos:**

- if else: ejecuta el bloque mientras la condicion sea verdadera
- Switch: se utiliza para controlar varios bloques de codigo con base a una misma condicional.

**¿Puedo combinar funciones y condicionales?**

Si, es posible combinar funciones y condicionales. Esta es una de las herramientas principales de los programas modernos. 

**Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:**

```jsx
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}

/// Codigo de Respuesta ///

let tipoDeSusctipcion = "Expert";

if (tipoDeSuscripcion == "Free") {
	 console.log("Solo puedes tomar los cursos gratis");}
else if (tipoDeSuscription == "Basic") {
	console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
}
else if (tipoDeSuscription == "Expert") {
	console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
}
else if (tipoDeSuscription == "ExpertPlus") {
	console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}
else {
console.log("Tipo de suscripcion no Reconocido");
}
```

**Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).**

💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays u objetos y un solo condicional.

```jsx
let tiposDeSuscripcion = [
	{tipo: "Free", mensaje: "Solo puedes tomar los cursos gratis"},
	{tipo: "Basic", mensaje: "Puedes tomar casi todos los cursos de Platzi durante un mes"},
	{tipo: "Expert", mensaje: "Puedes tomar casi todos los cursos de Platzi durante un año"},
	{tipo: "ExpertPlus", mensaje: "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"}
]

function tipoDeSuscription(suscripcion) {
	for (let i=0; i < tiposDeSuscription.length; i++) {
			if (tiposDeSuscription[i].tipo == suscription) {
					console.log(tiposDeSuscripcion.mensaje);
					return;
			}
	}
	console.log("Suscripcion Invalida)
}

tiposDeSuscripcion("Free");
```

**Responde las siguientes preguntas en la sección de comentarios:**

**¿Qué es un ciclo?**

Un ciclo es un bloque de codigo que se repite hasta que se cumplan una condicion.

**¿Qué tipos de ciclos existen en JavaScript?**

**For:** repeticion las veces mientras se cumpla una condicion predeterminada, en este caso se sabe cuantas veces se va a repetir el ciclo.

**While:** repeticion las veces mientras se cumpla una condicion predeterminada.

**¿Qué es un ciclo infinito y por qué es un problema?**

Un ciclo infinito es cuando la codicion de un ciclo nunca se cumple y el codigo se ejecuta de manera infinita.

**¿Puedo mezclar ciclos y condicionales?**

Si, es posible combinar ciclos y condicionales. esto es la base  del desarrollo de codigo moderno.

**Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:**

```jsx

**// Replicacion de Codigo  //**

for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

let i = 1;
while (i < 5) {
	console.log("El valor de i es: " + i);
	i = i + 1;
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}

let i = 10;
while (i >=2) {
	console.log("El Valor de i es: " + i)
	i = i - 1;
}
```

**Escribe un código en JavaScript que le pregunte a los usuarios cuánto es `2 + 2`. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.**

Pista: puedes usar la función prompt de JavaScript.

```jsx
let respuesta = '';
do {
    
	respuesta = Number(prompt('Cuanto es 2 + 2?:'));
	if (respuesta =='4') {
		alert('Felicitaciones! Eso es Correcto!');
  } else {
		alert('Eso no es correcto. Por favor, intentalo de nuevo.');
	}
} while (respuesta !='4');

```

**Listas**

**Responde las siguientes preguntas en la sección de comentarios:**

**¿Qué es un array?**

Es una estructura de manejo de datos que permite crear coleccion ordenada de elementos. 

**¿Qué es un objeto?**

Es una coleccion de propiedades, donde cada propiedad donde cada propiedas esta relacionados entre clave y un valor. Un valor de propiedad puede ser una funcion, que entonces considerada un metodo del objeto.

 
**¿Cuándo es mejor usar objetos o arrays?**

Usa un array cuando se necesite una lista ordenada de elementos. Usa un objeto cuando necesites agrupar datos relacionados y funcionalidades.

**¿Puedo mezclar arrays con objetos o incluso objetos con arrays?**

Si es posible mezclarlos. Aqui unos ejemplos de como podria mezclarse.

```jsx
**// Un Array de Objetos**
let estudiantes = [
  { nombre: 'Maria', edad: 20 },
  { nombre: 'Carlos', edad: 21 },
  { nombre: 'Ana', edad: 19 }
];
```

```jsx
**// Un objeto con propiedades que son Arrays**
let estudiante = {
  nombre: 'Maria',
  cursos: ['Matemáticas', 'Ciencias', 'Historia']
};
```

```jsx
**// Un Objeto con propiedades que son objetos
let estudiante = {
  nombre: 'Maria',
  direccion: {
    calle: 'Calle 123',
    ciudad: 'Ciudad XYZ',
    pais: 'País ABC'
  }
};**

```

```jsx
// Un array de arrays

let matriz = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];
```

**Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.**

```jsx
arrayto = ['primero','dos','tres','cuatro'];

function imprimirArreglo(array) {
	alert(array[0])
}

imprimirArreglo(arrayto);
```

**Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).**

```jsx
arrayto = ['primero','dos','tres','cuatro'];

function imprimirArreglo(array) {
	for (let i=0; i<=array.length; i++) {
			alert(array[i])
	}
}

imprimirArreglo(arrayto);
```

**Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).**

```jsx
let vehiculo = {
  marca: 'Toyota',
  modelo: 'Corolla',
  color: 'Azul',
  año: 2020,
  tipo: 'Sedán',
  kilometraje: 15000
};

function imprimirVehiculo(vehiculo) {
		for (let propiedad in vehiculo) {
					console.log(propiedad + ": " + vehiculo[propiedad]);
		}
}

imprimirVehiculo(vehiculo);
```

**¿Cómo te fue? 🏆**

¡**Felicidades por completar la prueba de JavaScript! Confío en que hayas completado cada paso y hayas pausado para repasar los temas de los ejercicios que se te complicaron.**

**Ahora sí, continúa a la siguiente clase, pero recuerda que ya no puedes abandonar el curso, debes completarlo hasta el final. No importa cuánto tiempo te tome. Yo sé que tú puedes. Y tú deberías de saberlo también.**

**¡Te espero en la siguiente clase para comenzar!**

## Variables
