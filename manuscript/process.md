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
but haven't given much dtail about them.
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