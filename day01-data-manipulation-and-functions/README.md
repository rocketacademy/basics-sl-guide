# Day 1: Data Manipulation and Functions

## Overview

The first formal lesson of the course sets the tone for the rest of the sessions.

This day has a heavier section of content than the other days so be prepared for the review portion to take a bit longer. There may also be setup questions.

### Some things to keep in mind overall for the first meeting:

**Repeatedly encourage questions from the students.**

**Running on time is important.** Respect people's time - begin the session on time and don't end only after the end time.

## 1.1 Basic Operations

### Overview

This section is relatively intuitive. It is important to establish here that an operation is the smallest bit of computation we can start with. All other code we'll write stems from doing operations, though they may not all be with integers.

### Code Examples and Discussion Questions

For the code examples listed in `script.js`, it will be best to show them in the Chrome Dev Tools console because the results will be printed.

**Question:** Which of the following is the correct use of the multiplication operator?

**Answer:** The `4 * 2` example is correct. The `4 x 2` example will throw an error stating that there is an unexpected identifier: JavaScript thinks the `x` in the syntax refers to a name of a variable.

**Question:** What does `5 % 2` give us, and what does the `%` in `5 % 2` do?

**Answer:** The `%` in `5 % 2` is a modulo operator. It gives the non-negative remainder of the result of a division. `5 % 2` is equivalent to `5 / (2 * 2)` or `5 - 2 - 2`, which is `1`.

## 1.2 Variables

### Overview

From operations we add in variables. Here it is important to re-emphasise the concept of accurate representation vs correct calculation.

### Code Examples and Discussion Questions

Again, it will be useful to demonstrate these in the Chrome Dev Tools console. This is because the Chrome Dev Tools console can print the output and results immediately, without the need for any use of `console.log` on the instructors' end.

**Question:** What does the `=` in `var pi = 3.14` mean?

**Answer:** The `=` sign is an assignment operator. Assignment is not to be confused for equivalence, which is what we have come to know `=` to mean in mathematics. Equivalence operators will be taught much later in the conditional logic sections. 

A useful analogy for assignment is to imagine creating a box named `pi`. By assigning `3.14` into the variable `pi`, we are putting this number in the box we just created. When we want to use the `3.14` number elsewhere, like in `var area = pi * radius * radius;`, we will retrieve this value from the `pi` box.

**Question:** Compare the next 2 lines for the calculation of area with how the area is calculated earlier, `var area = pi * radius * radius;`. Why is the previous method better?

**Answer:** The variable naming is much better in the previous method. Variable naming is important because accurate representation is just as important as correct calculation.

For `var area = 3.14 * 4 * 4;`, there is a repetition of the number `4` which represents the radius. Should the calculation require a change in the radius, the number `4` would have to be changed twice. It will be better to store the radius in a variable first to avoid repetition and use of arbitrary numbers which may not be obvious on first glance.

For `var a = x * y * y;`, it can be tricky to understand the formula is for calculating the area of a circle on first glance. `a` can be better named as `area`, while `x` can be changed to `pi` and `y` to `radius`.

**Question:** Which of the following lines represent the correct use of camel casing for naming variables?

**Answer:** `var areaOfCircle = 1;` is the correct line. Do enforce camel casing when naming your variables. Conventions and standardisation are important for readability, especially when working on larger code bases with multiple developers.

**Question:** What is the value stored in `result`?

**Answer:** We will get `"33"`, not `6`. This is because the `+` operator, when used on strings, concatenates them. The `3` from `num` will be converted into a string, and joined with the `"3"` string. Thus, you get `"33"`.

## 2.1 Pseudocoding

### Overview

This section introduces ***pseudocode*** as a way to bridge logical English sentences into running JavaScript code.

We can add two forward slashes at the start of a line to mark it as a comment, so our computer ignores it when executing code. 

Pseudocoding is also useful for thinking about the program's logic and technical requirements. You can demonstrate this in the in-class exercises: have the students copy and paste the exercise requirements in their JavaScript so that they need not constantly switch windows and tabs to refer to them.

## 2.2 Our First Program

### Overview

