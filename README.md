# esbuild-plugin-esmcss

esbuild plugin to build *.css.ts/*.css.js files as css assets

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
// ... Component definition
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
