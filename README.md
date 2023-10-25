# CSharp (Free Code Camp)
## https://www.freecodecamp.org/learn/foundational-c-sharp-with-microsoft/write-your-first-code-using-c-sharp/write-your-first-c-sharp-code

### Things To Remember
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
12. 
13. 

### Coding Style
1. Variables should use camel case i.e. thisIsCamelCase
2. Starting with underscore (_VariableName) is for a special purpose
3. Combine strings in the Console.Write() instead of making a new variable
4. 


### List of Commands / Methods
1. Console.WriteLine()--> Prints a new line after output
2. Console.Write()--> Prints output
3. var--> sets datatype itself (var myName = "Abdul Moeez", var auto sets myName to be of type STRING), keeps things dynamic when we don't know what to use, the compiler selects the type  
4. \ --> escape sequence
5. + --> string concatenation
6. @ --> verbatim string literal
7. $ {} --> String internpolation expression is indicated by {}, prefixed by $. 