This is the first introduction on the starter code. Some students will have some questions about what functions are (especially the main function(s) they will be working with in their exercises), but keep in mind that functions will be covered in the next section.

Be ready to demonstrate the starter code for the students and have it setup in case you need to demonstrate anything related to their questions.

It will be useful to show simple number or string operations on the `input`, and how it will be displayed in the grey box through `myOutputValue`.

### Discussion Questions

There won't be specific code examples provided in `script.js` for this section, and frequently asked questions will pertain to the use of the starter code instead.

**Question:** When I type something in the input in the browser how do I get it to display in the grey box?

**Answer:** Use `input` as part of the `myOutputValue` variable, or assign `input` directly to `myOutputValue`.

## 2.3.1 Functions I

The Basics curriculum is trying to emphasize functions as the most important unit of computation. The idea is that when the computer must do something the easiest way to think about it is wrapped in a function.

There are a few key ideas that students should take away:

* functions can be named and the action of computation can also stand in for the value itself. `calcCircleArea(3)` is both an expression of a calculation but is also the value (the return value). Clear naming is key to writing a good function.
* writing code that decomposes into input (parameters) and output (return value) is much easier to reason about than code that deals with multiple global values. Therefore, we should try to emphasize writing functions that take input and return values.

You can begin demonstrating the code examples in `script.js` by copying them over to your starter code, since our examples are reliant on functions and getting more complex.

### Code Examples and Discussion Questions

**Question:** What does this `main` function do?

**Answer:** This `main` function, when executed, will first log the string `"papaya"` into the browser console. It then converts a distance in kilometres (from the `input`) into miles.

**Question:** What will `console.log` results be for the following 2 lines?

**Answer:** For the function call in `result2`, `a` will be `1` and `b` will be `2`. For the function call in `result3`, `a` will be `2` and `b` will be `1`.

The order of the function arguments will match the order of the function parameters. `a` and `b` will be swapped in the function calls for `result2` and `result3` because the arguments are flipped.

**Question:** What will `addMultiple` return? Why?

**Answer:** The answer is `6`. In `var myOutputValue = add(1,add(2,3));`, `add(2,3)` gets executed first, giving us `5`. Subsequently, `add(1,add(2,3))` is mathematically equivalent to `add(1,5)`. This will be executed after `add(2,3)`, and `add(1,5)` gives us `6`.

This is a demonstration that we can put the result (return value) of executing a function in the argument.

### FAQ

Some common misconceptions around functions:

Q: Students think that the function must be run on the line after it is defined.

A: A function can be called from anywhere. Control flow means that when the function is called it jumps to whatever line it was defined on.

Q: Students think that in order to run more code, they copy the function and use similar lines from the previous operation.

A: Refactoring or recognizing a pattern that repeats itself within the code is something that the students should have in mind to practice.

## In-Class Material

### Overview

***This is the first pairing exercise the students will do.*** Set the tone for the exercise because this is the first time students have heard of pairing. It's important to emphasize the ideal pairing culture we want to build in Basics.

**You might touch on the following points:**

* Pairing only works when both people are willing to commit to the experience and be open to learning from the other person and / or patiently explaining what the other person may not be familiar with.
* Be coachable. Make an effort to listen well when someone wants to explain something.
* Teaching is the best way to understand something deeply. Try to give the clearest explanations possible. This can be very difficult but will really cement a concept.

**Things to look out for in the pairing session:**

It's important that everyone is on the same page with the setup. Some will not be completely setup yet. It is better to spend the pairing time to clear up any misconceptions or setup errors now so the students can move forward easily.

Keep note of any students who already seem lost or confused.

## **Look Ahead / Wrap-up**

After today, we would have named some values, made basic calculations and formatted strings. We've introduced a wrinkle into naming things, using camel casing conventions and functions as action (verb). Clear representation is very important.

It's still early days and the programs are still very simple. Next we add in another kind of control flow, conditions. This is the point at which the code can actually make decisions. When we add in this branching logic things become a lot more complex. In fact logic as a topic on it's own is huge, but we'll be able to apply some simple concepts that are very intuitive for our purposes.