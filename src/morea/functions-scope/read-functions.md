---
title: "Functions"
published: true
morea_id: read-functions
morea_summary: "An introduction to writing functions in JavaScript."
morea_type: reading
morea_sort_order: 1
morea_labels:
 - textbook

---

# {{ page.title }}
Read Chapter 6 from your textbook *Learning JavaScript* ([errata](http://www.oreilly.com/catalog/errata.csp?isbn=0636920035534)). Chapter 6 covers functions in JavaScript in quite a bit of detail.

## Important Things to Note
I expect you to be familiar with the idea of functions, arguments (input parameters), and return values already, but there are several unexpected things about functions in JavaScript you need to pick up on in this chapter.

1. Functions in JavaScript are objects.  You can pass them around by reference (by name).  Make the distinction between calling a function and referencing a function is clear.  See "Calling Versus Referencing" on page 102-103.
2. There is no *signature* to a function in JavaScript. In some languages, the number and type of the function arguments are part of the function's definition.  This is not true with JavaScript.  See "Do Arguments Make the Function?" on page 105-106.
3. When a function is *in* an object, it's now called a __method__.
4. The `this` keyword is not *always* object-oriented in JavaScript. Sometimes the value of `this` is determined by context when a function is not called directly on an object instance.  Understanding how that works is complex and I approve of the book not discussing it because you shouldn't do it.  However understanding that it is not strictly object-oriented can help understand why unexpected things in JavaScript might happen. See "The `this` Keyword" on pages 108-109.


## Less important things

1. Destructuring arguments
2. Arrow functions, which are new in ES6.  These can be handy and will be used later, but for now knowing they exist is good enough.
3. Call, apply, and bind.  Good to know as well, but you can go a long way without need for these.
