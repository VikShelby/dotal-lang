# DOTAL Language

<p align="center">
  <img src="[LINK_TO_YOUR_ICON_IMAGE_URL_ON_GITHUB]" width="128" height="128" alt="DOTAL Logo">
</p>

<p align="center">
  <strong>A dynamic, object-oriented programming language with an Albanian-based syntax, built from scratch in C.</strong>
  <br>
  <br>
  <a href="https://github.com/[YOUR_USERNAME]/dotal-lang/releases"><strong>Download Installer</strong></a>
  ·
  <a href="https://github.com/[YOUR_USERNAME]/dotal-lang/issues">Report Bug</a>
  ·
  <a href="https://github.com/[YOUR_USERNAME]/dotal-lang/discussions">Request Feature</a>
</p>

---

## About DOTAL

**DOTAL** is a complete, multi-paradigm programming language created from the ground up as a journey through the art of language design. It features a clean, Albanian-based syntax designed to be intuitive and expressive.

The entire language is implemented in C99 with no external dependencies. It is not just an interpreter; it features a full **single-pass compiler** that generates a custom bytecode format, which is then executed on a fast, stack-based **Virtual Machine (VM)**.

This project was created by **[Your Name] ([@your-github-username]([Link to Your GitHub Profile]))**, inspired by the incredible book ["Crafting Interpreters"](https://craftinginterpreters.com/) by Bob Nystrom.

### Core Architecture

*   **Compiler:** A single-pass compiler that parses source text and emits a dense, linear bytecode representation.
*   **Virtual Machine:** A stack-based VM that interprets bytecode and manages a call stack for function execution.
*   **Memory Management:** An automatic Mark and Sweep Garbage Collector manages all heap-allocated objects (strings, lists, functions, classes, instances).
*   **Foreign Function Interface:** A simple FFI allows native C functions to be exposed to and called from DOTAL scripts.

---

## Language Features

DOTAL is a feature-complete language supporting a powerful blend of procedural and object-oriented programming.

*   **Syntax:** Albanian-based (`shpall`, `funksion`, `nese`, `per`, `tip`, `kthe`).
*   **Data Types:** Numbers, Booleans (`vertet`/`gabuar`), Strings.
*   **Data Structures:** Lists (Arrays) with index-based access (`lista[0]`).
*   **Control Flow:** `if/else`, `while`, and `for` loops.
*   **Functions:** First-class functions with lexical scoping (closures).
*   **Full OOP System:**
    *   **Classes** (`tip`) with methods.
    *   **Instances** with fields and method invocation (`obj.emer`, `obj.metoda()`).
    *   **`this`** keyword for instance context.
    *   **Inheritance** using the `<` operator.
*   **Standard Library:** Built-in native functions like `koha()` (time) and `lexo()` (user input).
*   **Built-in Methods:** Core types like Lists and Strings have methods (e.g., `lista.gjatesia()`).

---

## Getting Started

### 🚀 Using DOTAL (Recommended)

The easiest way to use DOTAL is to download the pre-compiled installer for Windows.

1.  Navigate to the **[Releases Page](https://github.com/[YOUR_USERNAME]/dotal-lang/releases)**.
2.  Download the `DOTAL_Setup.exe` from the latest release.
3.  Run the installer. It will add the `dotal` command to your system PATH and associate `.al` files.

You can then run any DOTAL script from your command line:
```bash
dotal path/to/your/script.al```

### 🛠️ Building from Source

For those who want to build the language themselves.

#### Prerequisites
*   A C99 compliant C compiler (GCC on Windows via MSYS2/MinGW is recommended).

#### Build Command
From the root of the repository, run the following command:
```bash
# For a release build with optimizations
gcc -Wall -O2 -o dotal src/*.c

# For a debug build with execution tracing
gcc -Wall -g -DDEBUG_PRINT_CODE -o dotal_debug src/*.c
```

---

## Example: The `kryeveper.al` script

This script showcases many of DOTAL's features, including functions, lists, loops, classes, and methods.

```albanian
# Gjuha DOTAL - Prova Finale

funksion fib(n) {
  nese (n < 2) { kthe n; }
  kthe fib(n - 1) + fib(n - 2);
}

shpall lista_e_numrave =;
per (shpall i = 0; i < lista_e_numrave.gjatesia(); i = i + 1) {
  printo fib(lista_e_numrave[i]);
}

tip Kafe {
  servir() {
    printo "Ju sherbyem nje kafe espres.";
  }
}

shpall porosia = Kafe();
porosia.servir();
```

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for full details.

Copyright (c. 2024 **[Your Name]**