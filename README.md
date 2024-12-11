# if-and-switch-expressions
In Swift 6.0, if and switch expressions have been enhanced to work as expressions that return values. This allows for a more concise and functional style of programming. Here's how these work:

## If Expressions

The `if` statement can now return a value. You use it when there are conditions, and each branch (e.g., `if` and `else`) produces a value.

### Syntax:
```
let result = if condition {
    value1
} else {
    value2
}
```

### Example:
```
let isEven = true
let description = if isEven {
    "The number is even"
} else {
    "The number is odd"
}
print(description) // Output: "The number is even"
```

## Switch Expressions

Similarly, `switch` can now act as an expression that returns a value. Each `case` must produce a value, and you can also use a `default` case to handle any unmatched conditions.

### Syntax:
```
let result = switch value {
case pattern1:
    value1
case pattern2:
    value2
default:
    value3
}
```
### Example:
```
let number = 2
let description = switch number {
case 1:
    "One"
case 2:
    "Two"
case 3:
    "Three"
default:
    "Other"
}
print(description) // Output: "Two"
```

## Key Points:

- Value Requirements: Every branch in both if and switch must return a value of the same type.
- Type Inference: Swift infers the type of the expression based on the returned values.
- No Break Required: In switch expressions, there’s no need to explicitly write break to prevent fall-through.
- Versatile Use: They can be directly assigned to variables or used inline, e.g., in function calls or return statements.

## Use Case Comparison

Using expressions can simplify logic, reducing boilerplate code and improving readability.

### Traditional if-else:
```
let number = 10
let description: String
if number % 2 == 0 {
    description = "Even"
} else {
    description = "Odd"
}
```

### New if Expression:
```
let description = if number % 2 == 0 { "Even" } else { "Odd" }
```

## Example Combining if and switch Expressions:
```
let number = 15
let description = if number % 2 == 0 {
    "Even"
} else {
    switch number {
    case 1...10:
        "Odd and small"
    case 11...20:
        "Odd and medium"
    default:
        "Odd and large"
    }
}
print(description) // Output: "Odd and medium"
````
