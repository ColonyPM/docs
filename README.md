# ColonyPM Documentation

This repository contains the source code for the ColonyPM documentation website, built with [Docusaurus](https://docusaurus.io/).

The documentation covers how to use the ColonyPM CLI, including its available commands. It also describes the package format as well as the manifest format.

You can read the documentation in two ways:

1. **Read the raw Markdown files** directly in the [`/docs`](./docs) directory.
2. **Build and run the website locally** to browse the documentation via the website.

## Running the documentation website

To view the documentation as a website, you can either build it or start a local development server.

### Start a development server

This is useful while writing or editing documentation:

```bash
npm install
npm run start
```
This will start a local development server and open the site in your browser.

## Building the documentation website
To generate a production build of the documentation site:
```bash
npm install
npm run build
```
The static site will be generated in the build directory.
