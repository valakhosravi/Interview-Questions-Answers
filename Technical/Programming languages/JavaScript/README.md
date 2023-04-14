# JavaScript
## Basic
**Q: What is JavaScript?**  
A: JavaScript is a high-level, interpreted programming language that is used to create dynamic web pages and web applications. It is a client-side scripting language that runs in the browser and is used to add interactivity to web pages.

**Q: What is the difference between == and === in JavaScript?**  
A: The double equals (==) operator checks for equality only in terms of value, while the triple equals (===) operator checks for equality in terms of value and data type. For example, 5 == "5" would return true, while 5 === "5" would return false because they are of different data types.

**Q: What are the data types in JavaScript?**  
A: JavaScript has six primitive data types: string, number, boolean, null, undefined, and symbol. In addition, it also has one non-primitive data type: object.

**Q: What is hoisting in JavaScript?**  
A: Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their respective scopes before the code is executed. This means that you can use a variable or function before it has been declared. However, only the declaration is hoisted, not the assignment or initialization.

**Q: What is the difference between var, let, and const in JavaScript?**  
A: var, let, and const are used to declare variables in JavaScript. The main difference between them is in their scope and how they can be reassigned. var has a function scope and can be reassigned. let and const have a block scope and cannot be redeclared, but let can be reassigned while const cannot.

**Q: What is closure in JavaScript?**  
A: A closure is a feature in JavaScript that allows a function to access and remember the variables and functions that are present in its lexical scope even after the outer function has returned. This allows for a function to have private variables and functions that cannot be accessed from outside the function.

**Q: What are the different types of errors in JavaScript?**  
A: There are three types of errors in JavaScript: syntax errors, runtime errors, and logical errors. Syntax errors occur when the code is not written correctly and cannot be parsed by the browser. Runtime errors occur when the code is executing and encounters a problem, such as trying to access a variable that does not exist. Logical errors occur when the code runs without error, but produces the wrong output.

**Q: What is the difference between let and var in JavaScript?**  
A: The main difference between let and var in JavaScript is their scope. Variables declared with var have function scope or global scope, while variables declared with let have block scope. Additionally, variables declared with var can be redeclared within the same scope, while variables declared with let cannot.

**Q: What is event bubbling in JavaScript?**  
A: Event bubbling is the process in which an event first triggers on the most specific target element, and then "bubbles up" to the containing elements in the DOM hierarchy until it reaches the document object. This means that if you have nested elements that each have an event listener for the same event, the innermost element's event will trigger first, followed by the outer elements.

**Q: What is the purpose of the "use strict" directive in JavaScript?**  
A: The "use strict" directive is a way to enable strict mode in JavaScript. Strict mode is a way to opt into a restricted version of JavaScript that disallows certain syntax that is prone to errors or considered bad practice. It also enables more thorough error checking and makes the code more secure.

**Q: What is the difference between a method and a function in JavaScript?**  
A: A method is a function that is associated with an object and can be called on that object using dot notation. A function, on the other hand, is a standalone block of code that can be called with or without an object reference.

**Q: What is the difference between synchronous and asynchronous programming in JavaScript?**  
A: Synchronous programming is when each task is executed one after the other in a single thread, while asynchronous programming is when tasks are executed concurrently in separate threads, allowing other tasks to run while waiting for a slow operation to complete.

**Q: What are the different types of loops in JavaScript?**  
A: There are three types of loops in JavaScript: for, while, and do-while loops. The for loop is used to iterate a specific number of times, the while loop is used to iterate while a condition is true, and the do-while loop is similar to the while loop but guarantees that the loop body will be executed at least once.

**Q: How do you convert a string to a number in JavaScript?**  
A: You can convert a string to a number in JavaScript using the Number() or parseInt() function. The Number() function converts a string to a number, while parseInt() function converts a string to an integer.

**Q: What is the difference between slice() and splice() methods in JavaScript?**  
A: The slice() method is used to return a copy of a portion of an array, while the splice() method is used to add or remove elements from an array at a specific index.

**Q: What is the difference between null and undefined in JavaScript?**  
A: Null and undefined are both used to represent absence of value, but they have different meanings. Null represents a deliberate non-value, while undefined represents an unintentional absence of value.

**Q: What is the difference between call() and apply() methods in JavaScript?**  
A: The call() and apply() methods are both used to invoke a function with a specific object as the value of "this", but they differ in how arguments are passed to the function. The call() method passes arguments as a comma-separated list, while the apply() method passes arguments as an array.

**Q: What is JavaScript scope and how does it work?**  

A: JavaScript scope refers to the visibility and accessibility of variables and functions in different parts of your code. When you declare a variable or function, it is added to a specific scope that determines where it can be accessed from. JavaScript has two main types of scope: global scope and local scope.

