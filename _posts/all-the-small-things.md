---
title: "All the small things"
excerpt: "A few lessons ago, we briefly touched on collections like lists, tuples, and dictionaries—special types that can hold multiple values. In this post we'll dive deeper into how to use Python lists, and we'll explore one of the most important concepts in programming: iteration"
coverImage: "/assets/blog/thats-logic/cover.webp"
date: "2024-10-10T03:25:00.000"
author:
  name: Emmanuel G.
  picture: "/assets/blog/authors/emmg.png"
ogImage:
  url: "/assets/blog/thats-logic/cover.webp"
---

**Do you remember** how we use variables to store information, like names, prices, or even True/False values? That's super useful, but what if we need to store more than one thing at a time, like when you are returning home from a shopping spree with as many bags as you have fingers? Being limited to carrying one bag at a time won't be very practical, right? It would be like a wallet that can only hold a single bill.

Luckily, every programming language has a solution for this, in Python we have **lists**. A few lessons ago, we briefly touched on collections like **lists**, **tuples**, and **dictionaries**—special types that can hold multiple values. In this post we'll dive deeper into how to use Python lists, and we'll explore one of the most important concepts in programming: **iteration**

## Write me a shopping list

Brace yourself because once you know how to use lists you'll be ready to code your own operating system or, if you dare, you could use one to write your shopping **list**.

Let's take a look at how lists are written:

```py
non_planets = ["Titan", "Phobos", "Moon", "Pluto :("]
whatever_else = [42, "William Shakespeare", ["Gemini", "Capricorn"], True]
```

As you can see, a list can hold any type of value and can store any mix of data types, even other lists. The syntax is pretty straightforward: a list is any group of comma-separated values enclosed by square brackets.

Now try creating a shopping list using a Python list. Here's mine as an example:

```py
healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk"]
```

Mine's really not a healthy shopping list and I should fix it. However, right now we only know how to create a list, we do not know how to access its items. **The next part is really important**. A list is like an office with PO Boxes, where each element goes inside a box, and this box has a number to identify it, so every time you need to retrieve a certain item you just look to the PO Box with the right number, well this number is the **index**

In Python indexes start from zero, and are added sequentially, to illustrate better let me show you what are the indexes in my shopping list:

```py
healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk"]
# Index                            0,               1,              2,               3,              4,              5
```

As you can see, my list has _six_ items, but the last index is _five_. Be mindful of this difference, because if you ignore you can get Python to yell you mean things like:

```
IndexError: list index out of range
```

So an easy way to know what index is a specific element is to subtract _one_ from the number it takes when you count them normally. In my list, `"Chocolate bar"` is in the third position, so its index is 3 - 1, that's 2 (quick maths!). And if you think about it, the last item's index is just the list length minus one.

A quick way to know how long a list is just using the `len()` function (`len` stands for length), here's how you would use it to calculate the index of the last item from a list:

```py
healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk"]
list_length = len(healthy_shopping_list) # 5
last_item_index = list_length - 1 # 4
```

I think I deviated from the main point here, I told you how to get the index from an element, but as just knowing a PO Box number is not the same as going to the office and get the mail from that PO Box, knowing the index doesn't tell Python to go fetch the item we want.

Yup, you might think Python is dumb, but an important part of any programming is to make no assumptions on what to do, so you can have full control of your program, and you know what to expect every single time.

Now, here is how you access an element from a list using your precious index, let's say I want to know what was the fourth element in my list:

```py
healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk"]
print(healthy_shopping_list[3]) # Remember: 4 - 1
# Outputs: Frozen Pizza
```

The cool thing about this access is that it also allows you to modify the selected item. Finally, I'm going to fix my shopping list:

```py
healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk"]
healthy_shopping_list[5] = "Instant noodles"
```

What do you think this code does? If your answer was "improving the overall nutritional value by replacing the awful celery stalk with a cup of instant noodles", you're right (and should see a nutritionist). To be clear, we assigned `"Instant noodles"` to the element with index 5 in the `healthy_shopping_list` variable.

