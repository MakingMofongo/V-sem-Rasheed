A syntax tree, also known as a parse tree, is a hierarchical representation of the syntactic structure of a program or expression according to its grammar rules. It visually depicts how the input code is parsed and organized based on its grammar.

In a syntax tree:

- Nodes represent language constructs such as expressions, statements, or operators.
- Edges represent relationships between these constructs, typically indicating parent-child relationships.

For example, consider the expression "3 * (2 + 4)" represented as a syntax tree:

```
      *
     / \
    3   +
       / \
      2   4
```

Parameter passing refers to the mechanism by which arguments are passed to functions or procedures during invocation. There are several methods of parameter passing, including:

1. **Pass by Value**: Copies the value of the actual parameter into the formal parameter. Changes made to the formal parameter do not affect the actual parameter. Example:

```C
void square(int x) {
    x = x * x;  // Changes to x do not affect the original value outside the function
}
int main() {
    int num = 5;
    square(num); // num is passed by value
    // num is still 5 after the function call
    return 0;
}
```

2. **Pass by Reference**: Passes a reference (memory address) of the actual parameter to the formal parameter. Changes made to the formal parameter affect the actual parameter. Example:

```C++
void increment(int& x) {
    x++;  // Changes to x affect the original value outside the function
}
int main() {
    int num = 5;
    increment(num); // num is passed by reference
    // num is now 6 after the function call
    return 0;
}
```

3. **Pass by Pointer**: Passes the address of the actual parameter using pointers. Similar to pass by reference, changes made to the formal parameter affect the actual parameter. Example:

```C++
void decrement(int* x) {
    (*x)--;  // Changes to *x affect the original value outside the function
}
int main() {
    int num = 5;
    decrement(&num); // Address of num is passed
    // num is now 4 after the function call
    return 0;
}
```

Syntax trees are useful in understanding how parameters are passed and manipulated within a program, as they provide a visual representation of the program's structure and execution flow.