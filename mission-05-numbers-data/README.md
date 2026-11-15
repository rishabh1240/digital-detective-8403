# Mission 05 — Numbers and Data

## Mission Objective

The objective of this mission is to understand how computers represent information using binary and hexadecimal number systems, verify number conversions using Python, build a small number converter, and learn how text is stored using character-encoding standards.

In this mission, I performed manual number conversions, verified the results using Python, created a Python number converter, and explored ASCII and UTF-8 encoding.

---

## Task 5.1 — Convert Numbers by Hand

In this task, I manually converted decimal, binary, and hexadecimal numbers into different number systems and showed the steps involved.

### 1. Convert Decimal 13 to Binary

Decimal numbers are converted into binary using powers of 2.

| Power | 2³ | 2² | 2¹ | 2⁰ |
|---|---|---|---|---|
| Value | 8 | 4 | 2 | 1 |
| Binary digit | 1 | 1 | 0 | 1 |

Calculation:

8 + 4 + 1 = 13

**Answer:**

(13)₁₀ = (1101)₂

### 2. Convert Decimal 25 to Binary

| Power | 2⁴ | 2³ | 2² | 2¹ | 2⁰ |
|---|---|---|---|---|---|
| Value | 16 | 8 | 4 | 2 | 1 |
| Binary digit | 1 | 1 | 0 | 0 | 1 |

Calculation:

16 + 8 + 1 = 25

**Answer:**

(25)₁₀ = (11001)₂

### 3. Convert Binary 1010 to Decimal

Each binary digit is multiplied by its corresponding power of 2.

Calculation:

(1010)₂ = (1 × 2³) + (0 × 2²) + (1 × 2¹) + (0 × 2⁰)

= 8 + 0 + 2 + 0

= 10

**Answer:**

(1010)₂ = (10)₁₀

### 4. Convert Binary 1101 to Decimal

Calculation:

(1101)₂ = (1 × 2³) + (1 × 2²) + (0 × 2¹) + (1 × 2⁰)

= 8 + 4 + 0 + 1

= 13

**Answer:**

(1101)₂ = (13)₁₀

### 5. Convert Hexadecimal A to Decimal

In hexadecimal, A represents 10.

Calculation:

A × 16⁰ = 10 × 1 = 10

**Answer:**

(A)₁₆ = (10)₁₀

### 6. Convert Hexadecimal 1F to Decimal

In hexadecimal, F represents 15.

Calculation:

(1F)₁₆ = (1 × 16¹) + (15 × 16⁰)

= 16 + 15

= 31

**Answer:**

(1F)₁₆ = (31)₁₀

### 7. Convert Binary 1111 to Hexadecimal

Calculation:

(1111)₂ = 8 + 4 + 2 + 1

= 15

In hexadecimal, 15 is represented by F.

**Answer:**

(1111)₂ = (F)₁₆

### What I Learned

I learned how to convert numbers between decimal, binary, and hexadecimal systems using powers of their respective bases.

---

## Task 5.2 — Verify Using Python

In this task, I used Python's built-in conversion functions to verify my manual calculations.

### Python Expressions and Results

| Conversion | Python Expression | Result |
|---|---|---|
| Decimal 13 to binary | `bin(13)` | `0b1101` |
| Decimal 25 to binary | `bin(25)` | `0b11001` |
| Binary 1010 to decimal | `int("1010", 2)` | `10` |
| Binary 1101 to decimal | `int("1101", 2)` | `13` |
| Hexadecimal A to decimal | `int("A", 16)` | `10` |
| Hexadecimal 1F to decimal | `int("1F", 16)` | `31` |
| Binary 1111 to hexadecimal | `hex(int("1111", 2))` | `0xf` |

### Python Functions Used

- `bin()` converts an integer into its binary representation.
- `hex()` converts an integer into its hexadecimal representation.
- `int(value, base)` converts a number from the specified base into a decimal integer.

The prefix `0b` represents binary, while `0x` represents hexadecimal.

### Verification

All Python results matched my corrected manual calculations.

### What I Learned

I learned how to use Python's built-in conversion functions to verify number-system calculations and understand how different number systems represent the same value.

---

## Task 5.3 — Build a Small Number Converter

### Program Description