Now you have learned how to create lists and retrieve its items, play a little with your own lists: print the list items and modify them. If you are of the curious kind, try using negative indexes and notice what happens (I will not explain further that, it's blasphemy).

## Changing the shopping list

Storing and accessing data in lists is pretty straightforward, but what happens if you forgot one item in the shopping list, or you need to remove one? Well, here's where list **methods** come in handy. But first, let's define what a method is. A **method** is a special kind of function tied to a data type, it allows the data type to have different behaviors. Think of a method as a special command that can only be used with a specific type of data, like a list. It's like a built-in tool that lets you do different things with your list, like make it grow or make it shrink.

### Pushing the limits

The first list method allows you to add new items to the end of the list. This operation is also known as _appending_. In Python, we can append an item to a list using the `append` method. For example, if I forgot to add a box of Hot Pockets into my shopping list I can add it like this:

```py
healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk"]
healthy_shopping_list.append("Hot Pockets")
# healthy_shopping_list will now be:
# healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk", "Hot Pockets"]
```

Here are a couple of things to notice in the example:

1. As you can see you need to tell `append` what to add to the list by writing `"Hot Pockets"` inside the parentheses.
2. We call `append` differently than how we use other functions like `len()` or `print()`, that's because a method is tied to a data type, so `pop` is not available for every variable you have in your program, and to be able to use it we use the notation shown above.

### Removal service

Yes, now I have some Hot Pockets coming on its way, but then I checked my freezer and discovered there are two boxes sitting there unopened. Now, I need to undo my hard work and remove the **last item** from the list. Fortunately, there's an easy way to do this in Python, I just need to use the `pop` method:

```py
healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk", "Hot Pockets"]
healthy_shopping_list.pop()
# healthy_shopping_list will now be:
# healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk"]
```

Notice how we called `pop` with empty parentheses? Calling pop without anything inside the parentheses tells Python to remove the last item from the list. This is not the only way to use `pop`. If you put an item index inside the parentheses, that is, passing an argument, Python will remove the element at that specific location. Let's get rid of the frozen pizza:

```py
healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk"]
healthy_shopping_list.pop(3)
# healthy_shopping_list will now be:
# healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Pork rinds", "A celery stalk"]
```

Now you can remove any element of the list, cool, isn't it? But what if you don't know the index of the thing you want to remove, but you know its value. Well there's another method for that: `remove`. Imagine this scenario: for some strange reason escaping human comprehension you can't count, but miraculously you can read. Again you want to remove the frozen pizza from the shopping list. Here's how you would accomplish it using `remove`:

```py
healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk"]
healthy_shopping_list.remove("Frozen pizza")
# healthy_shopping_list will now be:
# healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Pork rinds", "A celery stalk"]
```

Be mindful if you have repeated values, `remove` will only _remove_ the first appearance. So don't think `remove` is not removing, it's just working as intended.

### Read the friendly manual

There are a lot more list methods that I'm not covering. It's not that they are not important, but I want you not to get overwhelmed and more importantly I want you to learn where to find information about Python.

The first place I would recommend checking out is [W3Schools](https://www.w3schools.com/python/python_lists.asp). This site's information is clear and provides a sandbox where you can test the methods.

The second place is the official [Python documentation](https://docs.python.org/3/library/stdtypes.html#list), it's not beginner-friendly and let's be honest the UI makes it hard to navigate, however it provides a lot of information about how things work.

You've now mastered the basics of Python lists! Before we move on, take some time to play around with the code examples, explore the Python documentation, and try creating your own lists. Can you figure out how to add items to the beginning of a list? Or how to sort the items? In the next section, we'll unlock even more power with
iteration, which will allow us to perform actions on every item in a list automatically.

## Iterate till it hurts

In this section we'll tackle what is **iteration**. If it sounds like a magical word, it's because it is, using iteration you can accomplish a lot of incredible functions ranging from a simple playlist to training an artificial intelligence capable of dooming the human race.

So what is this **iteration** thing? To keep it simple it's just a way of doing a task multiple times without explicitly writing every single case. As Kevin from The Office stated: "Why say many word, when few word do trick?"

Now that we understand what iteration is, let's see how it works in Python.

### While you exist, program

Imagine a world where people can't count from 1 to 10, and you are tasked with the monumental task of creating a program to solve this problem. Certainly you can do:

```py
print(1)
print(2)
print(3)
print(4)
print(5)
print(6)
print(7)
print(8)
print(9)
print(10)
```

But that's really unwieldy, we should have a better way of doing this, after all we programmers are lazy people. We should, we must have a solution. And yes, Python offers the `while` loop to solve this problem. Let's review the main parts of a `while` loop:

```py
while condition:
    do_something()

    modify_the_condition()
```

Let's break this example down:

1. `while`: Is the keyword that tells Python it should expect iteration to happen.
2. `condition`: Is anything that outputs a boolean value, if it's true the iteration will continue, otherwise it'll stop.
3. `do_something()`: Can be any action you need to perform inside the while loop
4. `modify_the_condition()`: Is the part where you modify the initial condition, if you don't do this, your loop will never stop and most certainly will crash your program.

Now we'll write the magic program that will count from 1 to 10:

```py
number = 1
while number <= 10:
    print(number)
    number += 1
```

Go ahead and try running this program, it should output the expected numbers. But what does every line in this code mean? It doesn't look as straightforward as just printing each number one by one. So let's go through each line and understand what it does:

1. `number = 1`: We start by storing our initial number (1) in a variable, so we have something to print the first time.
2. `while number <= 10`: Read it as: "while the variable `number` has a value equal to or less than 10 do this:". That is because we are not interested in counting any number greater than 10
3. `print(number)`: This is the action we perform in each of the steps run by the `while` loop.
4. `number += 1`: Here we increment the number by one. This action allows two things, to advance to the next number, and by doing so ensures our loop ends. If we omit this line, our program will print 1 a bazillion times and then the program will crash.

To be honest, the previous example was kind of lame. Nobody will find this kind of program useful by itself. So let's create a more practical program. We'll create a playlist and reproduce it. After you complete this program Spotify will be in shambles.

#### A better example

Our counting program worked really nice. It was the nicest program in the history of counting programs, but it was lacking real applications. Think of this: if we can increment numbers using loops, then we can loop through all the list items because their index is a number, we just need to know the starting point and the ending point. The starting point will always be zero, and the ending point will be the list's length minus one.

Here's how we will loop through the items of a fruit basket represented as a list:

```py
fruit_basket = ["apples", "bananas", "oranges", "grapes"]

index = 0
while index < len(fruit_basket) - 1:
    current_fruit = fruit_basket[index]
    print("The basket has " + current_fruit + ".")
    index += 1
```

There you go, run this little program and verify how sweet it is to be able to access each of the list items without writing the action you want to perform over and over again.

Let's start coding our playlist. Here are the steps to follow:

1. First create a list with song names
2. Then create a variable to hold the list index value, and assign zero to it
3. Create a `while` loop condition that checks the index doesn't go after the end of the list
4. Print `"Now playing: "` and the name of the song
5. Increment the index by one

Before reading my solution, try doing it by yourself.

_Take your time..._

Ok, now that you have coded your amazing playlist reproducer, let me show you mine:

```py
# Cool songs vol. 1
songs = ["Darude - Sandstorm", "Panjabi MC - Mundian To Bach Ke", "Rick Astley - Never Gonna Give You Up", "Haddaway - What is Love", "Yes - Roundabout"]

index = 0
while index < len(songs) - 1:
    current_song = songs[index]
    print("Now playing: " + current_song + " 🎶")
    index += 1
```

It looks pretty ok, doesn't it? Just one thing is bothering me, everything is printed almost at the same time, that's such a bad bug for a playlist (or should we call it a feature?).
Let me add a couple of lines for the sake of getting the program to work as expected:

```py
from time import sleep

# Cool songs vol. 1
songs = ["Darude - Sandstorm", "Panjabi MC - Mundian To Bach Ke", "Rick Astley - Never Gonna Give You Up", "Haddaway - What is Love", "Yes - Roundabout"]

index = 0
while index < len(songs) - 1:
    current_song = songs[index]
    print("Now playing: " + current_song + " 🎶")
    sleep(5)
    index += 1
```

Do not worry about the new lines I've added, we will explore what they mean in the next lessons. What those lines do is add a wait time of 5 seconds between each iteration. Feel free to add those lines to your playlist too. Have you done it?

```py
if you_have_done_it:
    print("You are such a great programmer!")
else:
    print("You are such a great programmer, too. But, please, take some risks")
```

Whoa! We wrangled the `while` loop as pros. As you can see this kind of loop allows us to repeat the same actions many times until we tell Python to stop, which is great! I hope you are starting to see why iteration is useful and why we programmers rely on it so much. However, `while` is not the only way to iterate things in Python: A new foe enters the arena, the `for` loop!

### For the Love of Loops (and Lists!)

Alright, buckle up buttercup, because we're about to dive headfirst into the world of `for` loops. If you thought `while` loops were cool, hold onto your hats, because `for` loops take iteration to a whole new level of awesome.

Remember our playlist program? We had to create a separate variable to track the index, and then manually increase it with each loop. That's a hassle! `for` loops are like the express train of iteration – they handle all that messy index business for you, so you can focus on the meaty stuff.

#### Looping Like a Pro

Here's the basic rundown of how a `for` loop works its magic:

```python
for item in my_list:
  # Do something with each item
```

See? No more index juggling! Using a `for` loop is like saying, "Hey Python, take each item from `my_list` and let me do something with it."

Let's rewrite our fruit basket example using a `for` loop to see this in action:

```python
fruit_basket = ["apples", "bananas", "oranges", "grapes"]

for fruit in fruit_basket:
  print("The basket has " + fruit + ".")
```

Boom goes the dynamite! Just like that, we've looped through our fruit basket with style and grace. No index variables, no manual increments, just pure, unadulterated iteration bliss.

#### A Playlist Paradise

Now, let's give our playlist a `for` loop makeover.

```python
# Cool songs vol. 1
songs = ["Darude - Sandstorm", "Panjabi MC - Mundian To Bach Ke", "Rick Astley - Never Gonna Give You Up", "Haddaway - What is Love", "Yes - Roundabout"]

for song in songs:
  print("Now playing: " + song + " 🎶")
  sleep(5) # Still need this to avoid a musical mosh pit!
```

See how effortlessly we glide through our playlist? It's like Python is our personal DJ, spinning the hottest tracks without breaking a sweat.

#### Why `for` Loops are the GOAT

`for` loops are the go-to choice for iterating over lists (and other sequences) because they're:

- **Concise and readable:** No more clunky index management, just clean, elegant code.
- **Less prone to errors:** Say goodbye to "index out of range" headaches! `for` loops handle the boundaries for you.
- **More efficient:** Python optimizes `for` loops behind the scenes, making them faster for many tasks.

So, embrace the power of `for` loops and unlock a whole new level of programming prowess! But remember, with great power comes great responsibility. Don't let your loops run wild–always make sure they have a clear purpose and a well-defined end.

And there you have it! You've officially conquered iteration, wielding both `while` and `for` loops like a true code master. Remember, iteration is your secret weapon for automating tasks, tackling repetitive chores, and making Python do the heavy lifting. Whether you're crafting killer playlists, building intricate games, or training AI overlords, iteration will be your ol' trusty tool.

## The power of the many

Congratulations, Python Padawan! You've journeyed through the land of lists and emerged victorious, armed with the knowledge to create, manipulate, and iterate like a pro. Remember those single-bill wallets? Ancient history! You're now a multi-bag shopping spree master, juggling data with the grace of a seasoned programmer.

But the learning doesn't stop here. The Python universe is vast and filled with endless possibilities. Keep experimenting, keep exploring, and keep that playful coding spirit alive. Who knows? Maybe you'll be building the next killer app or revolutionizing the world with your code. The only limit is your imagination (and maybe your caffeine supply).

> "Oops, I did it again" - Britney Spears
