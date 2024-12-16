---
title: TypeScript Tutorial
description: This is TypeScript tutorial and this is for learning TypeScript
slug: ts-programming-tutorial
date: 02/03/2025
author: Muhammad
image: /ts.png
---

Welcome to this comprehensive TypeScript tutorial! Whether you're a complete beginner or looking to deepen your understanding of TS, this guide will take you through the fundamentals and introduce advanced concepts as you progress.



## Introduction to TypeScript


TypeScript is a versatile and modern programming language that builds upon JavaScript by adding static typing. It is widely used for developing scalable web applications, server-side development, and large codebases. TypeScript enhances code reliability, maintainability, and tooling support while maintaining compatibility with JavaScript, making it a preferred choice in the software industry.

### Why Learn TypeScript?

- **Foundation for Other Languages**: TS provides the building blocks for many modern languages, such as JS, Java, and Python.
- **Performance**: TS is highly efficient and is used in performance-critical applications.
- **Low-level Control**: TS allows you to work closely with memory and hardware, providing more control over system resources.

## Setting Up TypeScript

To get started with TypeScript, you'll need to set up a development environment. Here are the steps:

1. **Install a C Compiler**: You can use GCC (GNU Compiler Collection) for Linux/macOS or MinGW for Windows. Both are free and widely used.
2. **Choose an IDE/Text Editor**: Popular options include Visual Studio Code, Code::Blocks, or Eclipse. Alternatively, you can use a simple text editor like Sublime Text.
3. **Verify Installation**: Once the compiler is installed, verify it by typing `gcc --version` in the terminal or command prompt.

## TypeScript Basics

Now that your environment is set up, let’s start with the basics. In this section, we'll cover:

- **Variables and Data Types**: Learn how to declare and use variables in TypeScript.
- **Control Structures**: Understand how to use conditional statements and loops.
- **Functions**: Learn how to write reusable code blocks.

### Variables and Data Types

```c showLineNumbers {1-3} /printf/
function main(): number {
    let age: number = 25;
    let height: number = 5.9;
    let initial: string = 'A';

    console.log(`Age: ${age}, Height: ${height.toFixed(1)}, Initial: ${initial}`);
    return 0;
}

main();
```

### Control Structures

```c
function main(): number {
    const age: number = 20;

    if (age >= 18) {
        console.log("You are an adult.");
    } else {
        console.log("You are a minor.");
    }

    for (let i: number = 0; i < 5; i++) {
        console.log(`Count: ${i}`);
    }

    return 0;
}

main();
```

### Functions

```c
function greet(name: string): void {
    console.log(`Hello, ${name}!`);
}

function main(): void {
    greet("Alice");
}

main();
```

## Intermediate TypeScript

Once you are familiar with the basics, it's time to explore more advanced features of C:

- **Arrays and Pointers**: Learn how to work with arrays and pointers, which are fundamental in TypeScript.
- **File I/O**: Understand how to read from and write to files.
- **Dynamic Memory Allocation**: Explore memory management using `malloc`, `calloc`, and `free`.

### Arrays and Pointers

```c
const numbers: number[] = [1, 2, 3, 4, 5];

for (let i = 0; i < numbers.length; i++) {
    console.log(`Number: ${numbers[i]}, Index: ${i}`);
}
```

### File I/O

```c
import * as fs from 'fs';

const main = (): number => {
    try {
        fs.writeFileSync('example.txt', 'Hello, File!\n');
        return 0;
    } catch (error) {
        console.error('Error opening file!');
        return 1;
    }
}

main();
```

### Dynamic Memory Allocation

```c
function main(): number {
    let arr: number[];
    const size: number = 5;

    arr = new Array(size);

    for (let i: number = 0; i < size; i++) {
        arr[i] = i + 1;
        console.log(`Value: ${arr[i]}`);
    }

    return 0;
}
```

## Advanced TypeScript

Now that you are comfortable with intermediate topics, let’s move on to some advanced TypeScript concepts:

- **Structures**: Learn how to group different data types together.
- **Pointers to Functions**: Explore how to use pointers with functions for flexibility.
- **Memory Management**: Delve deeper into memory management and optimization.

### Structures

```c
interface Student {
    name: string;
    age: number; 
    grade: number;
}

function main(): void {
    const s1: Student = {
        name: "Alice",
        age: 20,
        grade: 85.5
    };

    console.log(`Name: ${s1.name}, Age: ${s1.age}, Grade: ${s1.grade.toFixed(2)}`);
}

main();
```

### Pointers to Functions

```c
function add(a: number, b: number): void {
    console.log(`Sum: ${a + b}`);
}

const func_ptr: (a: number, b: number) => void = add;
func_ptr(10, 20);
```

### Memory Management

```c
function main(): number {
    let arr: number[];
    const size: number = 10;

    // Initialize array
    arr = new Array(size);

    if (!arr) {
        console.log("Memory not allocated.");
        return 1;
    }

    for (let i: number = 0; i < size; i++) {
        arr[i] = i * 2;
        console.log(`Value: ${arr[i]}`);
    }

    // TypeScript/JavaScript handles memory management automatically
    // No need for explicit free()

    return 0;
}
