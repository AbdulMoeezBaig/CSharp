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


### Chapter 5  Create Methods in C# Console Applications
1. Normally, string is reference typed, so once its changed at address, all instances of it should be changed HOWEVER string is special, when u change a string, a new string is created and therefore, outside the scope the original string appears (which would not happen for a normal reference type).. the string inside the method scope is lost  therefore use string as global and don't pass it via method  
2. Explanation: method signature by e.g. void SetHealth(string health) wont get updated above... the keyword "string" must be removed here, they can't be altered once assigned and can only be written by a new value
3. 
4. 


### Chapter 6  Debug C# Console Applications
1.  Functional testing - Unit testing - Integration testing - System testing - Acceptance testing
2.  Nonfunctional testing - Security testing - Performance testing - Usability testing - Compatibility testing
3.  errors that occur during the application runtime are referred to as exceptions.. these exceptions should be managed in code
4.  Exception handling is the process of managing errors that occur during runtime, and developers are responsible for handling exceptions by using "try" and "catch" statements in their code.
5.  Code debugging is a process that developers use to isolate an issue and identify one or more ways to fix it
6.  Software devs and tests both respondible for testing
7.  if exception isn't managed, application closes with error
8.  In C#, errors in the program at runtime are propagated through the program by using a mechanism called exceptions. Exceptions are thrown by code that encounters an error and caught by code that can correct the error. Exceptions can be thrown by the .NET runtime or by code in a program. Exceptions are represented by classes derived from Exception. Each class identifies the type of exception and contains properties that have details about the exception.
9.  The terms "throw" and "catch" can be explained by evaluating the definition of an exception.
The second sentence of the definition says "Exceptions are thrown by code that encounters an error and caught by code that can correct the error". The first part of this sentence tells you that exceptions are created by the .NET runtime when an error occurs in your code. The second part of the sentence tells you that you can write code to catch an exception that's been thrown. In addition, the code that catches the exception can be used to complete a corrective action, hopefully mitigating the situation caused by the code that resulted in the error. In other words, you can write code that protects your application when an error occurs.
11. The type of exception determines the information it contains
12. An exception is created and thrown by the .NET runtime.
13. exceptions can be accessed and used to take corrective action at runtime
14. A debugger is a software tool used to observe and control the execution flow of your program with an analytical approach. Debuggers help you isolate the cause of a bug and help you resolve it. A debugger connects to your code using one of two approaches: By hosting your program in its own execution process..By running as a separate process that's attached to your running program.

