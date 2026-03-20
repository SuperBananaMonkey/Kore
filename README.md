# The Kore Programming Language
-----------------
The programming language designed to make developing big web applications easier.Kore enforces types, scopes, and structure at compile time so bugs are caught before the browser ever sees your code.
------------------------------------------------------------------------------------------------------------
# NOTICE:
This tutorial mainly documents developing Kore applications on Windows!
----------------------------------------------------------------------------------------------
# A basic hello, world program in Kore that outputs 'Hello, World!' to the browser console:
```kore
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
To get started, make sure you have installed The Kore Compiler (a zip file) from this repository's releases. Once you get it on your machine, make sure to extract it, put it in an important folder such as Program Files (On Windows). Then, it is good practice to set up an environment path variable. This can be done by creating a new environment path variable, for example: Kore -> OS\Example\Kore (and make sure that you only include the folder that contains only the main files, not any file sitting in it), and then edit the existing 'Path' variable, clicl 'New' and add %YOUR_VARIABLE_NAME%, for example, it can be: Kore, so you do %Kore%. To check if Kore is successfully set up, go to a command-line/terminal and type out: `kore version`.
