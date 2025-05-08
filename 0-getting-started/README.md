# Get started

* Install Node.js
* Install TypeScript

```shell
npm install -g typescript
```

* Create a simple TypeScript file

```javascript
// app.ts
let greeting: string = "Hello world";
console.log(greeting);
```

* Build ts to js

```shell
tsc --outDir js app.ts
```

* Check the result

```javascript
// cat js/app.js
var greeting = "Hello world";
console.log(greeting);

```

* Run the js file with Node.js

```javascript
cd js
node app.js
// output
// Hello world
```

* Run the compiler in watch mode

```shell
tsc --outDir js app.ts --watch
// [8:11:26 PM] Starting compilation in watch mode...

// [8:11:26 PM] Found 0 errors. Watching for file changes.
```