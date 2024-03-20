---
sidebar_position: 1
---

# Introduccion

TypeScript es un lenguaje de programación de código abierto desarrollado y mantenido por Microsoft. Es un superconjunto de JavaScript que agrega tipos estáticos opcionales a la sintaxis de JavaScript estándar. Esto permite a los desarrolladores detectar y corregir errores en tiempo de compilación en lugar de en tiempo de ejecución, lo que puede llevar a un código más robusto y menos propenso a errores.

**Características principales:**

- **Tipado estático:** TypeScript permite definir tipos estáticos para variables, parámetros de función y valores de retorno, lo que ayuda a detectar errores de tipo durante el desarrollo.

- **Compatibilidad con JavaScript:** Al ser un superconjunto de JavaScript, TypeScript es compatible con el código JavaScript existente, lo que facilita la adopción gradual del lenguaje.

- **Compilación:** El código TypeScript se compila a JavaScript estándar, lo que significa que puede ser ejecutado en cualquier entorno que admita JavaScript.

- **Orientado a objetos:** TypeScript soporta características orientadas a objetos como clases, interfaces, herencia y módulos, lo que facilita la construcción y organización de código.

- **Herramientas de desarrollo:** Dispone de herramientas de desarrollo integradas como IntelliSense, que proporciona sugerencias de código y detección de errores en tiempo real durante la edición del código en editores compatibles como Visual Studio Code.

- **Adopción comunitaria:** TypeScript cuenta con una amplia comunidad de desarrolladores y una gran cantidad de bibliotecas y frameworks compatibles, lo que facilita el desarrollo de aplicaciones robustas y escalables.

**Ejemplo:**

```typescript
// Definición de una interfaz
interface Persona {
  nombre: string;
  edad: number;
}

// Función que recibe un objeto de tipo Persona
function saludar(persona: Persona) {
  return `Hola, ${persona.nombre}. Tienes ${persona.edad} años.`;
}

// Objeto de tipo Persona
const usuario = { nombre: 'Juan', edad: 30 };

// Llamada a la función
console.log(saludar(usuario));
```

# Tutorial Intro

Let's discover **Docusaurus in less than 5 minutes**.

## Getting Started

Get started by **creating a new site**.

Or **try Docusaurus immediately** with **[docusaurus.new](https://docusaurus.new)**.

### What you'll need

- [Node.js](https://nodejs.org/en/download/) version 18.0 or above:
  - When installing Node.js, you are recommended to check all checkboxes related to dependencies.

## Generate a new site

Generate a new Docusaurus site using the **classic template**.

The classic template will automatically be added to your project after you run the command:

```bash
npm init docusaurus@latest my-website classic
```

You can type this command into Command Prompt, Powershell, Terminal, or any other integrated terminal of your code editor.

The command also installs all necessary dependencies you need to run Docusaurus.

## Start your site

Run the development server:

```bash
cd my-website
npm run start
```

The `cd` command changes the directory you're working with. In order to work with your newly created Docusaurus site, you'll need to navigate the terminal there.

The `npm run start` command builds your website locally and serves it through a development server, ready for you to view at http://localhost:3000/.

Open `docs/intro.md` (this page) and edit some lines: the site **reloads automatically** and displays your changes.
