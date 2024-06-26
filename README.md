# vue-nl2br

![main workflow](https://github.com/inouetakuya/vue-nl2br/actions/workflows/main.yml/badge.svg)

A vue component which turns new lines into line breaks.

## Why not just use CSS?

See [Why not just use CSS `white-space: pre;`? · Issue #7](https://github.com/inouetakuya/vue-nl2br/issues/7)

## Requirement

- [Vue.js](https://github.com/vuejs/vue) `^3.0.0`

## Installation

```shell
npm install --save vue-nl2br
```

## Usage

```html
<nl2br tag="p" :text="`myLine1\nmyLine2`" class-name="foo bar" />
```

is rendered to

```html
<p class="foo bar">myLine1<br>myLine2</p>
```

## Props

- `tag`: HTML tag name which is passed to [createElement function](https://vuejs.org/v2/guide/render-function.html#createElement-Arguments)
  - Type: `String`
  - Required: true
- `text`: Text in the tag.
  - Type: `String`
  - Default: null
- `className`: HTML class name(s) 
  - Type: `String`
  - Required: false

Note: when `text` property is empty or null, it renders an empty tag. ex) `<p></p>`.

If you prefer to render nothing at all, use `v-if` directive:

```html
<nl2br v-if="myText" tag="p" :text="myText" />
``` 

## License

[MIT](https://opensource.org/licenses/MIT)
