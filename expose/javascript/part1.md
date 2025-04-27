# Part 1. A Quick Introduction

For this section (questions 1-7), observe the effect that the keywords const, var, and let have on the sumValues() function and those differences are caused by their differing variable scopes. Write your answers to the questions in `part1.md`.

## var declaration - AVOID USING VAR WHENEVER POSSIBLE

1. Given the function call `sumValues(10, 10, true);` line 9 would print `values added: 20`.
2. Given the function call `sumValues(10, 10, true);` line 13 would print `final result: 20`.
3. You should not use `var` because we can experience unintended side-effects when our variables are not scoped properly within our `if` and `for` blocks (it is function-scoped not block-scoped). We can also run into a lot of cases where we will end up using a variable declared using `var` and it might be `undefined` causing unexpected behaviors at runtime (because it is hoisted).
4. Given the function call `sumValues(10, 10, true);` line 9 would print `values added: 20`.
5. Given the function call `sumValues(10, 10, true);` line 13 would return an error: `ReferenceError: result is not defined` because `let` variables are block-scoped, meaning they only exist within the "block" they are defined in, and in this case it is within a `if` block.
6. Given the function call `sumValues(10, 10, true);` line 9 would never get executed because line 7 tries to modify the `const` variable `result` by assigning it to a new value. Therefore, this would return an error and stop executing at line 7.
7. Given the function call `sumValues(10, 10, true);` line 13 would never get executed because line 7 tries to modify the `const` variable `result` by assigning it to a new value. Therefore, this would return an error and stop executing at line 7.
