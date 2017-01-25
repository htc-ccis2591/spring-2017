---
title: "Program Scope"
published: true
morea_id: read-scope
morea_summary: "An explanation of scope in JavaScript, and techniques for managing visibility of variables, functions, and objects in a JavaScript application."
morea_type: reading
morea_sort_order: 3
morea_labels:
 - textbook

---

# {{ page.title }}
Read Chapter 7 from your textbook *Learning JavaScript* ([errata](http://www.oreilly.com/catalog/errata.csp?isbn=0636920035534)). Chapter 7 covers program scope and common techniques and best practices for managing the visibility of your program variables, functions, and objects.

{% include alert.html type="note"
    content="Understanding scope is incredibly important to understanding how JavaScript differs from many other programming languages."
%}

This chapter introduces many of the best practices you will be accountable for throughout the course.  However, instead of just saying "Do this", the author takes the time to explain *why* these are best practices. This material covers things that are often used in interviews to assess a developers level of expertise specifically with JavaScript.  It also lays the groundwork for what might be considered more advanced JavaScript coding techniques.  

## What is Scope?
When programming, it is important to know *if* variable, constants, and functions are defined and what their values are at various points throughout your program.  Whether or not something is defined, is determined by its __scope__.

Scope and existence are not the same thing.  While it is true that if a variable does not exist (is not defined), then it is not in scope.  The reverse is not true.  If a variable is not in scope, that does not mean that it does not exist.  A variable might exist (be defined & hold a value), even if it is not in scope or visible in a particular part of a program.

## ES6 changes JS Scope Rules
Note that the idea of block scope is new in ES6. There is some discussion in this chapter about how things were done before ES6, and even though we are learning the latest, greatest stuff you will encounter *a lot* of old code out in the real world. It will take a long time before all the pre-ES6 code is gone. You need to understand how scope used to function just as much as you need to know how it will function in ES6.

Pay attention to the discussion of `let` and `const` vs. `var`.  Make sure you understand what an IIFE is and why you might use one.  They are often used by libraries and *modularized* code for scope and to protect most data and functions while clearly exposing those intended for outside use.  

## Use strict mode
A best practice is to use __strict mode__ for your code to prevent errors from pre-ES6 scope fun as well as other things. We are aiming to write code that follows industry best practices so I will expect you to do this.  You should be careful however to keep this scoped to only the code you write, not the global scope.  Use an IIFE for this, or as we begin working with jQuery you can use the jQuery.ready function.
