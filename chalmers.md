# Fail forward - modular code development
## Nine practices to exented the life and value of your software
* Say What, Why and for Whom Before How
* Build in small batches
* integrate continously
* collaborate
* Create CLEAN code
* Write the test first
* Specify Behaviours with Tests
* Implement the Design Last
* Refactor Legacy Code


## From the Checklist Manifest:
"All learned occupations have a definition of professionalism, a code of
conduct. It is where they spell out their ideals and duties. The codes
are sometimes stated, sometimes just understood. But they all have at
least three common elements. 
First and understanding of selflessness:that we who accept
responsibility for others - whether we are doctors, lawyers, teachers,
public authorities, soldiers, or pilots -- we will place the needs and
concerns of those who depend on us above our own. Second is an
expectation of skill: that we will aim for excellence in our knowledge
and expertise. Third is an expectaion of trustworthiness: that we will
be responsible in our personal behavour toward our charges.
Aviators, however, add a fourth expectation, discipline:discipline in
following prudent procedure and in functioning with others. This is a
concept almost entirely outside the lexicon of most professions.
...
Discipline is hard -- harder than trustworthiness and skill and perhaps
even than selflessness. We are by nature flawed and inconstant
creatures. We can't  even keep from snackin between meals. We are not
built for discipline. We are built for novelty and excitement, not for
careful attention to detail. Discipline is something we have to work at.
...
To be sure, checklists must not become ossified mandates that hinder
rather than help. Even the simplest requires frequent revisitation and
ongoing refinement. Airline manufacturers put a publication date on all
their checklist, and there is a reason why - they are expected to change
with time. In the end, a checklist is only an aid. If it doesn't aid, it
is not right. But if it does, we must be ready to embrace the
possibility.

Developing reproducible and reusable software involves establishing
software engineering practices. This represents a cultural change 
since new ways of doing software development needs to be learnt,
experienced and agreed upon. In this talk we will focus on what Software
Engineering is. How encapsulation, modularization, testing will
influence the individual code developer. How code-review, automatic
testing and integration testing influence the process within the code
development group, especially the need for a permissive learning
culture. It should all add up to contribute to a software of higher
quality, to the benefit of the community.


## The (lack) of Efficiency with batching:

| *Release cycle* | *Average Wait* | *Efficiency* |
| 1 week          | 1.5 weeks      | 100%         |
| 2 weeks         | 3 weeks        | 50 %         |
| 1 month         | 1.5 months     | 23 %         |
| 2 months        | 3 months       | 12 %         |
| 3 months        | 4.5 months     | 7.7 %        |
| 4 months        | 6 months       | 5.8 %        |
| 6 months        | 9 months       | 2.6 %        |
|                 |                |              |


## Small is better for four essential reasons:
* It is easier to understand.
* It is easier to estimate.
* It is easier to implement.
* It is easier to test.
* Smaller tasks are also far less risky because they give us more opportunity for feedback.

## Divide et impera
### WIP - Work In Progress
Work-In-Progress-the number of items on our "to-do-list"-divided by the
time necessary to complete each item equals our cycle time.

By reducing the number of items on your to-do-list, your cycle time
decreases accordingly, providing faster feedback and revealing issues
while they're still small problems more easily fixed.

In traditional requirements-based development, everything is
front-loaded onto that "to-do list", which is precisely what a set of
requirement is. That makes a huge number for work-in-progress, which
then makes cycle times jump into months, even years, leaving small
problems time to fester and multiply into system-crashing bugs.

This isn't only true in Waterfall software development;it's also true in
many organizations claming to be Agile. Whenever you put off integration
and testing until later, you're keeping work-in-progress high. Taking a
task to 99% completion isn't good enough because the amount of risk is
still unknown (Black Swan). The only way to elimante the risk associated
with adding a new feature is to fully integrate that feature into the
system as it is being developed.

The solution, as we will se, is to integrate continously, which provides
instant feedback as to whether or not bugs have been introduced. This
kind of feedback helps developers fix defects when they're small so they
can move on without much effort.

## Force field
The shortest path between to point is a straight line. Introduce a
gravity field, and its no longer a straight line, at least a throw will
be follow a cure trajectory.

As a developer you are moving through a force field with more forces
that just gravity. Ejecta "things thrown out". You might think you are
able to move in straight line - "It is obvious. I will do it right the
first time." - but you are setting you up for failure. Verify your
assumptions by testing.

Practice = the freedom to be able to make mistakes. 
