# Week 19, Day 3 Written HW

## Q1. What are all the JavaScript data types?
Null, Undefined, Boolean, Number, BigInt, String, Symbol, Object. An array is a type of Object

## Q2. What is the difference between Const, Let, and Var? Consider scope and give examples.
"const" is a variable declaration that prevents changing of said variable. A "const" string variable would not let you later assign a new string as its value, for example; however, if you use "const" to define an object, such as an array, you can change the "contents" within the object or the array. The "const" in this case is actually the location in memory at which the variable lives. "let" is a variable declaration that is possible to change or re-assign to later. "var" acts like "let" but has the unique property of not being bound by the scope within which it is declared; rather, it is defined within the global scope, whereas "const" and "let" only exist within the scope in which they are declared, which could be the global scope or within an object of some kind, like a function.

## Q3. Pass by Value or Pass by Reference? Why would you say a String is pass by value or a value type? Why is an object a reference type?
Pass by value means that the variable name is equal to the actual data type's value. A string is pass by value because defining a string such as [ let x = "apple" ] means x is actually equal to "apple." An object is not a value type, rather a reference type, because declaring one as a variable means that the variable is only a reference to the location of that object's data. This is why using "const" to declare an object, like an array, still allows you to modify the contents of that object; you are not altering the actual address in memory of that object, only the data contained within.

## Q4. What do Map, Filter, and Reduce do? Do they mutate the array you call them on?
1. Map - takes each element of an array and performs operations using each element. It does not mutate the parent array
2. Filter - creates a new array that contains elements from a parent array that pass a given "filter" function. It does not mutate the parent array
3. Reduce - runs a callback function over elements in the array that effectively results in an accumulation of all elements in the array. It does not mutate the parent array on its own, but it is possible for the callback function itself to mutate it

## Q5. What are all the Falsey values in JavaScript? Why do you think this is important to know?
false, 0, -0, 0n, "", '', ``, null, undefined, NaN, and document.all. They are important because they are type-coerced into Boolean in Boolean contexts, and as a result they can influence a program's behavior in ways that aren't always intuitive. They are also, however, very helpful in other contexts, such as checking whether or not given data that is required for a certain function even exists before performing an operation that would then throw an error due to that data not existing. This is especially helpful to understand when working with APIs and async operations in general.

## Q6. What are Async and Await?
"async" and "await" are implementations of promises that allow a given function to "await" data from an asynchronous operation, such as fetching data from an API. 

## Q7. What is an async function?
Using "async" as part of the function declaration allows you to use the "await" keyword within that function. It allows for a given operation to run asynchronously and to have other operations "await" completion of that operation or operations.

## Q8. What are try and catch?
Try and catch are implementations of error handling that instruct the program to "try" a given chunk of code via a "try" block, and in the event of an error, the "catch" block runs code defined by the programmer to handle said error.