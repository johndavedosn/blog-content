+++
date = '2026-05-13T20:04:03+01:00'
draft = false
title = 'MPC - P3'
+++

Woah! Long time no see, readers!

I really am sorry for this long, long stop, I kind of got caught in the middle of university exams, work, and a bunch of other things. Additionally, my SSD failed and....came back to life, I think.

##### (Western Digital is totally to blame for that one).

Anyhow, we are very much back with the Malevolent Programming Course. I'm here now to continue your journey into mastering the art of instructing a piece of shiny rock to do stuff for you. So, without further clutter, **allow me to begin**.

# Section 2: Deep Into The Spells.

In the last section, which was written about an eternity ago, we prepared our code editor and ran our first piece of code (Hello World). Today, we are going to dive deeper into the wizardry of the machine, and utilize more programming concepts to learn more about how Mr. Computer (Or Miss Computer, depending on who you ask) can do fancy things.

## Section 2.1: The Machine Never Forgets.

Before we dive into this post's concept, I want you to firstly understand what happened in the previous post's code. Since I kind of let you on a cliff hanger. This is what we wrote and ran last time:

```python 
print("Hello, World!")
```

Let me explain what this basic line of Python code is doing; 

``print`` is a functionality provided by Python itself. It allows us to get the computer to display text, numbers, and many other things. Let's play with it a little!

Pull up your code editor, and open the same file you used last time to print hello world. Replace the text inside the quotation marks with "Python!!!". To clarify, this is what the end result must look like: 

```python
print("Python!!!")
```

> **Note**: Make SURE that the text is INSIDE the quotations or Python will yell at you. You do not want an angry snake yelling at you, do you?

After that, run your code. Click on the green triangle on the top right of your screen. Watch your program run and display "Python!!!". Feel the victory, my friend!

We conclude from our little experiment that any sort of text we put inside those brackets and quotations will be displayed back to us. 

Wanna see something cool?

Replace what's inside those brackets with a math operation, such as below:

```python
print(5 + 4)
```

> 
**Note**: Do NOT put any quotations here. You will understand why later.

If you run the program now, you'll get `9` as the output. The computer did the math for you, cool, isn't it?

Alright, now, let's learn about something completely new, shall we?

Let"s say we have a very special piece of information, for example, someone's name or age. We'd surely want the computer to remember said piece of information, right? right, *well, how do we do that?* you may ask.

In Python, this is extremely easy to do and understand. You simply set a name for this piece of information, and you set that name to equal your information. Let's see how this work, using my name as an example.

```python
name = "Mohammed Ali Moumen"
```
> Note: Notice how whenever we want to use any sort of text, we have to use quotations. This'll mean a lot later on.

As you may see, ``name`` is the name we choose for our information, and we set it to equal...well...my name.

(I highly advice you to play with the text inside the quotes. Maybe try YOUR own name or someone else's. Make the code yours!)

This, my endeared reader, is called a **Variable** - It essentially is how we make the computer remember things, such as texts, numbers, and more things. Why is it called a variable? Well, because its value can change!

In order to know the value of your variable, you can use the ``print`` function to print it: 

```python
name = "Mohammed Ali Moumen"
print(name)
```
> Note: Here, we don't use quotation marks when referring to the variable name. This signals to Python that the word ``name`` already is part of our program. Fun fact: if you had added quotes by mistake, the program would output ``name``. Completely disregarding your variable, what a dumb machine!

When you run this code, it should output the value you've set for your variable. Which in my case is ``Mohammed Ali Moumen``.

As I said earlier, the value of a variable (as denoted by its name) can change. Let's demonstrate this practically too.

Add another line before the print one which changes the value of the variable as follows:

```python
name = "Mohammed Ali Moumen"
name = "Dwayne The Rock Johnson"
print(name)
```
> Note: You may use another name if you like to. I only used that one because...it's funny, I guess.

Running this would output the name you set the variable to equal in the second line. So, in my case, it would be ``Dwayne The Rock Johnson``. Thus, the value of the variable changed.

Additionally, variables are short-lived values. They live in the program's memory space (will be explained later on) and essentially disappear when the program finishes its job. 

Phew! This one quite lengthy, right? Take a break, go grab a snack or something to drink (water preferably), and let what you learnt today sink in. Later on (after you've rested), I do advice to do some basic research on next post's topic - Data Types. Below are some resources to help: 

* [LearnPython.org](https://www.learnpython.org/)
* [TutorialPoint](https://www.tutorialspoint.com/python/index.htm)
* [W3Schools](https://www.w3schools.com/python/)

This is a very important part of the learning process as it teaches you an extremely important skill for programming: Researching. So, please do not skip this and do it when you do have the time.

Until next time, see ya! Stay safe, stay malevolent!
##### (This is gonna be the official way to end MPC posts from now on :3)