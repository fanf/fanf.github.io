---
title: "Stay Up"
date: 2019-01-14T00:00:00Z
draft: false
---

### Journey of a Free Software Company 

***One decade in search for a sustainable model***

In mid-November, Nicolas Vérité called for an interesting track for
Paris Open Source Submit conference three weeks later.


{{< figure src="tweet-nyconyco.png" title="Call for open-source companies">}}


And well, Normation, the company I co-founded almost 10 years ago,
fitted quite correctly the description. We are located in Paris. We are
the publisher of the free software Rudder. And we went through an
incubator, met Venture Capitalists (VCs) for fundraising, and well,
people generally describe us as a startup. So, quite naively, I answered
the call.

Ten years is a long time at startup scale. We did a lot of things wrong,
and some others in hindsight were very good. We certainly had some
stories to talk about... For example, the business model. Finding a
business model is always hard (at least I comfort myself thinking so),
but a free software business model is a horror from the deepest abyss.
Look, you chose to put « free » in the place where normally one puts
« extremely lucrative licenses and captive users ». A bit strange.

I shared the idea with Nicolas, and unfortunately for me, he found it
very good. Unfortunately, because the subject matters a lot for me, and
I wanted to give it the time and care it deserves. And also because it
was supposed to do the talk in 15 minutes, and I had **many** more
things to tell. Long story short, my main flaw is my slowness --- or is
it may be my fear to speak in public --- and I spent the major share of
the next week's working on that talk.

Once given, feedbacks about the talk were extremely good and attendees
told me that there were important topics in it, around the idea of
sustainability, about what it means to start a company, and about free
software. In the better spirit of devops and free software, I had no
real choice but to share it. So here is a transcript of the talk I gave
on the 6th of December for Paris Open Source Submit :

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*mS7NV6yO0mkJ6wZQMVkjTg.png"
>}}

Let met tell you our story...

### Once Upon A Time... 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*Jx8mT1gUkC47rD83qfk50Q.png"
>}}

Ten years ago, we told each other that we could do better than that.
Better than the catastrophic human management and short sight view of
consulting companies which used to employ us. Better than proprietary
editors, with their habit to extract a ton of value and give back very
little in return. Better than all the people who missed the ongoing
disruption in IT management that was the rise of cloud computing and the
explosion of the number of virtual machines.

We decided to create Normation, our company. Today, I took the time to
look behind me the path we wandered along. Of course that's our own
experience, but I'm sure I can share with you some of our learning.

#### The Journey 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*D29KcTr6rcphn-Di-V0Tfw.png"
>}}

As that talk is a very short 15 min format, I chose four important
cases, almost caricatural in the life of a startup. I will be brief and
miss some shades but please come to ask me for any questions after the
talk. We will look at :

-   [the beginning of the adventure, and the founding team,]
-   [the incubation phase,]
-   [our meeting with VCs,]
-   [and the building of a business model.]

As I said, classical to exaggeration. But as it took us 10 years to
understand them, perhaps there's some value to share what we found. By
the way, don't wait for The Next Big Truth from me. I can only provide
feedback from our experience.

So let's start the journey... by the end, from today.

#### Hello! 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*ZK42gSokPOQDUjigk__I_Q.png"
>}}

Oh sorry, I forgot to tell you who I am! I'm François, cofounder of
Normation and CTO of Rudder. I learned about Free Software before
knowing how a computer worked --- in fact, I became a developer because
of free software. The idea of expanding knowledge, building new things
while standing on the shoulders of our predecessors... That was exactly
the bigger vision I was looking for when I was a student. Today, I'm
mostly known in the Scala ecosystem that I've been haunting for 12
years.

