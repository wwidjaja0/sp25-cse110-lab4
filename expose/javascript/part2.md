# Part 2. A Little More of a Challenge

In this next section, use what you understand about the differences between declaring variables with var, let, and const to help you work with a more complicated block of code. Write your answers to the questions below in `part2.md`.

## var declaration - AVOID USING VAR WHENEVER POSSIBLE

1. Given the function call `discountPrices([100, 200, 300], 0.5);` line 12 will print `2` because `var i = 0` hoists the variable `i` into the function-scope so `console.log(i)` will not throw an error.
2. Given the function call `discountPrices([100, 200, 300], 0.5);` line 13 will print `150` because `var discountedPrice` hoists the variable `discountedPrice` into the function-scope so `discountedPrice` takes on the value `prices[2] * (1 - 0.5)` which will not throw an error. `var` variables are also allowed to be redeclared without issue.
3. Given the function call `discountPrices([100, 200, 300], 0.5);` line 14 will print `150` because `var finalPrice` puts the variable into function-scope. `discountedPrice` takes on the value `prices[2] * (1 - 0.5)` which will not throw an error. `var` variables are also allowed to be redeclared without issue. Modifying `finalPrice` in the loop body modifies the function-scoped `finalPrice` so after the loop body completes, line 14 will print `150`.
4. Given the function call `discountPrices([100, 200, 300], 0.5);` this function will return an array of `[50, 100, 150]` because we calculate the discounted price on line 7, line 8 is redundant, and line 9 pushes the value onto the array.
5. Given the function call `discountPrices([100, 200, 300], 0.5);` line 12 would return an error: `ReferenceError: i is not defined` because `let` variables are block-scoped, meaning they only exist within the "block" they are defined in, and in this case it is within a `for` block.
6. Given the function call `discountPrices([100, 200, 300], 0.5);` line 13 would return an error: `ReferenceError: discountedPrice is not defined` because `let` variables are block-scoped, meaning they only exist within the "block" they are defined in, and in this case it is within a `for` block.
7. Given the function call `discountPrices([100, 200, 300], 0.5);` line 14 will print `150` because `let finalPrice` is scoped at the function level, and the inner loop will modify this function level variable.
8. Given the function call `discountPrices([100, 200, 300], 0.5);` the function would return the array `[50, 100, 150]` because `let discounted` is scoped at the function level, and the inner loop will modify this function level variable.
9. Given the function call `discountPrices([100, 200, 300], 0.5);` line 11 will print `2`. Although the `discounted` array is a `const` variable, we are still able to modify the contents of the array so long as we do not reassign the variable on line 8. Therefore, the code runs without error.
10. Given the function call `discountPrices([100, 200, 300], 0.5);` line 12 will print out `3` because we declare `length` as a `const` and (using the same reasoning as the last question,) the code runs without error.
11. Given the function call `discountPrices([100, 200, 300], 0.5);` the function will return the array `[50, 100, 150]`. (Using the same reasoning as the last question, there is no error.)

12A. `student["name"]`

12B. `student["Grad Year"]`

12C. `student['greeting']()`

12D. `student["Favorite Teacher"]["name"]`

12E. `student["courseLoad"][0]`

13A. `'3' + 2` -> `'32'` - When using `+`, if one operand is a string, JavaScript concatenates them.

13B. `'3' - 2` -> `1` - The `-` operator forces both operands to be treated as numbers.

13C. `3 + null` -> `3` - `null` is treated as 0 in numeric operations.

13D. `'3' + null` -> `'3null'` - With `+` and a string, `null` is converted to the string `'null'`.

13E. `true + 3` -> `4` - `true` becomes 1 in a numeric context.

13F. `false + null` -> `0` - `false` becomes 0, `null` becomes 0.

13G. `'3' + undefined` -> `'3undefined'` - String concatenation happens, and undefined becomes the string `'undefined'`.

13H. `'3' - undefined` -> `NaN` - forces a numeric operation. `'3'` becomes `3`, but `undefined` cannot be converted to a number.

14A. `'2' > 1` -> `true` - `'2'` is coerced into a number 2.

14B. `'2' < '12'` -> `false` - JavaScript uses lexicographical order. '2' comes after `'1'`.

14C. `2 == '2'` -> `true` - `==` allows type coercion. `'2'` is converted to `2`.

14D. `2 === '2'` -> `false` - `===` does not allow type coercion. One is a number (`2`), the other a string (`'2'`).

14E. `true == 2` -> `false` - `true` becomes `1`.

14F. `true === Boolean(2)` -> `true` - `Boolean(2)` converts `2` to `true`, because any non-zero number as a boolean is `true`.

15\. The `==` operator simply checks for equality and attempts to reconcile (coerce) differing datatypes, whereas the `===` operator compares the value of the two variables/values being compared as well as their types and only returns true if their types and values are equivalent. Essentially, `===` type checks but `==` does not.

17\. Given the function call `modifyArray([1,2,3], doSomething);` this function will return an array of `[2, 4, 6]`. A new empty array called `newArr` is created. The for loop is run with the callback function being `doSomething` which doubles the number passed into it which gets pushed into the `newArr` object. Finally, `newArr` gets returned which is just the same array with the doubled version of all the numbers in it.

19\. The output of the above code is `1` followed by a `4` followed by a `3` followed by a `2`. The reason why the output is in this order is because the synchronous code runs first printing `1` then `4`, then the timers run printing `3` and then `2` because of their delays.
