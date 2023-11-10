# CSharp (Free Code Camp)
## https://www.freecodecamp.org/learn/foundational-c-sharp-with-microsoft/write-your-first-code-using-c-sharp/write-your-first-c-sharp-code

## Things To Remember
### Chapter 1 (7/7) Write Your First Code Using C#
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

### Chapter 2 Create and Run Simple C# Console Applications
1. Stateless vs Stateful (Console.Write is stateless, some methods are stateful and must have access to state of application (rely on values stored in memory by previous lines of codes)
2. A single class can support both stateful and stateless methods. However, when you need to call stateful methods, you must first create an instance of the class so that the method can access state.
3. Instance of a class = object
4. Overloaded methods --> Methods that can take multiple types of input parameters
5. Use docs.microsoft.com for information about overloaded methods

### Chapter 3 Add Logic to C# Console Applications
1. instantiating the array without initializing any values, you use the new operator (the new operator is used to create a new instance of a type).
2. signed and unsigned, signed means + and - both
3.  Reference types include arrays, classes, and strings. Reference types are treated differently from value types regarding the way values are stored when the application is executing.
4.  A value type variable stores its values directly in an area of storage called the stack. The stack is memory allocated to the code that is currently running on the CPU (also known as the stack frame, or activation frame). When the stack frame has finished executing, the values in the stack are removed.
5.  A reference type variable stores its values in a separate memory region called the heap. The heap is a memory area that is shared across many applications running on the operating system at the same time. The .NET Runtime communicates with the operating system to determine what memory addresses are available, and requests an address where it can store the value. The .NET Runtime stores the value, and then returns the memory address to the variable. When your code uses the variable, the .NET Runtime seamlessly looks up the address stored in the variable, and retrieves the value that's stored there.
6.  Value types can hold smaller values and are stored in the stack. Reference types can hold large values, and a new instance of a reference type is created using the new operator. Reference type variables hold a reference (the memory address) to the actual value stored in the heap.
7.  Reference types include arrays, strings, and classes.
8.  From the C# compiler's perspective, the safer operation would be to convert int into a string and perform concatenation instead.
9.  To perform data conversion, you can use one of several techniques:
  Use a helper method on the data type  
  Use a helper method on the variable    
  Use the Convert class' methods
10. The term widening conversion means that you're attempting to convert a value from a data type that could hold less information to a data type that can hold more information.
11. decimal myDecimal = myInt; (implicit conversion -- widening)
12. int myInt = (int)myDecimal; (explicit conversion -- casting) () is the casting operator, in this case, narrowing conversion
13. 
14. 





---

## Coding Style
### Chapter 1 Write Your First Code Using C#
1. Variables should use camel case i.e. thisIsCamelCase
2. Starting with underscore (_VariableName) is for a special purpose
3. Combine strings in the Console.Write() instead of making a new variable

### Chapter 2 Create and Run Simple C# Console Applications
1. red squiggly line appears --> compilation error
2. 'parameter' refers to the variable that's being used inside the method. An 'argument' is the value that's passed when the method is called.
3.  To examine the second overloaded version of the method, press ALT + Down Arrow on the keyboard.
4.  Code block is enclosed by {} i.e. brackets
5.  The { and } symbols create code blocks. Many C# constructs require code blocks. These symbols should be placed on a separate line so that their boundaries are clearly visible and readable.

### Chapter 3 Add Logic to C# Console Applications
1. Keep scope of variables as narrow as possible
2. casting truncates, converting rounds up
3. You can't cast a string into a decimal
4. Array.Clear() will remove an array element's reference to a value if one exists. To fix this, you might check for null before attempt to print the value.




---

### List of Commands / Methods
### Chapter 1 Write Your First Code Using C#
¬. dotnet new console -o ./CsharpProjects/TestProject  
1. Console.WriteLine()--> Prints a new line after output
2. Console.Write()--> Prints output
3. var--> sets datatype itself (var myName = "Abdul Moeez", var auto sets myName to be of type STRING), keeps things dynamic when we don't know what to use, the compiler selects the type  
4. \ --> escape sequence
5. "+" --> string concatenation
6. @ --> verbatim string literal
7. $ {} --> String internpolation expression is indicated by {}, prefixed by $.

### Chapter 2 Create and Run Simple C# Console Applications
1. Random dice = new Random(); --> reserves memory enough to store object based on 'random' class, creates object and stores its memory address, returns the memory address to variable dice i.e. connects them together
2. Random.Next()  --> Stateful --> Generates next random number  
3. Console.Clear() --> Clears screen
4. Math.Max() --> returns max value
5. message.Contains() --> checks the string "message" to contain another string ()
6. || = OR OPERATOR
7. && = AND OPERATOR
8. Array.Length --> returns length of array
9. foreach (string name in names) --> Loop
10. if (name.StartsWith("B")) --> .StartsWith usage
11. "/* --> */" adds comment block
12. string.ToUpper(), string.ToLower() --> string methods
13. string.Trim() --> Remove blank spaces... value.Trim().ToLower() == value2.Trim().ToLower()  
14.  string.Contains("search word")

### Chapter 3 Add Logic to C# Console Applications
1. switch() ... { case "string": { ... break;} case ... ... } default: (if no case matches) and case1:case2 for 2 cases corresponding to 1 flow
2. string[] product = sku.Split('-');  (string sku = "01-MN-L";)  
3. break --> breaks the entire loop, continue --> skips the iteration only
4. ?string --> nullable type string designation (used for Console.WriteLine type)
5. [,] --> 2D array declaration e.g. string[,] ourAnimals = new string[maxPets, 6];
6. 2. dotnet run... dotnet build  
7. DataType.MinValue, DataType.MaxValue --> Console.WriteLine($"float  : {float.MinValue} to {float.MaxValue} (with ~6-9 digits of precision)");
8. int[] data = new int[3]; --> array declaration
9. var.To.String() --> int to string
10. int.Parse(var) --> string to int
11. Convert.ToInt32(value1) --> string to int (rounds up the usual way)  (casting truncates, converting rounds up)  
12. TryParse() when possible instead of using Convert
14. using System.Globalization; (to use US culture settings for solving . and , problems)  
15. CultureInfo.CurrentCulture = new CultureInfo("en-US");. (to use US culture settings for solving . and , problems)
16. if (int.TryParse(value, out result)) --> returns true if converted with conversion in var result + The out keyword instructs the compiler that the TryParse() method won't return a value the traditional way only (as a return value), but also will communicate an output through this two-way parameter.
17. Array.Sort(Array_name); --> sorts and saves the main array
18. Array.Reverse(Array_name); --> reverses and saves the main array
19. Array.Clear(Array,Index,Length) --> clears an array element
20. 
21. 





---
