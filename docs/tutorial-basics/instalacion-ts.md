---
sidebar_position: 1
---

# Instalacion

## TypeScript

**Descripción:**

TypeScript es un lenguaje de programación de código abierto desarrollado y mantenido por Microsoft. Es un superconjunto de JavaScript que agrega tipos estáticos opcionales a la sintaxis de JavaScript estándar. Esto permite a los desarrolladores detectar y corregir errores en tiempo de compilación en lugar de en tiempo de ejecución, lo que puede llevar a un código más robusto y menos propenso a errores.

**Instalación:**

Para comenzar a usar TypeScript, primero necesitas tener Node.js instalado en tu sistema. Luego, puedes instalar TypeScript globalmente utilizando npm (Node Package Manager) mediante el siguiente comando:

```bash
npm install -g typescript
```

Una vez que TypeScript esté instalado, puedes verificar la versión instalada utilizando el siguiente comando:

```bash
tsc --version
```






Add **Markdown or React** files to `src/pages` to create a **standalone page**:

- `src/pages/index.js` → `localhost:3000/`
- `src/pages/foo.md` → `localhost:3000/foo`
- `src/pages/foo/bar.js` → `localhost:3000/foo/bar`

## Create your first React Page

Create a file at `src/pages/my-react-page.js`:

```jsx title="src/pages/my-react-page.js"
import React from 'react';
import Layout from '@theme/Layout';

export default function MyReactPage() {
  return (
    <Layout>
      <h1>My React page</h1>
      <p>This is a React page</p>
    </Layout>
  );
}
```

A new page is now available at [http://localhost:3000/my-react-page](http://localhost:3000/my-react-page).

## Create your first Markdown Page

Create a file at `src/pages/my-markdown-page.md`:

```mdx title="src/pages/my-markdown-page.md"
# My Markdown page

This is a Markdown page
```

A new page is now available at [http://localhost:3000/my-markdown-page](http://localhost:3000/my-markdown-page).
