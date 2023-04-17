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
narrative is particularly effective at persuading people by engaging our natural sense of empathy.
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

## 5. Turn the outline into prose

Everything we've talked about so far has been aimed at preparing you for this part of the process.
You should know your goal, audience and structure.
And your outline gives you a game plan.
Now it's time to turn all that into something for others to read.

### Putting flesh on the bones

Right now what you've got is a skeleton.
It's vaguely in the shape you want,
but if it tried to walk around it would quickly fall apart.
There are two principle things that it is lacking:
muscle to give it strength,
and ligaments to hold things together.
Let's start with the muscle.

Bare statements of fact rarely carry much weight with readers,
regardless of how important those facts might be.
They have to be elaborated on
and placed into their proper context.
And usually the most important context for a reader is the answer to 
"Why do I care about this?"
A reason to care gives your prose strength.

Consider this example:

> Continuous integration improves the development process.

> Continuous integration improves the development process by helping us detect defects sooner.
> That means fewer late night calls to debug production.

The latter includes more supporting detail about _how_ it helps,
as well as a reason for developers to care about it.

In addition to muscle we need ligaments.
The ligaments are what actually connects one bone to another.
The prose equivalent is a transition.

Sudden jumps from one topic to another
(even closely related)
are jarring.
Transitions serve to smooth that over by
clearly signaling the close of one topic,
the introduction of the next,
and possibly how they are related.

A transition can be a simple phrase.
It can be an entire sentence.
It can be a paragraph.
Or multiple paragraphs.
It all depends on the size of the pieces you're transitioning between.

