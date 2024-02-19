# esbuild-plugin-esmcss

esbuild plugin to build *.css.ts/*.css.js modules as css assets.

## install

[//]: @formatter:off
```
npm i -D esbuild-plugin-esmcss
```
[//]: @formatter:on

## usage

Build file

[//]: @formatter:off
```ts
import { build } from 'esbuild'
import esmcss from 'esbuild-plugin-esmcss'
await build({
  entryPoints: [/* source code entry point */],
  plugins: [esmcss()]
})
```
[//]: @formatter:on

Component file

[//]: @formatter:off
```ts
import './component.css.js'
export function html_() {
  return `
<!DOCTYPE html>
<html>
  <head>
  link_({ rel: 'stylesheet', type: 'text/css', href })
    <link rel="stylesheet" type="text/css" href="/path/to/cssBundle.css">
  </head>
  <body>
    <div class="my_component">Hello!</div>
  </body>
</html>
  `.trim()
}
```
[//]: @formatter:on

component.css.ts

[//]: @formatter:off
```ts
export default ()=>`
.my_component {
  color: green;
}
`
```
[//]: @formatter:on
