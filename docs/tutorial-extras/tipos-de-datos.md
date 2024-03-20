---
sidebar_position: 1
---

# Tipos de datos

En TypeScript, hay varios tipos de datos disponibles para definir variables. Aquí hay una lista de los tipos de datos básicos:

## 1. Números (number)

Representa tanto enteros como números de punto flotante.

```ts
let edad: number = 30;
let precio: number = 10.5;
```

## 2. Cadenas de Texto (string)

Representa secuencias de caracteres, como palabras o frases.

```ts
let nombre: string = "Juan";
let mensaje: string = "¡Hola Mundo!";
```

## 3. Booleanos (boolean)

Representa valores lógicos verdadero o falso.

```ts
let activo: boolean = true;
let esMayorDeEdad: boolean = edad >= 18;
```

## 4. Arreglos (array)

Representa una colección de elementos del mismo tipo.

```ts
let numeros: number[] = [1, 2, 3, 4, 5];
let colores: string[] = ["rojo", "verde", "azul"];
```

## 5. Tuplas (tuple)

Permite expresar un arreglo con un número fijo de elementos, cuyos tipos son conocidos, pero no necesariamente del mismo tipo.

```ts
let persona: [string, number] = ["Juan", 30];
```

## 6. Objetos (object)

Representa una colección de pares clave-valor.

```ts
let empleado: { nombre: string; edad: number } = { nombre: "Ana", edad: 25 };
```

## 7. Tipos de Datos Especiales

- Any: Representa cualquier tipo de dato. Se utiliza cuando no conocemos el tipo de dato en tiempo de compilación.

```ts
let variable: any = 10;
variable = "Hola";
```

- Void: Indica la ausencia de tipo, típicamente se utiliza como tipo de retorno de funciones que no devuelven ningún valor.

```ts
function imprimirMensaje(): void {
  console.log("Hola Mundo");
}
```

Estos son algunos de los tipos de datos más comunes en TypeScript. Puedes encontrar otros tipos más avanzados y personalizados según tus necesidades.

# Manage Docs Versions

Docusaurus can manage multiple versions of your docs.

## Create a docs version

Release a version 1.0 of your project:

```bash
npm run docusaurus docs:version 1.0
```

The `docs` folder is copied into `versioned_docs/version-1.0` and `versions.json` is created.

Your docs now have 2 versions:

- `1.0` at `http://localhost:3000/docs/` for the version 1.0 docs
- `current` at `http://localhost:3000/docs/next/` for the **upcoming, unreleased docs**

## Add a Version Dropdown

To navigate seamlessly across versions, add a version dropdown.

Modify the `docusaurus.config.js` file:

```js title="docusaurus.config.js"
export default {
  themeConfig: {
    navbar: {
      items: [
        // highlight-start
        {
          type: "docsVersionDropdown",
        },
        // highlight-end
      ],
    },
  },
};
```

The docs version dropdown appears in your navbar:

![Docs Version Dropdown](./img/docsVersionDropdown.png)

## Update an existing version

It is possible to edit versioned docs in their respective folder:

- `versioned_docs/version-1.0/hello.md` updates `http://localhost:3000/docs/hello`
- `docs/hello.md` updates `http://localhost:3000/docs/next/hello`
