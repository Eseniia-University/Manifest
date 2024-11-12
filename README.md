# CoreLang Manifest

Welcome to the **CoreLang** Manifest repository! This project, developed by Eseniia University, presents an ambitious new open-source low-level programming language designed for system programming tasks such as developing operating systems, bootloaders, drivers, and other essential components. CoreLang aims to offer developers complete control over hardware while maintaining a high level of security, readability, and portability.

## Project Overview

**CoreLang** is a language focused on:
- **Full Hardware Control:** Enabling direct access to system resources, including memory and registers, without unnecessary abstractions.
- **Enhanced Security:** Incorporating built-in mechanisms like bounds checking and error handling to reduce common vulnerabilities in low-level programming.
- **Cross-Platform Compatibility:** Supporting major architectures (x86, ARM, RISC-V) to ensure adaptability and extend system capabilities across platforms.

## Key Language Features

- **Strict Static Typing:** Reduces errors and improves efficiency.
- **Direct Memory and Register Access:** Grants developers low-level control for precise optimization.
- **Minimalistic Standard Library:** Essential functions for system-level programming, focusing on performance without unnecessary overhead.
- **Inline Assembly Support:** Allows embedding of assembly code within CoreLang to enhance critical performance sections.
- **Modular Design:** Supports a microkernel architecture, making CoreLang ideal for modular system development.

## Example Code

Here’s a brief example of CoreLang syntax for working with memory and registers:

```rust
// Simple function to write a byte to memory
fn write_byte(ptr: *mut u8, value: u8) {
    *ptr = value;
}

// Register manipulation
register eax: u32;

fn main() {
    eax = 0; // Reset the register
    write_byte(0xB8000 as *mut u8, 0x41); // Write to memory
}

Getting Started

Requirements

LLVM: For building and optimizing the CoreLang compiler.
TinyCC or Clang: Basis for the minimal compiler.
NASM and ld: For assembling and linking machine code.

Installation
Clone the Repository:

git clone https://github.com/Eseniia-University/Manifest.git
cd Manifest

Build CoreLang Compiler:
Use the provided Makefile to compile CoreLang code. Ensure LLVM, NASM, and other dependencies are installed.

Usage

To test basic CoreLang code, use:
make run

Project Roadmap

Research and Design
Define language objectives and specifications for low-level programming needs.

Compiler Development
Develop the CoreLang compiler (clc) to support essential low-level operations, optimize for performance, and cross-compile for multiple architectures.

IDE and Debugger
Create CoreIDE, an integrated environment with debugging, profiling, and performance analysis tools.

Community and Feedback
Release a beta version, gather community feedback, and iteratively improve the language based on user needs.

Stable Release and Expansion
Establish CoreLang as a stable, reliable language for critical low-level applications.

Contributing
We welcome contributions! Here’s how you can help:

Fork the Repository and create a new branch for your changes.
Add or Improve Features, focusing on enhancing language functionality, compiler optimizations, or documentation.
Submit a Pull Request with a clear description of your changes.
For more details, see our CONTRIBUTING.md file.

License
This project is licensed under the MIT License. See the LICENSE file for more details.

Contact
For any questions, discussions, or feedback, feel free to join our community or reach out to the maintainers through the issues tab.

Thank you for exploring CoreLang! We look forward to building an innovative, open, and accessible low-level programming language together.

---

This **README.md** provides a detailed introduction to the **CoreLang** Manifest project, covering its objectives, features, usage, roadmap, and contribution guidelines. Let me know if you need additional customization!
