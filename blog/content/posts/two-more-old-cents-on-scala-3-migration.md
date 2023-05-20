---
title: "Two More Old Cents on Scala 3 Migration"
date: 2023-05-20T22:55:57+02:00
draft: true
---

## Once upon a time, Scala 2

> Ed. (and TL;DR, likely) I really tried to just share our (my, mainly) sentiment and understanding  of the situation. I don't want that text to be some kind of rant, but more it to highlight **"Scala is a wonderful language, but the migration to Scala 3 does not work for us for these reasons. I hope it will, because I want Scala 3 to be a success story, and to share it"**. In case it get lost, get back here to read it again. Also, I hope I didn't over-generalized from our specific place (too much). Dear reader, don't forget I don't have much more experience than my own to share. I still hope it may be useful. 
 
 
There is a lot of chat recently around Scala 3 migration. We are directly impacted by that topic, and I wanted to share our experience on the subject, as one more anecdotal data point.

But some context before that. 

### Rudder, myself, Scala

We are very long time enterprise users of Scala. Long enough to have suggested Paul to chose ##. For the one who are not aware of such ancient and private lore, we are building our product [rudder.io](https://rudder.io), deployed to managed hundred of thousands of servers around the world in Scala since 2009. I personally discovered Scala around version 2.6. 

Even after all that time, I really, really love that language. Since I discovered it in 2007, Scala has always been the best language to express my ideas in code. And the Java ecosystem was a sound enough credibility anchor for `Real World App Where You Don't Need To Write Everything Yourself`. 

I really love (loved?) the community and ecosystem too, full of ideas and advancing the state of the Art - and that, despite its masochist willingness to splitting a tiny village into lots of antagonistic churches and the resulting internecine wars. And despite the fact that so many of the talented and oh so nice people got exhausted and chose to respire on greener grass, or at least out of blaming side of the code. These cost (emotional but also translated in direct loss of community size and capacity to do things) were not completely outbalancing the nice parts.

Beyond the personal love, Scala served us so very well. With a tiny team (like 3 people in a garage), we were able to evolve and **keep evolvable** an app that grew to more than several hundred thousands LoC of codes, with a complex public & private plugin architecture, and we were able to do one massive refactoring impacting more than 40% of the LoC every 30 months or so. Yeah, we learned a lot, and we were extremely wrong about all sort of things - but Scala allowed us to make errors, to correct them and keep code maintainable. 
We were happy to keep up to date with Scala release, which were more or less easy, but our use cases at language level were very simple (no type wizardry and macro on our own for ex). And things were getting better, even tooling and bincompat (if anybody remember eclipse in 2007, or binary breakage between patch release...). 

Moreover, Odersky leadership on Scala 2 found a balance that made Scala such an amazing, productive, versatile, language with a power so great that people are inventing the future of industrial functional programming tools and abstractions and putting it in prod along the way. OK, the balance was not often toward the boring mass usage crispation (like fast compilation time, amazing tooling UX, IDE...), but even in these parts, real efforts were made and resources were spent - not always successfully, but these problems were recognized and worked on. 

## Scala 3 disruption

Then, Scala 3 came along. 

