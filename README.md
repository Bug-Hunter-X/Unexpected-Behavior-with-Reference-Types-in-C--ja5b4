# Unexpected Behavior with Reference Types in C#

This example highlights a potential issue when working with reference types in C#.  Changes made to one variable can unexpectedly affect another if they both point to the same object in memory.

## Bug Description
The code creates two variables, `obj1` and `obj2`, both referencing the same `MyClass` instance. Modifying a property of `obj2` also modifies the same property in `obj1` because they share the same memory location.

## Solution
The solution involves creating a copy of the object to prevent unintended side effects.  This can be achieved using techniques like cloning or creating a new object with the values copied from the original.