Normation, our company, has existed for 10 years. The co-founders were
already quite involved in Free Software when it happened and still
today, we try to be good citizen of the ecosystem. From a business point
of view, we wanted to change things in the ops world. We were present at
the beginning of the devops movement in Belgium 10 years ago. We
organized devops days in Paris the following years and we continued with
[*devops REX*](http://www.devopsrex.fr/).

We are the software engineers of Rudder, one of the main IT [continuous
and auditing configuration
solutions](https://www.rudder.io/en/).
As of today, it is deployed on tens of thousands of servers in a whole
range of companies from big to small, from banking to life-critical
environments to check and ensure that there's not drift between the
server configuration system operator would like to have and the actual
configuration present on servers.

During the trip, in addition to the amazing feedback devops REX got or
the trust we build with our users and our customers, we collected quite
a lot of labels, like "Young Innovating Company" when we were still
actually a young company, "Innovating Company of Systematic Cluster,"
and lots of others. But even with all these successes, **we are barely a
startup. We didn't do any fundraising. We don't have hypergrowth**.

#### Conventions 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*76_w-t5QPeJyUvGo4SP0Pw.png"
>}}

But just before going further on, I use some colour code in the
following slides:

-   [Green for our starting idea or question,]
-   [Black for all the mess we discover in the way of implementing
    it,]
-   [And blue for the learning we got from that experience.]

Let's come back to the business model...

### In Search For A Business Model 

Exactly like any startup, we did have some pain to find a working
business model. Actually, our search for a business model could be a
journey story by itself.

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*rpT_JePTmFDilUbI0yFCVA.png"
>}}


When I use the term "journey", I have something like the Odyssey of
Ulysse in mind, not exactly the cool trip for Sunday lunch at parents'
home. So you may wonder, "why was it so hard for us to find a working
business model?"

#### Wishful Thinking 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*OvLsXC6UqdIVIpdATIFb-w.png"
>}}

Perhaps we were a little bit naive. We put on our shoulders a lot of
constraints. Obviously, we wanted to build a profitable business model
to ensure the sustainability of our company. We also wanted to be an
exemplary citizen of the free software ecosystem and durably contribute
to its thriving. We wanted to let everybody get the same user
experience, be they a simple user or a big company --- no proprietary UI
for us! And we wanted to democratize continuous configuration with an
affordable (both by price and by accessibility) software.

We thought that the best fit for that set of constraints was a "support"
business model, where the software will be totally Libre (ie we wanted
to ensure freedom to run, study, redistribute and improve it), and we
will sell insurance to enterprises with a professional support contract.

#### It's Complicated 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*SCyUdCZOSjUNEOBIWENXGw.png"
>}}

We quickly found that the plan wasn't going on as well as expected. Now
we understand that there were three blocking factors for it to succeed.

1.  [Our selling model was just plain too complex. It was accurate.
    Extremely accurate. And fair. But we discovered that most
    enterprises don't want accuracy in price models, they want
    simplicity. We lost a lot of leads because of that.]
2.  [And it was just too hard to repeat a sale. We spent so much time
    transforming a lead into a client, understanding all the subtilities
    of his use case and explaining how our product was a perfect match.
    That was good for some key big corporations, but what we needed at
    that time was more a large base of clients to test for adjustment
    and build resilience.]
3.  [And lastly, we were living in a big inconsistent mess
    where:]

-   [the support plan was bringing money, but we spend very little time
    on it, and that time was experienced as a loss,]
-   [whereas we spent most of our time building the product and its
    roadmap, a long-term value for Rudder, without being directly paid
    for that,]
-   [and finally, most of our customers weren't even wanting to pay for
    what we had to propose. They didn't want professional support --- we
    even had some of the maybe-clients asking us to just sell something
    that they can show to their boss, whatever it was!]

On that last point, there's that quote from Marten Mickos, the past CEO
of MySQL.

> When you sell, it's never a problem of selling to the person you're
> selling to; it's that person who has to go up to the budget boss and
> say, "Boss, I just paid \$50,000 for something I could have gotten
> free of charge." You can't do that.

This is the best solution to alienate your supporting users against you!
We needed to go back to the drawing board.

