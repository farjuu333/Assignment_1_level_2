# Type vs Interface in TypeScript: Key Differences

### Introduction
One of the most common questions for anyone learning TypeScript is figuring out when to use a `type` alias and when to use an `interface`. At first, both seem to do the exact same thing defining the shape of an object. However, a few core differences help in writing cleaner and more maintainable code.

### The Core Differences

First, an `interface` is exclusively used for defining the shape of objects and classes. On the other hand, a `type` alias is much more flexible. A `type` alias works not just for objects, but also for primitives, unions, and tuples.


// Only possible with type
type ID = string | number;
type Point = [number, number];

Second, the way they handle extending is different. Interfaces use the extends keyword to inherit properties from other interfaces, while types use the intersection operator (&) to merge multiple types together.


// Extending interface vs type
interface Animal { name: string; }
interface Dog extends Animal { bark(): void; }

type Pet = { name: string; } & { meow(): void; };


The most significant difference is Declaration Merging. Declaring two interfaces with the exact same name causes TypeScript to automatically merge them into one single interface. This is impossible with types, as declaring the same type twice throws a compiler error.


interface User { name: string; }
interface User { age: number; }
// User is now automatically merged into: { name: string; age: number; }

When to Choose Which?
As a general rule of thumb, use interface when defining object shapes, building OOP class contracts, or creating public libraries that benefit from declaration merging. Choose type when creating union types, working with complex utility types, or creating aliases for primitive values.

Conclusion
In simple terms, both type and interface help write safe and clean code in TypeScript. Use interface when working with objects or classes, and use type when dealing with unions or basic data types. Picking the right tool for the job makes code easier to read and maintain!