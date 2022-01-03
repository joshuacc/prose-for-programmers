# General Rules

Rules.
The very word can trigger skepticism.
And understandably so.
We are often confronted with seemingly arbitrary rules
which make our lives harder for no apparent reason.

In this chapter I will give you rules to follow,
but I will also explain each rule's rationale.
So if you find yourself in a situation beyond the scope of the rule,
you'll be equipped to make intelligent decisions about how or if to apply it.

It is also important to acknowledge the limits of these rules.
They are targeted principally at writing within a professional business context.
If you are writing a novel,
these rules will be of limited use.
And if you are writing poetry,
they will probably be entirely useless.
But if you need to communicate ideas to your coworkers,
then these rules will serve you well.

Now that we've set the appropriate context, let's look at those rules.

## 1. Be goal oriented.

> "In my end is my beginning."
> 
> -- T.S. Eliot

### Everything you write has a goal

Suppose a boss or client came to you and said they needed you to build a web application.
Your first question would probably be,
"What is the application for?"
The very idea of writing an application without knowing its purpose is ridiculous.
Yet when it comes to writing prose,
we too often fail to ask the obvious question.

Everything you write has a goal,
whether explicit or implicit.
Those API docs?
The stated goal is to inform other developers how to use your library.
That weekly status report you email your client?
The unstated goal is reassuring them that their money is being well spent.

The goal of a document isn't always obvious,
but in the next chapter, we'll look at some tools to figure it out.

### Knowing the goal equips you to fulfill it.

Let's go back to our hypothetical web application above.
Suppose you did try to build it without actually knowing its purpose?
You are just given a list of features and told to start building.
What would happen?

You'd have no way to evaluate how well or poorly the application was doing.
And that's not just a problem at the end.
All along you'd have questions about how best to build each feature.
But without knowing the application's purpose,
you'd have no way of choosing between the alternatives.
That kind of uncertainty is crippling.
And I suspect that is why many people avoid writing.

But when you do know the goal you are writing toward,
decisions are easier,
and it is simpler to tell whether your writing succeeds in achieving its end.

### The structure of goals

We've talked about goals a lot,
but so far we haven't really clarified what kind of goals we're talking about.
It's all about the document.

In this book,
when I talk about goals,
I mean the purpose intrinsic to the document[^telos],
not the author's personal motivations.
For instance,
your goal in writing API docs may be to keep your tech lead from bugging you about it yet again.
But the purpose of the docs themselves is to assist users of the API.

A document's goals will generally fall into one of two categories:
to inform or to persuade.
Most documents will include a bit of both,
but one will be primary.
To go back to the API docs example,
it may help persuade people to use your library,
but the primary purpose is just to inform them about how to do so.

[^telos]: If you're familiar with ancient Greek philosophy,
this is what Aristotle would call the document's _telos_.

## 2. Be concise.

In a professional context,
everyone is pressed for time.
Being concise is about respecting your readers' time.
Don't force them to read a page when a paragraph will do.

Conciseness also helps you achieve your goal.
The more time investment your text requires,
the more reluctant readers will be to give it to you.
So we should do our best to keep the required investment to a minimum.

At the same time, conciseness does not mean being excessively terse.
Conciseness means saying the exact amount necessary to achieve the goal:
no more and no less.

## 3. Be Clear

### Avoid ambiguity

Human language is rife with ambiguity.
Take as an example my first title idea for this book:
"Writing for Developers."
Only three words,
yet it could be read in two totally different ways.
That title could have meant
-- as I intended --
"A book for developers on the subject of writing."
But another equally reasonable interpretation was,
"A book on writing for an audience of developers."

Ambiguous language is useful in art and poetry,
but not when we are trying to communicate as efficiently as possible.

### Avoid jargon

It is also wise to avoid unfamiliar terms and jargon.
Of course, this is dependent on your audience.
To a developer, this sentence makes perfect sense:

> "Hoth is a lightweight MVVM framework
> which leverages dirty checking
> and immutable data structures for performance."

To a non-developer,
it sounds more like this:

> Hoth is a lightweight magic framework
> which leverages scary magic
> and scarier magic for performance.

For readers unfamiliar with the terminology it communicates next to nothing.

### Narrow the scope of your words

We love to speak in generalities.
Perhaps because it is difficult to definitely prove a generality wrong.
The problem is that the more general a statement is,
the more difficult it is to understand and apply.
Consider this example:

> Object-oriented programming is terrible.

It's not completely meaningless,
but it is extremely broad,
and the implications are unclear.
Should readers avoid all object oriented languages?
It's hard to tell what the author is thinking.

Contrast with this:

> Class-based inheritance tends to make code unnecessarily complex.

