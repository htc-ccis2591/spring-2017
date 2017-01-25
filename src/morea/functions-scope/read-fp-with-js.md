---
title: "Functional Programming in JavaScript"
published: true
morea_id: read-fp-with-js
morea_summary: "A discussion of functional programming in JavaScript."
morea_type: reading
morea_sort_order: 2


---

# {{ page.title }}
{{ page.morea_summary }}

## What is Functional Programming?
Functional programming is the process of building software using pure functions and avoiding:

- shared state
- mutable data
- side-effects

This is a stark contrast to object oriented programming where state is frequently shared and modified by public methods.

Why is this a big thing?  It makes code more predictable and easier to test. This is becoming increasingly popular in the JavaScript world in particular.

## Pure functions
I will *generally* expect you to write __pure functions__ for this course. With a pure function, you can effectively replace a call to the function with its resulting value. (If you want to sound smart, this is called referential transparency.)

To write pure functions, you want to avoid shared state and side-effects. When the function is called with the same input, it must always returns the same output value.

## Side-effects
It's a good practice to write methods that do not have side-effects.  This means that they don't indirectly change anything visible outside the scope of the function itself.  Side-effects often occur through shared state (see below).  

Other side-effects include:
- Logging to the console
- Writing to the screen
- Writing to a file
- Writing to the network
- Triggering any external process

## Shared State
Shared state is any data that exists in a shared scope such as a global scope or properties in an object.  

For example, a common program in my introductory programming class is to build a simple hangman game.  In this game, a secret word is chosen by the computer and the player tries to guess the word letter by letter.  This game needs to be aware of things like what the secret word is, the player's name, the letters the player has guessed, etc.  All of those values define the application's state.

Often what will happen is that that application state is defined in shared global variables that are modified by various functions as the program runs. This state is shared across all of the program code, and functions may internally change that state when they are called (side-effects). This is generally considered *BAD* programming practice, and is particularly problematic for web and distributed environments.  

## Immutable Objects
An immutable object is one that cannot be modified after creation. It's state (values of it's properties) is fixed.  Using immutable objects makes your code more predictable.  Instead of changing the objects properties a new object is created with the desired state.

{% include alert.html type="note" content="Note that when a constant refers to an object, that only means that the constant cannot be reassigned to a new object.  It does not mean the properties of that object itself may not change."
%}

## More information
We're just skimming the surface of these topics here, and we'll expand on them throughout the course. While functional programming is not the main goal or objective of this course it is a very relevant topic for JavaScript programmers.

If you want to dive a little deeper, check out the following blog posts from Eric Elliot:
- [Master the JavaScript Interview: What is a pure function?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-pure-function-d1c076bec976#.mh9l1qwgn)
- [Master the JavaScript Interview: What is functional programming?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0#.wqpw2re0c)
