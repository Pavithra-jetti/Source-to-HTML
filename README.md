# Source to HTML Converter in C

## Overview

This project is a **Source-to-HTML Converter developed in C**. It reads a C source file, parses it token by token (preprocessor directives, keywords, comments, strings, numeric constants, etc.), and generates a syntax-highlighted HTML file as output.

The project demonstrates the practical use of **file handling, event-driven parsing, structures, and enums** in C, modeling a simplified version of a syntax-highlighting engine.

## Features

* Converts any `.c` source file into a syntax-highlighted `.html` file
* Detects and highlights preprocessor directives (`#include`, etc.)
* Distinguishes user-defined header files from standard header files
* Highlights reserved keywords (data and non-data keywords separately)
* Detects and highlights numeric constants and strings
* Handles single-line and multi-line comments
* Supports custom output file naming via command-line argument
* Uses an event-based parser (`pevent_t`) to classify each token before conversion

## Technologies Used

* **Programming Language:** C
* **Compiler:** GCC
* **Platform:** Linux / Windows
* **Concepts:** Structures, Enums, File Handling, Event-Driven Parsing, Modular Programming
* **Libraries:** `stdio.h`

## Project Structure

```text
Source-to-HTML-Converter-in-C/
│
├── s2html_main.c
├── s2html_conv.c
├── s2html_conv.h
├── s2html_event.c
├── s2html_event.h
├── styles.css
├── test.c
├── README.md
└── .gitignore
```

### File Description

| File             | Description                                                               |
| ---------------- | ------------------------------------------------------------------------- |
| `s2html_main.c`  | Program entry point; opens source/destination files and drives conversion |
| `s2html_conv.c`  | Core conversion logic; writes HTML tags and formatted output              |
| `s2html_conv.h`  | Conversion function declarations and HTML tag constants                   |
| `s2html_event.c` | Parser logic; scans the source file and generates parser events (tokens)  |
| `s2html_event.h` | `pevent_t` structure and event-type enum definitions                      |
| `styles.css`     | Stylesheet used to color and format the generated HTML output             |
| `test.c`         | Sample C source file used as input to test the converter                  |
| `README.md`      | Project documentation                                                     |
| `.gitignore`     | Specifies generated files that should not be uploaded to GitHub           |

## How to Run

### 1. Clone the Repository

Open **Command Prompt / Terminal** and run:

```bash
git clone <your-github-repository-link>
```

### 2. Open the Project Directory

```bash
cd Source-to-HTML-Converter-in-C
```

### 3. Compile the Program

```bash
gcc s2html_main.c s2html_conv.c s2html_event.c -o a.out
```

### 4. Run the Program

```bash
./a.out test.c
```

This generates `test.c.html` in the same directory.

**To specify a custom output filename:**

```bash
./a.out test.c output
```

This generates `output.html`.

## Run

The converter takes a `.c` file as a command-line argument and produces an HTML file with syntax highlighting:

```text
./a.out <source_file.c> [output_name]
```

If no output name is given, the result is saved as `<source_file.c>.html`.

## Learning Outcomes

* Gained practical understanding of how syntax highlighters and parsers work
* Learned event-driven parsing design using structures and enums
* Practiced generating formatted HTML output programmatically from C
* Improved understanding of file I/O and token classification
* Learned to structure a multi-file C project with separate `.c` and `.h` modules
* Practiced modular programming and clean code organization
* Improved debugging and problem-solving skills

## Author

**Pavithra Jetti**
