# Learning Plan: Methods in Python

- [ ] 1. Method vs Function: Dot-Call Mental Model
  - **Action:** Explain difference between standalone functions and object-bound methods; show how `obj.method()` binds the instance. Exercise: Given a string variable, ask the learner to call two different methods (e.g., transform case and strip spaces) and explain results. Verify correct use of dot-call and accurate explanation of outcomes.
  - _Requirements: 1_

- [ ] 2. Instance Methods and `self`
  - **Action:** Explain that `self` is the first parameter referring to the current instance. Exercise: Implement a `Counter` class with `increment()` and `reset()` methods that read/write `self.value`. Verify that methods update state correctly and `self` is used consistently.
  - _Requirements: 2, 3_

- [ ] 3. Designing a Class with Methods
  - **Action:** Explain adding behavior to a class via methods. Exercise: Create a `BankAccount` with `deposit(amount)` and `balance()`; ensure internal state changes via `self`. Verify deposits accumulate and `balance()` returns the correct value.
  - _Requirements: 3, 5_

- [ ] 4. Method Parameters: Positional and Keyword
  - **Action:** Explain positional vs keyword arguments in methods. Exercise: Add `withdraw(amount, *, fee=0)` to `BankAccount`; practice both calling conventions. Verify parameter binding and fee handling.
  - _Requirements: 4_

- [ ] 5. Defaults, `*args`, and `**kwargs`
  - **Action:** Explain defaults and variable arguments. Exercise: Create a `Logger.log(level='INFO', *messages, **meta)` method that formats messages. Verify defaults apply, multiple messages are accepted, and meta is captured.
  - _Requirements: 4_

- [ ] 6. Return Values vs Side Effects
  - **Action:** Explain `return` vs mutating internal state; clarify that methods without `return` yield `None`. Exercise: Show difference between `list.sort()` (in-place) and `sorted(list)` (returns new). Verify learner can predict result type and list content after each operation.
  - _Requirements: 5_

- [ ] 7. Built-in Type Methods: Strings
  - **Action:** Explain core `str` methods (e.g., `strip`, `split`, `replace`, `upper`). Exercise: Given a messy string, clean and split it using methods. Verify chosen methods achieve the described transformation.
  - _Requirements: 6_

- [ ] 8. Built-in Type Methods: Lists
  - **Action:** Explain `append`, `extend`, `insert`, `pop`, `remove`. Exercise: Transform a list per a set of instructions. Verify final list matches the expected sequence and the learner notes in-place behavior.
  - _Requirements: 6, 5_

- [ ] 9. Built-in Type Methods: Dicts and Sets
  - **Action:** Explain `dict.get`, `update`, `keys`, `items`; `set.add`, `discard`, `union`. Exercise: Merge two dicts with defaults and compute set operations. Verify correct use of methods and resulting collections.
  - _Requirements: 6_

- [ ] 10. Instance vs Class vs Static Methods
  - **Action:** Explain differences and use-cases of instance methods, `@classmethod` (with `cls`), and `@staticmethod`. Exercise: Implement `Temperature` with `from_celsius` (classmethod) and `is_valid_scale` (staticmethod). Verify correct decorators and behavior.
  - _Requirements: 7_

- [ ] 11. Special (Dunder) Methods: Construction and Representation
  - **Action:** Explain `__init__`, `__repr__`, `__str__`. Exercise: Add these to a `Point(x, y)` class; ensure `repr(point)` is unambiguous and `str(point)` is user-friendly. Verify outputs meet conventions.
  - _Requirements: 8_

- [ ] 12. Special (Dunder) Methods: Protocols
  - **Action:** Explain `__len__`, `__eq__` and how they enable `len(obj)` and comparisons. Exercise: Create a `Bag` container supporting `len()` and equality by content. Verify `len(Bag([...]))` and equality checks work as intended.
  - _Requirements: 8_

- [ ] 13. Inheritance and Overriding
  - **Action:** Explain overriding methods and extending behavior with `super()`. Exercise: Define `Animal.speak()` and override in `Dog`; show `super().__init__` to extend base initialization. Verify overridden method is called and base logic is preserved when intended.
  - _Requirements: 9_

- [ ] 14. Binding, Bound Methods, and Scopes
  - **Action:** Explain bound vs unbound functions and name lookup within methods. Exercise: Inspect `type(obj.method)` and access local vs `self.attr` variables. Verify learner can articulate binding and scopes and predict attribute resolution.
  - _Requirements: 10_

- [ ] 15. Encapsulation Conventions and Name Mangling
  - **Action:** Explain `_name` (internal-use convention) and `__name` (name mangling). Exercise: Demonstrate attribute access differences and how mangling affects subclassing. Verify correct explanation and usage.
  - _Requirements: 11_

- [ ] 16. Properties and Validation
  - **Action:** Explain `@property` with getter/setter for controlled access. Exercise: Add a `percentage` property with validation to a class; raise error on invalid values. Verify setter enforces constraints and property reads computed value.
  - _Requirements: 12, 13, 14_

- [ ] 17. Error Handling in Methods and Docstrings
  - **Action:** Explain raising and handling exceptions; write clear docstrings (purpose, params, returns, exceptions). Exercise: Add input checks to a method, raise `ValueError`, and document behavior. Verify exception is raised appropriately and docstring meets style.
  - _Requirements: 13, 14_

- [ ] 18. Type Hints for Methods
  - **Action:** Explain annotating parameters and return types; introduce `typing` for collections/generics. Exercise: Annotate methods in a small class and run a basic type check (conceptually). Verify annotations reflect intended types.
  - _Requirements: 15_

- [ ] 19. Fluent APIs and Method Chaining
  - **Action:** Explain when to return `self` and chaining trade-offs. Exercise: Implement a `QueryBuilder`-like class where methods return `self` for chaining; provide one method that returns data to contrast. Verify chain works and learner can discuss readability/side effects.
  - _Requirements: 16_

- [ ] 20. Synthesis Mini-Project
  - **Action:** Guide the learner to build a small `TodoList` library using instance methods, at least one `@classmethod` or `@staticmethod`, properties with validation, clear docstrings, error handling, selected dunders, type hints, and one fluent method. Verify all components meet earlier success criteria and work together in a short demo script.
  - _Requirements: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16_