15. Run and Debug controls panel. Used to configure and start a debug session.
16. VARIABLES section. Used to view and manage variable state during a debug session.
17. WATCH section. Used to monitor variables or expressions. For example, you could configure an expression using one or more variables and watch it to see when a particular condition is met.
18. CALL STACK section. Used to keep track of the current point of execution within the running application, starting with the initial point of entry into the application. The call stack shows which method is currently being executed, as well as the method or methods in the execution path that led to the current point of execution (current line of code).
19. BREAKPOINTS section. Displays the current breakpoint settings.
20. Debug toolbar. Used to control code execution during the debug process. This toolbar is only displayed while the application is running.
21. Current execution step. Used to identify the current execution step by highlighting it in the Editor. In this case, the current execution step is a breakpoint (breakpoints are marked with a red dot to the left of the line number).
22. DEBUG CONSOLE. Used to display messages from the debugger. The DEBUG CONSOLE panel is the default console for console applications and is able to display output from Console.WriteLine() and related Console output methods.
23. two simple scenarios when updating the launch configuration file is required: Your C# console application reads input from the console. Your project workspace includes more than one application.
24. Common scenarios that require exception handling include:  
User input: Exceptions can occur when code processes user input. For example, exceptions occur when the input value is in the wrong format or out of range.  
Data processing and computations: Exceptions can occur when code performs data calculations or conversions. For example, exceptions occur when code attempts to divide by zero, cast to an unsupported type, or assign a value that's out of range.  
File input/output operations: Exceptions can occur when code reads from or writes to a file. For example, exceptions occur when the file doesn't exist, the program doesn't have permission to access the file, or the file is in use by another process.  
Database operations: Exceptions can occur when code interacts with a database. For example, exceptions occur when the database connection is lost, a syntax error occurs in a SQL statement, or a constraint violation occurs.  
Network communication: Exceptions can occur when code communicates over a network. For example, exceptions occur when the network connection is lost, a timeout occurs, or the remote server returns an error.  
Other external resources: Exceptions can occur when code communicates with other external resources. Web Services, REST APIs, or third-party libraries, can throw exceptions for various reasons. For example, exceptions occur due to network connections issues, malformed data, etc.
25. The try code block contains the guarded code that may cause an exception. If the code within a try block causes an exception, the exception is handled by a corresponding catch block.
26. The catch code block contains the code that's executed when an exception is caught. The catch block can handle the exception, log it, or ignore it. A catch block can be configured to execute when any exception type occurs, or only when a specific type of exception occurs.
27. The finally code block contains code that executes whether an exception occurs or not. The finally block is often used to clean up any resources that are allocated in a try block. For example, ensuring that a variable has the correct or required value assigned to it.
28. A runtime instance of a class is generally referred to as an object, so exceptions are often referred to as exception objects.
29. Although they are sometimes used interchangeably, a class and an object are different things. A class defines a type of object, but it's not an object itself. An object is a concrete entity based on a class.
30. When an exception occurs, the .NET runtime searches for the nearest catch clause that can handle the exception. The process begins with the method that caused the exception to be thrown. First, the method is examined to see whether the code that caused the exception is inside a try code block. If the code is inside try code block, the catch clauses associated with the try statement are considered in order. If the catch clauses are unable to handle the exception, the method that called the current method is searched. This method is examined to determine whether the method call (to the first method) is inside a try code block. If the call is inside a try code block, the associated catch clauses are considered. This search process continues until a catch clause is found that can handle the current exception.
31. Once a catch clause is found that can handle the exception, the runtime prepares to transfer control to the first statement of the catch block. However, before execution of the catch block begins, the runtime executes any finally blocks associated with try statements found during the search. If more than one finally block is found, they are executed in order, starting with the one closest to the code that caused the exception to be thrown. If no catch clause is found to handle the exception, the runtime terminates the application and displays an error message to the user.
32. 

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
5. Composite formatting uses numbered placeholders within a string. At run time, everything inside the braces is resolved to a value that is also passed in based on their position.
6. String interpolation --> variables, composite formatting --> numbers like {0} replacing strings, can put multiple {0} ...  
7. Notice how adding the :C to the tokens inside of the curly braces formats the number as currency regardless of whether you use int or decimal.
8. The N numeric format specifier makes numbers more readable. Update your code as follows:
9. :N by default = 2 digits after decimal, :N4 = 4 digits after decimal
10. :P2 for percentages with 2 decimal
11. String Methods: PadLeft(), PadRight(), Trim(), TrimStart(), TrimEnd(), GetHashCode(), Length, Contains(), StartsWith(), EndsWith(), Substring(), Remove(). IndexOf()  
12. input.PadLeft(12, '-') --> overload method
13. message = String.Format("{0:P}", currentReturn).PadRight(10);  
14. message.IndexOf(')'); (finding the paranthesis in this case) (returns -1 if cannot find a match)  
15. const string var1 --> value can never be changed  
16. IndexOfAny() --> first location of string + searches from an array (of symbols) , LastIndexOf() --> last location of string 
17. IndexOfAny(symbols array) + with overload IndexOfAny(symbols, start position)
18. Remove(), Replace()
19. string.Trim() --> removes leading white spaces
20. 
21. 


