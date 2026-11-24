# Tier 3 — Simple Calculator

## 1. Introduction

A simple calculator receives two numbers, performs a mathematical operation and displays the result.

It follows the model:

**INPUT → PROCESSING → OUTPUT**

## 2. Input

The calculator receives:
- First number: 20
- Second number: 5
- Selected mathematical operation.

## 3. Processing and Output

| Operation | Processing | Output |
|---|---|---|
| Addition | 20 + 5 | 25 |
| Subtraction | 20 - 5 | 15 |
| Multiplication | 20 × 5 | 100 |
| Division | 20 ÷ 5 | 4 |

## 4. Division by Zero

If a user enters 0 as the second number during division, the calculator should:

- Check if the second number is zero.
- Display an error message: "Division by zero is not allowed."
- Allow the user to try again.

The calculator should not crash.

## 5. Invalid Input

If a user enters text instead of a number, the calculator should:

- Identify the invalid input.
- Display an error message: "Please enter a valid number."
- Request another input.

## 6. Conclusion

This exercise demonstrates how a program receives input, processes information and produces output.

It also shows why input validation and error handling are important in programming.