This version has narrowed the scope in two ways.
It has narrowed from all object-oriented programming to class-based inheritance.
And it has narrowed from "terrible" to "tends toward unnecessary complexity."
As a result,
this sentence is much easier to understand and evaluate.

Given the choice between the specific and the general, choose the specific.

## 4. Be organized.

For many people this is the most difficult part.
They know the goal.
They can write clear, concise sentences.
But they have a hard time putting those pieces together into a coherent whole.

In the next chapter we'll look at how to do it.
For now let's explore why.

### Structure aids comprehension

The human mind is built for pattern matching.
And it is pretty good at its job,
otherwise we'd have all been eaten by tigers long ago.

Consider two different lists:

* Apple pie
* Blueberry pie
* Cranberry pie

* Wrench
* Justice
* Puppy

The first list is much more memorable and comprehensible.
Why?
Because it is organized into a structure that our minds can easily extract.
Each item in the list was a pie.
Each of the pies was fruit-based.
And the pies were alphabetically ordered.
But the second list had no unifying organizational structure.

### Structure is fractal

Writing structures are simultaneously high level and low level.
They encompass everything
from your three main points
to that sub-sub-sub-point in paragraph 45.
And if you've chosen your structure well,
the micro and macro levels will tend to mirror each other.
For example, consider this outline for an article on the Hoth Framework.

> * Intro to Hoth
> * Immutable data structures
>   * Intro
>   * Benefits
>   * Examples
> * Dirty checking
>   * Intro
>   * Benefits
>   * Examples
> * Example application
> * Conclusion

Both of the main sub-points follow the same structure as the outline as a whole.
The mirroring isn't always this obvious,
but it is generally present.

### Projects may come with built-in structure

Certain kinds of projects come with ready-made,
very detailed structures,
simply because of how common that type of project is.
API docs,
for example,
may vary a bit by language,
but will generally look pretty close to this.

* Modules
  * Name
  * Description
  * Classes
    * Name
    * Description
    * Methods
      * Name
      * Arguments
      * Return value
      * Description

Not every predetermined structure is that specific, though.
Library websites have several things they need to include,
like language,
purpose of the library,
and how to install it,
but they also have more flexibility.

### General purpose structures

In addition to these very specific structures,
there are also many general purpose structures.
These are things like the inverted pyramid, objection-response, etc.

Typically you will pick two or three of these general purpose structures
and use them as the organizing principle of the project.

## 5. Be scannable.

While the previous rule was about the conceptual structure of a text,
this rule is about the visual typographic structure.
The point of scannability is to allow readers to locate important information at a glance,
rather than reading every word on the page.
Even for readers that do read every word,
scannable typography makes it easier to refer back to key ideas in the text.

### Break text into bite-sized pieces

Have you ever read a paragraph that took up an entire printed page?
They are no fun to read.
With no visual breaks,
it is difficult to keep track of where you are,
much less follow the flow of ideas.

To maximize scannability,
text should be broken into bite-sized units of thought.
Paragraphs, for example, should generally be 2-5 sentences long.
Much longer and it becomes difficult to read.
Shorter and you may want to use a heading instead.

### Divide and conquer with headings

The primary purpose of headings is to make your text's conceptual structure explicit.
However, they also have two important scannability implications.

First, headings provide a visual anchor allowing readers to locate where a concept is discussed.

Second, headings breaks the text into units of progress which help the reader stay motivated to continue.
This is part of the reason list posts are such a popular article format.
Each time the reader reaches the next heading,
they get to cross something off their mental checklist.

### Use lists for your lists

While not as common as paragraphs,
the humble list is one of the author's most helpful tools.
It provides:

* Visual attraction for the list
* Visual attraction for each item in the list
* A break from the monotony of paragraphs
* A sense of progress

You can, of course, embed lists directly into your sentences and paragraphs.

> While not as common as paragraphs,
> the humble list is one of the author's most helpful tools.
> It provides:
> visual attraction for the list,
> visual attraction for each item in the list,
> a break from the monotony of paragraphs,
> and a sense of progress.

However, doing so relegates the list contents to a secondary status.
In general,
using typographic lists
(bulleted, numbered, etc.)
for your conceptual lists makes sense if the exact contents are worth emphasizing.

### Emphasize key ideas with bold or italics

Ordinary paragraphs are the parts of a text most likely to be skipped over.
But sometimes important ideas only make sense as part of a paragraph.
That's where typographic emphasis comes in.

Highlighting important ideas with bold or italics allows readers to see key ideas at a glance.

However, there are some rules of thumb to keep in mind.

* Only highlight one phrase or sentence per paragraph.
* Don't highlight something in _every_ paragraph.
* **Never** highlight something with both bold and italics.

Go beyond these limits and readers are likely to feel that you are shouting at them.