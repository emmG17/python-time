---
title: "Ah, that's logic!"
excerpt: "Whether is to decide to rot in bed or go to the office, life's about making decisions, programming is no different."
coverImage: "/assets/blog/thats-logic/cover.webp"
date: "2024-09-26T03:25:00.000"
author:
  name: Emmanuel G.
  picture: "/assets/blog/authors/emmg.png"
ogImage:
  url: "/assets/blog/thats-logic/cover.webp"
---

Whether it's deciding to rot in bed or head to the office, or choosing between the blue pill or the red one, life's all about making decisions. Programming is no different. The ability to take a specific set of steps instead of others, is known as conditional execution and is one of the key features that makes programming languages—and by extension, software—so useful. Consider this thoughtful examples about conditional execution:

1. Restricting teenagers from accessing content targeted to a more mature audience by making them select their own age (an unbreakable spell).
2. Determining who is logging in by checking the user's email and secure password.
3. Enabling banks to detect when you overdraw your account, so they can charge you a _lovely_ fee.

In short, decisions drive actions in programming. By using conditions, we can perform different actions depending on one or multiple factors.

## Nothing compares to you

It's cool that we know we can trigger certain actions based on some factors. However, how do we actually know if a condition is met or not?

Enter the **comparison operators**. These operators allow us to compare a value against an expectation and check whether it fulfills what we're hoping for. Imagine this scenario: You are craving something really expensive, and because you are financially responsible, you first check if you have enough money. If, and only if, you do, then you treat yourself to the bag of Flamin Hot Cheetos you desperately need. A computer can do something similar using the ✨comparison operators✨:

| Operation           | Symbol (operator) |
| ------------------- | ----------------- |
| Equal               | ==                |
| Not equals          | !=                |
| Greater than        | >                 |
| Less than           | <                 |
| Greater or equal to | >=                |
| Less or equal to    | <=                |

These operators will tell you whether the comparison is true or false, using the keywords: **True** and **False**

**Example**

```py
account_balance = 3.50
flaming_hot_cheetos = 5

should_buy_cheetos = account_balance >= flaming_hot_cheetos
# Unfortunately, this is False
```

In the example above, we compared two numbers (but you can compare many things): `account_balance` and `flaming_hot_cheetos`. These values represent how much money you have in your bank account and the cost of a bag of Flamin Hot Cheetos. Then we ran a comparison to check if the account balance is greater than or equal to the cost of our precious snack. Sadly, in this case, the account balance was less, so the result was **False**—meaning, no Cheetos today.

## And, or, not: The three magic words

Wouldn’t life be simpler if you only had to make one decision at a time—like whether to buy that bag of Flamin Hot Cheetos? Unfortunately, reality isn’t so kind, and neither is programming. Most of the time, you’ll need to evaluate **multiple conditions** before making a decision.

To tackle this complexity in programming, we use **logical operators**. If you’ve dabbled with truth tables before, this will feel like a walk in the park. If not, don’t worry—we’ll take it step by step.

Let’s imagine you have two conditions, `x` and `y`, and you want to perform different actions based on whether these conditions are true or false. Here’s the setup:

**Conditions**

- `x`: Are you feeling lucky today?
- `y`: Does your crush love unicorns?

**Actions**

1. If you’re feeling lucky **and** your crush loves sloths, you ask them out. (Risky but brave!)
2. If you’re feeling lucky **or** your crush loves sloths, you post a story to get their attention.
3. If you’re feeling lucky **and** your crush does **not** love sloths, you send them a cute sloth meme to win them over.

To make these decisions, Python gives us three logical operators: `and`, `or`, and `not`. These operators help us combine and manipulate conditions. Let’s break them down:

---

### 1. The **and** operator

The `and` operator checks if **both** conditions are true. If even one condition is false, the entire result is false.

Example: Should you ask your crush out?

```py
x and y
```

| Feeling lucky | Crush loves unicorns | Ask them out |
| ------------- | -------------------- | ------------ |
| true          | true                 | true         |
| true          | false                | false        |
| false         | true                 | false        |
| false         | false                | false        |

Only when both conditions (`x` and `y`) are true will the result be `True`.

---

### 2. The **or** operator

The `or` operator returns `True` if **at least one** condition is true.

Example: Should you post a story to get their attention?

```py
x or y
```

| Feeling lucky | Crush loves unicorns | Post story |
| ------------- | -------------------- | ---------- |
| true          | true                 | true       |
| true          | false                | true       |
| false         | true                 | true       |
| false         | false                | false      |

Even if just one of the conditions is true, you get a `True` result.

---

### 3. The **not** operator

The `not` operator flips a condition’s value. If it’s true, it becomes false, and vice versa.

Example: Should you send them a cute sloth meme? (Only if they _don’t_ love sloths.)

```py
x and not y
```

| Feeling lucky | Crush loves unicorns | Send meme |
| ------------- | -------------------- | --------- |
| true          | true                 | false     |
| true          | false                | true      |
| false         | true                 | false     |
| false         | false                | false     |

---

And there you have it—the magic of `and`, `or`, and `not`. These operators may seem a bit tricky at first, but Python makes them easy to grasp with straightforward names and behavior. Once you get used to them, you’ll be combining conditions like a pro in no time.

## The Power of Choice

Now that we’ve mastered comparing conditions, you're ready to harness the true power of programming. If you're feeling a bit tired by now, go stretch, grab some water, and come back refreshed. Else, buckle up for one of the most important lessons you'll ever learn—at least in the world of coding.

Understanding whether something should happen is only half the battle. Knowledge without action is useless. Knowing you can't afford that bag of Cheetos is pointless if you buy it anyway. The same rule applies to programming. Identifying that a condition is met means nothing if it doesn't influence what your program actually does.

