# TypeScript
**Q: What is TypeScript?**  
A: TypeScript is a typed superset of JavaScript that compiles to plain JavaScript. It was created by Microsoft to make building large-scale applications in JavaScript more manageable by providing optional static type checking and other features not available in standard JavaScript.

**Q: What are the benefits of using TypeScript?**  
A: Some of the benefits of using TypeScript include improved type safety and code maintainability, better tooling support, and the ability to catch errors early in the development process.

**Q: How does TypeScript differ from JavaScript?**  
A: TypeScript is a superset of JavaScript that adds optional static typing and other features, such as classes and interfaces, that are not present in standard JavaScript. TypeScript code must be compiled to JavaScript before it can be executed.

**Q: What are interfaces in TypeScript?**  
A: Interfaces in TypeScript are used to define the shape of an object, including its properties and methods. Interfaces can be used to enforce type checking and provide documentation for objects and functions.

**Q: What is type inference in TypeScript?**  
A: Type inference is a feature in TypeScript that allows the compiler to automatically determine the type of a variable based on its initialization value. This can help to reduce the amount of type annotations required in TypeScript code.

**Q: What is a union type in TypeScript?**  
A: A union type in TypeScript allows a variable to be of more than one type. Union types are denoted using the "|" operator, for example: "string | number".

**Q: What is an enum in TypeScript?**  
A: An enum in TypeScript is a way to define a set of named values. Enums can be used to improve code readability and type safety by providing a way to define a fixed set of possible values for a variable.

**Q: How does TypeScript handle null and undefined values?**  
A: By default, TypeScript allows null and undefined values to be assigned to any type. However, it is possible to configure TypeScript to disallow these values by using the "strictNullChecks" compiler option.

**Q: What is the "readonly" keyword in TypeScript?**  
A: The "readonly" keyword in TypeScript is used to indicate that a property or variable cannot be modified after it has been initialized. This can help to improve code safety and prevent accidental modifications.

**Q: How does TypeScript handle inheritance?**  
A: TypeScript supports inheritance through classes, which can inherit properties and methods from a parent class using the "extends" keyword. TypeScript also supports the use of interfaces for inheritance and code reuse.

**Q: What is the difference between "null" and "undefined" in TypeScript?**  
A: In TypeScript, both "null" and "undefined" represent absence of value, but they have different use cases. "null" is an assignment value that represents the intentional absence of any object value, while "undefined" is a type that indicates the absence of a value in variables that have not been assigned.

**Q: What is the difference between "any" and "unknown" types in TypeScript?**  
A: Both "any" and "unknown" are types that can hold any value. However, there are important differences:
- Variables of type "any" can be assigned and re-assigned any value without type-checking, while variables of type "unknown" require explicit type-checking before performing any operations.
- "unknown" is a safer type than "any" because it forces you to perform type-checking and narrowing before using the value.

**Q: Explain the concept of "structural typing" in TypeScript.**  
A: Structural typing is a type system used by TypeScript, where compatibility is based on the structure of types rather than their explicit declaration. If two types have compatible structures, they are considered assignable to each other, even if they were defined separately.

**Q: How can you create an immutable object in TypeScript?**  
A: TypeScript does not have built-in language support for immutability. However, you can achieve immutability by using techniques like:
- Using the `readonly` modifier to define read-only properties or array elements.
- Creating new objects or arrays instead of modifying existing ones.
- Using libraries like Immutable.js or Immer that provide immutable data structures and utilities.

**Q: What is a conditional type in TypeScript?**  
A: Conditional types in TypeScript allow you to create type transformations based on conditions. They are defined using the `extends` keyword and conditional expressions. Conditional types are often used in generic type definitions to create more flexible and reusable types.

These are just a few examples of tricky TypeScript interview questions. Remember to dive deeper into each topic to gain a more comprehensive understanding. Good luck with your interview preparation!
