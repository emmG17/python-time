---
title: "The very basics"
excerpt: "We'll dive into three important aspects of any programming language that will help you, whether you're creating some lame meme program or building gargantuan AI models that compete with the ones from OpenAI."
coverImage: "/assets/blog/the-very-basics/cover.webp"
date: "2024-09-21T03:25:00.000"
author:
  name: Emmanuel G.
  picture: "/assets/blog/authors/emmg.png"
ogImage:
  url: "/assets/blog/the-very-basics/cover.webp"
---

## The very basics

Previously, on "It's PYTHON time", we wrote a simple program that displayed _"Hello, world!"_ on the screen. But we know that you —and Python— are capable of much more. So let's dive into the very basics. We are about to unleash some serious power and learn how actual code is written by people with neckbeards—whether you like it or not.

Today, we'll dive into three important aspects of any programming language that will help you, whether you're creating some lame meme program or building gargantuan AI models that compete with the ones from OpenAI.

### Math 101

Back in the Boomer Age, computers were essentially glorified calculators. They could perform basic arithmetic operations faster than any human could and were also capable of comparing things using simple logic. By combining arithmetic and logic, early computers were able to tackle problems that would have taken teams of geniuses ages to figure out. While technology has evolved and computers have become faster (and flashier, thanks to RGB lighting), at their core, they still rely on math and logical operations to function.

In programming languages, just like in regular math, to perform even the simplest mathematical operation, you need to work with at least a pair of numbers. The operation applied to those numbers could be an addition, subtraction, multiplication, division, etc. To represent these operations we use special symbols like '+' for addition or '÷' for division. These symbols are called **operators**.

Here are the mathematical operators you can use in Python

| Operation        | Symbol (operator) |
| ---------------- | ----------------- |
| Addition         | +                 |
| Subtraction      | -                 |
| Multiplication   | \*                |
| Division         | /                 |
| Integer division | //                |
| Modulo           | %                 |
| Exponentiation   | \*\*              |

All right, you are probably wondering what integer division and modulo are, so let's clear that up. Integer division gives you the result of dividing two numbers, but it removes any decimal portion. Be careful though—it doesn't round the number; instead, it performs a floor operation. For example, if we divide 8 between 3, the result will be 2, not 2.6667.

The modulo operator gives you the reminder left over from a division. For example, the modulo of 5 and 2 is 1. Think of it like the way you did division by hand in elementary school, before learning about decimals.

Let's put these operators into action. In Python, they work like this:

```py
3 + 5 # Outputs 8
13 - 8 # Outputs 5
21 / 3 # Outputs 7
8 / 3 # Outputs 2
7 // 2 # Outputs 3
8 % 3 # Outputs 2
2 ** 2 # Outputs 4
```

These operators can be used in longer expressions, and yes, you can use parentheses to group operations together. Mathematical operations in Python follow the PEMDAS order, so plan accordingly. For example:

```py
(3 + 5) / 2 + 4 ** 2
# Will yield 20
```

Now you can perform the foundational mathematical operations, meaning, you can cheat in your math tests from now on (if you have access to a computer).

### Where did I put my keys?

It's great that you can perform some wild math operations using Python, but imagine you need to solve a problem with a lot of steps and need to store those steps somewhere for later use. **Variables** are that space where things can be stored—they are like drawers where you stash your socks and random stuff. To create a variable in Python, all you need to do is give it name and assign it a value, like this:

```py
first_programmer="Ada Lovelace"
```

Let me explain what this code does:

1. 'first_programmer': This is the name of the variable we're creating. When the interpreter reads it the first time, it creates a new "drawer" where we can store things. It's useful because we can refer to this name later to retrieve or change what's stored in there.
2. '=': This isn't the mathematical equals sign. In most programming languages, including Python, this is known as the _assignment operator_. It tells Python to store whatever is on the right side into the variable on the left side
3. "Ada Lovelace": This is the value we are storing in the "drawer" named 'first_programmer'. Besides, [Ada Lovelace](https://en.wikipedia.org/wiki/Ada_Lovelace) was such an amazing woman.

Now that we understand how to create a variable, let's use one to improve (if possible) the "Hello, world!" program.

Using either the Python REPL or a text file write this:

```py
name = "World"
print("Hello, " + name + "!")
```

Run the program and notice the difference. If you noticed a difference, you are a liar, the output is the same as the original one. However, try assigning a different value to the 'name' variable and run the program again. Have you noticed the change? Pretty cool right? Just imagine all the possibilities.

_Note: If you get an error about something not being defined, don't worry—you'll learn why in the next section. It's great that you are exploring!_

Be mindful of the names you use for variables. They should be clear so that anyone reading your code— including your future self—can understand what's going on. Ask any programmer if they’ve ever had to read an old piece of code, found it unintelligible, got frustrated with the person who wrote it, and then realized they were the one who wrote it. Every single one will likely answer "yes," at least when they were beginners. To showcase the importance of good variable names, check this snippet and try to figure out what it's about without jumping to the answer:

```py
e = 3.1416
j = 4

v = (4/3) * e * (j ** 3)

```

Even if the value of Pi (e) gives you a hint, it's not obvious what this formula is. The formula here is used to calculate the volume of a sphere. It would be clearer if the program had better variable names. Let's fix it:

```py
pi = 3.1416
radius = 4

sphere_volume = (4/3) * pi * (radius ** 3)
```

As you see using variables is a key aspect of programming, not only they enable a program to store values for later use, but also helps people read and understand what's happening in the code.

### Multiverse of madness

If you were paying attention, you might have noticed that we’ve used both numeric values and text values. In programming, we call these different types of values data types. Data types are important because they allow us to represent various things from the real world, and programming languages provide specific tools to work with each type. Python has many data types beyond just numbers and text. Let’s review some of them.

**String**
This is the data type for any text in Python. For example, in our previous program, the 'name' variable had a string data type. To distinguish variable names from strings, Python requires text to be enclosed in either single or double quotation marks.

```py
name="Velma Dinkley"
catchphase='Jinkies'
number="370"
```

Strings also behave differently with basic operators. For example, the '+' symbol concatenates two strings (joins them together).

```py
greeting="Oh, hi!"
person="Mark"

full_greeting=greeting + " " + person # Oh, hi! Mark
```

The multiplication operator (\*) also works with strings:

```py
bar="They not like us "
chorus=bar*3 #They not like us They not like us They not like us
```

However, other mathematical operators can't be used with strings. We can only imagine what string division or exponentiation would look like. If you wanna sound like a computer science savant, you can refer to the different behaviors of operators with different data types as _operator overloading_—it's such a cool term.

Be mindful whenever you write a string: if you forget to enclose it in quotation marks, the interpreter will assume you are referring to a variable. This can lead to some funky things happening to your program. Most likely, you'll get an error, but sometimes you may unintentionally assign the value of an existing variable.

**Integer**
As the name suggests, integers are whole numbers without decimal parts. In Python, you simply type the number—no need for quotations.

```py
eaten_hotdogs=4
most_hotdogs_eaten_record=83
```

**Float**
Floats, short for "floating point numbers", are numbers with decimal parts. Like integers, floats don't need to be enclosed in quotations.

```py
pi=3.141592
silver_atomic_weight=107.8682
```

One important note: whenever we perform division in Python, whether using floats or integers, the result will always be a float unless we use integer division.

**Boolean**
This data type is named after [Boo](https://es.wikipedia.org/wiki/George_Boole), the little girl from Monsters Inc. A Boolean’s purpose is to represent whether a condition is true or false. It’s a unique data type because it only has two possible values: **True** or **False**.

```py
dwight_misses_jim = False
we_are_doomed = True
```

We’ll dive deeper into how to use boolean values effectively in upcoming posts.

**List**
So far, you've been storing a single value in each variable, but what if you need to store a collection of things in one place? Fear not—lists are here to help! Lists allow you to store multiple values in the same variable. In Python, the items in a list don’t need to be of the same data type. Here's how we create a list:

```py
shopping_list=["bananas", "kale", "vitamins", "greek yogurth", "cigarettes", "corn syrup"]
random_stuff=["Cleopatra", 2.71934, True, 5]
#Notice the brackets surrounding the items and the commas separating each one.
```

If you are wondering if you can have a list of lists, the answer is yes! These are known as multidimensional lists.

Having a collection of items is cool, but what if you want to pick one specific item? That's where indexes come in handy. Indexes are both a blessing and a curse: a blessing because they let you select any item from a list, and a curse because they start at 0, which can be confusing if you're used to counting from 1. In fact, 90% of the errors you will have are because of this offset (this wasn't fact-checked).

Let's see how indexes work:

```py
nice_movies = ["Star Wars IV", "Star Wars V", "Star Wars VI"]
# The indexes will be 0, 1, 2
```

To access a single element, write the variable name followed by the index number in brackets:

```py
nice_movies[0] # Star Wars IV
nice_movies[1] # Star Wars V
nice_movies[2] # Star Wars VI
```

Be cautious when using indexes: if you request an index greater than the number of elements minus one, you'll get an error.

**Tuple**
Tuples are similar to lists but immutable—meaning you can't modify them. While you can add or remove items from lists, you can't do that with tuples. Here's how to create and access a tuple, which looks very similar to list syntax:

```py
the_fellowship_hobbits = ("Frodo", "Sam", "Pippin", "Merry")
# Notice the parentheses instead of the brackets
```

**Dictionary**
A dictionary in Python is similar to a phone book (do those still exist?), where a name is associated with a phone number. In a dictionary, each "key" (like the name in the phone book) has an associated "value" (like the phone number). Unlike lists, dictionaries let you retrieve data using a meaningful key instead of an index. A dictionary is created like this:

```py
salaries = { "john": 10000, "paul": 80000, "george": 85000, "ringo": 20 }

salaries["ringo"] # 20
```

The syntax differs from other collections: a dictionary is composed of key-value pairs. The key can be of almost any immutable data type (strings, numbers, tuples), though strings are most common, and the value can be of any data type.

### You did it!

This isn’t an easy-breezy lesson for a newbie. It might feel overwhelming, but don’t worry—practice makes perfect. Just keep going, experiment, and have fun (while you can). This post is the first of two that will cover the backbone of programming in any language. If you grasp these concepts well in Python, learning other programming languages will be much easier. But, please, don’t try programming in Haskell—nobody’s ever deployed anything serious with it! Give yourself a high five and a chai latte.