I created a Python program named `number_converter.py` inside the Mission 5 folder.

The program asks the user to enter a decimal number and converts it into binary and hexadecimal representations using Python's built-in functions.

### Python Code

```python
n = int(input())
b = bin(n).partition("b")
h = hex(n).partition("x")

print("Binary=", b[2])
print("Hexadecimal=", h[2])
```

### Explanation of the Code

1. `input()` accepts a number from the user.
2. `int()` converts the entered value into an integer.
3. `bin(n)` converts the decimal number into binary.
4. `hex(n)` converts the decimal number into hexadecimal.
5. `partition("b")` and `partition("x")` separate the prefixes from the converted values.
6. `print()` displays the binary and hexadecimal results.

### Test Results

I tested my program with five different positive decimal numbers.

| Test Number | Binary Output | Hexadecimal Output |
|---:|---|---|
| 23 | `10111` | `17` |
| 67 | `1000011` | `43` |
| 45 | `101101` | `2d` |
| 100 | `1100100` | `64` |
| 50 | `110010` | `32` |

All five test cases produced the expected results.

### What Do the Conversion Functions Do?

The `bin()` function converts a decimal integer into its binary representation using base 2.

The `hex()` function converts a decimal integer into its hexadecimal representation using base 16.

Both functions return strings containing the converted values.

### What I Learned

I learned how to take user input, convert it into an integer, use Python's built-in number conversion functions, and display the results. I also learned how to test a program using different input values.

---
## Task 5.4 — How Is Text Stored?

Computers store text using character-encoding standards. These standards represent characters using numerical values that computers can store and process.

### 1. ASCII Decimal Codes Using Python

I used Python's built-in `ord()` function to find the ASCII decimal codes of uppercase A and lowercase a.

**Python commands:**

```python
ord("A")
ord("a")
```

**Output:**

```text
65
97
```

| Character | Python Expression | ASCII Decimal Code |
|---|---|---:|
| Uppercase A | `ord("A")` | 65 |
| Lowercase a | `ord("a")` | 97 |

The `ord()` function returns the Unicode code point of a character. For these two characters, the values are also their ASCII decimal codes.

### 2. Why Does a Computer Need an Encoding Standard to Store Text?

A computer needs an encoding standard to convert characters into numerical values that it can store and process. Encoding standards ensure that different computers and applications can correctly understand and display the same text.

### 3. Example of a Character Not Part of Basic ASCII

The Indian Rupee symbol (₹) is an example of a character that is not included in basic ASCII.

It can be represented using UTF-8 encoding, which supports a much wider range of characters, symbols, and languages.

### What I Learned

I learned that computers store text using character-encoding standards. ASCII represents a basic set of characters, while UTF-8 supports a much wider range of characters and symbols. I also learned how to use Python's `ord()` function to find the numerical code of a character.

## Tools Used

| Tool | Purpose |
|---|---|
| Python 3.14.7 | Verifying number conversions and running the number converter |
| VS Code | Writing and editing Python programs |
| macOS Terminal (Zsh) | Executing Python programs |
| Python built-in functions | Performing binary and hexadecimal conversions |

---

## Difficulties Faced and Solutions

**Difficulty 1: Understanding Binary to Decimal Conversion**

While performing manual calculations, I initially made an arithmetic mistake while converting binary 1010 into decimal.

**Solution:** I checked the place values of each binary digit using powers of 2 and corrected the answer to 10.

**Difficulty 2: Understanding Conversion Outputs**

Python's `bin()` and `hex()` functions include prefixes in their output.

**Solution:** I used the `partition()` method to separate the prefixes and display only the converted values in my number converter.

---

## Overall Learning Outcomes

After completing Mission 5, I learned:

1. How to convert numbers between decimal, binary, and hexadecimal systems.
2. How to verify manual calculations using Python.
3. How to use Python's built-in `bin()`, `hex()`, and `int()` functions.
4. How to build a simple number converter using Python.
5. How computers represent text using ASCII and UTF-8 encoding.
6. Why character-encoding standards are important for storing and displaying text.

## Conclusion

Mission 5 helped me understand how computers represent numerical and textual information. Through manual calculations, Python verification, and building a number converter, I gained practical knowledge of binary, decimal, hexadecimal, and character-encoding systems.