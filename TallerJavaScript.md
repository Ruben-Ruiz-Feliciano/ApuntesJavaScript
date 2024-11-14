Lenguaje Makdown :
Objetivo:Proporcionar una herramienta para documentar codigo,
o aspectos tecnicos para compartirlos o tenerlos de referencia en Git U
Otra plataforma  


Makdown es un lenguaje de mercado ligero creado en el 2004
John Gruber, trata de conseguir la maxima legibilidad y .....

El objetivo de su creador fue hacer que la gente pudiera escribir usando
un formato de texto palno facil de leer, facil de escribir y con la 
posibilidad de convertir su documento en HTML valido

La gran simpleza de su sintaxis hizo que tuviera una rapida
adaptacion y popularidad en la comunidad de desarrolladores.

Actualmente aparte de permitir generar codigo HTML de forma
dinamica, tambien se emplea (casi deforma estandar) para la creacion
de documentacion tecnica y con la proliferacion de la arquictectura



Conocer sintaxis Mardown
1.-Parrafos [Parrafo 1...]
Lorem Ipsum es simplemente el texto de relleno de las imprentas y archivos de texto. Lorem Ipsum ha sido el texto de relleno estándar de las industrias desde el año 1500, cuando un impresor (N. del T. persona que se dedica a la imprenta) desconocido usó una galería de textos y los mezcló de tal manera que logró hacer un libro de textos especimen. No sólo sobrevivió 500 años, sino que tambien ingresó como texto de relleno en documentos electrónicos, quedando esencialmente igual al original. Fue popularizado en los 60s con la creación de las hojas "Letraset", las cuales contenian pasajes de Lorem Ipsum, y más recientemente con software de autoedición, como por ejemplo Aldus PageMaker, el cual incluye versiones de Lorem Ipsum.



cursivo
*negrita*
tachado
_cursiva y negrita
cursiva y tachado
*negrita y tachado*
*cursiva, negrita y tachado*
encabezados
#Encabezado Nivel 1
## Encabezado Nivel 2
### Encabezado Nivel 3
#### Encabezado Nivel 4
##### Encabezado Nivel 5
###### Encabezado Nivel 6

Divisiones
Un bloque de contenido
---
Este es otro bloque de contenido 


listas 
podemos utilizar las listas ordenadas y listas desordenadas

1. html5
1. css
1. javascript
1. Ajax
1. Json

listas desordenadas
- html5
- css
- javascript
- ajax
- json

Citas
Podemos dar formato de cita a un texto anteponiendo a la linea de texto un caracter de mayor que (>).
>la IA en el futuro remplazara muchas profesiones de TI. -
Ruben

>Chat Gpt debe poteciar el aprendizaje no suprimir mi estado autodidacta
>
>Ruben Ruiz Feliciano

enlaces

[YouTube](https://www.youtube.com)
[Enlace a Google](https://www.google.com)

Imagenes

![Texto alternativo](URLdelaimagen)


tablas
|Columna 1|Columna 2|Columna 1|
|---------|---------|---------|  
|A        |    B    |    C    |
|D        |    E    |    F    |
|G        |    H    |    I    |


codigo 
podemos dar formato de codigo a un texto para ello se usa el acento grave(`).

este es codigo en linea.

En javascript una varible se define asi:
let saludo = "Hola Mundo;



pero si queremos sacar un bloque completo de codigo utilizamos :

   
js
let estudiante="juan perez";
let edad=19;
let isestudiante=true;
let calificacion=90.0;

<!--esto es un comentario-->
   
//alert("Estamos en el archivo EstructuraCiclo.js");

//Estructura de control for
for(let i=0; i<=10; i++){
	console.log("No interacion: "+ i);
}

//estructura de control while
let contador=1;

while(contador < 10){
	console.log("[while]No interacion: "+ contador);
	contador++;
}
//Estructura de control do/while
let numero=1;
do{
	console.log("[do/while]No interacion: " + numero);
	numero++;
}while (numero < 10);

//for in
//este bucle itera las propiedades enumerables de un objeto 
let estudiante = { nombre:"Juan Perez", edad:19, calificacion:80 };
for (let propiedad in estudiante){
	console.log(propiedad + ": " + estudiante[propiedad]);
}

//Bucle for..of
//Este ciclo itera sobre los valores de un objeto iterable (como un array)
let mis_numeros=[10,20,30,40,50];
for (let numero of mis_numeros) {
	console.log(numero);
}

console.log("Bienvenido Aquí calcularás tu IMC");

let peso;
let altura;

peso = prompt("Ingresa tu peso en kg:");
altura = prompt("Ingresa tu altura en metros:");

// Convertir las entradas a números
peso = parseInt(peso);
altura = parseInt(altura);

if (peso > 0 && altura > 0) {
    // Calcular el IMC
    let imc = peso / (altura * altura);
    let rango;

    // Determinar el rango del IMC
    if (imc < 18.5) {
        rango = "Bajo peso";
    } else if (imc >= 18.5 && imc <= 24.9) {
        rango = "Normal";
    } else if (imc >= 25 && imc <= 29.9) {
        rango = "Sobrepeso";
    } else if (imc >= 30 && imc <= 34.9) {
        rango = "Obesidad I";
    } else if (imc >= 35 && imc <= 39.9) {
        rango = "Obesidad II";
    } else if (imc >= 40 && imc <= 49.9) {
        rango = "Obesidad III";
    } else if (imc >= 50) {
        rango = "Obesidad IV";
    }

    // Mostrar el resultado
    console.log("Tu IMC es: " + imc);
    console.log("Rango: " + rango);
} else {
    // Mostrar mensaje de error si los valores no son válidos
    console.log("Por favor, ingresa valores válidos para peso y altura.");
}
document.getElementById("emailForm").addEventListener("submit", function (e) {
  e.preventDefault();

  const to = document.getElementById("toEmail").value;
  const subject = document.getElementById("subject").value;
  const message = document.getElementById("message").value;

  fetch("/sendEmail", {
    method: "POST",
    headers: {
      "Content-Type": "application/x-www-form-urlencoded",
    },
    body: to=${encodeURIComponent(to)}&subject=${encodeURIComponent(subject)}&message=${encodeURIComponent(message)}
  })
  .then(response => response.json())
  .then(data => {
    if (data.status === "success") {
      document.getElementById("notification").innerText = "Correo enviado exitosamente";
      document.getElementById("notification").classList.add("text-success");
    } else {
      document.getElementById("notification").innerText = "Error al enviar el correo";
      document.getElementById("notification").classList.add("text-danger");
    }
  })
  .catch(error => {
    document.getElementById("notification").innerText = "Error al enviar el correo";
    document.getElementById("notification").classList.add("text-danger");
    console.error("Error:", error);
  });
});