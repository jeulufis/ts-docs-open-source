# Website

![image](https://github.com/jeulufis/ts-docs-open-source/assets/92868937/128b5132-ad5e-4588-994a-cbb85e75f160)

![image](https://github.com/jeulufis/ts-docs-open-source/assets/92868937/91e355b4-d3b1-4bfb-80c3-fba0887a6e25)


![image](https://github.com/jeulufis/ts-docs-open-source/assets/92868937/4dcd40af-c6c9-4e92-b176-0527697270b1)


This website is built using [Docusaurus](https://docusaurus.io/), a modern static website generator.

### Installation

```
$ yarn
```

### Local Development

```
$ yarn start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

### Build

```
$ yarn build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

### Deployment

Using SSH:

```
$ USE_SSH=true yarn deploy
```

Not using SSH:

```
$ GIT_USER=<Your GitHub username> yarn deploy
```

If you are using GitHub pages for hosting, this command is a convenient way to build the website and push to the `gh-pages` branch.
