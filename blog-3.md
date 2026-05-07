Blog 2: How Generics Help Us Write Reusable Code
Introduction

Generics help us write one function that can work with many types of data.

What Are Generics?

A generic function uses a type variable.

```ts
function identity<T>(value: T): T {
    return value;
}
```
Here, T means the type will be decided when the function is used.
```ts
const text = identity("Hello");
const number = identity(100);
```
TypeScript knows text is a string and number is a number.

Why Generics Are Useful

Without generics, we may need many functions for different types. With generics, one function can work with many types safely.

Example:
```ts
function getFirstElement<T>(items: T[]): T {
    return items[0];
}
const firstNumber = getFirstElement([10, 20, 30]);
const firstName = getFirstElement(["John", "Jane"]);
```
The same function works for both numbers and strings.

Conclusion

Generics make code reusable and type-safe. They help us avoid repeated code and keep TypeScript checking active.