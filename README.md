# xeokit-sdk examples

Examples for [xeokit-sdk](https://github.com/xeokit/xeokit-sdk).

Running live on [xeokit.io](https://xeokit.io/sdk-v2/examples)

## Usage

### Included version of xeokit-sdk (default)

A cold clone works immediately.


```sh
git clone https://github.com/xeokit/examples
cd examples
```

Serve the repo root with any static HTTP server:

```sh
npx serve .
# or: python3 -m http.server 8080
```


### Use remote / CDN mode 

To make examples load the xeokit-sdk from jsDelivr CDN, for instance `@latest` 
edit `dist/xeokit-sdk.js` and replace its content by:

```js
// export * from './xeokit-sdk/index.js';
// export * from './xeokit-sdk.min.es.js';
export * from "https://cdn.jsdelivr.net/npm/@xeokit/xeokit-sdk/dist/xeokit-sdk.es.min.js";

```

## Run from  xeokit-sdk sources directly

### Clone xeokit-sdk source if not yet done

```bash
git clone https://github.com/xeokit/xeokit-sdk.git
cd xeokit-sdk

# apply path which allow to use source directly
git apply <path-to-examples-repo>/use-from-source.patch
npm i
npm run vendor
```

> **Note:** In case the patch does not apply, try changing the line endings in the patch file (`dos2unix use-from-source.patch`). This depends on your local git setup.

### Create symlink in examples to patched xeokit-sdk
```
cd examples/dist
# ln -s <your-path>/xeokit-sdk ./xeokit-sdk
# in case xeokit-sdk is side by side with examples 
ln -s ../../xeokit-sdk ./xeokit-sdk
# or on Win: New-Item -ItemType SymbolicLink -Path "xeokit-sdk" -Target "..\..\xeokit-sdk"
```

### Point `dist/xeokit-sdk.js` to xeokit-sdk source (simlink)

```js
export * from './xeokit-sdk/index.js';
// export * from './xeokit-sdk.min.es.js';
// export * from "https://cdn.jsdelivr.net/npm/@xeokit/xeokit-sdk/dist/xeokit-sdk.es.min.js";
```

### Start web server
```
npx serve .
```

## 📜 Licensing 

xeokit SDK examples are licensed under [**AGPLv3**](./LICENSE) 
