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
Short feedback cycles. This high addictive game has a short feedback cycle. This how our development evironment should be. But there must be many feedback cycles, and at many levels. This essential for our learning exeperience.
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

# Write tests first!

--
.. but I know what I am doing, why should I write tests first?

___

# What you "know is a mix of...

* True knowledge
* A set of assumptions 
  
---

## Some of the assumptions are wrong.
A test written first can reveal this.

??? 
- Since you have to think thoroughly about have to write a test testing a  new behaviour, already the thought process may reveal wrong assumptions.

---
# Implementing a feedback cycle
* By writing tests first you implement a feedback cycle. 
* Writing tests specifying behaviour, you create a active environment which relates to your code base.
* If behaviour is broken, it shows up immediately.

---
# Test-first development
* It is a design methodology
* "It helps developers build high quality code by forcing them to write testable code and by concretizing requirements"

???
We are not talking QA here...
- Emphasize testing behaviour - not edge cases.
- Thinking about QA-cases is a separate task.
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

* Focus on one test at a time, and implement the new behaviour step by
  step - with short feedback cycles.
* Name the the test properly - it is the test of a new
  behaviour/feature.
  
???
"Take great care with naming. The small investment of deriving highly
descriptive test names pays well over time, as tests are read and reread
by others who must maintain the code. Crafting a good test name will
also help you, the test writer, better understand the intent of what
you're about to build.

You'll be writing a number of tests for each behaviour in the system.
Think about the set of test names as a concordance that quickly provides
a developer with a concise summary of that behavior. The easier the test
names are to digest, the more quickly you and other developers will find
what you seek."
--Jeff Langr, Modern C++ Programming with Test-Driven Development

--- 
# Getting to green.

---
# Pair programming and Test Driven Development
"TDD supported with pair programming is a natural fit. Learning TDD is
made dramatically easier with a support system in place. Developers are
more likely to revert to old, non-TDD habits without a bit of peer
pressure from their teammates. Sittint with an experienced TDDer can be
more than half the time need to ingrain the habit of TDD. Swapping pairs
can help ensure that tests are writte first and with care.

How to balance pair programming?
"But a team full of siloed devlopers, with little review and no shared
knowledge, will create paint that will only continue to increase over
time.
---
# References
* tmux 2 productive mouse-free development by Brian Hogan, The Pragmatic Programmers / Chapter 5 pair programming with tmux
* Beyond Legacy Code - Nine practices to extend the life (and value of) of Your Software , by David Scott Bernstein* Test Driven Development: By Example, by Kent Beck
* Modern C++ Programming with Test-Driven Devleopment
