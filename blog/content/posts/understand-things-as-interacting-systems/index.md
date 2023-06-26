---
title: "Understand Things as Interacting Systems"
date: 2019-09-27T00:00:00Z
draft: false
---

{{< summary >}}

Understanding a complicated topic as interacting systems helps you learn
its properties and gain agency. So what are systems?

A system is what is does.


{{< tableOfContents >}}


## Understand Things As Interacting Systems 

{{< figure
src="https://cdn-images-1.medium.com/max/800/0*l2SctsEb3IUJeGVb"
title="Dr Katie Bouman interacting with a black hole, a team, and the world"
}}

> TL;DR: jump to paragraph "Thinking in systems: why it helps" for why
> it matters, and then "Systems: tentative definition" (last paragraph)
> to have the short version :)

Lately, I discovered that most developers don't conceptualize their
applications as a set of interacting systems. I thought it was the
"architecture 101" of application development, but after some more
inquiring, I discovered that that view of the world was almost unknown,
and not only among developpers.

This came as a surprise to me because it is one of the most useful and
powerful tools I have to systematically understand a topic, what its
parts are, and what the contracts between them are. In the context of
application development, it allows me to evolve large parts of the
application letting other untouched. It allows to make communication
easier with the team. It allows making actual contracts on the behaviour
of your application with users, especially for long-term period. It
allows evolving our internal understanding of the application domain
without impacting third parties out of clear chosen changes.

This tool is so useful that I conceptualize most of my
macro-interactions with the world as systems interacting together.

## Seeing the world as systems is a useful tool 

People believe [systems are
complicated](https://en.wikipedia.org/wiki/Systems_theory){.markup--anchor
.markup--p-anchor
data-href="https://en.wikipedia.org/wiki/Systems_theory" rel="noopener"
target="_blank"}. Perhaps linked to mechanics. Or physics. Or economy.
Hard and boring stuff. They may be, but they don't need to. I use
'system' loosely as a tool to better understand and contextualize a lot
of topics.

Oh, notice how I introduced the subject? Systems are a **useful learning
model** of the subject at hand. If they are not, change the model. Of
course, useful is extremely subjective, so it means that your relation
with the system is key to its definition. It's OK if other groups of
people come with other models, it can even help you to better
communicate with them by understanding how they see the world.

So systems help me **understand how thingies interact with each other**.

### Thinking in systems: why it helps (me, at least) 

Concretely, thinking in interacting systems helps me to:

