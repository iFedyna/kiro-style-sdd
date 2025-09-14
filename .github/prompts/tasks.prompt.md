
### 3. Create Learning Task List

Now, create an actionable **Learning Plan** with a checklist of interactive teaching tasks, based on the approved requirements and learning design. This document will guide a tutoring agent through the process of teaching the user.

The `tasks.md` document should be based on the `design.md` document just created.

**Constraints:**

* The model MUST create a '.kiro/specs/{feature_name}/tasks.md' file if it doesn't already exist
*   The model MUST return to the design step if the user indicates any changes are needed to the design.
*   The model MUST return to the requirement step if the user indicates that we need additional requirements.
*   The model MUST use the following specific instructions when creating the learning plan:

``` text
Convert the learning design into a series of prompts for a **tutoring LLM**. Each prompt will guide the agent to deliver a complete micro-lesson:
1. Provide a theoretical explanation of a concept.
2. Create a small, practical coding exercise for the user to practice that concept.
3. Wait for the user's submission and then verify if it is correct.

Prioritize a gradual learning curve, incremental progress, and immediate feedback. Ensure each task builds logically on the previous one. Focus ONLY on tasks that involve this explain-practice-verify loop.
```

*   The model MUST create a `tasks.md` file and format the learning plan as a numbered checkbox list with a maximum of two levels of hierarchy.
*   The model MUST ensure each task item includes:
    *   A clear learning objective as the task description.
    *   A sub-bullet with a clear **Action** for the tutoring agent, describing what to explain, what exercise to create, and the success criteria for verification.
    *   A sub-bullet referencing the specific learning requirements from the `requirements.md` document.
*   The model MUST ensure the plan is a series of discrete, manageable learning steps.
*   The model MUST assume that the tutoring agent will have access to all context documents (requirements, design).
*   The model MUST ensure the plan covers all topics from the learning design.
*   The model MUST NOT include tasks unrelated to teaching, such as deploying applications or user acceptance testing.
*   The model MUST ensure each task is concrete enough that a tutoring agent can execute it without further clarification.
*   After creating or updating the `tasks.md` document, the model MUST ask the user: **"Does this final learning plan look good?"**
*   The model MUST make modifications to the task list if the user requests changes.
*   The model MUST ask for explicit approval after every iteration of edits and continue the feedback cycle until approval is received.

**Example Format (based on our "Functions in Python" topic):**

```markdown
# Learning Plan: Functions in Python

- [ ] 1. Introduction to Defining and Calling Functions
  - **Action:** Explain the `def` keyword, function naming rules, and syntax. Create an exercise asking the user to write a simple `say_hello` function that prints "Hello, World!" and then call it. Verify the function is defined correctly and the expected output is printed.
  - _Requirements: 1.1, 1.2_

- [ ] 2. Understanding Parameters and Arguments
  - [ ] 2.1 Explain and practice positional arguments
    - **Action:** Explain how to pass data to functions using positional arguments. Create an exercise for a `greet(name)` function that prints a personalized greeting. Verify the user's function accepts one argument and uses it in the output.
    - _Requirements: 2.1_
  - [ ] 2.2 Explain and practice default arguments
    - **Action:** Explain how to set default values for parameters. Modify the previous exercise, asking the user to give the `name` parameter a default value of "Guest". Verify that calling `greet()` with no arguments works correctly.
    - _Requirements: 2.2_

- [ ] 3. Getting Data Back from Functions
  - **Action:** Explain the `return` keyword and how it sends a value back from a function. Create an exercise for an `add(a, b)` function that returns the sum of two numbers. Verify the function returns the correct numerical value, not just prints it.
  - _Requirements: 3.1, 3.2_

[Additional learning tasks continue...]
```