# Python
## Basic
**Q: What is Python?**  
A: Python is a high-level, interpreted programming language that is used for a wide range of applications, including web development, scientific computing, and artificial intelligence.

**Q: What is PEP 8?**  
A: PEP 8 is a set of guidelines for writing Python code. It covers topics such as naming conventions, code layout, and documentation.

**Q: What is a module in Python?**  
A: A module in Python is a file containing Python code. It can be imported into another Python program to provide additional functionality.

**Q: What is a decorator in Python?**  
A: A decorator in Python is a function that modifies the behavior of another function. It is used to add functionality to a function without modifying the function itself.

**Q: What is a list comprehension in Python?**  
A: A list comprehension is a concise way to create a new list by applying an operation to each element of an existing list. It is often used to filter and transform data.

**Q: What is the difference between a tuple and a list in Python?**  
A: A tuple is an immutable sequence of values, while a list is a mutable sequence of values. Tuples are often used to group related data together, while lists are used for more general-purpose data storage.

**Q: What is a lambda function in Python?**  
A: A lambda function in Python is a small anonymous function that can be defined inline. It is often used for simple operations and as a shortcut for creating small functions.

**Q: What is a generator in Python?**  
A: A generator in Python is a special type of function that can be used to generate a series of values on-the-fly. It is often used for processing large amounts of data in a memory-efficient way.

**Q: What is the difference between '==' and 'is' in Python?**  
A: '==' is used to compare the values of two objects, while 'is' is used to compare the identities of two objects (i.e., whether they refer to the same object in memory).

**Q: What is the difference between a class and an object in Python?**  
A: A class in Python is a blueprint for creating objects, while an object is an instance of a class. Classes define the attributes and methods that objects can have, while objects store the specific values for those attributes.

## Advanced
**Q: What is the difference between a generator function and a regular function in Python?**  
A: A generator function in Python is a special type of function that uses the 'yield' keyword to generate a series of values on-the-fly. Each time the 'yield' keyword is encountered, the function returns the current value and saves its state so that it can be resumed later. In contrast, a regular function returns a single value and then terminates.

**Q: What is the Global Interpreter Lock (GIL) in Python, and how does it impact multi-threaded applications?**  
A: The Global Interpreter Lock (GIL) in Python is a mechanism that ensures only one thread executes Python bytecode at a time. This means that multiple threads in a Python application cannot run in parallel on multiple CPU cores. As a result, multi-threaded Python applications may not see significant performance gains when running on multi-core systems.

**Q: What is monkey patching in Python, and when might you use it?**  
A: Monkey patching in Python is the practice of modifying an existing module or object at runtime. It can be useful in situations where you need to patch a bug or add a new feature to an existing library without modifying the library's source code. However, monkey patching can also make code harder to debug and maintain, so it should be used with caution.

**Q: What is a metaclass in Python, and how might you use it?**  
A: A metaclass in Python is a class that defines how other classes should be created. When a new class is created using the 'class' keyword, Python uses the metaclass to create the class object. This allows you to customize the behavior of the class creation process, for example by adding additional methods or attributes to the class. Metaclasses can be a powerful tool, but they are also complex and can be difficult to use correctly.

**Q: What is a coroutine in Python, and how does it differ from a generator?**  
A: A coroutine in Python is a special type of function that can be paused and resumed during execution, allowing for asynchronous programming. Unlike generators, coroutines use the 'await' keyword to suspend execution until a result is available from an asynchronous operation. Coroutines are a fundamental building block of asynchronous programming in Python and are used extensively in frameworks such as asyncio.
