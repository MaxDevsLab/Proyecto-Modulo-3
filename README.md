# 🖥 Aplicación de Consola JS — Módulo 3

| | |
|---|---|
| 📅 **Fecha** | 23 de febrero de 2026 |
| 👩‍🏫 **Docente** | Sabina Romero |
| 🎓 **Estudiante** | Maximiliano Vilugrón |
| 📚 **Módulo** | 3 — Fundamentos de Programación en JavaScript |


Aplicación JavaScript que se ejecuta en la **consola del navegador**. Cubre los 5 pasos del ABP: introducción al lenguaje, variables y condicionales, arreglos y ciclos, funciones y objetos.

---

## 📁 Estructura del Proyecto

```
consola-app/
├── index.html   → Página de instrucciones para abrir la consola
├── style.css    → Archivo .css con estilos del index.html
├── app.js       → Aplicación completa (5 lecciones)
└── README.md    → Este archivo
```

---

## 🚀 Cómo ejecutar

1. Abre `index.html` con doble clic en tu navegador.
2. Abre la consola del navegador:
   - **Windows/Linux:** `F12` → pestaña "Consola"
   - **Mac:** `Cmd + Opt + J`
   - O: clic derecho → "Inspeccionar" → "Consola"
3. Para iniciar la app debes ejecutar la fx iniciarApp() en la consola,
   a continiuación pedirá tu nombre y se iniciará la app.
5. Responde los `prompt()` con los datos que se solicitan.

> ✅ No requiere instalación, servidor ni conexión a internet.

---

## 📐 Paso a paso — Las 5 Lecciones

### Lección 1 — Introducción a JavaScript

**Conceptos:** `console.log()`, `prompt()`, `alert()`

```javascript
// Mostrar mensajes en la consola
console.log('¡Hola mundo!');

// Pedir datos al usuario (devuelve un string)
const nombre = prompt('¿Cuál es tu nombre?') || 'Estudiante';

// Mostrar un aviso emergente
alert(`¡Hola, ${nombre}!`);
```

---

### Lección 2 — Variables, Operaciones y Condicionales

**Conceptos:** `let`, `const`, operadores matemáticos, `if/else`, `switch`

```javascript
const APP_VERSION = '1.0.0';    // const: no cambia
let resultado = 0;               // let: puede cambiar

const num1 = Number(prompt('Primer número:'));
const suma  = num1 + num2;

// if / else if / else
if (resultado > 100) {
    console.log('Número GRANDE');
} else if (resultado > 10) {
    console.log('Número MEDIANO');
} else {
    console.log('Número PEQUEÑO');
}

// switch: múltiples casos
switch (diaSemana) {
    case 1: console.log('Lunes'); break;
    case 5: console.log('Viernes'); break;
    default: console.log('Otro día');
}
```

---

### Lección 3 — Arreglos y Ciclos

**Conceptos:** Arrays `[]`, `for`, `for...of`, `while`, `filter()`, `push()`

```javascript
const numeros = [15, 3, 42, 8, 27, 11];

// for: cuando sabes cuántas veces repetir
for (let i = 0; i < numeros.length; i++) {
    console.log(numeros[i]);
}

// for...of: recorrer array directamente (ES6)
for (const num of numeros) {
    console.log(num * num);
}

// while: cuando no sabes cuántas veces repetir
let pos = 0;
while (pos < numeros.length) {
    if (numeros[pos] > 20) break;
    pos++;
}

// filter(): crear nuevo array con condición
const pares = numeros.filter(n => n % 2 === 0);

// push(): agregar al final
const lista = [];
lista.push('elemento');
```

---

### Lección 4 — Funciones

**Conceptos:** `function`, parámetros con default, `return`, arrow functions, funciones dentro de funciones

```javascript
// Función básica
function sumar(a, b) {
    return a + b;
}

// Parámetro con valor por defecto (si no se envía, usa 1)
function dividir(a, b = 1) {
    if (b === 0) return 'Error: división por cero';
    return a / b;
}

// Arrow function (ES6) — forma corta
const elevarAlCuadrado = (n) => n * n;
const esPar            = (n) => n % 2 === 0;

// Función que llama a otras funciones
function calcularArea(base, altura) {
    return multiplicar(base, altura); // llama a otra función
}

// Función que devuelve un objeto con estadísticas
function calcularEstadisticas(arr) {
    return {
        suma:     arr.reduce((acc, n) => acc + n, 0),
        min:      Math.min(...arr),
        max:      Math.max(...arr),
        promedio: (arr.reduce((acc, n) => acc + n, 0) / arr.length).toFixed(2)
    };
}
```

