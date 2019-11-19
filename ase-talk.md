layout: true
class: middle, inverse

--

# Fail Forward: Development of Reproducible and Reusable software is a learning experience

## Bjørn Lindi and [Radovan Bast](http://bast.fr)

### [NeIC](https://neic.nordforsk.org)/ [NTNU](https://www.ntnu.no) & [NeIC](https://neic.nordforsk.org)/ [UiT The Arctic University of Norway](https://uit.no)

Text is free to share and remix under [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/).

Code examples: [MIT license](http://opensource.org/licenses/mit-license.html)

Credits: [Jonas Juselius](https://github.com/juselius),
[Roberto Di Remigio](http://totaltrash.xyz),
[Ole Martin Bjørndalen](https://github.com/olemb)

---
# Fail forward?

--
## Give yourself the freedom to make mistakes, establish short feed back cycles.
<img src="img/brio-34000-labyrint-i-tre-1.jpg" style="width: 40%;" />

???
Short feedback cycles. This high addictive game has a short feedback cycle. This how our development environment should be. But there must be many feedback cycles, and at many levels. This essential for our learning experience.
---
# Reproducibility?
--

## [Doubt about 150 published chemistry studies](https://arstechnica.com/information-technology/2019/10/chemists-discover-cross-platform-python-scripts-not-so-cross-platform/)
<img src="img/arts-technica-python-error.png" style="width: 40%;" />

???
WRF - support example:
- "It work a month a go". Is something changed? I don't think I have large-file-support
- 4-6 weeks to sort out what the problem really was (could have done much faster if one of us were more WRF-fluent)

---
# Reusable?
--
<img src="img/tumble-weed.jpg" style="width: 40%;" />
## The bush versus the tree
<img src="img/oak-tree-long-life.jpg" style="width: 40%;" />

???

- Witness development cycles like a bush not as a three.
- A cycle is a PhD-thesis.
- Loss of our most precious resource - time
- Someone comes after us - could be our future self

---
# Version Control System

---
# Central repository/ project place

---

# Write tests first!

--
.. but I know what I am doing, why should I write tests first?

---

# What you "know is a mix of...

* True knowledge
* A set of assumptions 
  
---

# Some of the assumptions are wrong.
A test written first can reveal this.

???
- Since you have to think thoroughly about have to write a test testing a  new behavior, already the thought process may reveal wrong assumptions.
-  Tests are specification; they define behavior.
-  Write just enough tests to specify the behaviors you're building and
   only write code to make failing test pass.

---
# Implementing a feedback cycle
* By writing tests first you implement a feedback cycle. 
* Writing tests specifying behavior, you create a active environment which relates to your code base.
* If behavior is broken, it shows up immediately.

---
# Test-first development
* It is a design methodology
* "It helps developers build high quality code by forcing them to write
  testable code and by concretizing requirements" --David Scott
  Bernstein [1]

???
We are not talking QA here...
- Emphasize testing behavior - not edge cases.
- Thinking about QA-cases is a separate task.
---
# Writing a  test first is ...
- making a hypothesis.
- It is a hypothesis that you understand the requirements.

???
- You are used to making hypothesis as a part of your scientific
  training. This is nothing new.
- Once the test passes, the tests serves as confirmation of behavior. If
  the tests breaks, some intend behavior is absent.
  
---

# Learn Test-Driven Development

<img src="img/red_green_refactor.png" style="width: 40%;" />

???

1. Write a test. Think about how you would like the operation in your
   mind to appear in your code. You are writing a story. Invent the
   interface you wish you had. Include all of the elements in the story
   that you imagine will be necessary to calculate the right answers.
2. Make it run. Quickly getting that bar to green dominates everything
   else. If a clean, simple solution is obvious, then type it in. If the
   clean, simple solution is obvious but it will take you a minute, then
   make a note of it and get back to the main problem, which is getting
   the bar green in seconds. This shift in aesthetics is hard for some
   experienced software engineers. Quick green excuses all sins. But
   only for a moment.
3. Make it right. Now that the system is behaving, put the sinful ways
   of the recent past behind you. Step back onto the straight and narrow
   path of software righteousness. Remove the duplication that you have
   introduced , and get to green quickly.
   
---
# Starting on red.

* Focus on one test at a time, and implement the new behavior step by
  step - with short feedback cycles.
* Name the test properly - it is the test of a new
  behavior/feature.
  
???
"Take great care with naming. The small investment of deriving highly
descriptive test names pays well over time, as tests are read and reread
by others who must maintain the code. Crafting a good test name will
also help you, the test writer, better understand the intent of what
you're about to build.

You'll be writing a number of tests for each behavior in the system.
Think about the set of test names as a concordance that quickly provides
a developer with a concise summary of that behavior. The easier the test
names are to digest, the more quickly you and other developers will find
what you seek."
--Jeff Langr, Modern C++ Programming with Test-Driven Development

---
# Getting to green.

* We only write as much code as needed to pass the test. If implies copy
  code, we copy code. If mean using constants, we use constants. 
  
* First we solve "that works" part of the problem. Then we solve the
  "clean code" part(that is part of the next step - refactoring). Divide et imperia.
  
???

"Make it run. Quickly getting that bar to green dominates everything
else. If a clean, simple solution is obvious, then type it in. If the
clean, simple solution is obvious but it will take you a minute, then
make a note of it and get back to the main problem, which is getting
the bar green in seconds. This shift in aesthetics is hard for some
 experienced software engineers. Quick green excuses all sins. But
only for a moment."
--Kent Beck, TDD by Example

---
# Refactor
Refactoring is defined by Martin Fowler as a:
- disciplined technique for restructuring an existing body of code,
  altering is internal structure without changing its external behavior. 
* To get passed the test, you did some sins. Now you make it right.
* Get rid of duplication.
* Refactoring is applying want you have learned from the test.
* Make the code readable and understandable. 
* Tidy up and make code CLEAN.

---
# Start over again, add new functionality

<img src="img/red_green_refactor.png" style="width: 40%;" />

???
- You are incrementally verifying and building new behavior in this way
- You are establishing a development path with feedback.
- You also train/exercise the ability to vary the "step size".
- Being able to vary the step size is valuable when things become brittle
 (your on thin ice.)
 
---
# What is the characteristics of CLEAN code?

--

* It is Cohesive.
* It is Loosely coupled.
* It is Encapsulated.
* It is Assertive.
* It is Non-redundant

This is taken from [1].

???
* Cohesive code reduce side effects
* Loosely coupled code is easier to test
* Encapsulated code is easier to extend
* Assertive code makes software more modular
* Non-redundant code reduces maintenance issues

---
# Quality Code is Cohesive
* In software development cohesive means entities should have a single
  responsibility.

<img src="img/RC_Series_Filter.png" style="width: 40%;" />

???
- The RC-circuit is not cohesive, but the Resistor is, and so is the
  Capacitor.
- By combining these two cohesive components, we get our preferred
  filter. The more complex functionality is achieved with composition.

---
# Quality Code is Loosely Coupled
* "Code that is loosely coupled indirectly depends on the code it uses
  so it is easier to isolate, verify, reuse and extend." [1]
  
<img src="img/knit_vs_lego.jpg" style="width: 100%;"/>

.cite[Slide taken from [Complexity in software development by Jonas Juselius](https://github.com/scisoft/complexity)]

???
- Knitwear is not loosely coupled.
- The power distribution to this room/floor is probably decoupled from
  the power distribution to another of the build. At some point they are
  depending upon the same source, but you can work on the distribution
  on this floor, without causing problems on another floor(,presumably).
---

# Quality Code is Encapsulated.

* Encapsulated code hide implementation details from the rest of the
  world.
* You separate what something does from how it is done, which gives you
  freedom to change how later on.
  
???
- Outside-In Programming vs Inside-Out Programming

---

# Quality Code is Assertive

* The opposite is inquisitive: *Don't be so inquisitive. It's none of
  your business.*
* Software objects should not be inquisitive; they should be
  authoritative, in charge  of them self.

???
- Martin Fowler (Refactoring: Improving Design of Existing Code, refers
  to "feature envy" or "inappropriate intimacy". This code smells
  related to lack of assertiveness.
- Behavior end up in wrong places - multiple object must remain in sync
  to achieve the correct results.

--- 

# Quality Code is Nonredundant
* Don't repeat your self (DRY)

???

---
## That was a nice acronym - CLEAN - So what?

---
## Increase Quality today to increase Velocity to tomorrow.

<img src="img/development-speed.svg" style="width: 80%;"/>


???
- The CLEAN properties are all different sides of the same gem. Focus on
one and the others follow along.
- Cohesive code reduces side effects
- Loosely coupled code easier to test
- Encapsulated code is easier to extend
- Assertive code make software more modular
- Nonredundant code reduces maintenance issues.
---
## "...ASE has grown organically..."

???
- This is cut from the invitation sent to Coderefinery, why we are here.
- My interpretation is codebase size, complexity is starting to be felt
  ( somewhere on the previous red-line, but you want to be on the blue)
-  At some point some of you will work with the "old stuff" - your
   legacy code - or parts of your common code base which hard to work
   with (fix,enhance and so on).
- Having experience CLEAN code and knowing how to change "things"
  incrementally will valuable assets, going forward with the changes you
  need to apply.

---
# Pair programming and Test Driven Development
"TDD supported with pair programming is a natural fit. Learning TDD is
made dramatically easier with a support system in place. Developers are
more likely to revert to old, non-TDD habits without a bit of peer
pressure from their teammates. Sitting with an experienced TDDer can be
more than half the time need to ingrain the habit of TDD. Swapping pairs
can help ensure that tests are written first and with care.

How to balance pair programming?
"But a team full of siloed developers, with little review and no shared
knowledge, will create paint that will only continue to increase over
time.
---
Code Review
---
# References
- [1] Beyond Legacy Code - Nine practices to extend the life (and value of) of Your Software , by David Scott Bernstein
- [2] Test Driven Development: By Example, by Kent Beck
- [3] Modern C++ Programming with Test-Driven Development, by Jeff Langr
- tmux 2 productive mouse-free development by Brian Hogan, The Pragmatic Programmers / Chapter 5 pair programming with tmux
