# Data Types

* boolean
* number
* string
* array
* enum (not available in JS)

## Hoisting (using `var`)

Hoisting in JavaScript is a behavior where variable and function declarations are moved to the top of their scope before code execution. This allows you to use variables and functions before they are declared in the code.

Hoisting happens when using `var` to declare variables.

```js
console.log(message);
var message = "Hello World!"
```

The above is valid code but hard to read!

## Using `let`

Variables declared with `let` may not be used before the declaration. The code below will become an compiler error.

```js
console.log(message);
let message = "Hello World!"
```

## Using `const`

Use const to declare constants.

## Type Annotations

Decide what data type may be assign to the variable

```js
let x: string = 'I will forever be a string'
// We cannot assign an int later
```

Type annotation is optional, it is for readability. If there is no type annotation, the type will be inferred by its value.

```js
let x = 'I will forever be a string'
// We cannot assign an int later
```

Type declaration for function call

```js
let z = GetSomeNumber();
let z: number = GetSomeNumber();
```

## Other types

* void
* null
* undefined
* never
* any: use to opt out type checking, can assign any value to the variable

By default, `null` and `undefined` can be assigned to any type. We can exclude null and undefined from other types using  `--strictNullChecks` compiler option. When using this option, union types must be used when wanting to allow `null`, `undefined` in other types, such as: `let someVar: string | null`

## Union types

The variable below can be a number or string. We can assign a type then change to the other type later.

```js
let someVar : number | string;
```

## Array

Declaration

```js
// normal syntax
let arr1: string[] = ["aaa", "bbb", "ccc"];

// generic syntax
let arr2: Array<string> = ["test1", "test2"];

// type mixed array
let arr3: any[] = [true, 1, "yes"] // mixed type is not recommended
```

## Flow control

for loop

```js
for (let i=1; i<=10; i++){

}
```

while loop

```js
let i: number = 1;

while (i <= 10)
{

}
```

switch

```js
let fruit: string = 'apple';

switch (fruit) {
  case 'banana':
    //...
    break;
    default:
      // ....
}
```

## Type analysis
