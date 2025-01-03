# Javascript + operator unexpected string concatenationThis bug demonstrates the unexpected behavior of the + operator in Javascript when used with strings. The + operator will perform string concatenation if one of the operands is a string. This can lead to unexpected results if you are not careful.## Bug DescriptionThe bug is in the following Javascript function:```javascriptfunction foo(a,b){return a+b;}console.log(foo(2,3)); //Expected output: 5console.log(foo(2,"3")); //Unexpected output: 23```The expected output of the first `console.log` statement is 5. The actual output is 5. The expected output of the second `console.log` statement is 5. The actual output is 23. This is because the + operator performs string concatenation when one of the operands is a string.## SolutionThe solution is to use the Number() function to convert the string to a number before performing the addition. The corrected Javascript function is:```javascriptfunction foo(a,b){return Number(a) + Number(b);}console.log(foo(2,3)); //Expected output: 5console.log(foo(2,"3")); //Expected output: 5```This solution ensures that the + operator performs addition instead of string concatenation, resulting in the expected output.