People whose living was depending on Scala got a bit stressed out, because it was derived from dotty that was supposed to be a R&D compiler, and some of them were remembering the early days of Scala 2, and everyone had Python 3 horror migration in head because we were in the same same time frame (and yes everything not ancient has same time frame than Python because the 3 is number of decades it takes, but still, **Scala /3/, Python /3/**...).
And that even more so when the Scala team was keeping telling everyone it won't be like that. And actually, a lot of effort were put into avoiding some of the aspect of Python 3 migration, and we had a powerful type system to avoid some more of the pain. 

At some point, **the idea emerged that Scala 3 will be the last time ever that books will be rewritten for** (for the youngers among us, /book/ were things that we used to pass knowledge on dead trees before digital everything, they were very slow and costly to produce and distribute along, so you wanted to avoid changing things written on them - Yes I'm kidding and I know that books still need to be written, but it really felt like a scapegoat at the time, and even more in retrospective, especially since big features keep getting added in Scala 3). And so, huge amount of breaking changes - source and code - were tidy packed and started to pilling up. 

The fallacy has its own chain of logic that goes "Last time book will be rewritten" => "Need to get it right the first time" => "Accept ALL THE Changes - even if breaking source  without B plan".
The most notable of them was of course the spaced-based syntax. But their was a lot of others, like `enum`, `given`, but the biggest was the `macro` system. 

That broke a lot of things, and especially the trust of a lot of people that industrial usage of Scala was really important and not just a pretext to make a very good school language for learning advanced programming concepts. 


## Risk/costs for a small team

So, in that context, what does Scala 3 migration means for us, `rudder.io`?

There's 3 big aspects that prevent that migration thing to float for us. 

### 1/ Risk and direct cost of migration, iterating impossible

The migration is not easy at all for old code base with lots of dependencies. 

Actually, just trying to **understand the cost** is a project by itself, which need investing a fair amount of resources just to study the difficulty of the migration and if it is possible at all. Amazingly, we were helped by VirtuLabs on that, and they spent days on studying the migration and finding bugs and workaround - but that just points to a bigger problem : they **were needed**. We won't have been able to do it by ourselves in less than several weeks or months, loosing days each time a bug in `scalac` would have been thought to be one in our code (there was several, as you can see [in the PR](https://github.com/Normation/rudder/pull/4603).

This is a very clear cost. We are a very small team (nowadays 2.5 people on the Scala part).
Even if VirtuLabs helped on a big part of path, perhaps the 80% first percents, there's the remaining 80% where we go from *PoC to prod*, with all tedious little things to polish (plugins to port, workaround for the ecosystem mis-alignments, etc). 


The nature of Scala 3 also means that as of today, **we don't see how achieving source compatibility between Scala 2 and Scala 3 code would be possible**. There is so many differences in language structure (`enum`, `given`, etc), dependencies, linter, and of course macro.


That means that **it is impossible to iterate** to the point were the switch from Scala 2 to Scala 3 is just a compiler option. 

These has two main costs:

- one is that **there is a tension between completing the migration and changing code**: until the port is completed, we won't want to add new features or change too much existing code (like adding tests, correcting bug with the corresponding refactor, etc). Because each change means that the work on the port may be broken, and any new code will need to be ported

- the other is **the risk of death march fueled by sunk cost fallacy**. Such a migration means that at some point, you have a huge leap of faith: the migration must end. No more or, you spent to much on it. So you throw resources on it, and keep throwing until it's over. It's a bit like if Scala 3 forces every old users to pay the price of a worse practice (not iterating with small steps, controlled risk, and possibility to stop anytime) for something they didn't asked for.

With our team and the other things we have to do (like developing our product), paying that cost means that we need at least one more dev. Which won't be coding on feature for the product, but just one migration, for months. So for something without any business revenue to compensate. So we aren't exactly eager to do it for now.

### 2/ Overhead of maintenance

A major migration is a complex thing, and in our case it's worse because it's absolutely not a tipping point that we pass and then forget. I'm almost sure it's the same for most complex system and companies having lots of subsystems, but for us it's caricatural and so it's very easy to grasp : we have 2 years of maintenance on our on premise software, so we will have to maintain a version of Scala 2 code base along one of Scala 3, whatever the scenario for the migration. 

And to make things a bit more funny, we also always correct bug in the oldest maintained branch and then upmerge patches. So our dev regularly switch ten of times a day between these branches and the corresponding code. 

As of today, we don't see how achieving that would be possible without important difference in the code source and dependencies, leading to much more complexity in up merge, environment switch, etc. 

And even if we find ways, with directories for Scala 2 and Scala 3, macros, etc, it means that our build and maintenance complexity budget will be skyrocketing. 

So again, more people are needed to compensate those new cost.

I easily imagine that open source maintainer will quickly chose to abandon Scala 2 for these reasons. 

### 3/ Opportunity cost and gain balance

#### Gain

Really, I would love to have a long part on the gain, but they seem marginal. OK, it's a bit better everywhere, the language is much more consistent and mature, and if Scala 2 had been what Scala 3 is in 2006, it would have been **fabulous**. 

But as a disrupting evolution?

Where are the amazing gain that would make me want to pay for the cost ? Nothing amazing is there. We are not in a loom or Valhalla league. Previous migration of Scala had some very clear opportunity cost, even with the complex 2.8 migration - we earned a fabulous collection library, a macro system, an easier binary compat. 

But with that one, I'm not sure what I earn. Things like `enum` or `given` were already possible, like I think everything else. OK, `macro` are finally principled and good. OK, before everything was more clumsy, less nice. But for us, it doesn't look like it sustains its own disruption weight.

Oh, of course the migration earns the fact that we will be on a supported (by the ecosystem) version of Scala. And it's the first time I'm not sure this is enough. 

#### Costs

Because the cost is huge. 

I already explained the migration and maintenance cost, but others are pilling up. 

The tooling regressed 10y, the compiler is fragile again with new "won't fix" bugs, a part of the ecosystem is dying or flying away. And there will be a long lasting schism (already had for several years, and it look like it's just the beginning, the moment people **really** assess the migration and see the abyss). That includes the fact that we as an ecosystem are spending time on that question in place of doing amazing lib and app in Scala.

Plus, and more importantly, the trust budget was all spent. 

I tried during years to convinced myself that Scala was (very slowly) gaining nice tooling and reliability, that there was a place for R&D in a side compiler but that the company needs of stability, efficiency (hey, there was even work on a massively quicker compiler with hydra!) were heard, and then that last time book are written. And then new edgy things are added, with new big R&D project being worked on. Clearly, even the mirage of the possibility of a Scala 4 migration in the next 15 years make me sure that I won't choose Scala for anything but toy or personal projects. The risk is too high.

## On trust (in corporate settings)

I used the word "trust" several times. But trust is a complicated things. It's already complicated for a personal, 1 to 1, with immediate feedback loop, iterable setting with long term consequences, when you can choose who is the other. In more corporate set-up, I like to use the framework provided by "Feltman" *The Thin Book On Trust: An Essential Primer For Building Trust At Work**. It highlights **4 key components to build, or kill when missing, Trust**: 
  
  - **sincerity**, ie the assessment that you say what you mean and mean what you say,
  - **reliability**, ie the assessment that you meet the commitment you make, that you keep your promise, 
  - **competence**, ie the assessment to that you have the ability to do what your are doing or propose to do, 
  - **care**, the most important for long term trust, ie the assessment that you have the *other person's interests* as well as your own when you make decision and take action. 

With the help of that framework, I can assess that Martin Odersky has my trust for building an amazing language. But perhaps he misses the competence or reliability to make an ecosystem loved by industry, and it's how I explain my current distrust in Scala migration story.

Unfortunately, once trust is broken, it contaminates everything a person says, even in domains where trust was built, and it takes a long time to rebuild, more so than the first time it happened, like in an hysteresis where once you're on the lower branch, getting back to higher one needs a lot of energy.


## Toward a better balance?

So, at that point, there's two ways to change the balance (I really don't think it's a false dichotomy, and I would be happy if it was): either the gain get bigger (immensely so, that's not a linear scale, the minus weight more than the plus), or the cost decreases to the point where there's no threshold effect anymore.

### Bigger, free gains?

I don't see how to make the gain bigger without eroding even more the confidence of the ecosystem (**I'm extremely risk aware right now**). I would love to see it. But the only things I hear about like continuations and direct style are the opposite of that. They kind of validate the worse story about Scala being ever the same, forever. 

### Reimburse costs?

I very well see how to reduce the cost: 

- invest massively in restoring trust (not sure how, but at least saying that pain is heard and cared for is a start).
- making the transition from Scala 2 to 3 iterable and 0 risk, 
- make R&D happens - it's a need - but not as a liability for day to day use (jvm model works, other will likely so, too)
- and making Scala 3 loved by people using it not by passion, but because it's just the best tool for the job.

That last item encompasses long term stability and tooling performance and smoothness. 
 and that R&D will be done without impacting users (like in the jvm for ex, were it's just net benefits), make public announcement that the pain is heard and that people really care, and find ways to make the transition from 2 to 3 painless, and iterable. Perhaps by back porting some of the feature like enum/given. And certainly finding a way to be able to transition macro.

## Anecdotical hope

And don't even know if it will make the people switch to Scala 3. I don't even know if it's woth it.


Also, I understand how anecdotical that assessment is. I understand that Scala ecosystem is diverse even in its tiny size, and that I'm just but one voice in it. Even more so, I understand that I'm an old voice, and I have a bias against diruption, so that my anchor is in the conservative side of things for tech.

But I really like scala, I would love to see it transform a schism into a success story. I think it's still time, even if it needs to direct all available resources toward make the migration a nobrainer, and not adding new features to the language. 
