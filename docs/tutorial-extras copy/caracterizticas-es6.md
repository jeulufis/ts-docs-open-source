---
sidebar_position: 1
---

# Caracterizticas de ES6

## Variables let en TypeScript

En TypeScript, let es una palabra clave que se utiliza para declarar variables locales con ámbito de bloque.

```typescript
let x: number = 10;
```

La diferencia principal entre let y var es que let tiene un alcance de bloque, lo que significa que la variable solo es accesible dentro del bloque en el que fue declarada.

## Destructuración de Objetos en TypeScript

La destructuración de objetos en TypeScript permite extraer valores de objetos y asignarlos a variables individuales.

```ts
let persona = { nombre: "Juan", edad: 30 };
let { nombre, edad } = persona;

console.log(nombre); // Salida: Juan
console.log(edad); // Salida: 30
```

## Destructuración de Arreglos en TypeScript

La destructuración de arreglos en TypeScript permite extraer valores de arreglos y asignarlos a variables individuales.

```ts
let numeros = [1, 2, 3];
let [a, b, c] = numeros;

console.log(a); // Salida: 1
console.log(b); // Salida: 2
console.log(c); // Salida: 3
```

## Ciclo for...of en TypeScript

El ciclo for...of en TypeScript permite iterar sobre elementos de una colección, como arreglos o cadenas de texto

```ts
let colores = ["rojo", "verde", "azul"];
for (let color of colores) {
  console.log(color);
}
```

Este ciclo es especialmente útil para iterar sobre arreglos y cadenas de texto de una manera más legible y concisa.

## Clases de ES6 en TypeScript

Las clases de ES6 son una característica importante que TypeScript también soporta completamente. Permiten definir estructuras de datos y comportamientos utilizando una sintaxis de clase más limpia y orientada a objetos.

```ts
class Persona {
  nombre: string;
  edad: number;

  constructor(nombre: string, edad: number) {
    this.nombre = nombre;
    this.edad = edad;
  }

  saludar() {
    console.log(`Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años.`);
  }
}

let persona1 = new Persona("Ana", 25);
persona1.saludar(); // Salida: Hola, mi nombre es Ana y tengo 25 años.
```

Las clases en TypeScript son una herramienta poderosa para organizar y estructurar tu código de manera orientada a objetos. Permiten la encapsulación de datos y comportamientos en una sola unidad, lo que facilita la reutilización y el mantenimiento del código.
