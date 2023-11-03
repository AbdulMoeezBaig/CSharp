# CSharp (Free Code Camp)
## https://www.freecodecamp.org/learn/foundational-c-sharp-with-microsoft/write-your-first-code-using-c-sharp/write-your-first-c-sharp-code

## Things To Remember
## Chapter 1 (7/7)
1. Console.Write() --> Console is the class name, write is the method. The "." in between is a member access operator  
2. Methods have () after it. () is called the method invocation operator  
3. Double Quotes " " inclose a string called a "Literal String", use single quotes for characters
4. Literal value = constant that never changes
5. Data Types (char, string, int, float, double, decimal, bool ), append at end (0.0012312F) F or f for float, M or m for Decimal
6. Character Escape Sequence begins with backslash "\" such as \n \t (n = new line, t = tab). Use \ to show double quotes in output 
7. To write "\" in output, use \\ (double), one as escape sequence, and one for output
8. To not use escape sequence, a verbatim string literal ("@") can be used such as Console.WriteLine(@"   c:\source\..."); Does not make sense if using double quotes, only for backslash help and to keep all white spaces, kindof prints a paragraph type formatting  
9. To add encoded characters in literal strings, use \u escape sequence followed by a 4 digit character code representing the character in UTF-16 such as Console.WriteLine("I have 1000000000000\u20ac");
10. String concatenation works with just a "+" between the variables / strings
11. String interpolation --> string message = $" {var1} {var2} ..."; --> more precise
12. Both string concatenation and addition use the plus + symbol. This is called overloading an operator, and the compiler infers the proper use based on the data types it's operating on.
13. Casting is a type of data conversion used with variables such as (float) var1 / (float) var2 which would normally be 12f/5 or 12f/5f or 12/5f, we use cast cz we don't have numbers

## Chapter 2
1. Stateless vs Stateful (Console.Write is stateless, some methods are stateful and must have access to state of application (rely on values stored in memory by previous lines of codes)
2. A single class can support both stateful and stateless methods. However, when you need to call stateful methods, you must first create an instance of the class so that the method can access state.
3. Instance of a class = object
4. Overloaded methods --> Methods that can take multiple types of input parameters
5. Use docs.microsoft.com for information about overloaded methods
6. 



---

## Coding Style
### Chapter 1
1. Variables should use camel case i.e. thisIsCamelCase
2. Starting with underscore (_VariableName) is for a special purpose
3. Combine strings in the Console.Write() instead of making a new variable

### Chapter 2
1. red squiggly line appears --> compilation error
2. 'parameter' refers to the variable that's being used inside the method. An 'argument' is the value that's passed when the method is called.
3.  To examine the second overloaded version of the method, press ALT + Down Arrow on the keyboard.
4.  Code block is enclosed by {} i.e. brackets
5.  



---

### List of Commands / Methods
### Chapter 1
1. Console.WriteLine()--> Prints a new line after output
2. Console.Write()--> Prints output
3. var--> sets datatype itself (var myName = "Abdul Moeez", var auto sets myName to be of type STRING), keeps things dynamic when we don't know what to use, the compiler selects the type  
4. \ --> escape sequence
5. "+" --> string concatenation
6. @ --> verbatim string literal
7. $ {} --> String internpolation expression is indicated by {}, prefixed by $.

### Chapter 2
1. Random dice = new Random(); --> reserves memory enough to store object based on 'random' class, creates object and stores its memory address, returns the memory address to variable dice i.e. connects them together
2. Random.Next()  --> Stateful --> Generates next random number  
3. Console.Clear() --> Clears screen
4. Math.Max() --> returns max value
5. message.Contains() --> checks the string "message" to contain another string ()
6. || = OR OPERATOR
7. && = AND OPERATOR
8. 

---
