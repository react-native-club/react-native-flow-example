## Basic example using flow server

STEPS:

- ```react-native init ProjectName```

- open ```.flowconfig```

- check at the bottom of the file what flow version is required for this project

- ```npm i flow-bin@0.36.0 --save-dev```

- add following scripts to ```package.json```

```js
"flow": "node_modules/.bin/flow",
"flow-stop": "node_modules/.bin/flow stop"
```

- run flow ```npm run flow```

- you should see ```No errors``` at the bottom

- add some function to ```index.ios.js``` for example:

```js
function multiply(n1: number, n2: number): number {
  return n1 * n2;
}
```

and

```js
<Text>{multiply(14, 14)}</Text>
```

- run flow again: ```npm run flow```

- you should see ```No errors```

- change the passed parameters, for example:

```js
<Text>{multiply(14, 'b')}</Text>

```

- run ```npm run flow```

- you should see very descriptive error message


References:

- get started with Flow - https://flowtype.org/docs/getting-started.html#_

- why use Flow - https://flowtype.org/docs/type-annotations.html#_

- add Flow to any Redux application - https://blog.callstack.io/typed-redux-2aa8bff926ff#.nkj9ah5v2

- advance setup - https://flowtype.org/docs/advanced-configuration.html#_
