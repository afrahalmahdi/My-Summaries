# Advanced JavaScript

Before We Begin
---
This course is a continuation of the JavaScript fundamentals crush course

# Advanced Concepts
- Nested function's scope
    
    Nested functions have access to variables declared in their own scope as well as variables declared in the outer scope.

    Lexical scoping => which describe how JavaScript resolves variable names when functions are nested.

    ```js
    let a = 10
    function outer() {
        let b = 20
        function inner() {
            let c = 30
            console.log(a, b, c)
        }
        inner()
    }
    outer()
    ```

- Closures

    A Closure is the combination of a function bundled together with references to its surrounding state.

    (عبارة عن مزيج من وظيفة مجمعة مع إشارات إلى الحالة المحيطة بها.)

    Closures are created every time a function is created, at function creation time.

    Closure in JavaScript is a form of lexical scoping used to preserve variables from the outer scope of a function in the inner scope of a function.

    Lexical scoping is the process used to define the scope of a variable by its position in the source code.

    ```js
    function outer() {
        let counter = 0
        function inner() {
            counter++;
            console.log(counter);
        }
        inner()
    }
    outer()
    outer()
    ```

    **Best Definition:**
    In JavaScript, when we return a function from another function, we are effectively returning a combination of the function definition along with the function's scope. This would let the function definition have an associated persistent memory which could hold on to live data between executions. That combination of the function and its scope chain is what is called a closure in JavaScript.

    **The Key Point:**
    To keep in mind, is that the closure in inner function has access to variables at the outer function scope even after the outer function has finished execution.

    In JavaScript, a closure is a combination of a function and its lexical environment. It allows a function to retain access to variables from its outer (enclosing) scope even after the outer function has finished executing. This means that variables and functions defined in the outer scope are still accessible within the inner function, even when the outer function has completed.

    They are commonly used to create private variables and encapsulate data within a function, providing a way to maintain state between function invocations.

    Ex:
    ```js
    function outer() {
        let outerVariable = 'I am from outer';

        function inner() {
            let innerVariable = 'I am from inner';
            console.log(outerVariable + ', ' + innerVariable);
        }

        // Return the inner function
        return inner;
    }

    // Call the outer function and assign the returned inner function to closureFn
    const closureFn = outer();

    // Call the closure function
    closureFn();

    // When we invoke outer and assign the result to closureFn, it creates a closure. The closure retains a reference to the outerVariable even after the outer function has finished executing. Therefore, when we subsequently invoke closureFn(), it can still access and log the values of both the outerVariable and the innerVariable.
    ```

    Closures are powerful because they allow functions to "remember" the variables and scope they were created in. They are commonly used to create private variables and encapsulate data within a function, providing a way to maintain state between function invocations.

    Closures can be used to create private variables in JavaScript by leveraging the concept of lexical scoping. Here's an example:
    ```js
    function createCounter() {
        let count = 0;

        function increment() {
            count++;
            console.log(count);
        }

        function decrement() {
            count--;
            console.log(count);
        }

        return {
            increment: increment,
            decrement: decrement
        };
    }

    const counter = createCounter();
    counter.increment(); // Output: 1
    counter.increment(); // Output: 2
    counter.decrement(); // Output: 1
    ```

    ***

- Currying

- this keyword

- Prototype

- Prototypal inheritance 

- class

- Iterables and Iterators

- Generators