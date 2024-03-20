---
sidebar_position: 2
---

# Clases

## ¿Qué es una Clase en TypeScript?

En TypeScript, una clase es una plantilla para crear objetos que poseen propiedades y métodos. Las clases permiten organizar y estructurar el código de una manera más eficiente y orientada a objetos.

## Definición de la Clase Persona

La clase Persona es un ejemplo básico que representa a una persona con dos propiedades: nombre y edad. Esta clase también tiene un método llamado saludar() que imprime un mensaje de saludo utilizando el nombre y la edad de la persona.

```ts
class Persona {
  nombre: string; // Propiedad para almacenar el nombre de la persona
  edad: number; // Propiedad para almacenar la edad de la persona

  constructor(nombre: string, edad: number) {
    this.nombre = nombre; // Inicializa la propiedad 'nombre' con el valor proporcionado
    this.edad = edad; // Inicializa la propiedad 'edad' con el valor proporcionado
  }

  saludar() {
    console.log(`Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años.`); // Imprime un mensaje de saludo
  }
}
```

### Explicación del Código

- La palabra clave class se utiliza para declarar una nueva clase llamada Persona.
- Dentro de la clase, se declaran dos propiedades: nombre de tipo string y edad de tipo number.
- El método constructor es un método especial que se llama automáticamente cuando se crea una nueva instancia de la clase Persona. - Este método acepta dos parámetros: nombre y edad, que se utilizan para inicializar las propiedades nombre y edad respectivamente.
- El método saludar() es un método de instancia que imprime un mensaje de saludo utilizando las propiedades nombre y edad de la persona.

## Asignación Corta de Propiedades en el Constructor

En el ejemplo proporcionado, la clase Persona utiliza la asignación corta de propiedades en el constructor para definir las propiedades nombre y edad. Veamos cómo funciona:

```ts
class Persona {
  constructor(public nombre: string, public edad: number) {}

  saludar() {
    console.log(`Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años.`);
  }
}
```

### Explicación del Código

- La palabra clave public se utiliza antes de los parámetros del constructor (nombre y edad). Esto indica que estas propiedades son públicas y se pueden acceder desde fuera de la clase.
- Dentro del constructor, las propiedades nombre y edad se declaran y se inicializan directamente con los valores proporcionados como parámetros del constructor. No es necesario definir explícitamente las propiedades dentro de la clase.

### Ventajas

- Legibilidad: La asignación corta de propiedades en el constructor hace que el código sea más conciso y legible, ya que declara e inicializa las propiedades en un solo lugar.
- Reducción de Código: Elimina la necesidad de escribir líneas adicionales para declarar e inicializar las propiedades en la clase.

### Uso de la Clase Persona

El uso de la clase Persona sigue siendo el mismo que en el ejemplo anterior. Se pueden crear instancias de Persona y llamar a su método saludar() de la misma manera.

```ts
// Crear una nueva instancia de Persona
let persona1 = new Persona("Juan", 30);

// Llamar al método saludar() de la instancia persona1
persona1.saludar(); // Imprime: Hola, mi nombre es Juan y tengo 30 años.## Métodos Públicos y Privados
```

## Métodos Públicos y Privados

Los métodos públicos son accesibles desde fuera de la clase, mientras que los métodos privados solo son accesibles desde dentro de la clase misma. Esto proporciona encapsulamiento y control sobre el acceso a los miembros de la clase.

```ts
class Persona {
  private dni: string;

  constructor(public nombre: string, public edad: number, dni: string) {
    this.dni = dni;
  }

  public saludar() {
    console.log(`Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años.`);
  }

  private obtenerDni() {
    return this.dni;
  }
}
```

### Explicación del Código

- La palabra clave private se utiliza para declarar la propiedad dni, lo que la convierte en privada y solo accesible dentro de la clase Persona.
- El constructor de la clase Persona acepta tres parámetros: nombre, edad y dni. Este último se utiliza para inicializar la propiedad dni de la clase.
- El método saludar() es un método público que imprime un mensaje de saludo utilizando las propiedades nombre y edad.
- El método obtenerDni() es un método privado que devuelve el valor de la propiedad dni. Este método solo puede ser llamado desde dentro de la clase Persona.

## Herencia con super y extends

La herencia es un concepto importante en la programación orientada a objetos que permite a una clase heredar propiedades y métodos de otra clase. En TypeScript, se utiliza la palabra clave extends para establecer una relación de herencia entre clases. Además, la palabra clave super se utiliza dentro del constructor de una clase derivada para llamar al constructor de la clase base y pasarle argumentos.

