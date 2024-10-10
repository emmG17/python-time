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

So an easy way to know what index is a specific element is to subtract _one_ from the number it takes when you count them normally. In my list, `"Chocolate bar"` is in the third position, so its index is 3 - 1, that's 2 (quick maths!). And if you think it, the last item's index is just the list length minus one.

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

The first list method allows you to add new items to the end of the list, this operation is also known as _appending_. In Python, we can append an item to a list using the `append` method. For example, if I forgot to add a box of Hot Pockets into my shopping list I can add it like this:

```py
healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk"]
healthy_shopping_list.append("Hot Pockets")
# healthy_shopping_list will now be:
# healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk", "Hot Pockets"]
```

Here are a couple of things to notice in the example:

1. As you can see you need to tell `append` what to add into the list by writing `"Hot Pockets"` inside the brackets.
2. We call `append` differently than how we use other functions like `len()` or `print()`, that's because a method is tied to a data type, so `pop` is not available for every variable you have in your program, and to be able to use it we use the notation shown above.

### Removal service

Yes, now I have some Hot Pockets coming on its way, but then I checked my freezer and discovered there are two boxes sitting there unopened. Now, I need to undo my hard work and remove the **last item** from the list. Fortunately, there's an easy way to do this in Python, I just need to use the `pop` method:

```py
healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk", "Hot Pockets"]
healthy_shopping_list.pop()
# healthy_shopping_list will now be:
# healthy_shopping_list = ["Flamin Hot Cheetos", "Baja Blast", "Chocolate bar", "Frozen pizza", "Pork rinds", "A celery stalk"]
```

Noticed how we called `pop` with empty parentheses? Calling pop without anything inside the parentheses tells Python to remove the last item from the list. This is not the only way to use `pop`, if you put an item index inside the parentheses, that is, passing an argument, Python will remove the element at that specific location. Let's get rid of the frozen pizza:

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
