# Nightmare Wiki

Welcome to the Nightmare project wiki! Nightmare is a project developed by Eseniia University with the objective of creating an open and low-level programming language for use in cybersecurity, ethical hacking, and network defense. This wiki provides detailed guidance on the design goals, language features, compiler setup, and core components.

## Table of Contents
1. [Home](#home)
2. [Objectives and Language Design](#objectives-and-language-design)
3. [Language Features](#language-features)
4. [Compiler Core and Infrastructure](#compiler-core-and-infrastructure)
5. [Low-Level Construct Language](#low-level-construct-language)
6. [Example Code and Minimal Language Syntax](#example-code-and-minimal-language-syntax)
7. [Getting Started Tools](#getting-started-tools)
8. [Development Stages](#development-stages)
9. [Manifesto and Philosophy](#manifesto-and-philosophy)
10. [License](#license)

---

### Home

**Overview:**
Nightmare is a cybersecurity-focused project that introduces a low-level programming language aimed at providing developers with precise control over hardware, memory, and system resources. The language is designed for performance-critical tasks and is intended for applications such as operating system kernels, bootloaders, and drivers.

**Disclaimer:**
Nightmare is an educational project designed for use in controlled environments. Use responsibly and only on authorized or isolated systems.

---

### Objectives and Language Design

**Primary Objectives:**
- **Speed ​​and Control:** Offer predictable execution with low-level access, allowing developers to manage memory directly and work with hardware resources.
- **Minimal Runtime:** A minimal set of libraries ensures flexibility for developing microcodes and drivers without unnecessary overhead.

---

###Language Features

1. **Strict Static Typing:** Enforces strict type-checking to improve performance and minimize errors.
2. **Direct Memory Management:** Provides pointer support, manual memory management, and memory interaction functions.
3. **Machine Code Compilation:** The compiler is optimized to produce fast and compact machine code.
4. **Inline Assembly Support:** Built-in assembler instructions for critical optimization in performance-sensitive areas.
5. **Macro System:** Simplifies repetitive low-level operations for more efficient programming.

---

### Compiler Core and Infrastructure

1. **Compiler and Assembler:** Translates source code into assembly and then into machine code.
2. **Linker:** Handles memory allocation, static libraries, and initialization, critical for precise memory layout.
3. **Debugger:** Integrated debugging capabilities for error analysis.

---

### Low-Level Construct Language

1. **Pointer Arithmetic:** Supports direct manipulation of pointers for addressing specific memory locations.
2. **Register Access:** Offers support for direct manipulation of processor registers.
3. **Inline Intrinsic Instructions:** Enables embedding assembler instructions within the code.

---

### Example Code and Minimal Language Syntax

Here is a sample of what the syntax might look like:

```c
// Simple syntax for working with memory
fn write_byte(ptr: *mut u8, value: u8) {
 *ptr = value;
}

// Working with processor registers
register eax: u32;

fn main() {
 eax = 0; // zeroing the register
 write_byte(0xB8000 as *mut u8, 0x41); // writing to memory
}
Getting Started Tools
LLVM: A robust framework for building compilers.
TinyCC or Clang: Provides a minimal compiler foundation.
Debugger: An integrated debugging tool for error tracking and analysis.
Development Stages
Stage 1: Language Planning and Design

Define primary objectives, targeted uses, and design specifications.
Stage 2: Compiler Creation

Create a minimal compiler with basic syntax parsing, using LLVM or other frameworks.
Stage 3: Library Development for Low-Level Operations

Implement basic memory, I/O, and processor register functions.
Stage 4: Debugging and Testing

Integrate debugging and testing tools, with automated tests for memory and functionality.
Manifesto and Philosophy
Nightmare's design philosophy centers on openness, flexibility, and direct hardware access. This low-level language aims to bridge the gap between ease of use and absolute control over system resources, providing:

Openness and Freedom: All components are open source.
Simplicity and Transparency: Intuitive syntax with clear constructs for hardware interaction.
Backward Compatibility: Designed for compatibility with C/C++ for legacy system integration.
License
This project is licensed under the MIT License. See the LICENSE file for more details.

Thank you for exploring the Nightmare project! This wiki provides a guide to the project's setup, language features, and usage. Feel free to contribute, following the project's open-source philosophy.

yaml
Copy code

---

This markdown file provides a structured, concise wiki for the **Nightmare** project. 

