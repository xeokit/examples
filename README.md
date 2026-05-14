# xeokit-sdk examples

Live examples for [xeokit-sdk](https://github.com/xeokit/xeokit-sdk).

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

To make examples load the SDK from jsDelivr CDN for instance `@latest` edit `dist/xeokit-sdk.js`
and replace its content by:

```js
export * from "https://cdn.jsdelivr.net/npm/@xeokit/xeokit-sdk/dist/xeokit-sdk.es.min.js";
// or: export * from " https://cdn.jsdelivr.net/npm/@xeokit/xeokit-sdk@2.6.111/dist/xeokit-sdk.es.min.js"
```

## 📜 Licensing 

xeokit SDK examples are licensed under [**AGPLv3**](./LICENSE) 
