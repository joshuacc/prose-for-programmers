# The Writing Process

Many people are under the impression that writing is a mystical
-- or at least mysterious --
activity, governed entirely by inspiration.
While it is true that some authors work this way,
waiting for inspiration to strike isn't a common strategy among professional writers,
even novelists.

For programmers and others writing non-fiction in a business context,
there is a simple process that yields quality results.

1. Determine the goal
2. Determine the audience
3. Choose a suitable structure
4. Build an outline
5. Turn the outline into prose
6. Revise obvious weaknesses
7. Obtain feedback
8. Revise based on feedback
9. Publish

In this chapter, we will walk through what each of these steps entail.

## 1. Determine the Goal

### Why am I writing this, anyway?

Every time you start writing something,
ask yourself, "Why?"
Sometimes the answer is obvious,
but often it's not.
And even on those occasions when it is obvious,
asking the question helps keep you focused on the goal.

It's important to remember that we're trying to find the purpose of the document,
not your personal motivation for writing it.
If your answer to "Why am I writing this?" includes the words "I" or "me,"
it is worth evaluating whether you're really thinking of the document's goal.

For instance, if the answer to why you are writing a tutorial is,
"So that I can get a raise,"
you're thinking of the wrong thing.
It's not that the motivation is _wrong_.
It's just _irrelevant_ to producing a good tutorial.
A better answer is,
"To help others improve their game's performance."

Because this answer is focused on what the audience receives,
it is actually useful for guiding your writing efforts.

### Keep asking why.

Often, the first goal we come up with will be superficial.
"Teaching others how to use object pools,"
may be accurate,
and even somewhat useful,
but a bit more context can be even more useful.

There is a technique for root cause analysis called [5 Whys][],
the premise of which is that you need to ask "Why?" multiple times to find the root cause of a problem.
This technique also works well for determining a useful goal for writing.

Suppose the first goal that occurs to you is
"Teach developers how to use object pools."
That is a perfectly clear and useful goal.
But if you write only to that narrow goal,
your readers won't know why the technique is useful.
So ask yourself, "Why object pools?"

Perhaps the answer is "To improve performance."
But again we can ask "Why?"
And our answer is something like, "To keep gameplay smooth."

At this point we can state the goal as:
"Teach game developers how to keep their games running smoothly by using object pools."

With this more robust goal in mind we're more likely to communicate,
not just the technique,
but also its importance and trade-offs.

## 2. Determine the Audience

Once we understand the goal of the document,
we have enough information to start considering our audience.
Our first question, though, takes a step back from the goal.

### Who will be reading this?

Often the readership of documents is wider than we would initially expect.
A framework's website will be read by developers, of course,
but perhaps also:

* Architects evaluating technology choices
* Managers trying to keep abreast of what their team is using
* Technical recruiters trying to understand the skillset they are hiring for
* Designers trying to understand technical constraints on their designs
* Sysadmins figuring out the framework's deployment features

Take time to list the different types of potential readers.
Doing so will help draw out whether additional supporting material is needed.

### Which readers are primary?

Once you have the list of potential readers,
refer back to the goal to decide which readers are most important.
In most cases there will be a single group of readers who constitute your primary audience.

Continuing the previous example:
the primary audience of a framework website is developers.
Others are important, but secondary to that audience.

### What is their relation to the subject?

At this point we have our primary audience,
but haven't given much detail about them.
So it's time to consider their relation to the subject.

One important axis to consider is their current level of expertise.
Are they absolute beginners,
world class experts,
or somewhere in between?
The answer to this question drives
which sorts of things can be assumed
and which need to be explained in great detail.

Another axis is the readers emotional relationship with the subject.
Are they intimidated, enthusiastic, or something else?
A developer who fled Java for Ruby will have a very different attitude toward Haskell than a brand new developer.
They may both be fearful,
but about different things.
Those emotional concerns also need to be addressed.

### What is their relation to you?

In addition to the subject,
we must also consider how the audience is related to you,
the author.
Are they coworkers?
Then you can make certain assumptions about their familiarity with the business.

Are you on friendly terms or is some of the audience hostile?
You may need to focus more on your logical case for the latter.

Are you part of the same culture/subculture?
"Corporate suits" probably won't find image macros as amusing as your 22-year-old developer buddy.

[5 Whys]: http://en.wikipedia.org/wiki/5_Whys

## 3. Choose a Suitable Structure

Now that we know the goal and the audience
we can consider how to structure the document to serve them.

### Choosing a structure based on the goal

Goals can generally be placed on a spectrum between purely informational and purely persuasive.
On one end of the spectrum,
topical hierarchies are great at communicating lots of information efficiently.
The hierarchy conveys the big picture while also supporting scanning through subtopics.

