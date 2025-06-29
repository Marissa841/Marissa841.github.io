---
title: Wet vs. Dry Coding Principles
date: 2025-06-28
layout: post
category: General
---

When beginning to code, you will invariably be introduced to functions. Functions are simply defined as a “[…] block of code that performs a task. It can be called and reused multiple times. You can pass information to a function, and it can send information back.”
Functions are used for organization, reusability, testing, extensibility, and abstractions. For this post, I’ll focus on the reusability aspect of functions and the DRY and WET principles.

An essential part of functions is that they are great for reusability. This means it can be called repeatedly in a program. So when should you write a function? The DRY principle helps to answer that. DRY stands for “Do Not Repeat” and can be applied to all programming languages. DRY essentially means if you are going to use the same code twice, it’d probably be best to create a function. From DRY code came its opposite-sounding acronym, WET. WET stands for “Write Everything Twice” and arguably fine-tunes the principle of DRY code.

### The Dry Principle

The DRY term and principle were first coined by the two authors, David Thomas and Andrew Hunt, in their well-known 1999 book, “The Pragmatic Programmer.” The DRY principle was defined as, “[e]very piece of knowledge must have a single, unambiguous, authoritative representation within a system.” This principle was written just over 20 years ago and has stood out as a practical and highly relevant idea that can be used for all languages. The basic idea is to articulate to programmers the need to avoid repetition and simplify code maintenance for your “future” self, other programmers, and/or your team.

### WET(“Write Everything Twice”)

WET came from the DRY principle, which has a few different acronym interpretations; the most well-known is “Write Everything Twice.” The two lesser-known are “we enjoy typing” and “waste everyone’s time.” WET further elaborates on the DRY principle by giving some allowance and permitting two of the same code to exist instead of just the one instance. Once a third occurrence is inevitable, then consider creating a function. Thus, WET essentially gives parameters to DRY.

### The Pragmatic Programmer

The principle DRY came about when the two authors, Thomas and Hunt, viewed the common problems they would often see programmers up against. According to the authors’ Youtube interview, available on the GOTO Conferences YT channel (August 27, 2020), it was mentioned that before they wrote The Pragmatic Programmer, as consultants, one of the common problems they would often see was that there were “no agreements on requirements for programming.” This sparked their writing, among a few other reasons, which eventually led to The Pragmatic Programmer. In the book, the DRY principle was laid out, and not surprisingly, it has stood out, perhaps mainly because it encapsulates common sense when it comes to programming. As a side note, the terms “rubber duck debugging” and “code kata” were also popular terms coined by the two authors and are still applied today. “Rubber duck debugging” is a common debugging method. A person will explain each coding step to a rubber duck — or any inanimate object/ pet to better understand the code. A code kata is a technique used to better one’s skills in coding by regular repetition and practice.

### Why use DRY code?

Dry code can go hand in hand with keeping your code clean. It will simplify and allow for less repetition. If there is unnecessary repetition, that only makes code harder to maintain and adjust down the line. WET code has more leeway, as stated before. WET code allows for a looser, perhaps less strict, adherence to the same principle, with the idea that while keeping code DRY is an admirable aim, WET code may be better in real-world situations.
There are three main reasons why DRY code is preferred, however:
Avoids repetition — If there is a lot of code without any help from functions, the code will become more prone to errors. By eliminating unnecessary repetitiveness, the result is a much neater presentation of work.

Easy Maintenance — With code that is well commented and made into reusable functions, it will be a lot easier to debug or make any changes if need be.
Allows for unit testing.
There are also a few other things to consider when using the DRY principle:
It’s not always necessary to add code into one piece. Some code may look similar, but be sure to be discerning of any possible minor differences.
Avoid “overdried” code — This means you do not need a function unless you repeat the code. “Overdried” code can become difficult to read as well.
DRY can also be applied for database design, documentation, and several other applications.
DRY, to be clear, does not only apply to functions but also to classes and abstractions.

### AHA

Additionally, AHA is a newer acronym that has joined the fray in recent years. AHA stands for “Avoid Hasty Abstractions” and is another helpful principle/guidance. AHA can also be related to the sunk cost fallacy. The sunk cost fallacy is an economic and business idea that is defined by Cambridge Dictionary as “the idea that a company or organization is more likely to continue with a project if they have already invested a lot of money, time, or effort in it, even when continuing is not the best thing to do.” AHA, then, has been defined by Kent C. Dobbs in his article, “AHA Programming” as “optimiz[e] for change first, and avoid premature optimization.” For example, when coders are working on a project, they may create a function. After putting so much time and effort into making the function work, they will fall into the trap of thinking that too much time has been invested to go back and change it if need be. To remedy this problem, AHA suggests that instead of following a “rigid” DRY principle or even WET code, try creating the functions as the need arises.

In summary, the DRY, WET, and AHA principles are helpful for beginner coders to keep in mind. They are great guidelines when starting out and wondering how to manage the ever-growing list of code. When thinking about applying a function, remember DRY; avoid repeating the same code. If using a more WET code style, only consider making a function if there will be more than two instances of the same code. Then there’s AHA, which may be the most flexible, and apply functions only when needed. Hopefully, with these principles in mind, writing code will become an easier task to manage.

### Resources

https://www.learncpp.com/cpp-tutorial/why-functions-are-useful-and-how-to-use-them-effectively/
https://web.archive.org/web/20131204221336/http://programmer.97things.oreilly.com/wiki/index.php/Don't_Repeat_Yourself
https://kentcdodds.com/blog/aha-programming
Anniversary Edition of The Pragmatic Programmer • Dave Thomas & Andy Hunt • GOTO 2020


