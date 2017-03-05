---
layout: default
title: Fact and folklore in software engineering
---

** See [this](http://leanpub.com/leprechauns) instead. I no longer stand by this article, and the book offers a much improved version of the critique. **

# Fact and folklore in software engineering

The trouble with opinions is that everyone has their own; you can always find one to suit any given prejudice. "Test-driven development reduces defect count", says one expert; "test-driven development will wreck your architecture", says the next.

Knowledge cannot be disseminated merely by everyone having a blog of their own. Blogs are great for voicing opinions - are they ever - and for having debates, but it's unhealthy for debate to go on forever. We look to scientists for settling them.

One debate (if it can be called that) which has gone on for too long without a satisfactory resolution concerns programmer productivity and the often quoted "observation" or "fact" that the best programmers are 10 times better than the worst. I will come back to the origins of this observation, but it isn't quite the topic of this article.

This article is about why some "facts" refuse to die, and about how to avoid being fooled by opinion disguised as scientific "fact". We start, therefore, with some observations on science and facts.

## The messy workings of scientific discourse

Bruno Latour is one of the keenest observers I know of the work that scientists really do, and one of the most punctilious in clearing away the myths and misconceptions about how science is in fact done. I have found good use in some of the tools he created to assess the status of an *ongoing* debate about a matter that falls within the purview of science, one that hasn't been settled - what he calls a [controversy](http://www.demoscience.org/).

(I stumbled across Latour when someone recommended [Aramis](http://en.wikipedia.org/wiki/Aramis,_or_the_Love_of_Technology), a book which thoroughly changed the way I saw and thought about software projects, even though its subject is public transportation. I have been recommending it ever since to colleagues and friends involved in software in any capacity; it ranks near the top of my list of must-read books for the profession. It's remarkable not just for Latour's determined and meticulous manner of observation and of getting to the bottom of things, it also reads like a detective story.)

Latour draws attention in particular to the role of [**modality**](http://en.wikipedia.org/wiki/Linguistic_modality) in scientific discourse. The concept has complicated ramifications but is really simple at its core, as we'll see by walking through an example. Start with a statement of fact, such as "water boils at 100 degrees celsius". A modality is a way to alter the meaning of this statement, not by modifying but by extending it: "if I remember right, water boils at 100 degrees celsius" expresses uncertainty, whereas "everyone knows that water boils at 100 degrees celsius" implies authority. "Scientists know that water boils at 100 degrees celsius" lends a somewhat different authority to the same statement, implying that knowledge of it may be restricted to a select few.

In the practice of science, a **publication** takes on the role of an extended modality. A researcher may wish to state a conclusion: "water boils at 100 degrees celsius". Convention dictates that he should initially add various hedges to his conclusion: "subject to the threats to validity mentioned above, given our results it seems legitimate to claim that the boiling point of H2O under the experimental conditions lies, for a 95% confidence interval, within 0.01 of a 100 degrees celsius". The rest of the publication (or "paper") amplifies these precautions.

A lone experiment or study rarely being sufficient to establish a scientific fact, further "papers" are expected to build on an initial work, whether by the original author or by other researchers. One prerequisite is that the initial work be *interesting*; that often serves as a first filter, and probably a fair fraction of all scientific work is never cited by other researchers. Thus, **citations** play a crucial role in the acquisition by some statement of the status of a "scientific fact".

Now you can think of a citation as being itself a modality, one that can express a
degree of confidence: "Preliminary work by Jones (2001) suggests that the boiling point of water is 100 degrees celsius. We present a replication with slightly different equipment leading to conclusions which confirm the earlier result". The accumulation of citations of a given paper is often a measure of its importance, and if the statement is eventually confirmed the pattern of citations will also serve to establish **priority**.

What Latour has highlighted is the **pattern of progressive erosion, and eventual disappearance, of modalities as a statement becomes established as a fact in the sciences**. For instance, the next step might read as follows: "Numerous studies (Jones 2001, Smith 2002, Jones 2003, Bogdanoff 2010) have shown that the boiling point of water is around 100 degrees celsius, with minor variation; we show how this value depends on atmospheric pressure". Further still, one might read "it has been established that pure water boils at 100 degrees celsius; we investigate the effect of adjunction of various concentrations of salt in water".

At the endpoint of this process of acceptance of a fact, it becomes stripped of all modalities ("waters boils at 100 degrees celsius"), but even more importantly it becomes operant in producing further knowledge, or technical effects instrumental in the production of knowledge: "to ensure a temperature of 100 degrees in our experiment we bring water to a boil". (For a more realistic example of this transformation happening to actual scientific facts, see Latour and Woolgar's [Laboratory Life](http://en.wikipedia.org/wiki/Laboratory_Life).)

Obviously, what makes this scheme of citations a process properly called scientific is its empirical and conversational character; the erosion of modalities is not inexorable, a widely cited preliminary study may well be overturned by later work.

Another possibility is that the initial statement, the claimed "fact", never quite rids itself of all modalities. It remains spoiled by hedges and suspicions, and if no one can muster enough interest to follow it up in further publications, it may simply be forgotten. In the best case, that is - for in the worst case it may also persist in the collective discourse as **folklore**, myth or [misconception](http://en.wikipedia.org/wiki/List_of_common_misconceptions#Science).

## So what is known about programmer productivity?

We can now circle back to this widely circulated "fact" of the software profession, according to which "programmer productivity varies by a factor of 10 (or 5, or 20) between the best and worst individuals". This is a remarkable statement, not least because of its implications: for instance, programmer compensation does not vary accordingly.

Another arresting fact is the age of this statement. Interestingly enough, what seems to be the [first study](http://portal.acm.org/citation.cfm?id=362858) to mention this wide spread in productivity dates back to 1968 (not entirely coincidentally the year when [Software Engineering](http://confreaks.net/videos/282/) was born). It presents as a "true" scientific study (as opposed to an opinion piece or an essay), aiming initially to compare, under two experimental conditions, the performance of programmers facing... a **debugging** task. Time required for the programming part of the task are recorded during the study but aren't its main focus. The study finds a statistically significant difference between the two modes considered, "online" and "offline", with a slight effect on performance in favor of the first. The authors also note as a "surprising" observation the large magnitude of the disparity in scores obtained by the various subjects of the study, on several measures of performance.

The study rapidly came under fairly intense critical scrutiny, and we might expect that further studies attempted to confirm or reject the initial observations; leading, after over forty years of scientific activity, to a pattern conforming to Latour's observations as this became established as fact: erosion of the modalities, with attendant reduction into a bare "scientific fact".

That turns out not to be the case. Surprising as it may seem, **forty years** after the initial results, the statement still comes accompanied with its modalities. Nearly every time I've had occasion to come across this statement, it was under the form "**numerous studies have shown that** programmer productivity varies by a factor of 10 (or 5, or 20)" or some variation.

Not only has this statement not been stripped of modalities; more damningly this "fact" **has yet to yield instrumentally useful advice or applicable theoretical knowledge about programmer productivity**. There is no established manner of exploiting this remarkable "discovery", for instance through hiring criteria which would afford screening out "1x" programmers and giving preference to "2x to 10x" programmers. What we find in abundance is essays citing this "observation" in support of whatever opinion the author favors: "numerous studies show this, therefore you should heed my advice".

## How to cheat with citations

One of the better-researched pieces on this topic is Steve McConnell's ["The Origin of 10x"](http://forums.construx.com/blogs/stevemcc/archive/2008/03/27/productivity-variations-among-software-developers-and-teams-the-origin-of-quot-10x-quot.aspx). This essay was published in 2008 to explain the title of McConnell's blog "10x programming". McConnell acknowledges that the 1968 study came under harsh criticism but claims that its results have been confirmed:

> the general finding [...] has been confirmed by many other studies of professional programmers (Curtis 1981, Milss 1983, DeMarco and Lister 1985, Curtis et al. 1986, Card 1987, Boehm and Papaccio 1988, Valett and McGarry 1989, Boehm et al 2000).

What could be more scientific-sounding than this litany of citations? However, when we take a closer look we find that this "confirmation" is not as strong as it looks.

* the 1981 Curtis study included 60 programmers, which once again were dealing with a debugging rather than a programming task
* the 1986 Curtis article does not report on an empirical study, but is an essay calling for better integration of cognitive sciences within software engineering (with which I agree wholeheartedly, but which offers no support for the "10x" claim)
* the 1983 Mills citation refers to a book collecting various essays on the topic of programmer productivity, mostly experience reports and opinion pieces; none of which appears to report on a replication of the original study
* the 1985 DeMarco and Lister reference is similarly a book collecting essays; it is in fact the famous ["Peopleware"](http://www.amazon.com/Peopleware-Productive-Projects-Teams-Second/dp/0932633439), a landmark pamphlet denouncing a certain style of management by pressure which is unfortunately still in vogue today; the only "studies" reported on therein are the programming contests organized by the authors, which took place under loosely controlled conditions (participants were to tackle the exercises at their workplace and concurrently with their work as professional programmers), making the results hardly dependable
* the 1987 Card reference isn't an academic publication but an executive report by a private research institution, wherein a few tables of figures appear, none of which seem to directly bear on the "10x" claim
* the 1988 Boehm and Pappacio reference is a review of other publications on the topic of programmer productivity, and it cites only one which directly reiterates the "10x" claim; and that is... wait for it... the 1968 Sackman study!
* I have not been able to personally obtain and check out the 2000 Boehm reference, but it appears to be a book about COCOMO rather than an article reporting on an empirical study
* **Only one** in this long list of references seems to be related, albeit indirectly, to a study attempting to replicate the original finding; that is the 1989 Valett article, which reports on a 1982 study measuring productivity in terms of lines of code (something now frowned upon for good reason), and shows 1-to-8 ratios on "small" projects and 1-to-20 ratios on "large" projects, with the threshold at 20KLOC. What we have here is a citation of a citation, and thus almost no information about the 1982 study's methodology can be found in the 1989 article.

What is happening here is not pretty. I'm not accusing McConnell here of being a bad person. I **am** claiming that for whatever reasons he is here dressing up, in the trappings of scientific discourse, what is in fact an unsupported assertion meshing well with his favored opinion. McConnell is abusing the mechanism of scientific citation to lend authority to a claim which derives it only from a couple studies which can be at best described as "exploratory" (and at worst, maybe, as "discredited").

I have not done the equivalent critical work for the citations McConnell offers in support of the equivalent claims on between-team productivity variations. But "work" is the right term here: tracking down articles and sometimes entire books, some of them out of print, *just* to scan them for conclusions which turn out *not* to appear anywhere. It is a sad fact that **critical examination of ill-supported assertions takes a lot more time than making the assertions in the first place**; this asymmetry accounts for a lot of what is wrong with public perceptions of science in general, and possibly for the current state of our profession. At any rate the list above, I believe, is sufficient to make my point.

## Why is folklore so persistent?

The verdict seems clear: this supposed "scientific" observation on individual programmer productivity variations only deserves the name of **folklore**, unsubstantiated bits of opinion which are transmitted and kept alive for reasons more cultural than rational. I am most emphatically **not** claiming that **there aren't** variations in productivity of that order: I am only saying that this "fact" has not been demonstrated, and that as of today we do not know what to make of it even if it were true.

One reason for this unreasonable persistence is that we do not have a firm conceptual handle on the notion of "productivity", at least as it relates to what programmers do nowadays. Way back when, that used to be measured in terms of "lines of code per unit of time". The advent of "high level languages" caused researchers to question this measure of productivity, since you could now achieve the same functionality in fewer lines. There was an attempt to substitute Function Points instead, but they turned out to be complicated to use and they remained largely ignored by the profession. However, the more relevant question to ask is **what assumptions underlie the very notion of "productivity" in our field**.

For instance, should we assume (as seems reasonable in industrial contexts) that productivity could only be zero or greater? This is to ignore the (folkloric, but remarkable and provocative) notion of ["net negative productivity programmers":](http://www.software-thoughts.com/2009/08/net-negative-producing-programer.html), team members who not only do not contribute to a team's productivity but in fact *destroy* others'.

Do we clearly distinguish between *effort* and *outcomes* in our notions of productivity? A programmer may seem improductive because she doesn't appear to push out a lot of code, but that may be because she's busy thinking about a novel idea which results in the team *not having to code* some complex features, yielding great overall value.

An important concern in the social and cognitive sciences is [construct validity](http://en.wikipedia.org/wiki/Construct_validity). This aims to answer the question: does what we're measuring actually exist, and is it in fact reflected in the measurements we have chosen to make it quantifiable? (Take a look for instance at the Wikipedia article on [Psychometrics](http://en.wikipedia.org/wiki/Psychometrics).) Such questions seem seldom asked in our field.

## Leaving folklore behind

The 10x "observation" is referenced several times in McConnell's excellent 1996 book ["Rapid Development"](http://www.amazon.com/Rapid-Development-Taming-Software-Schedules/dp/1556159005), where the list of citations which accompanies it is nearly the same as in the above quote, with the addition of the "Boehm et al 2000" reference which is obviously posterior, and the "Boehm and Papaccio 1988" reference which does not show up in the book's bibliography. Also, the 2008 blog post has been reprinted with few changes as one chapter in the otherwise excellent 2010 book ["Making Software"](http://oreilly.com/catalog/9780596808303), a compliation of essays on empirical findings in software engineering.

I find it regrettable that the book's editors chose to include this particular essay. "Making Software" is one of the encouraging hints I have seen recently of what I hope is a growth trend for the years ahead: better and closer collaboration between the software engineering research community and a much broader base of software professionals than has been the case so far. The book ranges over varied topics from Agile to debugging to learning programming, but it is especially interesting for the first few chapters which make a strong case, aimed at software professionals, for learning the basics of scientific inquiry.

### Laurent Bossavit, Institut Agile

[Originally published](http://blog.institut-agile.fr/2010/11/folklore-ou-fait-scientifique-comment.html) on 11/1/2010, translated to English on 1/5/2011.

[I'm on Twitter. Drop me a line.](http://twitter.com/Morendil)

### Institut Agile

Institut Agile is a France-based independent organization funded by a consortium of businesses with a strategic interest in Agile approaches.

The goal of the Institute to raise the bar for business excellence in the software industry through Agile approaches.

Its missions include growing the Agile business ecosystem, creating stronger links between the business and research communities interested in Agile approaches, and providing stronger empirical evidence on the benefits of Agile practices (or lack thereof).
