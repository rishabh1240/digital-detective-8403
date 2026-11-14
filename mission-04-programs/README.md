# Mission 04 — How Programs Run

## Mission Objective

The objective of this mission is to understand how programs execute, run a simple Python program, and compare the working of compilers and interpreters.

In this mission, I learned how Python programs are executed and explored the differences between compilation and interpretation.

---

## Task 4.1 — Create and Run a Python Program

### Task Description

The task was to create a Python file named `hello.py`, write a simple program that displays a message, and execute it using Python 3 from the Terminal.

### Python Program

**File Name:** `hello.py`

```python
print("Hello from Python")
```

### Command Used

```bash
python3 hello.py
```

### Output

```text
Hello from Python
```

### Explanation

- `print()` is a built-in Python function used to display output.
- `"Hello from Python"` is a string containing the message to be displayed.
- `python3` runs the program using Python 3.
- `hello.py` is the Python source file containing the program.

### What I Learned

I learned how to create a Python file, write a simple program, and execute it using the Terminal. I also understood how the Python interpreter processes a program and displays its output.

---

## Task 4.2 — Compare Compiler and Interpreter

### Comparison Table

| Point | Compiler | Interpreter |
|---|---|---|
| When translation / execution happens | Translates source code into another form before execution. | Executes program instructions at runtime. |
| Typical output | Produces compiled code, often machine code or an executable file. | Executes instructions and produces program results. |
| One example | C using the GCC compiler | Python using the CPython interpreter |
| One advantage | Compiled machine code generally executes faster. | Allows convenient execution and testing without a separate manual compilation step. |

### Difference Between Compiler and Interpreter

A compiler translates source code into another form before the program is executed, whereas an interpreter executes instructions during runtime. Compilers often generate executable machine code that can run efficiently. Interpreters make it convenient to execute and test programs without a separate manual compilation step. Some programming language implementations, such as CPython, combine both approaches by compiling source code into bytecode and then interpreting it.

### What I Learned

I learned that compilers and interpreters are two approaches used to translate or execute programs. I also understood that Python uses an interpreter-based execution environment and that real language implementations can combine compilation and interpretation.

---

## Tools Used

| Tool | Purpose |
|---|---|
| Python 3.14.7 | Writing and executing the Python program |
| Antigravity IDE | Creating and editing `hello.py` |
| macOS Terminal (Zsh) | Running Python commands |

---

## Difficulties Faced

No major difficulties were encountered while completing this mission.

---

## Overall Learning Outcomes

After completing this mission, I learned:

1. How to create and execute a basic Python program.
2. How the `print()` function displays output.
3. How to run Python files using the Terminal.
4. The difference between compilers and interpreters.
5. How compilation and interpretation are used in program execution.

## Conclusion

Mission 4 helped me understand how programs run and how programming languages are translated or executed. By creating a simple Python program and comparing compilers and interpreters, I gained a basic understanding of program execution.