#### Simpler And Sustainable 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*aWTeL1eg-FgVQAJO1wLOwQ.png"
>}}

We asked our customers what their real pain points were, and what they
wanted to pay for. Oh, and for a change, we listened to their answers.
We looked where we spent time cooking the long-term value for our
company. Answers to these questions were "features and maintenance".

We also decided to choose our battles. We accepted that putting some
enterprisey features behind a paywall didn't paint us as bad citizens of
the Free Software World. Quite the contrary in fact, because it allowed
us to build a growing, sustainable business model without letting go our
core values and so it allows us to contribute back in the long term to
that ecosystem. Plus it had the nice side effect to sort out actors who
were there only for the free lunch without any will to contribute back
anything, not even money.

Finally, we also simplified a lot the selling formula. Now, it takes
only two numbers to explain it, and really, you don't want it to be any
more complex. The big boss in big companies will always see your B2B
product as a cost per unit of something, whatever you try to teach them.

### Fundraising. Or Not? 

And as we are talking about big money...

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*gzuaar9dvty_8X8mTXTkWQ.png"
>}}

Let's talk about VCs.

#### Be A Real Start-Up! 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*7nPvnp1mGe0oRXTyvkErsg.png"
>}}

You know, there's that proverbial wisdom which asserts than **YOU HAVE
TO RAISE FUNDS**. And to be crystal clear, your success will be weighed
up **only** from the standpoint of your fundraising. Did you ever hear
about companies with a sanely growing turnover coming from a sustainable
business model year after year? Absolutely not! You heard about the
biggest, wildest fundraising of the year! So we took up our pilgrims'
staffs and started a round of the Parisian VCs.

#### Meeting the VCs 

Do you know what a VC looks like?

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*bwl4VM24kfOaeqcJdjrj1Q.png"
>}}

That's a VC. Smart and old and sat on all the gold you are yearning for.
Not the least to say that we were a little bit intimidated. And soon, we
understood something fundamental about VCs.

#### VCs Faustian Bargain 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*sLPifw9ggWIKrdpL__gUnA.png"
>}}

A VC offers you a contract: he gives you money to *accelerate* a proven
business model. He gives you that money with the goal to get it back
*ten times*. And for that, there's a *deadline*. You have 3 years.

The VC need to optimize the evolution of your company on the *valuation*
axe, because it's *valuation* which is used after the fateful three
years to, well, value your company to sell it to a bigger fish, or when
you need another fundraising or try an IPO. Actually, it's the only
metrics of importance for him. So the goal of a VC is the *hyper-growth*
of the "valuation" metric, and he will do everything he can so that you
are focused on that metric only. Even if it means that other parts of
the company, perhaps important parts for you like company culture,
suffer from that focus.

Also, never forget that the VC can and will ask for a lot: he is on his
own ground here, in a position of strength. He sees companies like yours
every days --- that's actually his job! He has the experience, and he
has the money.

#### Your Rules! Stay Up! 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*n-E9fwGjeSE7B5W832CKQQ.png"
>}}

We learned a lot during these meetings. For a start, we learn that you
never ever go to see VCs if you can't tell them: "I don't need you. At
all. But with your money I can go faster". We also learned, or learned
again, that *you* define the rules. It's *your* company. There is no
preordained path and you can live without VCs if you choose so. We
decided that the proposed contract was in total contradiction with our
core values, with what we were trying to build with Rudder. We didn't go
ahead with the process.

In hindsight, it's around that time that we understood that we weren't
really a startup. We don't really share any of their characterizing
traits. In fact, we are more likely a "*stay-up*", to steal a term from
Aral Balkan, i.e. a sustainable business with no exit deadline. Oh, and
by the way, if you don't know who Aral Balkan is, please take 5 minutes
to read what he has [to tell about privacy in the digital
world](https://ar.al/notes/the-nature-of-the-self-in-the-digital-age/).

### **Advisors And Incubators** 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*ubp6fw4FmKUUx1LYRIrxKA.png"
>}}