At the other end of the spectrum,
narrative is particularly effective at pursading people by engaging our natural sense of empathy.
Telling a child that "Lying is a bad idea," is less likely to change their behavior than hearing _The Boy Who Cried Wolf_.
For an example closer to our industry, consider _The Phoenix Project_:
it vividly illustrates the problems of bureacratic IT departments
as well as the benefits of embracing the DevOps movement.

### Choosing a structure based on the audience

Your structure also needs to be suited to your audience.

If your primary audience is developers with deep experience in your topic,
then you may want to address them with an equally deep and detailed hierarchy of topics.
A beginner, however, would likely benefit from a shallower step by step "recipe" guide.

The reader's level of interest factors into which structure is best suited.
A highly motivated reader may want to get right to the heart of the matter.
But a distinterested reader
--who is only looking at your document because his boss made him--
may need to be enticed with a joke or anecdote explaining what is in it for him.
That sort of reader will probably also need frequent positive reinforcement.

The audience's relationship with you also makes a difference.
If they are familiar with you and trust your judgment,
they are more likely to be patient waiting for a payoff.
But if they don't know anything about you,
the internet is only a click away.

### Mixing and matching

Most writing structures are relatively flexible
and can be combined with other structures as warranted by the goal and the audience.
**Don't be afraid to mix and match them.**

For example, suppose that you need to convince business leaders that
it is worthwhile to break your large monolithic application into several separate services.
You'd probably start with a Problem-Solution structure like this:

* Problems with the current architecture
* Proposed solution

In order to help the businesspeople make a decision, you'd probably extend it with a Pro-Con analysis as well.

* Problems with the current architecture
* Proposed solution
* Costs and risks of change
* Costs and risks of not changing

A simple factual elaboration on that outline may win intellectual assent,
but is unlikely to elicit wholehearted support from non-technical leaders.
Why?
Because they lack experiential knowledge of the problems, solutions, and risks.

But parables and other metaphorical narratives can impart a degree of experiential knowledge without requiring actual experience.
What sort of narrative would work in this case?

Perhaps a story of a military building a single gigantic ship.
It is powerful,
but difficult to maneuver,
and if it somehow fails then its entire arsenal is useless.
(Business books are fond of military metaphors for some reason.)
Then contrast this with building a fleet of small independently maneuverable ships.

Revising the outline to incorporate this narrative gives us:

* Problems with the current architecture
    * Parable of the dreadnought
    * Supporting factual details
* Proposed solution
    * Parable of the fleet
    * Supporting factual details
* Costs and risks of change
    * Refer to parable
    * Supporting factual details
* Costs and risks of not changing
    * Refer to parable
    * Supporting factual details

Combining these three structures creates a much more powerful and persuasive account than any of them alone.

## 4. Build an Outline

With a structure
(or set of structures)
chosen for your project,
it is time to build an outline.
Some structures,
like API documentation,
may come with an outline template to follow.
But many others,
like the inverted pyramid,
do not.

This phase is all about taking your chosen structures
and combining them with the details of your subject
to produce the skeleton of your document.

The outline itself is a simple hierarchical list of
the things you want to communicate
and the approach you want to take at each step.
Particularly for smaller projects,
the line between choosing a structure and outlining can be rather blurry.
(Evidenced by the the section on choosing structures ending with an outline!)
But an outline should show in detail **how** you intend to implement your chosen structure.

### How detailed should an outline be?

This will likely vary from person to person,
but I prefer to outline in enough detail that
each low level bullet point corresponds to one or two paragraphs in the final text.
This gives me sufficient guidance that I don't get lost,
but also gives me enough flexibility to expand on some points without deviating from the outline.

### How do you actually create the outline?

There are two basic approaches:
depth-first
and breadth-first.
A depth-first approach starts at the top
and explores all the way down to the details one point at a time.
A breadth-first approach starts at the highest level
and only becomes more detailed after all the higher level points have been filled in.

**Partially completed depth-first outline**

* Point 1
    * Point 1.1
        * Point 1.1.1
        * Point 1.1.2
        * Point 1.1.3

**Partially completed breadth-first outline**

* Point 1
* Point 2
* Point 3
* Point 4
* Point 5

Breadth-first generally produces better results,
because it provides more overall context each time we step down a level of detail.
That extra context makes it much less likely that we will get stuck on trivia.

### Evaluate and revise

Once you've drafted your outline,
be sure to evaluate it with your goals and audience in mind.
It is much easier to move or edit a few bullet points
than to revise entire sections of your document.