Blog 1: Why any Is Risky and Why unknown Is Safer ?

Introduction

TypeScript checks types to make our code safer. But sometimes we do not know what type of data we will get. In that case, we can use any or unknown.

What Is any?

any means the value can be anything.
```ts
let value: any = 100;

console.log(value.toUpperCase());
```

TypeScript will not show an error here. But the code will crash because a number does not have toUpperCase().

So, any is risky because it turns off type checking.

What Is unknown?

unknown also means the value can be anything. But TypeScript does not allow us to use it directly.

```ts
let value: unknown = "Hello";

// console.log(value.toUpperCase()); // Error
```
We must check the type first.

```ts
if (typeof value === "string") {
    console.log(value.toUpperCase());
}
```

This is safer.

Type Narrowing

Type narrowing means checking the type before using the value.

```ts
function printValue(value: unknown): void {
    if (typeof value === "string") {
        console.log(value.toUpperCase());
    } else if (typeof value === "number") {
        console.log(value + 10);
    }
}
```
Conclusion

any is risky because it removes type safety. unknown is safer because it forces us to check the type first.