---
layout: post
title: Riemann and the Robot
date: 2026-11-24
description: Regarding the Claude "solution".
tags: [notes]
thumbnail: assets/img/1.jpg   # optional image on the card
---

So here we are: another “major breakthrough” in mathematics from another AI model. This time, it is Claude, from Anthropic.

To get straight to the point, what happened is that Levant Alpöge, a Turkish-North American mathematician from the Department of Mathematics at Harvard University, claims to have (probably) solved one of the *Millennium Prize Problems* : the Riemann Hypothesis, using a Claude AI model ([Alpöge, 2026](https://alpo.ge/remark.pdf)).

<div class="row justify-content-center mt-3 mb-3">
  <div class="col-sm-10">
    {% include figure.liquid loading="eager" path="assets/img/blog/post_1/img1.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
</div>

I would like to pause for a moment and try to rationalize what the hell is going on. Because, honestly, I am as lost as anyone should be in the current moment.

My goals in writing this text are:

- To try to communicate what is happening to a broader audience, explaining in a friendly way what all of this is about.
- To provide a somewhat “journalistic” develop of the lasts days, because, trust me, there are a lot of people writing about this.
- To reflect on an academic level about what all of this might mean for our jobs and for the way we do science.

This is probably too much stuff for a single essay, and I will probably fail spectacularly at trying to cover all of it since I am a terrible writter, but I will do what I can.

As Drago says, "*If he dies it dies*".

So to make this easier lets start with some dates.

## Historial

On November 19th, 2026, Anthropic had its IPO, opening the company to the public market. ([Wiki, 2026](https://en.wikipedia.org/wiki/Initial_public_offering_of_Anthropic))

As of today, November 24th, 2026, it has only been losing money (as expected, since no AI company has profits).

<div class="row justify-content-center mt-3 mb-3">
  <div class="col-sm-10">
    {% include figure.liquid loading="eager" path="assets/img/blog/riemann/image_1795496890172_0.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
</div>

On November 20th, 2026, Levant Alpöge made a claim that he may have solved the Riemann Hypothesis using a Claude agent model ([Alpöge, 2026](https://alpo.ge/remark.pdf)).

If you look through the various Reddit communities, people want to believe that his publication was prescheduled in an attempt to give Anthropic's stock a boost. But honestly, although it is a big coincidence, and even though Alpöge is a member of the Anthropic staff, I don't think this was the case.

Alpöge has been involved in solving many mathematical problems using Claude. He was also involved in the controversy surrounding the Navier–Stokes problem months before [Ref 1](https://www.tomshardware.com/tech-industry/artificial-intelligence/openais-breakthrough-solution-for-the-elusive-navier-stokes-problem-overshadowed-by-plagiarism-controversy-researcher-says-openai-scraped-codex-session-and-issued-career-threats) [Ref 2](https://officechai.com/ai/mathematician-tristan-buckmaster-says-he-cracked-a-fluid-dynamics-problem-with-ai-accuses-openai-of-trying-to-take-credit/). On the same day as the Riemann Hypothesis claim, they also announced that they had fixed some of the controversies surrounding the OpenAI Navier–Stokes solution [Ref 3](https://www.scientificamerican.com/article/ai-just-solved-the-real-navier-stokes-problem/).

And, to be honest, even if this was planned as some sort of marketing attempt, it did not seem to work particularly well for Anthropic. The shares are still dumping, and what really matters here is the solution claim itself.

## What is the problem?

The Riemann Hypothesis is one of the **Millennium Prize Problems**, selected by the Clay Mathematics Institute in 2000. Each of the problems carries a prize of one million US dollars, and before the advent of LLMs, only one of them had been solved: the Poincaré Conjecture.

In 2026, OpenAI claimed to have solved the Navier–Stokes problem, and now Alpöge, using Claude, claims to have solved the Riemann Hypothesis.

So, what exactly is the Riemann Hypothesis?

The problem starts with something that *seems* fairly simple: understanding infinite sums and convergence.

Imagine that we want to sum all the terms of the sequence

$$
\sum_{n=1}^{\infty}\frac{1}{n} = 1 +\frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \cdots
$$

This is a common undergraduate exercise, and we can demonstrate that this sum, known as the **harmonic series**, does not converge to a finite number. In other words, executing this *infinite* sum of terms gives us an infinite value.

Although this may look extremely obvious — “If I sum infinitely many things, I should get an infinite number” — this is not usually the case. In fact. Changing this sum just a little a bit to a $1/n^2$

$$
\sum_{n=1}^{\infty}\frac{1}{n^2} = 1 +\frac{1}{4} + \frac{1}{9} + \frac{1}{16} + \cdots = \frac{\pi}{6}
$$

Now of sudden this infinite sum does not return a infinite result. It converges to exactly $\pi/6$ .

Euler (the god of mathematics) announced this result in 1735 without a complete proof. He knew, from rough arguments, that it should be true, and later (1741) provided a proof.

He then generalized the question to a variable (s) and defined the Riemann–Euler zeta function is by

$$
\zeta(s)=  \sum_{n=1}^{\infty}\frac{1}{n^s}
$$

and the most important thing is that, Euler prove that there is a connection between the zeta function and the prime numbers,

$$
\zeta(s) = \sum_{n=1}^{\infty}\frac{1}{n^s}=  \prod_{p\ \text{prime}} \frac{1}{1-p^{-s}}
$$

This relationship is at the core of everything we are discussing, and it is one of the most beautiful and important relationships in mathematics.

In a simple, somewhat devoid-of-beauty translation, Euler tells us that *every integer number can be found from a product of prime numbers*.

Prime number are very important for modern criptography, If interested I recommend reading [Frank Zielen](https://www.mathnasium.com/math-centers/kirkwood/news/why-eulera-euro-trade-s-formula-for-primes-could-disrupt-the-world-30978191) text about it.

And if you want to visualize what I have just said, this 5 min segment of [FFP](https://ffppod.com/episodes/ep53/how-euler-connected-the-zeta-function-to-primes) illustrates well.

Riemann goes even further and thinks that this $s$ now is a complex number $s =a+ i b$ . Now the history is much more complicated but he managed to show that the zeta function can be represented in a not attractive functional form

$$
\zeta(s) = 2^s \pi^{s-1} \sin \bigg( \frac{\pi s}{2} \bigg) \Gamma(1-s) \zeta(1-s)
$$

So instead of simply thinking about an infinite sum, we transform this infinite sum into a function that can be plotted and analyzed continuously.

Riemann then made a remarkable conjecture about the zeros of this function — that all of its **non-trivial zeros** should lie on the vertical line

$$
a = 1/2 \,.
$$

<div class="row justify-content-center mt-3 mb-3">
  <div class="col-sm-10">
    {% include figure.liquid loading="eager" path="assets/img/blog/riemann/image_1795520969089_0.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
</div>

This is the Riemann hypothesis, this is the million dolar problem. (See the [3Blue1Brown video for the graphical visualization](https://www.youtube.com/watch?v=sD0NjbwqlYw))

Proving it is extraordinarily difficult because the zeros of the zeta function are deeply connected to the distribution of prime numbers. If even one non-trivial zero is found outside the line $(a=1/2)$ , the hypothesis is false.

## How he solved?

Well, first of all, the “solution” currently consists of a four-page PDF containing his notes and **17.4 million lines of Lean code**.

The PDF itself is not particularly clear. He mentions Stepanov's elementary proof from 1969. So we could guess that the solution is based on finding a argument that correctly bounds the possible interval of values closer to the critical line. But this is merely the idea of how it was solved, no one really understands, and the Lean code is obviously not humanly possible to read line by line.

If converted into something resembling ordinary mathematical prose, the code would reportedly correspond to roughly a quarter of a million pages. Around 250,000 pages...of human-readable text.

So, is it a solution?

Apparently, it has been formally verified by Lean. On November 21st, the Lean FRO [ref](https://officechai.com/ai/lean-community-certifies-levent-alpoges-claude-assisted-proof-of-the-riemann-hypothesis-as-correct/) released a statement saying that

> *A joint statement endorsed by the Lean FRO and the Mathlib Initiative says the 17-million-line proof states the right theorem, compiles and passes multiple independent proof checkers.*

But no human being can realistically read and understand the entire proof in its current form.

Well... hooray!! Congratulations!!!?... I guess?

I would say that, personally, it is easy to believe the Lean team's proof checks. And, generally speaking, the mathematical community already has a very strong feeling that the hypothesis is true.

The difference is going from 99.9% certainty to 100%.

Which is very nice and important, don't get me wrong.

But what is the actual gain?

On November 21st, just one day after Alpöge's claim, we got a first attempt at translating this mess into something more understandable: an 11-page document generated with the help of AI and published in the repository by Bartosz Naskręcki ([guide](https://nasqret.github.io/riemann-rev/guide/proof-guide.pdf)).
Is not a readable translation, but is a...schematics guiding the structure of the solution.

On November 20th, not even 24 hours after Alpöge's release, we also got these notes by J. Nielsen ([ref](https://philarchive.org/archive/NIEIOT-2v1)), claiming that the Alpöge solution contains fundamental problems that should invalidate it. I think is fair to assume that this is also a AI conclusion (presumably) because the amount of files to analyze and give a veridict to Alpoge's, is not possible by a single person.

The most important development is that on november 22th the was a rushed released [MATH216](https://math216.wordpress.com/2026/11/20/hurried-announcement-alessandro-masullo-grh/) of a human proof by [Alessandro Maria Massulo](https://math216.wordpress.com/wp-content/uploads/2026/11/the-music-of-the-primes.pdf)

Apparently he was working on this proof for many years and want to use another year to polish the text. However due to the sudden claim he rushed the publication.

I say this is very nice, because his approach appears to be very different from the one proposed by Claude.

But still Massulo's draft has almost 1000 pages. It will also requires time and effort of other mathematicians going throught his demonstration in order to validate it.

## Final considerations

Given all of this, I cannot stop thinking about the future as a whole.

Mostly because I am involved in research, and when I see a bunch of extremely hard problems being solved by machines, I cannot help but ask myself:

**What am I doing here?**

There are a few different points that can be addressed.

One big concern is: **“Is the machine the doom of our field?”**

Is it really?

Well, the fact is that AI does make theoretical science, specially mathematics, easier.
It is a convenient and powerful tool.
Period.

But it is also a tool that everyone can use.

<small>(\* sidenote: I am not entering in the fact that it is not for everyone. Who can paid for the subscription has much more power and it could be another way of seggregate places were science naturally struggles for financing in the future.)</small>

So if I am producing more, everyone else is producing more as well.

This makes an area that is already extremely stressful and competitive even more stressful and competitive.

Another concern is that we will end up with a bunch of shitty papers being produced that no one reads, no one cares about, and that add nothing to the field.

I do agree with this.

In fact, even arXiv has limited the number of submissions that some users can make to two per month, although I do not think this is the principal problem.

We have always had good and bad papers being published, and most of them are not read by most people.
Sometimes, they are not even properly read by the referees.

I think the truly good papers will eventually find a way to percolate through the pile of trash, as they always have.

The problem is the **speed**.
The competitiveness that AI introduces into the field.
And, perhaps most importantly, the undervaluation of researchers as professionals.

You can already imagine the argument:

> “Why pay the salaries of three PhDs if I can pay one PhD and give them an AI subscription?”

I think that, in the worst-case scenario, governments could use this as an argument to decrease funding for fundamental and theoretical sciences, prioritizing experimental research that still requires "human hands".

Which would, personally, make my life considerably harder.

Maybe, in the end, it does not change much.

When Deep Blue famously defeated Kasparov, the media went crazy. There was enormous public attention.

It was a major advance in computer science and, in many ways, a symbolic beginning of the modern society we understand today.

But chess survived.
Kasparov is still Kasparov.
Chess is still a human activity that we practice for pleasure, and Kasparov is still remembered as one of the GOAT's, despite a machine being able to play it better than him once.

I still want to believe that we will continue doing science simply for the pleasure of understanding things and learning.

But it is also true that we need to be aware of what is happening and rethink how we, as a community, conduct science.

Because things can always get worse.

Capitalism is still capitalism, and unfortunately, science is also a product.
