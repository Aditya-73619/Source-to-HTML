# 🎨 Source-to-HTML Converter in C

## 📌 Overview

This project implements a **C Source-to-HTML Converter** using the C programming language.

The program reads a C source file and converts it into an HTML file with syntax highlighting. It identifies different elements of C code, such as reserved keywords, numeric constants, strings, character constants, comments, and preprocessor directives, and applies corresponding CSS styles.

The generated HTML file allows C source code to be viewed in a web browser with color-coded syntax, making the code easier to read and understand.

---

## 🚀 Features

- **Syntax Highlighting** — Applies different colors to supported C language elements.
- **Keyword Recognition** — Identifies data-type keywords such as `int`, `char`, and `float`, along with control-flow keywords such as `if`, `else`, and `return`.
- **Numeric Constant Detection** — Recognizes numeric constants in the source code.
- **String and Character Recognition** — Identifies string literals and character constants.
- **Comment Detection** — Handles single-line and multi-line comments.
- **Header File Recognition** — Identifies header files used in `#include` directives.
- **Preprocessor Directive Handling** — Processes directives such as `#include` and `#define`.
- **HTML Generation** — Converts the input source code into an HTML document.
- **CSS Styling** — Uses an external stylesheet to apply syntax-highlighting colors.
- **State-Based Parsing** — Uses parser states and events to process source code character by character.

---

## 🛠️ Technologies Used

- C Programming
- HTML
- CSS
- File Handling in C
- Finite State Machine Concepts
- String Processing
- Structures and Enumerations
- Modular Programming
- Parser Design
- State and Event-Based Processing

---

## 📂 Project Structure

```text
Source-to-HTML/
├── s2html_main.c       # Main entry point
├── s2html_event.c      # Parser event and state handling
├── s2html_event.h      # Event-related declarations
├── s2html_conv.c       # HTML conversion and generation
├── s2html_conv.h       # Conversion-related declarations
├── styles.css          # Syntax-highlighting styles
├── test.c              # Sample C source file
├── test.c.html         # Generated HTML output
└── README.md           # Project documentation
```

---

## ⚙️ How to Run

### Prerequisites

- GCC compiler
- A Linux or macOS terminal
- A web browser to view the generated HTML file

### 1. Navigate to the Project Directory

```bash
cd Source-to-HTML
```

### 2. Compile the Program

Compile the source files according to their inclusion structure. If `s2html_main.c` already includes the implementation files, compile only the main file:

```bash
gcc s2html_main.c -o s2html
```

If the implementation files are compiled separately, remove their direct inclusion from the main file and compile the source files together instead.

### 3. Run the Program

Use the input C source file as required by your program's command-line interface. For example, if the program expects the filename as an argument:

```bash
./s2html test.c
```

### 4. View the Generated HTML

Open the generated HTML file in your browser:

```bash
open test.c.html
```

On Linux, you can use:

```bash
xdg-open test.c.html
```

The generated page displays your C source code with syntax highlighting according to the CSS styles.

---

## 🔄 How It Works

### Conversion Process

1. **Read the Source File** — The program reads the input C source file.
2. **Identify Characters and Tokens** — The parser examines the input character by character.
3. **Determine Parser States** — Parser states identify whether the program is processing a keyword, number, string, character constant, comment, header file, or preprocessor directive.
4. **Generate Parser Events** — Events represent the different source-code elements recognized by the parser.
5. **Apply HTML Formatting** — The converter wraps recognized elements in HTML markup with appropriate CSS classes.
6. **Generate the Output File** — The resulting HTML is written to an output file.
7. **Apply CSS Styling** — The browser uses `styles.css` to display the code in different colors.

---

## 🎨 Syntax Highlighting

The converter applies different CSS classes to recognized source-code elements.

| Element | Example |
|---|---|
| Data-type keywords | `int`, `char`, `float` |
| Control-flow keywords | `if`, `else`, `return`, `while` |
| Numeric constants | `10`, `3.14`, `100` |
| String literals | `"Hello World"` |
| Character constants | `'A'`, `'x'` |
| Single-line comments | `// comment` |
| Multi-line comments | `/* comment */` |
| Header files | `#include <stdio.h>` |
| Preprocessor directives | `#define SIZE 10` |

The exact highlighting depends on the elements recognized by the parser implementation.

---

## 🎯 Concepts Practiced

- File Handling in C
- Finite State Machine Design
- Parser States and Events
- Character-by-Character Processing
- String Manipulation
- Structures and Enumerations
- HTML Code Generation
- CSS-Based Syntax Highlighting
- Modular Programming
- Debugging and State Transitions

---


## 👨‍💻 Author

**Aditya Gupta**

This project helped me understand how source code can be processed using state-based parsing and transformed into a structured HTML document. It strengthened my knowledge of C programming, file handling, parser design, and the integration of C with HTML and CSS.