---

### Lección 5 — Objetos

**Conceptos:** `{}`, propiedades, métodos, `this`, array de objetos, `forEach()`, `map()`

```javascript
// Crear un objeto
const estudiante = {
    nombre:   'Ana',
    modulo:   3,
    aprobado: true,

    // Método: función dentro del objeto
    presentarse: function() {
        return `Soy ${this.nombre}, módulo ${this.modulo}`;
    }
};

// Acceder con punto
console.log(estudiante.nombre);
console.log(estudiante.presentarse());

// Array de objetos
const cursos = [
    { id: 1, nombre: 'HTML',        completado: true  },
    { id: 2, nombre: 'JavaScript',  completado: false },
];

// forEach: ejecutar algo por cada elemento (no devuelve nada)
cursos.forEach(curso => {
    console.log(curso.nombre, curso.completado);
});

// map: transformar cada elemento (devuelve nuevo array)
const nombres = cursos.map(curso => curso.nombre);
// → ['HTML', 'JavaScript']
```

---

## 🧩 Tabla de conceptos

| Concepto | Descripción | Ejemplo |
|---|---|---|
| `console.log()` | Mostrar en la consola | `console.log('hola')` |
| `prompt()` | Pedir dato al usuario | `const n = prompt('nombre?')` |
| `alert()` | Mostrar aviso emergente | `alert('¡Bienvenido!')` |
| `let` | Variable que cambia | `let contador = 0` |
| `const` | Constante, no cambia | `const PI = 3.14` |
| `if/else` | Bifurcación condicional | `if (x > 0) { ... }` |
| `switch` | Múltiples casos | `switch(n) { case 1: ... }` |
| Array `[]` | Lista de elementos | `const lista = [1, 2, 3]` |
| `for` | Ciclo con contador | `for (let i=0; i<n; i++)` |
| `while` | Ciclo con condición | `while (condicion) { ... }` |
| `filter()` | Filtrar array | `arr.filter(x => x > 5)` |
| `push()` | Agregar al array | `arr.push(elemento)` |
| `function` | Definir función | `function suma(a,b){ return a+b }` |
| Arrow fn | Función corta | `(n) => n * 2` |
| `return` | Devolver un valor | `return resultado` |
| Objeto `{}` | Colección clave-valor | `{ nombre: 'Ana', edad: 20 }` |
| `this` | Referencia al objeto actual | `this.nombre` |
| `forEach()` | Recorrer array | `arr.forEach(x => ...)` |
| `map()` | Transformar array | `arr.map(x => x * 2)` |

---

## ✅ Checklist de validación

| Criterio | Estado |
|---|---|
| `console.log()` para mostrar mensajes | ✅ |
| `prompt()` para recibir datos del usuario | ✅ |
| `alert()` para mostrar aviso | ✅ |
| Variables con `let` y `const` | ✅ |
| Operaciones matemáticas (suma, resta, mult, div) | ✅ |
| Estructura `if / else if / else` | ✅ |
| Estructura `switch` | ✅ |
| Arreglo con lista de elementos | ✅ |
| Ciclo `for` con recorrido de arreglo | ✅ |
| Ciclo `while` con condición | ✅ |
| `filter()` para filtrar elementos | ✅ |
| Al menos 3 funciones con parámetros y `return` | ✅ |
| Arrow functions | ✅ |
| Función que llama a otras funciones | ✅ |
| Objeto con propiedades y métodos | ✅ |
| Uso de `this` dentro de un método | ✅ |
| Array de objetos con `map()` y `forEach()` | ✅ |
| Comentarios explicativos en el código | ✅ |

---

## 🛠️ Tecnologías

- HTML5
- JavaScript ES6+ (la app es JavaScript puro, el HTML solo es la pantalla de inicio)