**1/** understand what are the bounds between vague and composite
things,

**2/** give names that evoke the same group of things to other people
that it does to me,

**3/** understand what vocabulary and private references should be made
explicit when communicating with other things,

**4/** discover and understand communication channels,

**5/** understand what is:

-   [the nominal behaviour of interaction with the entity;]
-   [what are the identified error cases and when I can expect
    them,]
-   [and what is out of scope for that entity, and failures that lies in
    the uncharted lands.]

**6/** know the implicit and explicit promises and the contracts that
these entities give about their behaviour.

More importantly, thinking in systems helps to discover where our
assumptions about the system of interest are false by sharing them and
confronting them to other models and their real behavior, so that we can
progress and refined our models to be less wrong. They will ever be, but
the learning is the useful part, and in the process we gain agency on
the world.

So it's really a great learning and normalization tools. A developer
dream, even if actually, it helps in many more situations. And I
discovered that most of the developers I chat with don't even know what
a system is.

------------------------------------------------------------------------

## System examples 

Systems can be more or less formalized, but a lot of formalization is
not necessary to make them a useful learning tool. Let's take some
examples of systems to get a feeling about what they are.

### Your band of friend at school 

You went to school? That's a nice set of interacting systems! A loosely
defined one:

{{< figure
src="https://cdn-images-1.medium.com/max/800/0*_2E041nS7tXqdpqu"
>}}

You and your friend formed a group (a system) in the school. There was
Alice, Bob, Charlie and you. You were interacting with other
macro-entities (other systems): other children, some of them belonging
to other groups; parents and teachers (the boring *adults*). Sibling of
friends. Etc.

Your group may even have been known by a nickname (hopefully something
along *Alice's band* more than *the little terrors of the canteen*).

You had your own private jokes and experiences which defined your
internal language and the fact that adults got mad when you broke into
laughs after a seemingly innocuous sentence.

Other people were getting in touch with each of you but Bob, because Bob
was far too shy. Bob wasn't an interface for chat, but a good one to get
info about the last comic book. Most of the time, you were nice and you
did as expected for 11-year-old children, apart from subjects regarding
one given superhero. You were living encyclopedia about that one,
especially Alice, and people expected long discussions and sharp
corrections on that topic from her.

You were a system interacting with other humans. Understanding that
helped other people interact efficiently with your group, using the
correct channel to get things done, and understand your behaviour in
school as a coherent entity.

### A shop 

Of course, any company is a system ---and hopefully a system interacting
with other ones. This time, we can even talk about a semi-formalized
system. Look at that little tea shop:

{{< figure
src="https://cdn-images-1.medium.com/max/800/0*iIBOU5rA4RLhak5a"
title="Wardley readers know how important tea shops are."
>}}

A shop is a legal entity with a lot of papers justifying so. It has a
name. It is built to last (at least) for some time. In our tea shop
case, and as it happens often, the two owners developed an internal
language with expert vocabulary like "I put it behind the red teapot,
you know which one" or "the Tuesday billing horror morning". These
sentences sumon perfectly unambiguous understanding of what they mean
for each of the co-owners, even if for you, it's totally opaque. They
also know that after the conniving smile they exchanged, they will need
to explain to you why they don't like that much Tuesday mornings.

Of course, a shop is useless if it doesn't interact with third parties
like customers, banks and suppliers. There have several channels of
exchange with the shop and they don't expect the same kinds of
interactions. Customers typically use the front door of the shop and are
likely to buy some tea, when the bank uses your time and money (ok I'm
kidding, the can use mail or fax for the most modern). Suppliers want to
speak about the supply chain and invoices.

And of course, other systems see the shop through its promises: promise
of experience projected by the brand and communication, promises of
timely paid invoices in exchange for good products for suppliers,
promises of positive accounts for the bank.

Again, understanding the shop interacting system can help us understand
what each actor expects and how he can get it. It can help identify the
tooling needed in each case, the different timelines. It helps gain
agency and define reaction to identified use cases, so that they are
better handled the next time.

### Mathematical proof & code 

Finally, system description can be *extremely* formalized, to the point
where we are able to prove interesting properties about the world they
model. [HoTT](https://homotopytypetheory.org/book/){.markup--anchor
.markup--p-anchor data-href="https://homotopytypetheory.org/book/"
rel="noopener" target="_blank"} is such a system.

But even without going to that extreme, any code can be seen as
interacting systems. Your application is composed of parts that deal
with different kinds of users and different kinds of tasks. You want to
know how what part talk to what others. What is the protocol and
interface point to do so. You want to understand what will be the
consequences of changing a line of code.

You want to name things to easily communicate what part of the
application you are talking about to your teammates. You want to trace
bounds to delimit responsibility and behaviour. You want to program to
interfaces, and use protocols so that internal changes don't leak to
third party code. You want to know what is the nominal case AND the
error modes to correctly react in each case.


------------------------------------------------------------------------

## So what are systems ? 

In each of the previous example, we found common properties that make
system useful tools. Let's walk through each of them.

### Systems are useful learning tools 

We already saw that at the begining: building the model is what makes
you understand it, question your assumptions, share your thoughts. Your
models will be false --- they are models! You learn with iterations,
making them less false is possible.

### Systems are entities... 

A system is a model about entities, so you need at least **things that
last** sufficiently long that you want to talk about them. It can be
anything, from people to items to ideas and more.

{{< figure
src="https://cdn-images-1.medium.com/max/800/0*JTbNigAdxlrA5D0i"
title="Abstract entities"
>}}

These things need to be in some sort of interaction, or at least
relation. Again, here interaction and relation are very loosely defined,
"the cars on the road" is totally fine, as much as "people who saw that
series" or "these lines of codes".

For example, the children from the previous school:

{{< figure
src="https://cdn-images-1.medium.com/max/800/0*UDV0b6JGVDK8yWEZ"
title="Sometime a little bit to concreate entities (if you are parents, you know)"
>}}

So, you have things and links between them:

{{< figure
src="https://cdn-images-1.medium.com/max/800/0*GQw3lZe9QnEkDYAE"
title="Abstractly interacting entities"
>}}

This is your world, the thing you need to better understand, or just
talk about with your friends.

{{< figure
src="https://cdn-images-1.medium.com/max/800/0*3puJTNuZ3ZvWBah4"
title="Noisigly interacting entities"
>}}

**Defining systems --- boundaries and names**

And then, to transform that into interacting systems, you need to do (be
careful, it will be very quick, don't lose the track of my hands): draw
**lines around groups of things that belong together**.

And tadaaaa, you have interacting systems --- an ecosystem:

{{< figure
src="https://cdn-images-1.medium.com/max/800/0*8F3Y4CSt1IvFDGUk"
title="Tada! Colorful systems ! Choosing where to draw lines and why is the interesting part."
>}}

And give a **name** to each group. As you can see, you don't even have
to be good for the naming part, but at least you will be able to easily
communicate to others (and yourself) what things you are talking about.

Again, "belong together" is up to you. It's the part that makes the
system definition helpful to reach your goal, to learn about the
entities at hand. Thinking about the **boundaries** is what makes you
understand your systems.

For example, if you want to build a long-lasting application, you could
group code by the service it provides to other parts of the application.
Or by how stable it must be because of third party integration. Or by
sensitivity of managed data if you are on the security side of
applications.

So each time you have interacting things, and you talk about a subpart
of them, you are actually --- even without knowing it --- defining
systems. Yep, you were doing it all that time.

Some examples of interacting systems:

*"I love that book so much".*

System. With at least the people mostly sharing the ideas of narrators,
and the ones who don't.

*"Did you correct the bug in that part of the application that looks if
the user is connected?".*

System. And you should give a memrable name for that part of the
application. And draw a big line around it, it seems important to be
able to talk about its behaviour.

Or for the previous school example:

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*AtoA_dJ7zDNzT-xZNIgPTw.png"
title="Creating systems is easy. Being ok with someone else (or you in 5min) about where to put the lines and what names should be used is the hard part"
>}}

**Internal language**

As you defined a part "in" a system and a part "out" of it, you will see
that the rules are not the same for things in and out.

A system develops **an internal language**. You know, your famous
"business domain", or even just your work expert vocabulary --- the
words that the outer world describes as "jargon" or "gibberish" most of
the time. This internal language makes intra-system communications full
of conventions, assumptions, non-obvious self-consistency. In exchange,
your intra-system communications can be more precise and efficient.

Making **explicit** the **boundaries** of your system make it clear
where you are allowed to use that internal language, and where you need
to give more context, or even adapt to a common, less efficient but more
broadly understood language.

Teachers talk to each other with pedagogical terms but they use common
words to talk to parents. Alice' Band has its private jokes and
references which differ from Gus Band, but both agreed on a common,
colorful language when they play together. And so on.

### ... interacting with other systems 

These explicit boundaries also make apparent how all systems interact
with each other.

Most of the time, you will be surprised by how much entangled systems
are in reality, and how naive your circles were --- that's good ! You
are learning about the topic at hand, and what you are starting to see
are **interfaces** and communication **protocols**.

**Interfaces**

**Interfaces** are gates in the boundary of a system. They are places
that other systems use to interact with your system --- identified
points of contact.

The fewer gates there are, the easier it is for a system to evolve and
change without impacting other systems. It's something very well-known
in code, where we have entire books explaining that modules should hide
their internal state. But actually, they just need to expose few
interfaces, hiding internal state is just a consequence of that.

**Protocols**

Interfaces per se are not useful. They take flesh once you know how to
use them to talk to the system, and what you get in return. We, experts,
call that chating. Sorry, a **protocol**.

## Promises and error modes 

Once you have an identified bounded system that can be contacted at
interface points thanks to protocols... You will like to actually
interact with the system, and you will expect some kind of behaviour
from it: the system make **promises** to the outer world about what it
will do. Promises can be kept --- it's the nominal case in a working
ecosystem --- , or not --- and that's an error.

Protocols and interfaces help to encode these promises in a way that is
useful for the other systems which want to interact with the firt one.
They describe:

-   [where you need to ask something,]
-   [what kinds of interactions will be processed,]
-   [what kinds of returns can be expected,]
-   [and what errors can happen along the way.]

And so you have an ecosystem interacting by protocol through interfaces.

{{< figure
src="https://cdn-images-1.medium.com/max/800/0*F4_4YgivDPirkDLI"
title="Promises on behavior is shared with protocols using interfaces"
>}}

Nothing surprising in a digital world actually built upon these
principles.

But you can use it on more down to earth systems, to better understand
how the parts interact and what are the protocoles. Again, drawing the
lines and putting the tags is what will make you discover the studied
world, and confronting your lines with others will make you understand
it: you will most likely disagree on where are the interfaces and what
are the correct protocols.

See, in the following example, what happens if Charlie is in Deborah's
class, contrary to the three others?

{{< figure
src="https://cdn-images-1.medium.com/max/800/0*wJlVP2uFsQ07oBGU"
title="Systems, protocol and interfaces don’t need to formally defined to share understanding of the world"
>}}

### Systems are fractal 

Systems can be composed of subsystems. Or be part of macro-systems. You
adapt the granularity to the problem at hand and zoom as needed.

Our school is its own system in the world, with its own interfaces to
other systems like the local administrations, its ministry, parents,
etc. You could zoom out to study the town as a system and better
understand what the place of the school is, or you can zoom in Alice's
Band inner complicated relationships.

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*uA2QLnmvibzzDEBfKqIsvA.png"
title="Zoom in and out of system to study different levels of interaction."
>}}

## Systems are rooted in a world 

One last thing: interacting systems are rooted in a world. So you have a
virtual horizon to your ecosystem beside which nothing useful happens
for that model of the world.

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*oSB42yfsp8UWYYKsNHUXTw.png"
title="Systems are rooted in a world."
>}}

That doesn't mean it doesn't exist, just that you don't want to consider
it in your model. And actually, if something from beyond that horizon is
important... It's part of your ecosystem, and you need to understand its
interaction. It isn't a contradiction with the previous fractal part
either: when you chose a level, you also choose to exclude what is
considered irrelevant for your eco-system at that level. Again, this is
part of being a mostly wrong model and not the reallity.

This horizon is extremely useful because it allows defining three modes
of interaction for systems:

-   [The nominal case, when an interaction went as expected for both
    parts.]
-   [The error mode, when something \*expected\* went wrong.]
-   [The failure mode, when something \*unexpected\* (i.e. beyond our
    horizon) happened.]

In our school example, we could have:

-   [nominal case: children are in school during break, they play marble
    and have some fun.]
-   [error mode: children are in school during break, they play marble,
    start a fight and their parents get called.]
-   [failure: in the morning, it's snowing a lot. Children can't go to
    school, all adults panic.]

Or perhaps that last case should be an expected error mode? It's a snowy
region, and the city is used to that. There is a special public service
that will take care of the children whom parents can't get a day off
---but most can, because remote is expected in that situation.

Well, you see: thinking in systems is useful. Now you know that you
decide what the expected errors are, and what is an unexpected failure.
It's the same in your code. You want to know what your world hypothesis
are and what events need to be considered to be fatal for your
application.

For example, in Java, most people consider the memory management as
beeing out of their world. In case of a memory allocation failure (the
famous "OutOfMemoryError"), you just have to terminate your application,
because you switched to an inconsistant state, out of your understanding
of your model. But in some rare cases, it's totally legit to draw lines
around a part of the code and to expect that that part may throw that
error (for example when loading a Big Thing in memory), with a recovery
scheme (when Thing is Too Big).

In economics, they call the things happening beyond your model horizan
[*externalities*](https://en.wikipedia.org/wiki/Externality){.markup--anchor
.markup--p-anchor data-href="https://en.wikipedia.org/wiki/Externality"
rel="noopener" target="_blank"}. Earth ecosystem is such an externality,
and we are just now noticing that perhaps we don't like the failure mode
going with that one, so we are starting to *internalise* it, i.e.
integrate it in our humanity models.


------------------------------------------------------------------------

## Systems: tentative definition 

{{< figure
src="https://cdn-images-1.medium.com/max/800/0*BTkoUbt7fZaayV3l"
title="Where to put the bounds?"
>}}

So, now that we have a good grasp of what I call interacting system
models, let's try to reach an actionable definition of *systems*:

**1/ Systems are useful, mostly wrong exploration models used to talk
about something.**

-   [Modelling interacting entities with systems is done to help you
    understand what the contracts between these entities are, what the
    hard links and the loose connections are, what the expectation of
    the parts are and how they interact. If it's not useful and you
    don't learn, you missed the point.]
-   [Systems don't need to be right. It's more interesting to have a
    simple system definition with clear boundaries allowing sharing
    ideas that one with thousands of interfaces that nobody can talk
    about.]
-   [Systems are interesting as a visual exploration and communication
    tool. So share them, discuss them, iterate to make them less
    wrong.]

**2/ Systems are entities**.

They have:

-   [**Bounds**. Think about these bounds, and why you want to put them
    there.]
-   [A **name**, so that you can talk about them. If a system model is
    well shared, other people should know what you are talking about
    when you use the chosen name.]
-   [**Persistence**. It lives for some time --- sufficiently so that
    you want to understand it.]
-   [An **internal language.** It's all the concepts and vocabulary used
    internally and accepted as an ever-present context to talk
    efficiently (precisely and succinctly). That language can use
    internal reference, made-up words, and is generally impenetrable for
    other systems. When you cross the system bounds, you need to adapt
    to a common language.]

**3/ Systems are interconnected.**

-   [They make **promises about their behaviour**, i.e. you can know
    what to expect from that system when you interact with it,
    especially what a nominal interaction is and what the error modes
    are.]
-   [They **talk** to each other **through interfaces**. Interfaces are
    access points for other systems. The clearer interfaces are defined
    and stable upon time, the easier it is to interact with a
    system.]
-   [They **use protocols for communication**, which is the way they
    will react to interactions coming through their interfaces. Like for
    interfaces, the clearer protocols are defined and stable upon time,
    the easier it is to interact with that system. The protocol use a
    **common language** undertood by all interacting systems.]

**4/ Systems are fractal.**

-   [Systems are composed of subsystems, and vice versa.]
-   [The granularity is up to you!]

**5/ Systems are rooted in a bounded world.**

-   [Besides that horizon nothing exists.]
-   [And if something from the outer world does have consequences on
    your system, you have only two choices: either that something should
    be part of your model (see, mostly wrong: iterate!), or it means
    that your system just switched to an unrecoverable / undefined
    failure mode: time to reboot it, or panic.]

Thus, systems have 3 modes:

-   [Nominal behaviour.]
-   [Expected errors (and corresponding reactions).]
-   [Failure modes (and undefined states).]

## That's all! 

So, next time you are faced with a situation which seems complicated,
with lots of moving parts, try to draw boundaries and ask yourself how
the parts are connected, what they expect and promise, what are their
internal language and if it leaks.

And if you are interested in much more formalized models of the world as
systems, you can look at:

-   [[Simon Wardley
    maps](https://medium.com/wardleymaps){.markup--anchor
    .markup--li-anchor data-href="https://medium.com/wardleymaps"
    target="_blank"}, which study evolving systems and what agency you
    can have on/in them,]
-   [Mark Burgess [promise
    theory](http://markburgess.org/TIpromises.html){.markup--anchor
    .markup--li-anchor
    data-href="http://markburgess.org/TIpromises.html" rel="noopener"
    target="_blank"}, and especially "[In Search of
    Certainty](http://markburgess.org/certainty.html){.markup--anchor
    .markup--li-anchor data-href="http://markburgess.org/certainty.html"
    rel="noopener" target="_blank"}", which is a formalized study of
    interacting systems at different scales.]

And there is certainly many more! You can look at that [wikipedia page I
linked](https://en.wikipedia.org/wiki/Systems_theory){.markup--anchor
.markup--p-anchor
data-href="https://en.wikipedia.org/wiki/Systems_theory" rel="noopener"
target="_blank"} at the begining, it's not that complicated :)

