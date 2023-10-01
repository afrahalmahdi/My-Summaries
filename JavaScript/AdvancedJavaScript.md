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

- Currying

- this keyword

- Prototype

- Prototypal inheritance 

- class

- Iterables and Iterators

- Generators