---
sidebar_position: 3
---

# Interfaces

Las interfaces en TypeScript proporcionan un mecanismo para definir la estructura y el comportamiento esperado de los objetos en tu código. Son una herramienta poderosa para establecer contratos entre diferentes partes de tu aplicación y mejorar la legibilidad y mantenibilidad del código.

## 1. Interfaces Básicas

Las interfaces básicas definen la estructura de un objeto. Pueden incluir propiedades y métodos que deben ser implementados por las clases que las utilizan.

### Ejemplo de Interface Básica:

```ts
interface Punto {
  x: number;
  y: number;
}
```

## 2. Estructuras de Datos Complejas

Las interfaces pueden definir estructuras de datos más complejas, como arreglos, objetos anidados y combinaciones de otros tipos de datos.

### Ejemplo de Estructura de Datos Compleja:

```ts
interface Estudiante {
  nombre: string;
  edad: number;
  cursos: string[];
  direccion: {
    calle: string;
    ciudad: string;
    codigoPostal: number;
  };
}
```

## 3. Métodos en Interfaces

Las interfaces también pueden definir métodos que deben ser implementados por las clases que las utilizan. Estos métodos pueden tener parámetros y tipos de retorno.

### Ejemplo de Método en una Interfaz:

```ts
interface Calculadora {
  sumar(a: number, b: number): number;
  restar(a: number, b: number): number;
}
```

## 4. Interfaces en Clases

Las clases pueden implementar interfaces para asegurar que cumplen con ciertos contratos. Esto garantiza que la clase implemente todas las propiedades y métodos definidos en la interfaz.

### Ejemplo de Implementación de una Interfaz en una Clase:

```ts
class Rectangulo implements Punto {
  constructor(
    public x: number,
    public y: number,
    public ancho: number,
    public alto: number
  ) {}
}
```

## 5. Interfaces para Funciones

Las interfaces también se pueden utilizar para definir la firma de funciones, especificando los tipos de parámetros y el tipo de retorno esperado.

### Ejemplo de Interfaz para una Función:

```ts
interface OperacionMatematica {
  (a: number, b: number): number;
}
```
