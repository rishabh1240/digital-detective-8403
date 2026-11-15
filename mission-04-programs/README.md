# Mission 04 — How Programs Run

## 1. Task / Objective

The objective of this mission is to understand how programs execute, run a simple Python program, and compare the working of compilers and interpreters.

In this mission, I learned how Python programs are executed and explored the differences between compilation and interpretation.

## 2. Work Completed

### Task 4.1 — Create and Run a Python Program

The task was to create a Python file named `hello.py`, write a simple program that displays a message, and execute it using Python 3 from the Terminal.

**File Name:** `hello.py`

**Python Program:**

```python
print("Hello from Python")
```

**Command Used:**

```bash
python3 hello.py
```

**Output:**

```text
Hello from Python
```

**Explanation:**

- `print()` is a built-in Python function used to display output.
- `"Hello from Python"` is a string containing the message to be displayed.
- `python3` runs the program using Python 3.
- `hello.py` is the Python source file containing the program.

### Task 4.2 — Compare Compiler and Interpreter

**Comparison Table**

| Point | Compiler | Interpreter |
|---|---|---|
| When translation / execution happens | Translates source code into another form before execution. | Executes program instructions at runtime. |
| Typical output | Produces compiled code, often machine code or an executable file. | Executes instructions and produces program results. |
| One example | C using the GCC compiler. | Python using the CPython interpreter. |
| One advantage | Compiled machine code generally executes faster. | Allows convenient execution and testing without a separate manual compilation step. |

**Difference Between Compiler and Interpreter**

A compiler translates source code into another form before the program is executed, whereas an interpreter executes instructions during runtime. Compilers often generate executable machine code that can run efficiently. Interpreters make it convenient to execute and test programs without a separate manual compilation step.

Some programming language implementations, such as CPython, combine both approaches by compiling source code into bytecode and then interpreting it.

## 3. Commands / Tools Used

| Command / Tool | Purpose |
|---|---|
| `python3 hello.py` | Executes the Python program using Python 3. |
| `print()` | Displays the message on the screen. |
| Python 3.14.7 | Used for writing and executing the Python program. |
| Antigravity IDE | Used to create and edit `hello.py`. |
| macOS Terminal (Zsh) | Used to run Python commands. |

## 4. My Understanding

Through this mission, I understood how a Python program is created and executed using the Python interpreter.

I learned that:

1. A Python program contains instructions written in the Python programming language.
2. The `print()` function displays output on the screen.
3. The Terminal can execute Python files using the `python3` command.
4. A compiler translates source code into another form before execution.
5. An interpreter executes program instructions at runtime.
6. Python's CPython implementation combines compilation into bytecode and interpretation.

I also understood that compilers and interpreters use different approaches to execute programs.

## 5. Difficulties Faced

No major difficulties were encountered while completing this mission.

The Python program executed successfully, and I was able to understand the comparison between compilers and interpreters.

## 6. How I Resolved Them

Not applicable, as no major difficulties were encountered during this mission.

## 7. Evidence / Files

The following files and outputs are included in this mission folder:

- `hello.py` — Python program that displays "Hello from Python".
- `README.md` — Documentation of Tasks 4.1 and 4.2.
- Terminal output confirming successful execution of the Python program.

## 8. Commit Details

**Suggested Commit Message:**

```bash
Compare compilers and interpreters
```

The mission files and documentation should be staged, committed, and pushed to GitHub separately.

## 9. Conclusion

Mission 4 helped me understand how programs run and how programming languages are translated or executed.

By creating a simple Python program and comparing compilers and interpreters, I gained a basic understanding of program execution and the role of Python in executing instructions.