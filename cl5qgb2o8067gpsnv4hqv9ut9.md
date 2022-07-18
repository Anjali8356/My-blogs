## Strict Mode in javascript

**What is "Strict Mode" in javascript?
**

"Strict Mode" is used in Javascript that allows preventing actions in javascript code and throws more exceptions. It was first introduced in ECMAScript 5 and helps to avoid bad syntax, and makes javascript code secure.

**For Instance:**

*//without strict mode*

```
str =" How are you";

document.write(str);
```

This code will not show any error and get executed successfully but assigning value to the variable before the declaration, is counted as bad practice for coders. it also affects the final output. , When there is a large project it becomes tough to debug the code.

*//with strict mode
*
```
'use strict'

str = "How are you";  //  throw a reference error

document.write(str);
```
as you can clearly see, the use of 'use strict' is giving a reference error for the same code as above.

so how can you correct it?

*declare the variable first before assigning it a value.

```
'use strict'

Let str = "How are you";

document.write(str);
```

**What are the other things "strict mode" doesn't allow?**

1. Use of undefined variables.
2. Use of reserved keywords as variable or function names (such as return, if, else, etc.)
3. Duplicate properties of an object
4. Duplicate parameters of a function.
5. Assign values to read-only properties
6. Modifying arguments object
7. Octal numeric literals.
8. with statement.
9. eval function to create a variable
10. Using an object without declaring it.

**Advantages of using "strict mode":
**
1. Eliminate JavaScript silent errors by throwing errors.
2. Fixes mistake that makes it difficult for the JavaScript engine to perform optimization.
4. Make code run faster sometimes than identical code that's not in strict mode.
**********
Follow for more!!
