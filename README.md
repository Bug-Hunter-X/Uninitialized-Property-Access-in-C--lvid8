# Uninitialized Property Access in C#

This repository demonstrates a common error in C#: accessing a property before it has been initialized. This can lead to unexpected behavior, such as printing a default value (0 for integers, null for objects) or, in some cases, runtime exceptions. 

## The Bug

The `bug.cs` file contains a simple class with a property `MyProperty`. The `MyMethod` function attempts to print the value of `MyProperty` without first assigning a value to it. This results in the program printing the default value of `MyProperty`, which is 0 for an integer.

## The Solution

The `bugSolution.cs` file demonstrates how to fix this issue by initializing `MyProperty` before accessing it.  This can be done in the constructor, or by assigning a value directly before use.

## How to Reproduce

1. Clone this repository.
2. Open `bug.cs` in a C# IDE.
3. Compile and run the code.  Observe the output (likely 0).
4. Open `bugSolution.cs`, compile and run. Observe the changed output.

## Lessons Learned

Always initialize class properties before use to avoid unpredictable behavior and ensure the robustness of your code.  Proper initialization prevents bugs and enhances code maintainability.