Global scope refers to variables and functions that are defined outside of any function or block. Global variables and functions can be accessed from anywhere in your code, including inside functions and blocks.

Local scope, on the other hand, refers to variables and functions that are defined inside a function or block. Local variables and functions can only be accessed from within the function or block where they are defined. This means that they are not accessible from outside the function or block.

When you reference a variable or function in your code, JavaScript looks for it in the current scope and then works its way up through the nested scopes until it finds the desired variable or function. This is known as the scope chain.

For example, if you have a variable x declared inside a function, and you reference it from outside that function, JavaScript will not be able to find it because it is in a different scope.

**Q: What is variable hoisting in JavaScript and how does it affect scope?**  

A: Variable hoisting is a JavaScript behavior where variables and functions that are declared anywhere in a scope are moved to the top of that scope by the JavaScript interpreter. This means that you can reference a variable or function before it has been declared, and JavaScript will still be able to find it.

However, only the declaration of the variable or function is hoisted, not its assignment or initialization. This means that if you reference a variable before it has been assigned a value, its value will be undefined.

Variable hoisting can affect scope because it means that variables and functions can be declared anywhere in a scope and still be accessible from anywhere else in that scope. However, it's generally considered best practice to declare all variables and functions at the top of their respective scopes to avoid confusion and potential bugs.

**Q: what is generator function?**  
A generator function is a special type of function in JavaScript that allows you to define an iterative algorithm by writing a single function that can generate a sequence of values over time. When you call a generator function, it doesn't run to completion right away; instead, it returns an iterator object that you can use to control the execution of the function.

Here is an example of a simple generator function in JavaScript:

    function* countUpTo(n) {
      let count = 0;
      while (count < n) {
        yield count++;
      }
    }

    const iterator = countUpTo(5);

    console.log(iterator.next().value); // 0
    console.log(iterator.next().value); // 1
    console.log(iterator.next().value); // 2
    console.log(iterator.next().value); // 3
    console.log(iterator.next().value); // 4

**Q: Write a function that takes an arbitrary number of arguments and returns a new function that will cycle through those arguments in order each time it is called. For example, if the function is called with the arguments "first", "second", and "third", the first call to the returned function should return "first", the second call should return "second", the third call should return "third", and the fourth call should return "first" again. Provide an implementation of the function and explain how it works.**  

    function toggler(...items) {
      let index = 0;
      return function() {
        const currentItem = items[index];
        index = (index + 1) % items.length;
        return currentItem;
      };
    }

This function takes an arbitrary number of arguments using the rest parameter syntax (...items), and returns a new function that will cycle through those items in order each time it is called. The index variable keeps track of the current index in the items array, and the function returns the item at that index. The index is then incremented using modulo arithmetic to ensure that it loops back to 0 when it reaches the end of the array.

**Q: What will be the output of the following code snippet when executed in a JavaScript environment?**

    var id = 'global id';
    const object = {
      id: 'object id',
      foo() {
         console.log(this.id) 
      },
    }

    object.foo();
    setTimeout(object.foo, 1000);

**and** 

    var id = 'global id';
    const object = {
      id: 'object id',
      foo: () => {
         console.log(this.id) 
      },
    }

    object.foo();
    setTimeout(object.foo, 1000);

**Explain your answer and discuss the difference in behavior between using a regular function and an arrow function as the method of an object in the context of this keyword.** 

### Foo() as a regular function
The output of the code will be:

    object id
    global id

Here's why:

When object.foo() is called, the function is invoked with this set to object, so the console logs object id.

When setTimeout(object.foo, 1000) is called, it creates a new function that is a reference to object.foo and schedules it to be called after a 1-second delay. However, when the function is actually called after 1 second, this is not bound to object anymore. Instead, it is bound to the global object (e.g. window in a browser or global in Node.js), which has a property id set to 'global id'. Therefore, the console logs global id.

This behavior can be modified by using bind method to bind this to object in the setTimeout call:

    setTimeout(object.foo.bind(object), 1000);

In that case, the output will be:

    object id
    object id

because this is bound to object in both calls to foo().

### Foo() as an arrow function

If we convert foo to an arrow function, then the this keyword inside the arrow function will refer to the this of the enclosing scope, which is the global this. Therefore, both console.log(this.id) statements will log "global id" instead of "object id".

Here's how the modified code would look like:

    var id = 'global id';
    const object = {
      id: 'object id',
      foo: () => {
         console.log(this.id) 
      },
    }

    object.foo()
    setTimeout(object.foo, 1000)
        
The output would be:

    global id
    global id
