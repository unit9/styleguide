UNIT9 Style Guide
================

[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](#badge)

> You can't run away <br>
> From these styles I got, oh baby, hey baby <br>
> Cause I got a lot, oh yeah <br>
>
> The Fugees - Ready or Not

---

Table of contents:

* [Editor code style](#editor-code-style)
* [Version control](#version-control)
* [Code Formatting](#code-formatting)
* [Code Linting](#code-linting)
* [HTML & CSS](#html-css)

---

## Editor code style

[EditorConfig](http://editorconfig.org/) is used to define indentation style and size, EOL, final new line, charset across a single project.

> EditorConfig helps developers define and maintain consistent coding styles between different editors and IDEs.

## Version control

[The Art of the commit](http://alistapart.com/article/the-art-of-the-commit)
> Be useful <br>
> Be detailed <br>
> Be consistent <br>
> Use the active voice <br>

[Feature Branch](https://www.atlassian.com/git/tutorials/comparing-workflows#feature-branch-workflow)
> feature development encapsulated <br>
> leverage pull requests <br>

[Git Flow](https://www.atlassian.com/git/tutorials/comparing-workflows#gitflow-workflow)
> master <br>
> develop <br>
> feature/ <br>
> release/ <br>
> hotfix/ <br>

## Code Formatting

Use [Prettier](https://github.com/prettier/prettier):

```bash
npm i -D prettier
```

|Editor|Plugin|Installation|
|:-----|:-----|:-----------|
|Sublime Text|[SublimeJsPrettier](https://github.com/jonlabelle/SublimeJsPrettier)| `Prettier` via Package Manager|
|Atom|[prettier-atom](https://github.com/prettier/prettier-atom)|`apm install prettier-atom`|
|VSCode|[prettier-vscode](https://github.com/prettier/prettier-vscode)|`ext install prettier-vscode`|

Prettier is an opinionated code formatter with support for:

* JavaScript, including [ES2017](https://github.com/tc39/proposals/blob/master/finished-proposals.md)
* [JSX](https://facebook.github.io/jsx/)
* [Flow](https://flow.org/)
* [TypeScript](https://www.typescriptlang.org/)
* CSS, [LESS](http://lesscss.org/), and [SCSS](http://sass-lang.com)
* [JSON](http://json.org/)
* [GraphQL](http://graphql.org/)

## Code Linting

Install the linter:

* [Sublime Linter](https://github.com/SublimeLinter/SublimeLinter3)
* [Atom linter](https://atom.io/packages/linter)

Install the linter's plugins:

|Editor|Plugin|Installation|
|:-----|:-----|:-----------|
|Sublime Text|[SublimeLinter-eslint](https://github.com/roadhump/SublimeLinter-eslint)| `SublimeLinter-contrib-eslint` via Package Manager|
|Atom|[linter-eslint](https://github.com/AtomLinter/linter-eslint)|`apm install linter-eslint`|
|VSCode|[vscode-eslint](https://github.com/Microsoft/vscode-eslint)|`ESLint from VS Code Marketplace`|

Use [ESLint](https://eslint.org/):

```bash
npm i -D eslint
```

Configure [ESLint](https://eslint.org/) for [Prettier](https://github.com/prettier/prettier):

* Use [eslint-plugin-prettier](https://github.com/prettier/eslint-plugin-prettier) as an ESLint rule:

```bash
npm i -D eslint-plugin-prettier
```

```json
{
  "plugins": [
    "prettier"
  ],
  "rules": {
    "prettier/prettier": "error"
  },
}
```

* Use [eslint-config-prettier](https://github.com/prettier/eslint-config-prettier) to disable all the existing formatting rules:

```bash
npm i -D eslint-config-prettier
```

```json
{
  "extends": [
    "prettier"
  ]
}
```

See [package.json](./package.json).

## HTML & CSS

### Conventions

[HTML Codeguide](http://codeguide.co/#html)

[SUIT CSS](https://github.com/suitcss/suit/blob/master/doc/naming-conventions.md):

* `.u-utility`
* `.ComponentName`
* `.ComponentName-descendentName`
* `.ComponentName--modifierName`
* `.ComponentName.is-stateOfComponent`

or sometimes [BEM](https://en.bem.info/):

* `.block-name`
* `.block-name__element`
* `.block-name--modifier-name`

### Base

[normalize.css](https://necolas.github.io/normalize.css/)
> Normalize.css makes browsers render all elements more consistently and in line with modern standards. It precisely targets only the styles that need normalizing.

---

For Google Projects, use the following:

- [JavaScript Style Guide](https://google.github.io/styleguide/javascriptguide.xml)
- [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.xml)
- [Google Closure Tools](https://developers.google.com/closure/) if required
