# Execution-context-in-detail-
In programming, an execution context refers to the environment in which a piece of code is executed. It consists of various components that determine how the code is executed and how it interacts with the surrounding environment. Understanding execution context is crucial for understanding how programs are executed and how variables, functions, and scopes are managed.

Execution contexts can be conceptualized as a data structure that holds all the necessary information for executing a piece of code. There are three types of execution contexts:

Global Execution Context:

The global execution context is created when the program starts running.
It represents the default context that contains the code that is not inside any function.
It defines global variables, functions, and objects that are accessible throughout the program.
There is only one global execution context per program.
Function Execution Context:

Whenever a function is invoked, a new function execution context is created.
It represents the context in which the function code is executed.
Each function invocation has its own separate execution context.
It includes information such as function arguments, local variables, and references to its outer environment (lexical scope).
Eval Execution Context:

The eval function in some programming languages creates a new execution context known as the eval execution context.
The eval execution context is used to evaluate code dynamically, usually in the form of a string.
It has its own lexical environment and can introduce new variables and functions.
Here is a diagram illustrating the relationship between these execution contexts:

sql

+-----------------------+
|                       |
|  Global Execution     |
|      Context          |
|                       |
|                       |
|  Variables            |
|  Functions            |
|  Objects              |
|                       |
+-----------------------+
           |
           |
           | Invokes a Function
           |
           V
+-----------------------+
|                       |
|  Function Execution   |
|      Context          |
|                       |
|                       |
|  Variables            |
|  Arguments            |
|  References           |
|  to Outer Scope       |
|                       |
+-----------------------+
           |
           |
           | Evaluates Code using "eval"
           |
           V
+-----------------------+
|                       |
|  Eval Execution       |
|      Context          |
|                       |
|                       |
|  Variables            |
|  Functions            |
|  Lexical Environment  |
|                       |
+-----------------------+


In the diagram, the global execution context is at the top, representing the default context for the entire program. When a function is invoked, a new function execution context is created, which has its own set of variables, arguments, and references to its outer environment. If the code includes an eval statement, it creates a separate eval execution context that evaluates the provided code string.

The execution context is crucial for managing variable scopes, accessing variables, handling function invocations, and maintaining the order of execution. It helps ensure that code is executed correctly and that variables and functions are properly scoped and accessible.
