# Learning Plan: Functions in Python

- [x] 1. Introduction to Functions and Basic Definition
  - **Action:** Explain what functions are using the recipe analogy (ingredients = parameters, steps = function body, result = return value). Introduce the `def` keyword, function naming rules, and basic syntax. Create an exercise asking the user to write a simple `say_hello` function that prints "Hello, World!" and then call it. Verify the function is defined correctly and produces the expected output.
  - _Requirements: 1.1, 1.2_

- [ ] 2. Understanding Parameters and Arguments
  - [ ] 2.1 Positional Arguments Fundamentals
    - **Action:** Explain how to pass data to functions using positional arguments. Create an exercise for a `greet_user(name)` function that prints a personalized greeting like "Hello, [name]!". Verify the user's function accepts one argument and uses it correctly in the output.
    - _Requirements: 2.1_
  
  - [ ] 2.2 Multiple Parameters and Order
    - **Action:** Explain functions with multiple parameters and how argument order matters. Create an exercise asking the user to write a `create_profile(name, age)` function that returns a formatted string "Name: [name], Age: [age]". Verify correct parameter usage and formatting.
    - _Requirements: 2.1_

- [ ] 3. Return Values and Function Output
  - [ ] 3.1 Basic Return Statements
    - **Action:** Explain the `return` keyword vs `print()`, and how it sends data back from a function. Create an exercise for an `add_numbers(a, b)` function that returns the sum (not prints it). Verify the function returns the correct numerical value that can be used in other expressions.
    - _Requirements: 3.1_
  
  - [ ] 3.2 Functions Without Explicit Return
    - **Action:** Explain that functions without return statements implicitly return `None`. Create an exercise where the user writes a function that only prints and demonstrate that it returns `None`. Verify understanding of the `None` return value.
    - _Requirements: 3.2_

- [ ] 4. Variable Scope and Lifetime
  - [ ] 4.1 Local vs Global Variables
    - **Action:** Explain local variables (inside functions) vs global variables (outside functions). Create an exercise where the user attempts to access a local variable outside its function to demonstrate scope limitations. Verify understanding of variable accessibility.
    - _Requirements: 4.1_
  
  - [ ] 4.2 Using Global Variables Correctly
    - **Action:** Explain the `global` keyword for modifying global variables within functions. Create an exercise where the user writes a function that modifies a global counter variable. Verify correct usage of the `global` keyword.
    - _Requirements: 4.2_

- [ ] 5. Function Documentation and Best Practices
  - [ ] 5.1 Writing Docstrings
    - **Action:** Explain the importance of docstrings and the Google style format. Create an exercise where the user adds proper docstrings to their previous functions. Verify docstrings include purpose, parameters, and return value descriptions.
    - _Requirements: 5.1_
  
  - [ ] 5.2 Function Naming and Readability
    - **Action:** Explain best practices for function naming (descriptive, snake_case) and single responsibility principle. Create an exercise where the user refactors a poorly named function. Verify improved naming and clarity.
    - _Requirements: 5.2_

- [ ] 6. Default Parameter Values
  - [ ] 6.1 Basic Default Parameters
    - **Action:** Explain how to set default values for parameters to make functions optional. Create an exercise modifying the `greet_user` function to have a default name value of "Guest". Verify the function works both with and without arguments.
    - _Requirements: 2.2_
  
  - [ ] 6.2 Common Pitfall - Mutable Defaults
    - **Action:** Explain the danger of using mutable objects (like lists) as default arguments. Show the problem and then the `None` pattern solution. Create an exercise where the user fixes a function with a mutable default. Verify correct usage of the `None` pattern.
    - _Requirements: 2.2_

- [ ] 7. Advanced Function Features
  - [ ] 7.1 Variable Positional Arguments (*args)
    - **Action:** Explain `*args` for accepting any number of positional arguments. Create an exercise where the user writes a `calculate_average(*numbers)` function that returns the average of any number of inputs. Verify the function works with varying numbers of arguments.
    - _Requirements: 6.1_
  
  - [ ] 7.2 Variable Keyword Arguments (**kwargs)
    - **Action:** Explain `**kwargs` for accepting any number of keyword arguments. Create an exercise where the user writes a `create_user_profile(name, **details)` function. Verify the function can accept any number of additional details as keyword arguments.
    - _Requirements: 6.2_
  
  - [ ] 7.3 Lambda Functions
    - **Action:** Explain lambda functions for simple, anonymous functions. Create an exercise where the user creates a lambda function to square a number and another to check if a number is even. Verify correct lambda syntax and usage.
    - _Requirements: 6.3_

- [ ] 8. Practical Application Project
  - **Action:** Guide the user through creating a simple utility library with 3-4 functions that work together (e.g., a text processing tool or simple calculator). The project should incorporate all learned concepts: parameters, returns, scope, docstrings, and default values. Verify the functions work together cohesively and demonstrate proper use of all concepts.
  - _Requirements: All previous concepts_