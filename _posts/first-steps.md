---
title: "First baby steps, baby"
excerpt: "So you want (or are being forced) to learn how to program in Python? Lemme lend you a hand partner."
coverImage: "/assets/blog/first-steps/cover.webp"
date: "2024-09-18T03:25:00.000"
author:
  name: Emmanuel G.
  picture: "/assets/blog/authors/emmg.png"
ogImage:
  url: "/assets/blog/first-steps/cover.webp"
---

So you want (or are being forced) to learn how to program in Python? Lemme lend you a hand partner.

## Programming language, what's that, bro?

A programming language is a system with syntax, keywords and constructs that allow regular folks like us tell a computer what to do. The set of instructions written in a programming language is known as a **program**. Programming languages are designed to be readable by humans, so they use words like _if_, _not_, _true_, or _while_ to help us humans understand what we are doing. However, computers only understand binary code, so how do the computer knows how to read a program? Well, just like we need a translator when we try to speak to someone in a foreign language, a program needs a translator to be converted in binary code, this translator is known as the interpreter or the compiler.

Now you might wonder, what's the difference between an interpreter and a compiler? Like a human translator working in real-time, the _interpreter_ translates a program as it reads it. A _compiler_, in the other hand, reads all the program once and produces an accurate translation that the computer can read any time without further need of a translator.

All this can be overwhelming, so let's illustrate what we just covered with a simple and yummy analogy:

1. **Our end product**: a hot & steamy bowl of ramen.
2. **The programming language**: the words, measurements and structure we use to write a recipe.
3. **The program**: the actual recipe. It's a set of instructions that, if followed, will produce delicious ramen.
4. **The interpreter/compiler**: is a bad-tempered chef. It reads your recipe and makes sure everything is right. If it's happy, it gives the recipe to the line cook, if not, it will yell at you with an error (and it's not subtle about it).
5. **The computer**: is the poor line cook the bad-tempered chef yells at the recipe. It follows it exactly. No questions asked!

## Whiskey, Tango, Foxtrot is Python?

Python is a **multipurpose, interpreted programming language** developed in the 90s, known for its ease of use and the vast number of libraries that enable users to perform a wide range of tasks, from running a web server, to plot statistics assignments (using dull colors) and training deep neural networks.

## How do I get a Python?

Most computers (stares at Windows) do not include Python by default, luckily it's really easy to install Python on any system, and there are a lot of ways to achieve it. In this post, we will only cover how to install Python on Windows. Linux users already know how to install things from source (right guys?), and macOS users shouldn't be programming anyway.

### 1. Install from the Windows Store

1. Open the Windows Store.
2. Search Python.
3. Install the most recent version (it should have a bigger number).
4. Voilà!

### 2. Install from the Python official site

1. Navigate to [Python Downloads](https://www.python.org/downloads/).
2. Click the download button.
3. Run the installer and follow the instructions. Here just go with the defaults.
4. All done!

### 3. Install from Anaconda

✨ **Please choose this** ✨

1. Navigate to [Anaconda Downloads](https://www.anaconda.com/download).
2. Register (or skip registration) and click the download button.
3. There are more instructions than I care to write. Just follow what it says here: [Anaconda Installation](https://docs.anaconda.com/anaconda/install/windows/).
4. There you go!

### 4. Install from source

1. I'm joking.
2. Seriously.

### Why Anaconda

Brought to you by the creators of the homonymous movies, Anaconda is a bundle of goodies that makes working with Python much easier:

1. **Everything everywhere, all at once**: Anaconda bundles Python with some of the most-used libraries and tools, so in most cases, you can hit the ground running.
2. **Conda**: Anaconda comes with _conda_, which is a program that helps you manage different versions of Python and all of your libraries without breaking anything.
3. **Quick maths**: As mentioned before, Anaconda includes a lot of useful libraries and tools. Most of them are targeted toward data analysis and machine learning, so you can ditch R and use Spyder (barely an improvement) or Jupyter (a big improvement).

In short, if Python is a burger, Anaconda is the deluxe combo with soda, fries, nuggets and an awesome (and cheap) toy.

## My first program 🧸

Now that you have installed Python it's time for your initiation, let's write your first program. Python comes with an interpreter that you can use directly or feed it a file with code. First, let's use the interpreter directly (also known as the REPL):

### Instructions

1. If you installed Anaconda, open the Anaconda Command Prompt. If you took a chance and installed Python another way, just open the regular Command Prompt. Not sure where to find either? Just use the Windows search bar to locate them (outstanding move, right?)
2. Type _python_ (in lowercase) and press Enter.
3. You will see something like this (the version time and compiler data might be different):

```bash
Python 3.12.5 (main, Aug  9 2024, 08:20:41) [GCC 14.2.1 20240805] on windows
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

4. You will see this weird ">>>" symbol, it's there to show you where the current line starts. Since we haven't written anything it is at the very top. Now write:

```py
print("Hello, world!")
```

5. Type enter and watch the magic happen. Yes! "Hello World" is written (or printed) in the command prompt.
6. Now try changing the message, adding or removing characters, and see what happens. You might get errors—we will cover those in future posts.

It might not seem like much, but think about what just happened. The interpreter parsed the text you wrote, figured out what "print" means, identified where your message started and ended, and then translated all of that into binary sequences your computer understood and executed.

## My second program

I bet you are ecstatic right now, and you should be—you just commanded some rock imbued with energy to cast a specific array of photons using nothing words. But what if your program doesn't contain just one or two lines, but a hundred? Writing it in the REPL each time you need it would be a hassle. Luckily for you, programmers are some of the laziest people around, so they've got you covered.

To store a program for later use, all you need is to write your code to a file and this file needs to have a special extension (.py). Let's recreate our program, but this time, we'll save it to a file.

### Instructions

1. Open a text editor, Notepad for example. (Later, we'll explore better options.)
2. Write this in the file:

```py
print("Hello, world!")
```

3. To save the file in Notepad, go to the File menu, click on Save, then in the "Save as type" box select "All formats", and in the "File name" field write your program's awesome name ensuring it has the .py extension. If you are not using Notepad just check how to save a file with the appropriate extension.
4. Open the Anaconda Command Prompt or the regula Command Prompt
5. Go to the directory where you saved your file (if it is not in the same place where the prompt starts). Check how to do so [here](https://www.lifewire.com/change-directories-in-command-prompt-5185508).
6. Type the following in the command prompt (replace the program name with the one you chose):

```bash
python my_awesome_program.py
```

7. Press enter and feel the programmer blood run through your veins for the second time.
8. **And that's it!**

## We're getting there

By now, you’ve created your first program in Python! Even though it was a simple one, you've already ventured into the unknown and taken the first big step. You’ve learned how to interact with the Python interpreter, how to write and run your code, and you’ve even saved your first program to a file, like a champ! That’s no small feat.

Sure, there’s still a long way to go before achieving basic proficiency in Python, but don’t worry—you’ve already tackled some important milestones. You're not just reading about code anymore; you're actually writing it!

And guess what? I’ll be writing more posts like this (at least I'll try), so stick around—you're on the right track!

> "Programming is the art of adding bugs to an empty text file."
