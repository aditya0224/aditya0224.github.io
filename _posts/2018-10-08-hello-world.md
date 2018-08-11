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

How does computer understand it? Machine understands only two characters, 1 and 0 namely binary characters. So there is something in between that translates our command “print Hello, World! on the screen” into binary language. 

Instructions will be processed in different phases. Different modules are used to convert high-level programming instructions to machine understandable binary code.The process can be divided into four phases:

## Preprocessing
Converting code from high level language to a pure high level language is done in this phase. <br />

Some of the actions to achieve this are, <br />

* Concatenate code split in multiple lines
* Remove the comments
* Process escape sequences
* File Inclusion: Remove headers and include file and stitch the code.
  <br />
  Ex: <#include> will be removed and code is added to the file.
* Macro Expansion: Textual transformation of the macros.
  <br />
  + \__FILE\__ replaces by filename as a string
  + \__LINE\__ replaces by current line number (as an integer)
 <br />

## Compiling:
<p>
Compilation is a multi step process starting with lexical analysis, breaking program into meaningful atomic instructions called tokens.
</p> 
<pre>
Ex: for the instruction
      float newValue = 10.5;
following tokens are generated
  {float, keyword}
  {newValue, identifier},
  {=, operator} 
  {10.5, constant}, {;, symbol}
</pre>

<p>
If the token is not valid, compiler will generate compilation error. As any langage has grammer to communicate, all programming langugaes have context free grammer to confer to. All the valid tokens will be used to construct a Parse tree. Parse tree is an ordered rooted tree that represents the syntactic structre of the string according to some context free grammer. Errors will be generated, if the code does not confer to language grammar. After parse tree construction, semantic analyzers perfom static analysis of code by checking type compatibility of tokens. 
</p>
<p>
In the next steps machine independent intermediate code is generated. Intermediate code is the data structure used internally by a compiler to represent source code. Assembly code will be generated using intermediate code.
</p>
<p>
In the compilation process data and tokens are stored in memory called symbol table. We access symbol table whenever a specific value is required. 
</p>

## Assembling
Assemblers will transform the assembly code to machine code optimized to hardware architecture. Machine Code is specialized instructions specific to the machine architecture.

There are two types of machine codes
* Relocatable machine code, which is not dependent on the memory location of program start.
* Absolute Machine Code, which is dependent on the memory location of the program start.
<p>
Since assembler is dependent on the architecture of the processor, it varies from machine to machine.
</p>

## Linking
Assembler removes traces and links to the code and stores in the symbol table. The assembler returns a different object file for each code module without any logical relation. Linker will combine all the related modules to a single file. 

Static linking is when the machine code is completely merged into single file. In some instances object files are not statically linked instead linker provides memory location of the library to loader. This process is often referred as dynamic linking.

In the instance where libraries are used by multiple processes, libraries are shared instead of creating duplicate instances. These libraries are called shared objects. Generally language speicific libraries are shared.

In the last phase, loaders based on type of machine code will place them in memory, create program and data stacks and initialize. 
Then Machine will run the instruction to "print Hello, World!".
