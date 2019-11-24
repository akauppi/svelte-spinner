[![npm][npm]][npm-url]

[npm]: https://img.shields.io/npm/v/svelte-spinner.svg
[npm-url]: https://npmjs.com/package/svelte-spinner

<img src="Logotype Primary.png" alt="Svelte Spinner" width="40%" height="40%" />

A Svelte SVG loading spinner.

This repo shows how to develop, test and export a Svelte component.


## Requirements

- npm

## Getting started

```
$ npm install
```

>Note: If you're on macOS Catalina and get a bunch of errors about `node-gyp`, see [here](https://github.com/nodejs/node-gyp/issues/1927#issuecomment-549349352).
>
>Essentially: 
>
>- `sudo rm -rf $(xcode-select -print-path)`
>- `xcode-select --install`
>- `/usr/sbin/pkgutil --packages | grep CLTools`    # should list some files


### Trying the component

```
$ npm run dev

  Your application is ready~! 🚀

  - Local:      http://localhost:5000

...
[2019-11-24 19:42:02] waiting for changes...
```

Observe the port mentioned and open [http://localhost:5000](http://localhost:5000).

>![](.images/example-screenshot.png)


## Developing

While you're running the `npm run dev`, changes to the code *should* be reflected in the app. Try to change something within the component, e.g. double the thickness.

>Note: Currently, changes don't seem to auto-propagate. You'll have to refresh the browser. <!-- tbd. -->


<!-- tbd.
## Publishing

-->


## Usage

```
<!-- App.svelte -->
<script>
  import Spinner from 'svelte-spinner';
</script>

<Spinner
  size="50"
  speed="750"
  color="#A82124"
  thickness="2"
  gap="40"
/>
```

### Spinner API
 
| Properties | Default Value | Description
|---|---|---
| `size`      | `25`  | The height and width of the SVG spinner.
| `speed`     | `750` | How many milliseconds it will take for the spinner to complete one rotation.
| `color`     | `'rgba(0,0,0,0.4)'` | The color of the spinner.
| `thickness` | `2`   | The thickness of the spinner.
| `gap`       | `40`  | How many percent of the spinner that will not be filled.




## References

- [EmilTholin/svelte-spinner](https://github.com/EmilTholin/svelte-spinner)

	The basis.
	
	Differences to the base repo:
	- using just one `package.json` instead of two. This less strict separation of `example` from the source allows us to do testing.

- [rollup-plugin-svelte/README](https://github.com/rollup/rollup-plugin-svelte)

	Read especially [this section](https://github.com/rollup/rollup-plugin-svelte#pkgsvelte) for knowledge on exporting/importing Svelte components, via npm.

- [lukeed/svelte-demo](https://github.com/lukeed/svelte-demo) used as a template for the `app` part (demo/testbed)

