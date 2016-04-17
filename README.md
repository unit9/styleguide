UNIT9 Style Guide
================

> You can't run away <br>
> From these styles I got, oh baby, hey baby <br>
> Cause I got a lot, oh yeah <br>
>
> The Fugees - Ready or Not

---

Table of contents:

* [Tooling](#tooling)
* [HTML](#html)
* [CSS](#css)
* [JavaScript](#javascript)

---

## Tooling

### Code formatting

[EditorConfig](http://editorconfig.org/) is used to define indentation style and size, EOL, final new line, charset across a single project.

> EditorConfig helps developers define and maintain consistent coding styles between different editors and IDEs.

### Version control

[The Art of the commit](http://alistapart.com/article/the-art-of-the-commit)
> Be useful <br>
> Be detailed <br>
> Be consistent <br>
> Use the active voice <br>

[Git Flow](http://nvie.com/posts/a-successful-git-branching-model/)
> master <br>
> develop <br>
> feature/ <br>
> release/ <br>
> hotfix/ <br>

### Code linting

Code is linted on the fly inside the editor to which plugins are added:

* [Sublime Linter](https://github.com/SublimeLinter/SublimeLinter3)
* [Atom linter](https://atom.io/packages/linter)

It requires projects to have the following dependencies: `npm install -D postcss stylelint stylelint-config-suitcss  eslint-config-airbnb eslint-plugin-import eslint-plugin-react eslint-plugin-jsx-a11y eslint`. See below.

## HTML

### Conventions

[HTML Codeguide](http://codeguide.co/#html)

### Tooling

If required:

* preprocessor: [JADE](http://jade-lang.com/)
* templating engine: [Handlebars](http://handlebarsjs.com/)

## CSS

### Conventions

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

### Linting

[Stylelint](https://github.com/stylelint/stylelint/) with this [SUITCSS config](https://github.com/stylelint/stylelint-config-suitcss) that can be [individually configured](https://github.com/stylelint/stylelint/blob/master/docs/user-guide/rules.md).

|Editor|Plugin|Installation|
|:-----|:-----|:-----------|
|Sublime Text|[SublimeLinter-contrib-stylelint](https://github.com/kungfusheep/SublimeLinter-contrib-stylelint)| `SublimeLinter-contrib-stylelint` via Package Manager|
|Atom|[linter-stylelint](https://atom.io/packages/linter-stylelint)|`apm install linter-stylelint`|

### Formatting

Stylefmt to automatically format files as it uses PostCSS.

|Editor|Package|Installation|
|:-----|:------|:-----------|
|Sublime Text|[Sublime Stylefmt](https://github.com/dmnsgn/sublime-stylefmt)|`Stylefmt` via Package Manager|
|Atom|[Language Grammar](https://github.com/1000ch/atom-stylefmt)|`apm install stylefmt`|

## JavaScript

### Conventions

JavaScript Style Guides for ES5/React/ES201x:

[Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)

`if CoffeeScript then` use this [guide](https://github.com/polarmobile/coffeescript-style-guide).

### Syntax

Definitions for ES201x JavaScript and React JSX syntax.

|Editor|Package|Installation|
|:-----|:------|:-----------|
|Sublime Text|[Syntax definitions](https://github.com/babel/babel-sublime)|`Babel` via Package Manager|
|Atom|[Language Grammar](https://atom.io/packages/language-babel)|`apm install language-babel`|

### Linting

[ESlint](http://eslint.org/) is the most complete solution for conforming to style guidelines and finding problematic patterns in JavaScript and JSX.

|Editor|Plugin|Installation|
|:-----|:-----|:-----------|
|Sublime Text|[SublimeLinter-eslint](https://github.com/roadhump/SublimeLinter-eslint)|`SublimeLinter-eslint` via Package Manager + `npm install --save-dev eslint-config-airbnb eslint-plugin-import eslint-plugin-react eslint-plugin-jsx-a11y eslint`|
|Atom|[linter-eslint](https://atom.io/packages/linter-eslint)|`apm install linter-eslint` + `npm install --save-dev eslint eslint-config-airbnb eslint-plugin-react`|
|...|[List of plugins](http://eslint.org/docs/user-guide/integrations#editors)||

### Formatting

All of the following solutions are not stable enough for a modern environment. Let's make the most out of linting.

* [esformatter](https://github.com/millermedeiros/esformatter)
* [JsFormat](https://github.com/jdc0589/JsFormat) using jsbeautifier
* [FixMyJS](https://github.com/jshint/fixmyjs) using JSHint
* [JSCSFormatter](https://github.com/TheSavior/SublimeJSCSFormatter)

---

For Google Projects, use the following:

- [JavaScript Style Guide](https://google.github.io/styleguide/javascriptguide.xml)
- [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.xml)
- [Google Closure Tools](https://developers.google.com/closure/) if required
