# The Kore Programming Language
-----------------
The programming language designed to make developing big web applications easier.Kore enforces types, scopes, and structure at compile time so bugs are caught before the browser ever sees your code.
------------------------------------------------------------------------------------------------------------
# NOTICE:
This tutorial mainly documents developing Kore applications on Windows since it is mainly available on there!
----------------------------------------------------------------------------------------------
# A basic hello, world program in Kore that outputs 'Hello, World!' to the browser console:
```
uses 'io'

public safe void func main() {
    io:print("Hello, World!");
}
```
----------------------------------------------------------------------------------------------
# What is Kore?
Kore is a statically typed, verbose, intuitive programming language and superset of JavaScript.
# How does Kore run?
Kore's CLI compiler takes a .kore as a command-line argument input and it will generate a .kgc file containing JavaScript in the same directory, which can be directly put into a HTML file with the `<script>` tag or changed into a .js file at release, though keeping it as a .kgc file is recommended during development.
---------------------------------------------------------------------------------------------
# Getting started
To get started, make sure you have installed The Kore Compiler (a zip file) from this repository's releases. Once you get it on your machine, make sure to extract it, put it in an important folder such as Program Files (On Windows). Then, it is good practice to set up an environment path variable. This can be done by creating a new environment path variable, for example: Kore -> OS\Example\Kore (and make sure that you only include the folder that contains only the main files, not any file sitting in it), and then edit the existing 'Path' variable, click 'New' and add %YOUR_VARIABLE_NAME%, for example, it can be: Kore, so you do %Kore%. To check if Kore is successfully set up, go to a command-line/terminal and type out: `kore version`.
# Syntax
Kore has an unique syntax, especially when compared to other languages that transpile to JavaScript (for example: TypeScript, CoffeeScript...), to make a program in Kore we first need to initialize a main function, that can be done by:
```
public safe void func main() {
    # This is a comment!
}
```
As you may have noticed, it's is quite verbose! Don't worry, we will tackle this together. When making a function the first step is telling the scope to the compiler, it can be `public` or `local`, public means it is available to everything in our program while local means that it is only available to the things inside the object where it is declared (AKA only available in the current scope), in this example we are using `public`. The second thing we need to tell is if the function is safe or unsafe, this is mainly for readability, but we will mostly put `safe`. Next is the return type, it is the data type of the value that the function returns, here in the example we use `void` because the function doesn't return a value. Next is `func` which is a mandatory keyword we should always put when declaring a function, and lastly is the name of the function, every non-module `.kore` file must include a main function so the function is named main. You also may have noticed that there is a hashtag and some text after it, don't worry that is just a comment and it is ignored by the compiler, the use of comments is reaching higher code readability.
