======== DATA TYPES =============
-QUESTION: "What is a data type?"

    * ANSWER: "A classification of data which tells the compiler or interpreter how the programmer intends to use the  data."

-QUESTION: "What are reference data types in JavaScript?"

    * ANSWER: "Object. Just object!"

-QUESTION: "What are the primitive data types in JavaScript?"

    * ANSWER: "String, number, boolean, null, undefined, symbol"

-QUESTION: "What's the difference between `null` and `undefined`?"

    * ANSWER: "`null` is explicitly set to an empty value, `undefined` has no value"

-QUESTION: "What's the difference between Primitive and Reference types in Javascript?"

    * ANSWER: "A primitive type has a fixed amount of memory that it takes up, where as a reference type does not. Examples of primitive types are boolean values or integers, where as examples of ref types would be arrays. ref types like arrays are made up of references to their values, hence the name"

-QUESTION: "What's the difference between `==` and `===` in JS?"

    * ANSWER: "Type Coercion -- `==` doesn't care about type (i.e. type coercion), so `\"2\" == 2` will evaluate to `true`. `===` does care about type, so `\"2\" === 2` will evaluate to `false`."

-QUESTION: "Why does `(1 / 3).toFixed(2) + 3` equal `0.333`?"

    * ANSWER: "toFixed() coerces to a string, which makes `+` act as a concatenation operator, so it appends 3 to the resulting string",
    
-QUESTION: "How big can a number be in JavaScript?"

    * ANSWER: "The range of safe numbers in JavaScript is -(2^53 - 1) to (2^53 - 1). This is roughly 9 quadrillion values."
    
-QUESTION: "Why doesn't 0.1 + 0.2 = 0.3 in JavaScript?"

    * ANSWER: "Because JavaScript stores data as double-precision floating point numbers, which can't accurately represent the infinite amount of decimal numbers there is."

========== SCOPE =========

 -QUESTION: "What is scope?"

    * ANSWER: "A container where references to variables and functions are shared."

 -QUESTION: "What is the difference between `var`, `let`, and `const`?"
 
    * ANSWER: "`var` is scoped to the function, `let` and `const` are scoped to the block, `const` cannot be reassigned."

-QUESTION: "Name 2 or more ways to define a global variable in Javascript"

    * ANSWER: "Leave off the `var`, assign it to the `window`, or declare it in the top-level scope"

-QUESTION: "Explain \"hoisting\"."

    * ANSWER: "A declared function is brought to the top of a scope before the code in the rest of the scope executes, which makes that function available everywhere in the scope"

-QUESTION: "Why is it dangerous to pollute or use the global scope?"

    * ANSWER: "Libraries and frameworks might have modified the global scope, which makes it unreliable."

 -QUESTION: "What is a closure, and how/why would you use one?"

    * ANSWER: "A closure is a function that maintains a reference to it's outer scope. These are useful in high-order functions."

  -QUESTION: "You declare a variable in the middle of a scope. Where is that variable accessible?"

    * ANSWER: "Anywhere after the declaration in the same scope, as well as any nested scopes created after the declaration."

 -QUESTION: "What does it mean to shadow a variable?"

    * ANSWER: "Redeclaring a variable that's available in an outer scope, which removes access to it."

 -QUESTION: "What is the difference between declaring a function vs. declaring a function expression?"

    * ANSWER: "A declared function is hoisted, a function expression is not."

========== DOM ===========================================================================

-QUESTION: "What is the DOM?"

    * ANSWER: "The document object model, the API the browser exposes for web pages"

-QUESTION: "How do you create a div element?"

    * ANSWER: "`const $div = document.createElement('div')`"

-QUESTION: "What are 5 ways you can access a DOM element?"

    * ANSWER: "`document.querySelector`, `document.querySelectorAll`, `document.getElementById`, `document.getElementsByClass`, `document.getElementsByTagName`"

-QUESTION: "How do you access the `form` element on a form submission event?"

    * ANSWER: "`event.target`"

-QUESTION: "How do you set the `background-color` of a given DOM element to red?"

    * ANSWER: "`element.style.backgroundColor = red;`"

-QUESTION: "How do you access the `src` attribute of an `img` element?"

    * ANSWER: "With `img.src` or `img['src']`"

-QUESTION: "What's the difference between setting the `innerHTML` of an element and using `appendChild()`?"

    * ANSWER: "`innerHTML` completely replaces the content and takes a string, `appendChild()` adds to the element's children and takes a DOM element"

-QUESTION: "What is event bubbling?"

    * ANSWER: "An event that happens on an element also happens on all parent elements sequentially unless `event.stopPropagation` is called."

-QUESTION: "What are the 3 phases of a DOM event firing?"

    * ANSWER: "Capture (going from the body down to the element that fired), Target (when the innermost element fires), Bubbling (when the event comes back through the DOM))"

 -QUESTION: "Compare and contrast a NodeList and an Array."

    * ANSWER: "Both are collections, but they have different prototypes and therefore different methods available. For instance, `NodeList`s don't have native array methods."

========== PATTERNS ==============================================================

-QUESTION: "Explain the difference between synchronous and asynchronous functions."

    * ANSWER: "When a function does not immediately return a value, it is asynchronous. The rest of the program continues executing, requiring special handling and callback functions for when asynchronous function calls complete."

