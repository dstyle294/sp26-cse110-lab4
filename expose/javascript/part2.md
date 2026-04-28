1. At Line 12, `3` will be printed, since `i` is declared as a `var` type, so it's scope is not limited to the for loop, and is defined for the entire function. Therefore, at the end of the for loop, since the length of the list is 3, we will increase `i` till it reaches 3 and then exit the for loop. 
2. We know that `discountedPrice` is declared as a `var` type, so it's scope is defined for the entire function. Using the discount factor, we find that at the end of the for loop, `i = 2`, so discountedPrice = $0.5(300) = 150$. So, we will print `150`. 
3. We know that `finalPrice` is declared in the function, so it's scope is throughout the function (doesn't matter that it is a `var` type). Using the `discountedPrice` at the end of the for loop, we find that `finalPrice` = $Math.round(150 * 100) / 100 = 150$, so we print `150`
4. This will return all of the `discountedPrice`, for each value of `i` as a list. This is `[50, 100, 150]`.
5. Line 12 will return an error, since `i` is defined as a `let` type in the for loop, meaning that it is not declared for the entire function's scope, so `i` is not defined here. 
6. Line 13 will return an error since `discountedPrice` is defined for the scope of the for loop only, and not the entire function's scope, so `discountedPrice` is not defined here. 
7. Line 14 will print the price at the end of the for loop, since it is declared for the entire function's scope. This final price is the same as Question 3, `150`.
8. Since discounted is declared for the entire function's scope, the discounted list will contain all of the discounted prices, the same as question 4, `[50, 100, 150]`.
9. Line 11 will return an error, since `i` is defined as a `let` type in the for loop, meaning that it is not declared for the entire function's scope, so `i` is not defined here. 
10. Line 12 will print the length of `prices`, which is `3`. 
11. This will return the discounted list of prices, as expected, `[50, 100, 150]`. Note that you can modify the contents of the list, even though it is defined as a `const` variable type. The `const` variable type simply makes sure that you cannot reassign `discounted` itself.
12. Here is the required notation:
    1.  A. Use `student.name`
    2.  B. Use `student['Grad Year']`
    3.  C. Use `student.greeting()`
    4.  D. Use `student['Favorite Teacher'].name`
    5.  E. Use `student.courseLoad[0]`
13. Arithmetic
    1.  A. `'32'` because the number 2 is converted to a string (numeric type conversion) and concatenated into one string
    2.  B. 1 because subtraction results in subtraction of numbers. So, '3' is converted to 3, and then we have 3 - 2 = 1. 
    3.  C. null is converted to  0, so we have 3 + 0 = `3`.
    4.  D. null is converted to  'null', so we have '3' + 'null' = `3null`
    5.  E. true is converted to  1, so we have 1 + 3 = `4`
    6.  F. The + operator triggers numeric conversion, so false becomes 0, and null becomes 0, so we have 0 + 0 = `0`.
    7.  G. undefined becomes 'undefined', so '3' + 'undefined' = `'3undefined'`
    8.  F. The - operator triggers numeric conversion, so '3' becomes 3 and undefined becomes NaN, so we have 3 - NaN = `NaN`
14. Comparison
    1. A. True, as '2' will get converted to the number 2, and 2 > 1 is `true`
    2. B. False, as string comparison will compare character by character, and since '2' > '1' by ASCII ordering, '2' < '12' is `false`
    3. C. True, as '2' will get converted to the number 2, and 2 == 2 is `true`
    4. D. False, as === is a strict equality operator that checks the equality without type conversion. So, since 2 and '2' are of different types, this immediately returns `false`
    5. E. False, as true will be converted to 1, and 1 == 2 is `false`.
    6. F. True, as Boolean(2) will return true, as all values except 0 are true. So, true == true returns `true`.
15. The == operator first performs type conversion if necessary, and then checks equality; the === operator is a strict equality operator, which checks equality without type conversion, allowing you to truly check whether two values are the same. 
17. Stepping through modifyArray, we see that for each element of index i of the array ([1, 2, 3]), we push callback(array[i]) to a new empty array. Since our callback is `doSomething` which doubles the value of the num we pass to it, we will get `[2, 4, 6]` returned to us from modifyArray, as that's what newArr will hold (doSomething(num) for num in [1,2,3]).
19. The code will output the following because even though there is a timeout of 3 for `console.log(3)`, it is first placed on a queue and scheduled to run at the next opportunity, not immediately, and thus console.log(4) is run first. 
- 1
- 4
- 3
- 2