Of course, taking such a decision with such implications was a big deal
for us. We didn't do that alone. We got advice from our coaches. We
started getting advised by coach thanks to an incubator.

#### Step One: Create Company. Step 2: ? 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*qnmZXIYujSd2oL_zwtQ2hQ.png"
>}}

During the project of starting a company, there's that moment when you
did it. You actually created a company. But in hindsight starting a
company, having a business idea... These are the easy parts. The real
question is "what's next?"

#### Tyrany Of The Daily Work 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*C7bx2eql062YoxSZt__euA.png"
>}}

Just after your company creation, you're going to learn that you have a
lot of things to manage, most of them extremely urgent, and for some you
didn't even know these things existed five minutes ago. You will need a
certified accountant. A lawyer. Write a shareholders' agreement --- you
will wonder, "what's that? And why I even need such a thing, the team is
rock solid!". And actually, you will spend most of your time discovering
new things to do. New decisions to take, some of them really hard.
Without any perspective. Quickly. And without knowing what is the
classical solution to these problems.

All that activity may distract you from taking care of the "long time"
of your company. You may end up in a situation where you say, "oops,
that's a very good strategic question, and I should have prepared for it
6 months ago. Now, I don't have much choice."

And all of that when you don't even have the good social networks --- we
didn't have them to get our entry tickets to the Tour of Parisian VCs.

#### Get Advisors 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*do_smRUHDNg6o2UL6dFnFw.png"
>}}

Because all of that, just **Get Advisors**! Find coaches, people who
know what you live. But --- and that's the most important part --- they
must not have a DIRECT link in your company: not be a shareholder, not
be on board. They need to have a benevolent feeling with regard to your
adventure. They will help you with insights for the classical answers
about operational problems. But of course, that's not their main role.
They will help you take a step back, even kick your ass so that you take
a step back, and force you to stop and think about important, strategic
matters. And they can help you open some doors with their networks.

We discovered the huge gift that such advisors are when we were in an
incubator. And clearly, we won't still be there without the incubator.
But just to be extremely clear: the value of an incubator lies in the
advisors it puts on your path. Not the cheap, noisy open space, the
crappy wifi or the one-size-never-fit-any contract templates.

### Founding Team And Mission 

We are coming to the last part of our trip, the beginning of the
journey.

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*Uf_JESMcwJV5Qj84sqzQKw.png"
>}}

#### We Can Do Better 

The beginning of the journey... Do you remember?

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*snIfmbm9XbWrQR-4LYRV8w.png"
>}}

You know, there was that founding assessment. "We can do better than
that." Most of the time, you are not alone on that analysis. You shared
the thinking with friends or colleagues. And you know that with the
team, a diverse team, you will go farther. So you talk, and then a goal,
a mission emerges.

Our mission had a triple goal:

-   [Build a sustainable Libre software ;]
-   [Ease the disrupting shift brought by virtual machines and the
    cloud, especially for everyone who can't afford to work full time on
    that;]
-   [And build a trusting work space where people can grow and be at
    ease --- that one was in counterpoint of our past work
    experience.]

#### ​Cohesion? 

But then, there's that question.

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*mmo7F_t4aWDL7bCdlaD5pA.png"
>}}

How to know --- or at least, to be reassured that --- the founding team
will be able to pass the first stress test? The tenth?

You **will** have a lot of hard time. Is there some way to check if
these hard times will make the team explode in all directions?

#### Agree On Your View Of The World 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*QISysXyK4-zhfiB9GS5tRA.png"
>}}

