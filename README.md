# CompilerD

CompilerD is a custom compiler/interpreter project implemented in Python. It defines and executes a simple programming language with its own lexer, parser, interpreter, grammar, runtime values, functions, control structures, and error handling.

The project demonstrates the fundamental stages involved in designing a programming language:

**Source Code → Lexer → Tokens → Parser → AST → Interpreter → Output**

## Features

- Custom programming language syntax
- Lexical analysis and tokenization
- Recursive-descent style parsing
- Abstract Syntax Tree generation
- Runtime interpreter
- Variables and expressions
- Integer and floating-point numbers
- Strings
- Lists
- Arithmetic operations
- Comparison operators
- Logical operators
- `IF`, `ELIF`, and `ELSE`
- `FOR` loops
- `WHILE` loops
- Functions and parameters
- `RETURN`, `BREAK`, and `CONTINUE`
- Built-in functions
- Runtime error reporting
- Syntax error reporting
- File execution using the `RUN()` function

## Language Keywords

The language supports keywords such as:

```text
VAR
AND
OR
NOT
IF
ELIF
ELSE
FOR
TO
STEP
WHILE
FUN
THEN
END
RETURN
CONTINUE
BREAK
```

## Built-in Functions

Some of the available built-in functions include:

```text
PRINT()
PRINT_RET()
INPUT()
INPUT_INT()
CLEAR()
CLS()
IS_NUM()
IS_STR()
IS_LIST()
IS_FUN()
APPEND()
POP()
EXTEND()
LEN()
RUN()
```

## Project Structure

```text
CompilerD/
│
├── cd project/
│   ├── basic.py
│   ├── shell.py
│   ├── strings_with_arrows.py
│   ├── grammar.txt
│   ├── example.myopl
│   └── qwerty.myopl
│
└── README.md
```

### File Description

**`basic.py`**  
Core implementation containing the lexer, parser, AST nodes, runtime values, interpreter, functions, symbol tables, and error handling.

**`shell.py`**  
Interactive command-line shell for executing language statements.

**`strings_with_arrows.py`**  
Utility used for displaying source-code locations when reporting errors.

**`grammar.txt`**  
Grammar definition for the custom language.

**`example.myopl`**  
Example program demonstrating functions, loops, lists, string operations, and built-in functions.

**`qwerty.myopl`**  
Simple example program demonstrating variables and output.

## Requirements

- Python 3.x
- No external Python packages are required.

## Running the Interactive Shell

Open a terminal inside the `cd project` directory:

```bash
python shell.py
```

You will see:

```text
basic >
```

You can then enter language statements, for example:

```text
PRINT("Hello World!")
```

Another example:

```text
VAR x = 10
PRINT(x)
```

## Running a Program File

Program files use the `.myopl` extension.

Example:

```text
RUN("example.myopl")
```

You can execute this from the interpreter shell.

## Example Program

```text
FUN oopify(prefix) -> prefix + "oop"

FUN join(elements, separator)
    VAR result = ""
    VAR len = LEN(elements)

    FOR i = 0 TO len THEN
        VAR result = result + elements/i
        IF i != len - 1 THEN VAR result = result + separator
    END

    RETURN result
END

PRINT("Greetings universe!")

FOR i = 0 TO 5 THEN
    PRINT(join(["l", "sp"], ", "))
END
```

## Error Handling

CompilerD includes custom error handling for:

- Illegal characters
- Invalid syntax
- Expected characters
- Runtime errors
- Function call errors
- Invalid operations

Errors include source-file and line information to make debugging easier.

## Technologies Used

- Python
- Lexical Analysis
- Parsing
- Abstract Syntax Trees
- Interpreters
- Programming Language Design
- Runtime Environments
- Error Handling

## Project Objective

The primary objective of this project is to understand how programming languages are designed and executed by implementing the major components of a compiler/interpreter pipeline from scratch.

## Contributors

- **Souvik Dey**
- **Taha Baba**
- **Sargun Singh Sandhu**

## Academic Project

This project was developed as part of an academic Compiler Design project.
