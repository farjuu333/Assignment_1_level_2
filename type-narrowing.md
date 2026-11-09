# Type Narrowing in TypeScript

--Introduction
When writing TypeScript, frequently encounter variables that can be of multiple types, such as union types. Type narrowing is the process of refining a broad, general type into a more specific one. By doing this, TypeScript understands exactly what type of data it is dealing with at a specific moment, which prevents unexpected runtime errors and provides accurate autocompletion.

--Examples of Type Narrowing
TypeScript offers several ways to narrow down types depending on the data you are working with. Here are three common approaches:

---1. Using 'typeof'
The 'typeof' operator is perfect for checking basic primitive types like strings, numbers, or booleans.

function formatValue(value: string | number) {
  if (typeof value === "string") {
    return value.trim(); // TypeScript knows this is a string
  }
  return value.toFixed(2); // TypeScript knows this is a number
}
2. Using instanceof
When working with classes and object instances, instanceof helps verify if an object was created by a specific class.


class Car { drive() {} }
class Boat { sail() {} }

function operateVehicle(vehicle: Car | Boat) {
  if (vehicle instanceof Car) {
    vehicle.drive(); // Narrowed down to Car
  } else {
    vehicle.sail(); // Narrowed down to Boat
  }
}
3. Using the in Operator
The in operator is incredibly useful for custom object types or interfaces. It checks if a specific property exists inside the object to determine its exact type.


type Admin = { accessCode: number };
type User = { email: string };

function login(person: Admin | User) {
  if ("accessCode" in person) {
    console.log("Admin logged in");
  } else {
    console.log("User logged in");
  }
}
Conclusion
Type narrowing is a core concept that makes TypeScript so reliable. By using operators like typeof, instanceof, and in, you give the compiler the context it needs to guarantee type safety, resulting in cleaner and more predictable code.