In our case, I believe it was one of the things we handle with care and
some success. We took the time to verbalize, in length, our deep
motivation. What we instinctively find normal or shocking, what
energizes us and what makes us feel crap, where is our comfort zone and
what terrifies us. We took the time to assess what the consequences of
these traits were. What our strengths and weaknesses will be. And most
importantly, we let emerged a deep, strong alignment between us on some
core values --- not bullshit words like "we value innovation" (who
doesn't in a startup?), but how we see the world.

Alignment is a powerful asset. It allows you to rely on a fixed
direction, acts as a beacon when a crisis will occur. And most likely,
without the coherency brought by it, the team will explode. Be careful!
I'm not saying that you mustn't have diversity, not at all, quite the
contrary! But you must agree on some core values, some truth wholly
accepted by all team members. And in the same idea, I don't tell you
that there's "good" and "bad" values. What is important here, it's that
you were able to agree on them, to share them, to understand some of the
consequences of these values for your future company. You need to be
able to look back at your younger self in 1, 3, 5 years and be at peace
with these values, even if you grew up and your values with you.

In our case, we knew that free software will have a central place in our
company. And we foresee that it may lead to some complication in our
business model.

And it's how we started our trip.

### **Burn Out** 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*lDe5gawLA_b_zYjEaQHO3g.png"
>}}

You see, and long, hard trip. And of course, there's something missing.
You can't have an initiatory trip without an arch enemy. And that arch
enemy, like in all initiatory trip...

#### You 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*ucI4zQiWoE4sIyE95NmZdw.png"
>}}

That enemy, it's you. You decided that you "can do better than that".
That you were ready to give the best of you to show the world that you
can actually do better. But the problem is that there are always ten
million things to do. And some of them will go awfully badly. And a fair
part of them will just be extremely boring and necessary. And you can
get so tired. And disheartened. And actually, you're not a superhero. Be
careful about depression, or even burnout.

#### Hope It Helps 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*7B4Fa-eBJkPsnJOryZtNxw.png"
>}}

Of course we don't have a miracle solution. We would be sharing it to
everybody if it was the case. But unfortunately, we have some experience
on that topic, and so there's our feedback.​

First off, try to prevent burnout. And what we learn can help a lot in
that regard is to be **dispensable**. No, not useless, quite the
contrary actually. Being dispensable means that you reached the point
where you can shift from a task to another one which required you full
dedication, and you can do it knowing that nothing will break. That the
world will continue to spin. That someone will take your place and know
what to do, and that actually he will have the tools to do it correctly.

Second point, you must learn to PRIORITIZE. There will always be too
many things to do. But you can, you must learn to choose what are the
ones you objectively chose to do, in what order. And accept that tasks
with lesser priority are less likely to be done. Choosing is the
important point, because what destroys your motivation is to believe
that you endure the arbitrariness of the world, that you have no agency.

​Finally, and it's the hardest, you need to share your knowledge, share
your priorities, and learn how to teach these two points to your whole
team. The goal is that everybody knows he is dispensable, and what are
the priorities of people. By sharing, you get feedback, which helps
reinforce dispensability and adjust priorities, lowering the level of
stress and setting common goals.

If you experience a burnout --- and I really hope you won't --- but if
so...

The first, hardest part is to accept that perhaps you're in such a
situation. It's hard, because remember, you are the doer, the builder of
things, people rely on you. You have quite an ego. In case you are
tired, you don't like to go to work any more... Please take 5 minutes to
do a quick online CBI self-evaluation test. It's 20 short questions, and
it's the first step toward recognition.

Then... Please, please find some help! Explain your situation to your
peers, to other founders so that you can build a plan together. But also
looks for help out of your company, for friends, or family. So that you
can freely share all you have in your heart.​

And finally, to really heal, you will need to find a way to take several
weeks away, far from what hurts you. You need that to be able to come
back later.

### **Our Journey: Learning** 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*FjUMySylUOut8CTO2-SNhQ.png"
>}}

There it is, that's our journey, until now. And we know that's just the
beginning, there's all these uncharted lands in front of us. We get to
them with all our learning... And if needed to only keep one these
learning, it would be learning to iterate on your learning. Because you
have to never forget running a company is before anything else learning
how to deal with new problems and solve them with your own approach.

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*o5y1ndXmvDbR2fbLveXhsg.png"
>}}

