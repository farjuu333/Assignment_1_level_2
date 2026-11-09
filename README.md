# Level-2 Web Development - Assignment 1 (B8A1)

This repository contains the complete solution for Assignment 1, demonstrating practical understanding of core TypeScript concepts including basic types, optional/default parameters, readonly tuples, type narrowing, generics, interfaces, Object-Oriented Programming (OOP), and asynchronous programming with Promises.

---

## File Structure

```text
 solutions.ts          # All 8 problem-solving implementations
 type-vs-interface.md  # Blog post on Type Aliases vs Interfaces
 type-narrowing.md     # Blog post on Type Narrowing in TypeScript
 README.md             # Assignment documentation
Coding Problems & Solutions (solutions.ts)
The solutions.ts file includes fully typed solutions for the following problems:

multiplyValue: Handles optional multipliers with default values and proper handling for 0.

processInput: Uses union types and typeof type narrowing for strings, numbers, and booleans.

formatCoordinate: Utilizes readonly tuples to format coordinates securely without mutations.

concatenateArrays: Implements generic rest parameters to merge multiple arrays of type T.

Course & getPopularCourses: Implements interfaces and filters published courses based on student thresholds.

pluckValues: Utilizes generic constraints (<T, K extends keyof T>) to extract specific object properties.

Employee & Manager: Implements OOP principles with access modifiers (private, protected, extends, super).

validateAgeAsync: Handles asynchronous promise resolution and rejection using setTimeout and Error.

Blog Posts
As part of the assignment requirements, two technical blogs have been written and submitted in separate Markdown files:

Type vs Interface in TypeScript

Understanding Type Narrowing in TypeScript

Author
Farjana Akter