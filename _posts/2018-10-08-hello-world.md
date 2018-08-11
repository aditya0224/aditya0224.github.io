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

## Preprocessing
Converting code from high level language to a pure high level language is done in the phase. <br />

Some of the actions to achieve this are <br />

* Concatenate code split in multiple lines
* Remove the comments
* Process escape sequences
* File Inclusion: Remove headers and include file and stitch the code.
  <br />
  Ex: <#include> will be removed from the file and code is added to the file.
* Macro Expansion: Textual transformation of the macros.
  <br />
  + \__FILE\__ replaces by filename as a string
  + \__LINE\__ replaces by current line number (as an integer)
 <br />

## Compiling:
<p>
Compilation is a multi step process starting with lexical analysis, dividing program into meaningful smallest indivisible instructions called tokens.
<br />
Ex: for instriction </br>
<pre>
float newValue = 10.5; 
</pre> 
following tokens are generated 
+ {float, keyword}
+ {newValue, identifier},
+ {=, operator} 
+ {10.5, constant}, {;, symbol}

If the token is not valid, it will generate compilation error. With these tokens, parse tree will be constructed. If the code does not confer to code grammar, error will be generated. After Parse tree construction, semantic analyzers perfom static analysis of code by checking type compatibility of tokens. 
</p>

<p>
In the next steps machine independent _intermediate code_ is generated. Intermediate code is the data structure used internally by a compiler to represent source code. Intermediate code is optimal to generate machine code in next phases.
</p>
<p>
In the compilation process data and tokens are stored in memory called symbol table. We access symbol table whenever a specific value is required in the complication process. 
</p>
<br/>
## Assembly process
<p>
Machine Code is specialized instructions specific to the machine architecture. Assemblers will transform the assembly code to machine code optimized to harwarde architecture.
There are two types of machine codes 
* Relocatable machine code
  + Relocatable Machine code is not dependent on the location of the memory where the program starts.
* Absolute Machine Code
  + Absolute Machine code is dependent on the memory location.
  </p>
<p>
Since assembler is dependent on the architecture of the processor, it varies from machine to machine.

Input: Assembly Level Language
Output: Machine Code [0/1]
</p>

## Linking
Each compiler returns a different object file for each code module. Linker will combine all the related modules to a another single file.

In the last phase, loaders based on type of machine code will place them in memory,create program and data stacks and initialize. 
Then Machine will run the instruction to "print Hello, World!".