Ah, I've one more thing! Yes, I know, I find that cliffhanger amazing,
perhaps I should try to spread it, perhaps I should talk about to people
at Apple or something.

### Free Software Is Our Digital Common Goods 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*KZVJuAQEpbyqzengSn3WMQ.png"
>}}

Our journey was lifted by free software, and we only saw an extremely
little bit of the vast world. Software is more and more present in our
lives, and free software are the infrastructure of that new digital
world. So I have a last point to highlight.

#### Sustainability 

{{< figure
src="https://cdn-images-1.medium.com/max/800/1*WLmo4sxkb1bkrmAwVpd-Ng.png"
>}}

That digital infrastructure is our new digital common goods. They share
a lot with their physical cousins, and so we need to learn how to avoid
the tragedy of our digital common goods. We need to learn how to [build
and sustainably maintain these digital
infrastructures](https://www.youtube.com/watch?v=WImJnCQhutc).

Elinor Ostrom wrote a lot on the subject. Actually, she won a Nobel
Prize (yes yes, the Nobel Memorial Prize in Economic Sciences) for it.
The basis seems to be that... Everyone must care for a common good to
have it be sustainably managed.​

So everyone of us has a role to play in that game:

-   [States, which have to take the measure of their responsibility upon
    these common goods with regards to accessibility, promotion, support
    and maintenance.]
-   [Enterprises, who often behave in a parasitic way, extracting as
    much value as possible without contributing back a fair share of it,
    with the clear risk to kill the goose that laid the golden
    eggs.]
-   [FLOSS communities that are far from being exempt of problems and
    need to take care of social problems which devours them. I already
    talked about burnout, which is a common issue for project
    maintainers, but there others, like believing that FLOSS is a
    meritocracy when you are the deserving
    white-educated-rich-cis-man,]
-   [And, of course, there's us, the users, who need to learn to
    outreach the comfortable state of **software consumers** to become
    an **acting citizen** of our new digital world, each of us for what
    he can do.]

​Tragedy of the common is avoidable. There is [an alternate ending to
it](https://medium.com/@nayafia/an-alternate-ending-to-the-tragedy-of-the-commons-446b4e960887).

### **References and links** 

Slides in english:
[https://www.slideshare.net/normation/stay-up-journey-of-a-free-software-company](https://www.slideshare.net/normation/stay-up-journey-of-a-free-software-company)

Slides in french:
[https://www.slideshare.net/normation/stay-up-voyage-dun-diteur-de-logiciels-libres/](https://www.slideshare.net/normation/stay-up-voyage-dun-diteur-de-logiciels-libres/)

Tragedy of the commons, 50 years latter:
[http://conversableeconomist.blogspot.com/2018/12/tragedy-of-commons-50-years-later.html](http://conversableeconomist.blogspot.com/2018/12/tragedy-of-commons-50-years-later.html)

Some Trends in Open Source & the State of the Scala Center --- Heather
Miller:
[https://www.youtube.com/watch?v=WImJnCQhutc](https://www.youtube.com/watch?v=WImJnCQhutc)

Keys to turn your open source project into a business --- Marten Mickos,
past MySQL AB CEO:
[https://opensource.com/business/14/9/open-source-business-models-part-2](https://opensource.com/business/14/9/open-source-business-models-part-2)

#### Credits 

Smaug painting:
[https://alpha.wallhaven.cc/wallpaper/127439](https://alpha.wallhaven.cc/wallpaper/127439)

"Building a World" world map:
[http://www.twcenter.net/forums/showthread.php?605421-BAW-Chapter-1-The-Map](http://www.twcenter.net/forums/showthread.php?605421-BAW-Chapter-1-The-Map)

A lot of pictures were found without reference to author or
copyrights... If you are the author of one of them, please let me know
what you want to do (quote your name/site, remove it...)