-QUESTION: "What is event delegation?"

    * ANSWER: "Letting a parent element's event handler respond to an event instead of the original element"

-QUESTION: "How does Array.prototype.reduce work?"

    * ANSWER: "It accepts a function and an initial value, and returns the last value returned from the passed-in function. The function's signature that it accepts an accumulator and a current value, and returns the value of the accumulator in the next iteration."

-QUESTION: "What is an IIFE and what does it do?"

    * ANSWER: "Immediately invoked function expression, creates a function and immediately runs it"

-QUESTION: "What's the difference a class and an object?"

    * ANSWER: "An class is a blueprint for making an object, an object is an instance of the blueprint."

-QUESTION: "What does the `this` keyword refer to in JavaScript?"

    * ANSWER: "1. The first value passed to call() or apply()\n2. The value that was bind()ed to the function\n3. The calling object\n4. The global scope"

-QUESTION: "What is the benefit of using event delegation?"

    * ANSWER: "Event listeners are relatively expensive, and this pattern allows you to use fewer of them"

-QUESTION: "What is the factory pattern?"

    * ANSWER: "An OOP pattern- When you create a new instance, but let an intermediate object determine the exact class of the instance."

-QUESTION: "What are the 4 pillars of OOP and what do they mean?"

    * ANSWER: "1. Encapsulation - State and behavior and contained together and access to state is mediated through getters and setters.\n2. Inheritance - State and behavior can be inherited by subclasses without redeclaring them\n3. Polymorphism - Changing the behavior of a subclassed object\n4. Abstraction - Only exposing the relevant details, not the inner implementation"

-QUESTION: "What are some tenets of functional programming?"

    * ANSWER: "1. Functional purity (no side-effects, output derived only from input)\n2. Simple functions\n3. First-class functions (functions as variables)\n4. Higher-order functions (functions that return functions or accept functions as arguments)"

=========== ENGINES ========================================================

-QUESTION: "What is a JavaScript runtime?"

    * ANSWER: "A platform that compiles and runs JavaScript code."

-QUESTION: "What is node.js?"

    * ANSWER: "A runtime that allows you to run JavaScript outside of a browser."

-QUESTION: "Is JS single or multi-threaded?"

    * ANSWER: "Single-threaded- it uses the event loop to achieve concurrency."

-QUESTION: "Name three major JavaScript engines and who maintains them."

    * ANSWER: "Mozilla - Rhino, Mozilla - SpiderMonkey, Google - V8, Safari - Nitro, IE/Edge - Chakra"

-QUESTION: "Name 2 global variables that exist in the browser, but not in node."

    * ANSWER: "`document`, `window`"

 -QUESTION: "Name 3 global variables that exist in node, but not in the browser."

    * ANSWER: "`process`, `global`, `module`, `require`"

-QUESTION: "Is JavaScript compiled or interpreted?"

    * ANSWER: "JavaScript is compiled at run-time with a JIT compiler."
    
-QUESTION: "What is the disadvantage of having a function return multiple types?"

    * ANSWER: "It prevents the JavaScript compiler can't optimize your code."

-QUESTION: "What does it mean if the maximum callstack size is exceeded?"

    * ANSWER: "It means there are more scheduled instructions than the browser is capable of handling, often because of an infinite loop."

-QUESTION: "What is the event loop?"

    * ANSWER: "The event loop listens for queued up messages and adds instructions to the call stack"

====== PROTOTYPES ======================================================================

-QUESTION: "What kind of inheritance does JavaScript have?"

    * ANSWER: "Prototypal inheritance"

-QUESTION: "How do you set the prototype of a class without using `extends`?",
    
    * ANSWER: "",

-QUESTION: "How does inheritance work in JavaScript?",
    
    * ANSWER: "JavaScript has prototypal inheritance. Rather than a blueprint, objects are linked to other object instances via prototypes.",
    
-QUESTION: "How do you set the prototype of a class that uses the `class` syntax?",
    
    * ANSWER: "Using the `extends` keyword.",

-QUESTION: "What is the prototype chain?",
    
    * ANSWER: "What you access a property or method on an object, it looks for it on the object, then the object's prototype, and then that object's prototype until it either finds it or reaches the top-level prototype",

 -QUESTION: "How do you create and use a class in JavaScript without the the `class` keyword?",
    
    * ANSWER: "Declare a function, and then call it with the `new` keyword.",

-QUESTION: "What is `.__proto__`?",
    
    * ANSWER: "`__proto__` is the actual object used in the lookup chain to resolve methods",

-QUESTION: "What is `.prototype`?",
    
    * ANSWER: "`.prototype` is the object that is used to build `__proto__` when you create an object with `new`.",

-QUESTION: "What are the dangers of extending built-in prototypes?",
    
    * ANSWER: "Similar to polluting the global scope, anything you modify in a built-in prototype may be changed in the Ecmascript spec in the future, and may be overridden by another library or framework.",

-QUESTION: "What's the advantage of putting a method on a prototype instead of an instance?",
    
    * ANSWER: "Reduces the memory used by reducing the number of copies of the method",
    