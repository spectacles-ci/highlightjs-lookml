# Contributing to highlightjs-lookml

Thanks for considering contributing to this repository! We're happy to review Pull Requests for improving the syntax highlighting of LookML.

## Setting up a development environment

#### Cloning the necessary repositories

Clone this repo and the highlight.js repo as separate repos.

#### Symlink highlightjs-lookml into highlight.js/extra

From inside the highlight.js repository, `cd extra` and symlink the highlightjs-lookml repository, naming the symlink `lookml`.

When you're done, you should have a symlink named `lookml` in the `extra` directory of your highlight.js repo. The symlink should point to your highlightjs-lookml repo.

Whenever you make changes in the highlightjs-lookml repo, they will be immediately reflected in the highlight.js repo. Immediate updates will be useful for building and testing with the tools there.

## Building

Depending on which build command you run (`npm run build`, `node tools/build.js`, minification for CDN, etc.), highlight.js will build itself differently. Depending on what you want to test, you will need to build highlight.js the right way. You may need to reference the highlight.js [Building and Testing docs](https://highlightjs.readthedocs.io/en/latest/building-testing.html).

You'll probably want to start by testing highlight.js in the browser. highlight.js ships with an in-browser development tool that's _extremely_ useful for testing changes to the language definition.

To use it, first build highlight.js, only building the `lookml` language and skipping compression for better error messages (`-n`). At the root of the highlight.js repo, run:

```bash
node tools/build.js -n lookml
```

## Testing in the browser development tool

Run `open tools/developer.html` to open the webpage in your browser. On this page, you can input text to be highlighted. You can change the theme and view the parsed structure of the document, which is very helpful for debugging the language definition.

Whenever you make changes to the language definition, rebuild (see above) and refresh the page to see changes.

## Helpful resources for developing 3rd-party languages

Good luck! Open an issue on this repo if you get stuck or need help configuring your development environment.

To understand highlight.js and how language definitions work, consult this documentation:

1. [3rd Party Language Quickstart](https://github.com/highlightjs/highlight.js/blob/main/extra/3RD_PARTY_QUICK_START.md)
1. [Language Contributor Checklist](https://highlightjs.readthedocs.io/en/latest/language-contribution.html)
1. [Language Definition Guide](https://highlightjs.readthedocs.io/en/latest/language-guide.html)
1. [Mode Reference](https://highlightjs.readthedocs.io/en/latest/mode-reference.html)
1. [Scope Reference](https://highlightjs.readthedocs.io/en/latest/css-classes-reference.html)
1. [Building and Testing docs](https://highlightjs.readthedocs.io/en/latest/building-testing.html)
