Reproduce https://github.com/npm/npm/issues/10887

To reproduce:
```sh
$ npm install
$ npm uninstall test-local
```

Observe that there's still files in `node_modules/test-local`:
```sh
$ find node_modules/
node_modules
node_modules/.bin
node_modules/test-local
node_modules/test-local/node_modules
node_modules/test-local/node_modules/.bin
```
