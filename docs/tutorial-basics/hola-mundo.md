---
sidebar_position: 2
---

# Hola Mundo


Creación de un "Hola Mundo" en TypeScript

En esta guía, aprenderás cómo crear y ejecutar un programa "Hola Mundo" en TypeScript paso a paso.

## Requisitos previos

Antes de comenzar, asegúrate de tener Node.js y TypeScript instalados en tu sistema. Puedes instalar TypeScript globalmente utilizando npm con el siguiente comando:

```bash
npm install -g typescript
```

## Paso 1: Crear un archivo TypeScript

Crea un nuevo archivo llamado hola-mundo.ts utilizando tu editor de texto o IDE favorito. Este será nuestro archivo fuente para nuestro programa "Hola Mundo".

```typescript 
// hola-mundo.ts
const msg: string = 'Hola Mundo';
console.log(msg);
```

- const: Es para crear una variable que no puede cambiar su valor.
- msg: Es el nombre de la variable que contiene el mensaje.
- : string: Indica que el tipo de datos de la variable msg es una cadena de texto.
- 'Hola Mundo': Es el mensaje que estamos guardando en la variable msg.
- console.log(msg): Muestra el contenido de la variable msg en la consola.

## Paso 2: Compilar el archivo TypeScript

Una vez que hayas escrito el código TypeScript, necesitas compilarlo a JavaScript. Abre tu terminal, navega hasta el directorio donde se encuentra tu archivo hola-mundo.ts y ejecuta el siguiente comando:

```bash 
tsc hola-mundo.ts
```

### Paso 3: Ejecutar el programa

Ahora que tenemos nuestro archivo JavaScript, podemos ejecutar nuestro programa "Hola Mundo". En la misma terminal, ejecuta el siguiente comando:

```bash 
node hola-mundo.js
```

Deberías ver el siguiente resultado en tu terminal:

```bash
¡Hola Mundo desde TypeScript!
```


Documents are **groups of pages** connected through:

- a **sidebar**
- **previous/next navigation**
- **versioning**

## Create your first Doc

Create a Markdown file at `docs/hello.md`:

```md title="docs/hello.md"
# Hello

This is my **first Docusaurus document**!
```

A new document is now available at [http://localhost:3000/docs/hello](http://localhost:3000/docs/hello).

## Configure the Sidebar

Docusaurus automatically **creates a sidebar** from the `docs` folder.

Add metadata to customize the sidebar label and position:

```md title="docs/hello.md" {1-4}
---
sidebar_label: 'Hi!'
sidebar_position: 3
---

# Hello

This is my **first Docusaurus document**!
```

It is also possible to create your sidebar explicitly in `sidebars.js`:

```js title="sidebars.js"
export default {
  tutorialSidebar: [
    'intro',
    // highlight-next-line
    'hello',
    {
      type: 'category',
      label: 'Tutorial',
      items: ['tutorial-basics/create-a-document'],
    },
  ],
};
```
