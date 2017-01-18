---
title: "Operators"
published: true
morea_id: read-operators
morea_summary: "An introduction to the various types in JavaScript, and how to create variables and constants."
morea_type: reading
morea_sort_order: 4
morea_labels:
 - textbook

---

# {{ page.title }}
Read Chapter 5 from your textbook *Learning JavaScript* ([errata](http://www.oreilly.com/catalog/errata.csp?isbn=0636920035534)). Chapter 5 covers mathematical and comparison operators, string concatenation, and boolean values and operators.

You can ignore the bitwise operators, void, and the ES6 destructuring assignment.  Glance over the object operators, but we will review and focus more on these as we discuss objects in a later module.  While I expect that you understand basic functional programming, we will spend more time introducing Object Oriented Programming later in this course.

Pay particular attention to `===` or the triple equals for strict equality.

`==` is more "equivalence"
`===` is more exactly the same  

For primitive types `==` will convert between types to check equivalence, while `===` will not.
For objects, `==` is not recommended but attempts to check equivalence, while `===` will only be true if they are two variables referring to the same object.
