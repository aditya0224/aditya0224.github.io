---
layout: post
title:  "Hello, World!"
author: "Adi Bhamidipati"
---

Most popular first tutorial we have for any programming language is printing “Hello, World!” on the screen. Based on the language it might be one of these or similar

- printf("Hello, World!"); in C
- echo "Hello, World!"; in PHP
- print 'Hello, world!' in Python(2.7)
- System.out.println("Hello, World!"); in Java

How does computer understand it? Machine understands only two characters, 1 and 0 and we named that as binary characters. So there is something in between that translates our command “print Hello, World! on the screen” into binary language. Instructions will be processed in different phases.

The use different modules to convert high-level programming instructions to machine understandable binary instructions.

The complete Process can be divided into four phases:

## Preprocessor
Converting code from high level language to a pure high level language is done in the phase. <br />

Some of the actions to achieve this are <br />

* Concatenate code split in multiple lines
* Remove the comments
* Process escape sequences,
* File Inclusion: Remove headers and include file and stich the code into this file.
  <br />
  Ex: <#include> will be removed from the file and code is added to the file.
* Macro Expansion: Textual transformation of the macros.
  <br />
  + \__FILE\__" replaces by filename as a string
  + \__LINE\__ replaces by current line number (as an integer)
 <br />

## Compiling Process:
The process starts with cleaning of code by removing white spaces and comments and divide our program into meaningful smallest indivisible instructions called tokens. This phase is also called lexical analysis.

Ex: float newValue = 10.5; following tokens are generated {float, keyword}, {newValue, identifier}, {=, operator} , {10.5, constant}, {;, symbol}

If the token is not valid, it will generate error. With the token from the Scanning step, a parse tree will be constructed. If the code does not confer to code grammar, error will be generated. After Parsing, Semantic analyzers check if the types are compatible. This is the phase of static analysis of code. In the next Steps Intermediate Code is Generated which is machine Independent. Some optimization like, Shortcircuit operations will be performed. Intermediate code will be optimal to generate the machine level code to the target machine. Then Machine Code, specialized instructions specific to the machine architecture is generated and optimized to Specific hardware.

In the compilation process data and tokens are stored in memory called symbol table. We access symbol table whenever a specific value is required in the complication process. 

In Interpreters, we does it few of these steps for each instruction or line of code instead of the whole code. We do scanning, parsing and generating and optimizing machine level instruction and executing it. We skip the steps of generating and optimizing intermediate code.

## Assembler
In this phase the assembly language is converted into machine code. 
There are two types of machine codes Relocatable machine code and Absolute Machine Code
Relocatable Machine code is not dependent on the location of the memory where the program starts. Where as Absolute Machine code is dependent on the memory location.
This module is dependent on the architecture of the processor. So, the assembler varies from machine to machine.

Input: Assembly Level Language
Output: Machine Code [0/1]

## Loader and Linker
Each compiler returns a different object file for each code module. Linker will combine all the related modules to a another single file.The loaders based on type of machine code will load it in the programs address space. All the program and data stack are created loaded and gets initialized. 

After all this phases, machine will get the instruction to print the instruction on the screen and prints it.