```ts
class Persona {
  nombre: string;
  edad: number;
  private dni: string;

  constructor(nombre: string, edad: number, dni: string) {
    this.nombre = nombre;
    this.edad = edad;
    this.dni = dni;
  }

  saludar() {
    console.log(`Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años.`);
  }

  obtenerDni() {
    return this.dni;
  }
}

class Empleado extends Persona {
  cargo: string;

  constructor(nombre: string, edad: number, dni: string, cargo: string) {
    super(nombre, edad, dni);
    this.cargo = cargo;
  }

  presentarse() {
    console.log(
      `Hola, soy ${this.nombre}, tengo ${this.edad} años y trabajo como ${this.cargo}.`
    );
  }
}
```

### Uso de las Clases Persona y Empleado

Después de definir ambas clases, se pueden crear instancias de ellas y llamar a sus métodos como se muestra a continuación:

```ts
// Crear una nueva instancia de Persona
let persona1 = new Persona("Juan", 30, "12345678A");

// Llamar al método saludar() de la instancia persona1
persona1.saludar(); // Imprime: Hola, mi nombre es Juan y tengo 30 años.

// Crear una nueva instancia de Empleado
let empleado1 = new Empleado("Ana", 25, "98765432B", "Gerente");

// Llamar al método presentarse() de la instancia empleado1
empleado1.presentarse(); // Imprime: Hola, soy Ana, tengo 25 años y trabajo como Gerente.
```

## Getters y Setters

Los getters y setters son métodos especiales que permiten acceder y modificar los valores de propiedades privadas de una clase de manera controlada. En TypeScript, puedes definir getters y setters utilizando las palabras clave get y set, respectivamente.

En el ejemplo proporcionado, la clase Persona utiliza un getter y un setter para la propiedad \_edad. Veamos cómo funciona:

```ts
class Persona {
  private _edad: number;

  constructor(public nombre: string, edad: number) {
    this._edad = edad;
  }

  get edad(): number {
    return this._edad;
  }

  set edad(nuevaEdad: number) {
    if (nuevaEdad > 0) {
      this._edad = nuevaEdad;
    }
  }
}
```

### Explicación del Código

- La clase Persona tiene una propiedad privada \_edad para almacenar la edad de la persona.
- En el constructor de la clase Persona, se inicializa la propiedad \_edad con el valor proporcionado.
- Se define un getter para la propiedad edad utilizando la palabra clave get. Este getter permite acceder al valor de la edad desde fuera de la clase.
- Se define un setter para la propiedad edad utilizando la palabra clave set. Este setter permite establecer el valor de la edad, con una validación para asegurar que la nueva edad sea mayor que cero.

## Clases Abstractas

Las clases abstractas son aquellas que no se pueden instanciar directamente, sino que deben ser extendidas por otras clases

```ts
abstract class Figura {
  abstract area(): number; // Método abstracto que debe ser implementado por las clases hijas
}

class Circulo extends Figura {
  constructor(private radio: number) {
    super(); // Llama al constructor de la clase base Figura (aunque no es necesario en este caso)
  }

  area(): number {
    return Math.PI * this.radio ** 2; // Implementación del método area() para calcular el área de un círculo
  }
}
```

### Explicación del Código

- La clase Figura es una clase abstracta que define un método abstracto area(). Como es abstracta, no se puede instanciar directamente.
- La clase Circulo extiende de la clase Figura, lo que significa que debe implementar el método area() definido en la clase base.
- En el constructor de la clase Circulo, se inicializa el radio del círculo.
- Se proporciona una implementación concreta del método area() en la clase Circulo, que calcula el área del círculo utilizando la fórmula πr².

### Uso de la Clase Circulo

```ts
// Crear una nueva instancia de Circulo
let circulo = new Circulo(5);

// Calcular el área del círculo utilizando el método area()
console.log(circulo.area()); // Imprime: 78.53981633974483 (aproximadamente)
```

## Constructores Privados

Puedes definir constructores privados en una clase para evitar que la clase sea instanciada directamente desde fuera de la misma. Esto es útil cuando quieres controlar la creación de instancias y asegurarte de que solo haya una instancia de la clase en toda la aplicación

```ts
class Singleton {
  private static instancia: Singleton;

  private constructor() {}

  static obtenerInstancia(): Singleton {
    if (!Singleton.instancia) {
      Singleton.instancia = new Singleton();
    }
    return Singleton.instancia;
  }
}
```

### Explicación del Código

- La clase Singleton tiene un constructor privado, lo que significa que no se puede instanciar directamente desde fuera de la clase.
- La propiedad instancia es una propiedad estática que almacena la única instancia de la clase Singleton.
- El método estático obtenerInstancia() se utiliza para obtener la instancia única de la clase. Si la instancia aún no existe, se crea una nueva instancia y se asigna a la propiedad instancia, de lo contrario, se devuelve la instancia existente.

Estos son algunos de los conceptos básicos y características avanzadas que puedes utilizar al definir y trabajar con clases en TypeScript.
