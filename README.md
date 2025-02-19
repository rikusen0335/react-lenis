[![Bibliotheca](https://assets.studiofreight.com/bibliotheca/header.png)](https://github.com/studio-freight/bibliotheca)

<!-- <p align="center">
  <a aria-label="Vercel logo" href="https://vercel.com">
    <img src="https://badgen.net/badge/icon/Next?icon=zeit&label&color=black&labelColor=black">
  </a>
  <br/>
  <a aria-label="NPM version" href="https://www.npmjs.com/package/swr">
    <img alt="" src="https://badgen.net/npm/v/swr?color=black&labelColor=black">
  </a>
  <a aria-label="Package size" href="https://bundlephobia.com/result?p=swr">
    <img alt="" src="https://badgen.net/bundlephobia/minzip/swr?color=black&labelColor=black">
  </a>
  <a aria-label="License" href="https://github.com/vercel/swr/blob/main/LICENSE">
    <img alt="" src="https://badgen.net/npm/license/swr?color=black&labelColor=black">
  </a>
</p> -->

## Introduction

react-lenis creates and manages an instance of the [Lenis](https://github.com/studio-freight/lenis).
It takes in a root prop and an options object that is spread into the Lenis constructor.

If `root` is true, `<ReactLenis>` will be the root Lenis instance and all other `<ReactLenis>` components in the app will get the instance from the context. If `root` is false, the component will create a new Lenis instance and provide it via the context. It's recommended to only have one `<ReactLenis root>` component in your app.

<br/>

## Usage

```js
function Layout() {
  const lenis = useLenis(({scroll}) => {
    // called every scroll
  })

  return (
    <ReactLenis root options={{ ...options }}>
      {/* Your scrollable website */}
    </ReactLenis>
  )
}
```
<br/>

## Options
The `options` object is passed directly to the Lenis instance, check [their readme for reference](https://github.com/studio-freight/lenis#instance-settings)

<br/>

## Extras
Once the Lenis context is set (components mounted inside `<ReactLenis>`) you can use these handy hooks:

`useLenis` is a hook that returns the Lenis instance

The hook takes three argument:
- callback: The function to be called whenever a scroll event is emitted
- deps array: Trigger callback on change
- priority: Manage callback execution order


<br/>

## Folder Structure

- **/bundled:** Generated by `microbundle` after running `build:bundled` script. Includes all external dependencies.
- **/dist:** Generated by `microbundle` after running `build:dist` script.
  - **/dist/types** Generated by `tsc` after running `build:types` script.
- **/docs:** Used by `vite` through `dev` script to serve the documentation.
- **/docs/App.jsx:** here's where you can test your library.
- **/src:** Your library's raw code.

<br/>

## @studio-freight/react-lenis in use

- [@studio-freight/compono](https://github.com/studio-freight/compono) Our Next.js/React component library.

- [@studio-freight/satus](https://github.com/studio-freight/satus) Our starter kit.

<br/>

## Authors

This tool is maintained by the Studio Freight Darkroom team:

- Clement Roche ([@clementroche\_](https://twitter.com/clementroche_)) – [Studio Freight](https://studiofreight.com)
- Guido Fier ([@uido15](https://twitter.com/uido15)) – [Studio Freight](https://studiofreight.com)
- Leandro Soengas ([@lsoengas](https://twitter.com/lsoengas)) - [Studio Freight](https://studiofreight.com)
- Franco Arza ([@arzafran](https://twitter.com/arzafran)) - [Studio Freight](https://studiofreight.com)

<br/>

## License

[The MIT License.](https://opensource.org/licenses/MIT)
