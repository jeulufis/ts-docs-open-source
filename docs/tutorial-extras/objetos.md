---
sidebar_position: 3
---

# Objetos

Los objetos en TypeScript pueden tener propiedades con tipos de datos específicos y métodos asociados.

```ts
// Definición de un objeto
let persona = {
  nombre: "Juan",
  edad: 30,
  saludar: function () {
    console.log(
      `¡Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años!`
    );
  },
};

// Acceso a las propiedades y métodos del objeto
console.log(persona.nombre); // Salida: Juan
console.log(persona.edad); // Salida: 30
persona.saludar(); // Salida: ¡Hola, mi nombre es Juan y tengo 30 años!
```

## Tipos de Objetos

También puedes definir tipos específicos para tus objetos usando interfaces o tipos.

```ts
// Definición de una interfaz para un objeto Persona
interface Persona {
  nombre: string;
  edad: number;
  saludar: () => void;
}

// Creación de un objeto que cumple con la interfaz Persona
let juan: Persona = {
  nombre: "Juan",
  edad: 30,
  saludar: function () {
    console.log(
      `¡Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años!`
    );
  },
};

juan.saludar(); // Salida: ¡Hola, mi nombre es Juan y tengo 30 años!
```

Estos son algunos de los conceptos básicos relacionados con funciones y objetos en TypeScript. Puedes explorar más sobre estos temas y sus características adicionales en la documentación oficial de TypeScript.

## Métodos Dentro de los Objetos

Los objetos en TypeScript pueden tener métodos, que son funciones asociadas a ese objeto y pueden acceder a las propiedades del objeto utilizando la palabra clave this.

```ts
let persona = {
  nombre: "Ana",
  edad: 25,
  saludar: function () {
    console.log(
      `¡Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años!`
    );
  },
};

persona.saludar(); // Salida: ¡Hola, mi nombre es Ana y tengo 25 años!
```

## Tipos Personalizado

En TypeScript, puedes crear tus propios tipos de datos personalizados utilizando interfaces o tipos.

### Interface

```ts
interface Persona {
  nombre: string;
  edad: number;
}

let usuario: Persona = {
  nombre: "María",
  edad: 30,
};
```

### Tipo

```ts
// Definición de un tipo personalizado 'Empleado' que incluye una función 'calcularSalarioAnual'
type Empleado = {
  nombre: string;
  salario: number;
  calcularSalarioAnual: () => number;
};

// Ejemplo de objeto empleado
let empleado: Empleado = {
  nombre: "Pedro",
  salario: 30000,
  calcularSalarioAnual: function () {
    return this.salario * 12;
  },
};

// Uso de la función dentro del objeto
console.log(empleado.calcularSalarioAnual()); // Salida: 360000
```

## Múltiples Tipos Permitidos

En TypeScript, puedes especificar que una variable puede tener múltiples tipos utilizando el operador de unión |.

```ts
let resultado: number | string;

resultado = 10; // Válido
console.log(resultado); // Salida: 10

resultado = "error"; // También válido
console.log(resultado); // Salida: error
```

Estos son algunos conceptos básicos y ejemplos sobre objetos, métodos, tipos personalizados y múltiples tipos permitidos en TypeScript. Puedes profundizar más en cada uno de estos temas en la documentación oficial de TypeScript.