For an example, take a look at the paragraph that started this section (#5) above.

### It's not necessarily exposition

When working from your outline,
beware of always choosing the most direct expansion of your points.
Simple exposition is the most common way of describing things,
but it isn't always the best.
Using other forms of expansion will give your prose variety and help maintain reader interest.

Especially in a longer text,
including the occasional story, joke, or anecdote
can make the difference between a pleasant read or an unbearably boring one.

Whatever you choose to use,
it should be integrally related to the points you're trying to make.

There is a story about a high school student who had to give a book report.
When he stood up in front of the class he yelled,
"Sex! Sex! Sex!"
then continued,
"Now that I have your attention,
I'd like to talk to you about The Complete History of World War II."

Don't be like the high school student.

## 6. Revise

At this point you have a fleshed out draft,
so now it is time to fix the gaps and rough edges.

### Evaluate

Starting at the beginnning, read each unit of your work.
Depending on the length of your document, that unit might be a paragraph, section, or chapter.
As you read, ask yourself the following questions:

* Does this advance the goal?
* Is it clear?
* Is it concise?
* Is it well organized?
* Is it scannable?

You'll likely want to read the unit multiple times to answer these questions.
For a longer unit, one read per question -- or even more -- may be appropriate.

> #### Tip: Try different contexts
>
> Reading in a different context than you usually write in can help you to see things differently and spot problems more easily.
> For example, if you usually write at a computer,
> try printing your document out on paper,
> or even reading it out loud.

### Plan your corrections

Take notes on each thing that needs to be improved,
but don't make corrections right away.
Introducing a slight delay between identifying the problem and attempting to fix it
will give your mind a chance to work on the problem,
and often arrive at a better solution than the first one you thought of.

Your notes can take many forms:
a separate text file,
using Track Changes in Microsoft Word,
and so on.
I tend to prefer annnotating a physical paper with pen or pencil,
but you should experiement and find what works best for you.

After you have a list of all the corrections you plan to make,
you may be able to spot common patterns for future improvement.
But the immediate task is to begin making corrections.

### Make your corrections

Proceed through your notes from beginning to end,
correcting each problem.
If you get stuck on something,
leave it to the side for now.
You'll come back to it later.

Once you've completed all the corrections you were able to make,
take another look at any you left behind.
You may know how to fix them now.
If so, go ahead.
If not, we'll leave them for the next stage of the writing process: feedback.

## 7. Get feedback

Up to this point everything has come from you,
even thinking about the audience.
But this is where you actually engage with other people for the first time.
Brace yourself,
because feedback from real people is almost certain to suprise you,
regardless of whether it's positive or negative.

### Sources of feedback

Generally you will be getting feedback from one of three types of readers:
members of the target aurdience,
experts on the subject,
and friends/coworkers.
Each of these groups has strengths and weaknesses.
Getting feedback from all three is ideal,
and occasionally the groups overlap,
but feedback from any of them is useful for checking your assumptions.

#### Target audience

Members of the target audience are extremely valuable
because they can tell you whether your writing is achieving the intended goal.
Unfortunately, they often can't tell you why.
And even if they do offer a reason,
it shouldn't always be taken at face value.

To help overcome this issue,
it can help to supply a list of specific questions for them to answer.
For example:

* By the end did you think that it is worth investigating the new technology I described?
* If not, was there a specific point where I lost you?
* Did any of my supporting evidence seem questionable?

Unfortunately, it can be difficult or impossible to get feedback from the audience.
After all, when drafting an email to your boss's boss,
you can't very well ask them to proofread it.

#### Experts

Expert feedback can also be very useful,
particularly for identifying inaccuracies and mistakes.
One issue to watch out for, though,
is that experts may not remember what it was like to be a beginner.
So if beginners and non-experts are in your target audience,
be careful of suggestions to includes lots of additional details which they won't have the context to understand.

#### Friends and coworkers

Friends and coworkers are often the easiest reviewers to obtain.
Unfortunately, they are often the least reliable in providing needed correction.
No one wants to hurt the feelings of someone they like.
But they are often excellent at providing encouragement,
and when working on a large writing project,
that can be invaluable.

### Evaluating feedback

When evaluating the feedback there are a few principles to keep in mind.

First, _readers are always right about their reactions_.
If a reader says that they were confused by a certain point,
then they were,
no matter how clear it may appear to you.

Second, _a reader's negative reaction does not automatically lead to revision_.
It is your responsibility to evaluate
whether issues raised are actually problems for your target audience
and serious enough to require addressing.

Third, _a reader's proposed solution may not be correct_.
Sometimes readers will suggest solutions without explaining the problem they identified.
For example, "I think you need a fancy graphic right here."
This suggestion might be a good one,
but you should work to understand the underlying problem.
Perhaps the text became boring,
or perhaps a diagram would help with clarity.
Whatever the case may be,
don't just take the suggestion at face value.

Finally, _a reader's feedback should be weighted differently based on who they are and what area their feedback is in._
An expert's feedback regarding correctness should be prioritized over a beginner's,
and an audience member's feedback regarding readability should be prioritized over the expert's.

### Compile the feedback into revision notes

After taking all of this in,
you should have a list of changes to make.
And you may also have a list of positive points which you should try to retain.
Despite the focus on improving problems,
you also don't want to edit away something that is working.

## 8. Revise based on feedback

Just like with your first revision notes,
you will go back through and make your changes one at a time,
evaluating the criteria of clarity, concision, organization, scannability and goal focus.
By the time you are done,
you should have a pretty solid draft.

As you revise, make changes one at a time,
assessing clarity, concision, organization, scannability, and goal focus.
Pay attention to common themes in the feedback you receive.
Those are the ones most likely to require revision.

Remember to prioritize the most significant changes first.
Tackle issues like organization or persuasiveness before minor details like grammar.
Getting something grammatically correct is a waste of time
if that entire section will be reworked or removed.
Throughout revision, continuously review your goals and audience,
and be prepared for multiple rounds of changes.

After you've revised, seek additional feedback,
both to verify initial concerns are addressed
and to ensure no new problems have been introduced.
Consult with both original and new readers to get different perspectives.
Remember, continuous revision is crucial for producing a polished and effective piece of writing.

## 9. Publish

Publishing your work is usually the most critical part of the writing process,
but remember, it can happen at any point, depending on the project.
In some cases, publishing might be part of an ongoing process,
with updates and revisions made after the first release.
This is especially true for things like wiki-based technical documentation
or presentations that are given multiple times and need tweaks based on audience feedback.

Before you publish, think about the context and the level of polish your writing needs.
Not every situation calls for super polished writing.
A quick email to a coworker won't need the same level of refinement as a formal report for the big boss.
Adapt the level of polish to the context so you strike the right balance between quality and getting things done.

Before hitting that publish button,
give your work a once-over for any errors or inconsistencies,
and make sure your formatting looks good,
based on what's required in your situation.
This final check is crucial for presenting your writing in the best light.

After publishing, don't forget to spread the word.
Share your work with the people who need to see it,
whether that's passing a report to colleagues,
posting a blog on social media,
or presenting your findings at a conference.
Keep in mind that publishing doesn't mean you're done with revisions.
Be open to feedback even after your work is out there,
and be ready to make updates or corrections as needed.
Embracing this back-and-forth will help you keep improving your writing skills
and adapt to the needs of your audience in all kinds of situations.

## Summing it up

The writing process is all about striking the right balance between the formal process and the needs of the situation.

From setting goals and figuring out who you're writing for,
to making an outline,
revising,
and hitting that publish button,
each step is important.
But not equally important.

Keep an eye on your context and switch things up as needed,
whether it's the level of polish or the amount of feedback and revision you're going for.
Don't forget, the process can and should be trimmed down when it makes sense for the situation,
helping you focus on what's most important in each specific context.
The more you work at it, the better you'll get at writing and connecting with your audience.

Writing takes time, practice, and being open to learning from both the things you nail and the things you, well, don't.
As you gain experience as a writer,
you'll find that this whole process starts to feel more natural,
and your ability to get your point across will only get better.
Just keep writing, learning, and tweaking your process to fit each unique writing situation you find yourself in.