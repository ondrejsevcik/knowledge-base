# The Coding Dojo Handbook

![Book Cover](https://s3.amazonaws.com/titlepages.leanpub.com/codingdojohandbook/hero?1518047894)

## Intro

http://codingdojo.org

> A young man is on the subway, carrying a guitar case. He’s a member of a band that is performing a concert at Carnegie Hall; and he’s running late. He dashes off the train and up the stairs, and realizes he’s lost. He knows that the performance hall is close, but he doesn’t know the direction. So he stops an old man on the street and asks: “Excuse me sir, but how do I get to Carnegie Hall?” The old man looks at the lad with his guitar case and says: “Practice son, Practice.”

- All professionals practice, but not all practice is equal. Professional practice games as well as drills.
- It's a great way to promote good practices amongst your colleagues
- The focus is not on delivering solutions, but rather on being aware what you actually do when you produce code and how to improve that process

> I’m not a great programmer, I’m just a good programmer with great habits - Kent Beck



## What is Coding Dojo?

It's a meeting where a bunch of coders get together, code, learn and have fun

Puzzling Code Kata + safe environment to discuss topics like design, testing, refactoring, tools... and you'll hardly be able to stop them talking

### Essential Dojo Elements

- Intro
- Moderation
- Retrospective
- Write tests
- Show your working

The `intro` and `moderation` are designed to make sure everyone feels safe to experiment and learn. The `retrospective` makes sure you reflect on what you've learned. Writing `tests` sets you up with a feedback mechanism on whether your code is working as you expect. Demonstrating `how you write the code` means you learn a mechanism to produce good code, not just what good code looks like.


## Collaborative Games for Programmers

A Collaborative Game is one where there is no individual winner, but rather all the participants must contribute to a solution.

### Randori

- Everyone can see the code, projected onto the wall, and everyone gets to write some code.
- No preparation needed
- Code to design decisions through discussion
- Suitable for groups of 4-10 people

#### Rules

1. If you have the keyboard, **you get to decide what to type**
2. If you have the keyboard and you don't know what to type, **ask for help**
3. If you are asked for help, **kindly respond to the best of your ability**
4. If you are not asked, but you see an opportunity for improvement or learning, **choose an appropriate moment to mention it.**

### Pair Switching Strategies

#### 1. Timebox

- each pair has 5-7 minutes
- after that, driver goes back to the audience, copilot becomes a driver and one from the audience step up as copilot
- ➕everyone has a go at driving
- ➖you get cut off in the middle of what you're doing

#### 2. Ping pong

- A writes test and hands the keyboard
- B writes the implementation, writes test and hands the keyboard

#### 3. NTests

- The pair write and implement N tests (1-3 tests)
- only works with experienced TTDers


### Randori Variants

#### 1. Driver/Navigator

Driver writes code. Navigator tells what to write (like in rally-car racing 🏎)

#### 2. Randori in Paris

Ideal for larger groups (10+). Pairs (or trios) work on a Kata for 45-90 minutes. Apart from learning from each other during the coding, some of them should also present how they build up the solution to the whole group. 

#### 3. Musical Chairs Programming

Same as Randori in Paris but every 10 minutes each pair switch one member. 


### Prepared Kata

In a prepared Kata demonstration, someone has practiced the kata many times and is showing the group their best solution (entire process from empty editor via TDD to a full working solution).

#### Screencast 

It's not possible to pause presenter and ask a question but if you already know the Kata, and have practiced it, it might be also beneficial to see someone else do it differently.


### Code Retreat

- day-long practice-intensive event for programmers
- practice usually [Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life)
- usually 5 sessions (5m intro, 45m coding, 5m retro, 5m break = 60m/session)
  - at the end of the session, you delete all the code - less stressful (you're not there to deliver)
- Every year, there is [Global Day of Code Retreat](https://www.coderetreat.org/)
- Another variant is Legacy Code Retreat
  - focus on refactoring and Approval Testing
  - [Trivia](https://github.com/jbrains/trivia)
 
#### Constraints

Idea is to force you out of your comfort zone and give you no choice but to work on a particular coding skill.

- Make a test list
- Keyboard only
- Plaintext editor
- Really small methods
- No Conditionals
- No Loops
- Mute pairing with "Find the Loophole"
- Collective Green Deadline (a.k.a. Customer is coming for demo)


### Using Production code in the dojo

- Sometimes, it's good to bring up your next (production) coding task in as a Dojo exercise
- Follow the usual meeting format
- Be very careful to keep the atmosphere safe and constructive
- Keep doing TDD
- Make progress in small steps

#### This code is impossible to TDD!

Alternatively, you might be finding TDD really hard with a particular piece of legacy code. Get your most experienced developer to do some preparation, and practice TDD:ing a tricky piece of code. They can then show this as a prepared Kata to the rest of the team. **The idea is to inspire everyone that TDD is possible after all**.

#### Identify a suitable Kata from production code

Sometimes when you're working on production code, you find TDD working really well, and that the piece of code you're building feels small and self-contained like a Kata. You might want to package it as such and try it out at your next dojo.

It needs to be quite small and self-contained so that you can code it from scratch in 1-2 hours.



## Organizing a Coding Dojo

Deliberate Practice - it is only by working at what you can't do that you turn into the expert you want to become.

> But what changes people is what they do, not what they read. How many diet books have I read? Am I thinner?...

- Finding Or Founding A Coding Dojo
  - find someone to co-found it with you. It's more fun that way and you keep each other moving.
  - meetup.com
  - agilealliance.org
