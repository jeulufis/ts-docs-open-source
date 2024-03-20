---
sidebar_position: 2
---

# Funciones

## Parámetros Obligatorios

Los parámetros obligatorios son aquellos que deben ser proporcionados cuando se llama a la función. Si no se proporcionan, TypeScript generará un error.

```ts
function saludar(nombre: string): void {
  console.log(`¡Hola, ${nombre}!`);
}

saludar("Juan"); // Salida: ¡Hola, Juan!
saludar(); // Error: "Se requiere un argumento, pero se proporcionó 0."
```

## Parámetros Opcionales

Los parámetros opcionales son aquellos que pueden ser omitidos al llamar a la función. Para definir un parámetro como opcional, se usa el signo de interrogación ? después del nombre del parámetro.

```ts
function saludar(nombre?: string): void {
  if (nombre) {
    console.log(`¡Hola, ${nombre}!`);
  } else {
    console.log("¡Hola, mundo!");
  }
}

saludar("Juan"); // Salida: ¡Hola, Juan!
saludar(); // Salida: ¡Hola, mundo!
```

## Parámetros con Valor por Defecto

Los parámetros con valores por defecto son aquellos que tienen un valor predeterminado asignado en caso de que no se proporcione un valor al llamar a la función.

```ts
function saludar(nombre: string = "Mundo"): void {
  console.log(`¡Hola, ${nombre}!`);
}

saludar("Juan"); // Salida: ¡Hola, Juan!
saludar(); // Salida: ¡Hola, Mundo!
```

Let's translate `docs/intro.md` to French.

## Configure i18n

Modify `docusaurus.config.js` to add support for the `fr` locale:

```js title="docusaurus.config.js"
export default {
  i18n: {
    defaultLocale: "en",
    locales: ["en", "fr"],
  },
};
```

## Translate a doc

Copy the `docs/intro.md` file to the `i18n/fr` folder:

```bash
mkdir -p i18n/fr/docusaurus-plugin-content-docs/current/

cp docs/intro.md i18n/fr/docusaurus-plugin-content-docs/current/intro.md
```

Translate `i18n/fr/docusaurus-plugin-content-docs/current/intro.md` in French.

## Start your localized site

Start your site on the French locale:

```bash
npm run start -- --locale fr
```

Your localized site is accessible at [http://localhost:3000/fr/](http://localhost:3000/fr/) and the `Getting Started` page is translated.

:::caution

In development, you can only use one locale at a time.

:::

## Add a Locale Dropdown

To navigate seamlessly across languages, add a locale dropdown.

Modify the `docusaurus.config.js` file:

```js title="docusaurus.config.js"
export default {
  themeConfig: {
    navbar: {
      items: [
        // highlight-start
        {
          type: "localeDropdown",
        },
        // highlight-end
      ],
    },
  },
};
```

The locale dropdown now appears in your navbar:

![Locale Dropdown](./img/localeDropdown.png)

## Build your localized site

Build your site for a specific locale:

```bash
npm run build -- --locale fr
```

Or build your site to include all the locales at once:

```bash
npm run build
```