### If, and only if

To tell a program written in Python to perform an action only when a certain condition is met, you need to use a special keyword: `if`. This keyword isn’t used alone—you also need to tell Python _what_ condition to check and _what_ steps to take if that condition is true. This combination forms an `if` block, and its syntax looks like this:

```py
should_buy_cheetos = account_balance >= flaming_hot_cheetos

if should_buy_cheetos:
    print("Alright, I'm going to the store")
```

Let’s break down the `if` block:

1. `if`: This keyword tells Python that the following code should only run if a condition is met.
2. `should_buy_cheetos`: This is the condition being checked. If it evaluates to `True`, the code within the block will be executed.
3. `print("Alright, I'm going to the store")`: This is the code that runs _only_ when the condition is true.

Notice the indentation of the `print` statement. In Python, indentation is crucial because it defines what code belongs to the `if` block.

As you can see, `if` blocks are easy to write. The tricky part is coming up with the right conditions to make them work as intended—and that, my friend, is your job!

### Plan B

In programming, decision-making is crucial. Most of the time, there’s an alternative action that should be taken when a certain condition is not met. For example, if you miss the bus to work, you might take an Uber instead. Similarly, in Python, you can establish this fallback plan using the keyword `else`. This keyword should only be used in combination with `if`; otherwise, your program may not function as intended or could throw an error. The combination of `if` and `else` blocks is known as the `if-else block`. Let’s take a closer look:

```py
should_buy_cheetos = account_balance >= flaming_hot_cheetos

if should_buy_cheetos:
    print("Alright, I'm going to the store")
else:
    print("Go get a better job")
```

The `else` block looks similar to the `if` block, with one key difference: it does not require a condition. This makes sense, as the `else` block will execute whenever the condition in the `if` block is not met.

Using `if-else` blocks is particularly useful in programming when you need to ensure that your code can handle multiple outcomes gracefully. For instance, you can provide an alternative action when a user input does not meet specific criteria, preventing unexpected errors and enhancing the overall user experience.

By understanding how to implement `if-else` blocks, you can create programs that respond dynamically to different situations, making your coding much more effective!

### Plan C

Let’s face it: we love having options! That’s why ice cream shops offer more than 20 flavors (even if 15 of them are just vanilla with something else). Similarly, programming languages, including Python, allow you to provide more than two ways to react to a certain value. In short, you can check multiple conditions within the same block using the `elif` statement. As you can imagine, `elif` is short for `else if` and works just like an `if` block. Here’s an example:

```py
craving = "soup"  # Options could be soup, sandwich, or something else

if craving == "soup":
    print("You should get pho")
elif craving == "sandwich":
    print("How about a Philly cheesesteak?")
else:
    print("Please, make up your mind first.")
```

In this code, the `elif` block is similar to the `if` statement, but it can only be used if there’s a preceding `if` block. You can have as many `elif` blocks as needed, but it’s best to limit them to avoid confusion; if you find yourself with more than five conditions, you might need to reconsider how you’re structuring your problem.

Try changing the program to reflect your favorite foods or beverages. Better yet, come up with an original program that helps you make a simple decision!

Here's the revised section with the suggested improvements incorporated:

### A Matroska of Decisions

Imagine you went to buy your delicious and healthy Flamin Hot Cheetos, and when you are about to pay, the cashier tells you they are on sale: you can get 2 for the price of 1! But you remember you are on a diet. As Eminem said, "Would you capture it or just let it slip?" Now you will need to make another decision. The first one was to go buy the Cheetos only if you had enough money. So we can think of this as a decision triggered by another decision. Of course, we can do that in programming languages; to do so, we just put an `if` block inside another one. For real! Let’s illustrate our Flaming Hot Cheetos journey:

```py
should_buy_cheetos = account_balance >= flaming_hot_cheetos
on_a_diet = True

if should_buy_cheetos:
    print("Alright, I'm going to the store")
    if on_a_diet:
        print("No, I'm a sad person, I'll just take one bag")
    else:
        print("This is the best day ever! Yes, I'm taking two bags")
else:
    print("Go get a better job")
```

**What do you expect this code will print?** I'm not telling you; you better code it if you want to know.

### Death by a Thousand Conditions

Please, use nested blocks only if you need them; they make reading the code harder with each added level. Here are some tips to consider:

1. **Simplicity**: Always aim for the simplest solution that meets your needs.
2. **Logical Operators**: Sometimes, you can avoid nesting altogether by using logical operators.

Look at this example:

**Awful code—don't do this:**

```py
if (a > b):
    if (a > c):
        if (a > d):
            print("'a' is the greatest of all")
```

**A better approach:**

```py
if (a > b and a > c and a > d):
    print("'a' is the greatest of all")
```

Notice how it is way easier to read the second option, and it's more compact. This word of advice is not to police your style but to make you think of the people who will read your code in the future (including yourself). It will make their lives easier, and they will not hold any grudge against you.

## The power of decision-making

Being able to assess conditions and perform a set of actions based on them is what sets computers and calculators apart. This ability, known as conditional execution, enables programs to handle multiple scenarios simultaneously. Thanks to this feature, developers have created a wide range of amazing tools, from spreadsheets that calculate complex formulas to ads that are tailored to show you products you want, to ad blockers that filter unwanted content, as well as life-changing experiences such as Goat Simulator.

Mastering conditional blocks, comparison operators, and logical operators is like learning how to use your magic wand, Harry. With these skills, you can conjure up flexible and powerful programs that respond to various inputs and situations.

> Making a decision is like trying to catch a fly with chopsticks