### Chapter 5  Create Methods in C# Console Applications
1. Notice that it isn't necessary to have the method defined before you call it. This flexibility allows you to organize your code as you see fit. It's common to define all methods at the end of a program.
2. Method signature = something u write method code in
3. Value types such as int, bool, float, double, and char directly contain values. Reference types such as string, array, and objects (such as instances of Random) don't store their values directly. Instead, reference types store an address where their value is being stored.
4. It is important to remember that string is a reference type, but it is immutable. That means once it has been assigned a value, it can't be altered. In C#, when methods and operators are used to modify a string, the result that is returned is actually a new string object.
5. Passing to function with name of attribute: RSVP(name: "Linh", allergies: "none", partySize: 2, inviteOnly: false); --> void RSVP(string name, int partySize, string allergies, bool inviteOnly)
6. A parameter becomes optional when it's assigned a default value. If an optional parameter is omitted from the arguments, the default value is used when the method executes
7.  Example of optional parameters: Default value: void RSVP(string name, int partySize = 1, string allergies = "none", bool inviteOnly = true)
8.  Optional parameters must appear after all required parameters
9.  

### Chapter 6  Debug C# Console Applications
The .NET runtime throws exceptions when basic operations fail. Here's a short list of runtime exceptions and their error conditions:

1. ArrayTypeMismatchException: Thrown when an array can't store a given element because the actual type of the element is incompatible with the actual type of the array.
2. DivideByZeroException: Thrown when an attempt is made to divide an integral value by zero.
3. FormatException: Thrown when the format of an argument is invalid.
4. IndexOutOfRangeException: Thrown when an attempt is made to index an array when the index is less than zero or outside the bounds of the array.
5. InvalidCastException: Thrown when an explicit conversion from a base type to an interface or to a derived type fails at runtime.
6. NullReferenceException: Thrown when an attempt is made to reference an object whose value is null.
7. OverflowException: Thrown when an arithmetic operation in a checked context overflows.







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
20. Array.Resize(ref oldArrayName, newSize); --> resize array
21. char[] charVar = value.ToCharArray(); --> string to char conversion
22. string result = String.Join(",", valueArray); --> to separate characters via , in a char array
23. string[] items = result.Split(',');
24. *NOTE* Array.Sort / Join etc will only work if string has been converted to a system array using string.split(" ").. something
25. string result = string.Format("{0} {1}!", first, second); composite formatting
26. Add :c at end of number to make it like currency
27. 
28. 

### Chapter 5  Create Methods in C# Console Applications
1.  string[] address = ipv4Input.Split(".", StringSplitOptions.RemoveEmptyEntries);
2.  Clear(array) --> makes all values 0 in array *Array is reference type so changing values at address will change values inside and outside "brackets defined scope"
3.  if(originalStr.Equals(searchStr)) --> compares original string with search string
4.  string[,] AssignGroup(int groups)  --> return 2D array
5.  Thread.Sleep(1000) --> Delay
6.  
7.  

### Chapter 6  Debug C# Console Applications
1. make a new project folder
2. open folder in terminal and write cli command: dotnet new console
3. project files are created, now can do, dotnet run
4. view --> command pallete --> type: .net: g  --> new folder .vscode is created (used to configure debug environment)
5. A 'hit count' breakpoint can be used to specify the number of times that a breakpoint must be encountered before it will 'break' execution. You can specify a hit count value when creating a new breakpoint (with the Add Conditional Breakpoint action) or when modifying an existing one (with the Edit Condition action). In both cases, an inline text box with a dropdown menu opens where you can enter the hit count value.
6. A 'Logpoint' is a variant of a breakpoint that does not "break" into the debugger but instead logs a message to the console. Logpoints are especially useful for injecting logging while debugging production environments that cannot be paused or stopped. A Logpoint is represented by a "diamond" shaped icon rather than a filled circle. Log messages are plain text but can include expressions to be evaluated within curly braces ('{}').
7. When inside a method, the Step Out button completes the remaining lines of the current method and then returns to the execution context that invoked the method.
8. 
9. 




---
