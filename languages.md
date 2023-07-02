---
title: On fancy languages
---

# We love this language, why not?

At the beginning computers were large and their programs were tiny. Programmers
could create them directly in machine codes or commands. However **Moore's Law** says
hardware improves roughly twice every year-and-half. As program sizes grew accordingly,
very soon programmers started inventing "high-level programming languages" which were
translated to machine codes before execution. It started in late 1950s with **Fortran** and
now, `60+` years later we have zounds of various languages.

And programmers generally like this diversity! Languages differ by their qualities, but we
can outline, perhaps, few critical:

- overall performance (this may mean how slow or how expensive is your application)
- easiness of use (which boils down to how costly it is to develop your product)
- popularity (how easy it would be for you to find and hire programmers)

We'll compile some comparison table of the most popular languages later, however right now let's
talk of few examples when some rare and exotic language was chosen for the project.

<h2 class="section-heading">Failure on Performance</h2>

Experience from "LA" project.

At job-listing web-site there were only `2` positions with **Erlang** language in my city (while
mainstream languages gave hundreds of hits). I by that time was in search of "something new", so
sent them my CV and after interview and quick test-task was accepted. It was supposed I can quickly
grasp the language (and I did).

The team consisted of smart and nice fellows with many good ideas. They were producing B2B solutions
for other IT-services which use Amazon - particularly my project was about solution allowing to store
immense amounts of log data. Neighboring team was working on the search functionality for this storage.

So to say it was "Big-Data" but using non-mainstream approach, and particularly non-mainstream language.

Key people were came from telecom background and they directly manifested "We love Erlang!"

Now **Erlang** is very specific and interesting. Language without variables and loops, but with threads
and messages between them out of the box. Somewhat archaic by nowadays standard (even couldn't store files
in subfolders by then). So I well understood these fellows "love" to this language.

Regretfully its main features, event-driven paradigm particularly - were of no use for this project. Really
our project was about **bulk-processing** huge amounts of data. And for this Erlang was quite poor choice.

First of all it was slow interpreted language. About 10 times slower than languages compiled to native code.
This is no harm in applications which mainly waits for user
actions and does some actions on them, produces some response and waits further. For bulk-processing the speed
does matter.

The second factor was Erlang operates immutable data. This means that when one needs to slightly modify, say,
kilobyte record, actually new copy of data should be created.

This approach is also not bad itself, it allows easines in simultaneous execution and is much favored in functional
languages. However, again, our project was mainly concerned with processing binary data and this made the work
another 10 times slower.

So what? 10 times slower due to language, and 10 times slower due to immutable data - we got 100 times speed reduction.
Users were supposed to pay, say, `$0.10` for each search query - but instead we found they would pay `$10` - because
the system cleverly launched `100` times more executors in Amazon to produce the result.

This was discovered bit too late (and particularly performance investigation were done by myself). Not sure why
project leaders failed to recognize this earlier. We tried in vain to rewrite parts of the project in `C`, but
performance still was lost greatly on copying data between Erlang and C parts.

The team started to dissipate and at some moment I left the project too, partly because I also loved Erlang and
was not much interested in re-doing project in C.

<h2 class="section-heading">Failure on Popularity</h2>

This story is not from my direct experience. I was interviewed for this project and knew people related to it.

Here is a company working on cutting-edge of healthcare industry and overall doing great things. Leaders of their
IT-department are much concerned about robustness of their services and follow the generally correct idea that
languages with stricter type system allow to avoid certain errors even during development phase.

However they almost reached absolute. Probably strictest language regarding types is **Haskell**. Downsides
are that it is notably difficult to master (and somewhat difficult to use even when mastered), is not
popular and has quite small number of proponents.

Thus unlike with **Erlang** above (to which it has some "relation" - both are of "functional" languages family) guys
came to situation when it is pretty difficult to find and hire mature developers for **Haskell**. They reside to
approaching bright and enthusiastic university graduates, but there are not many of them interested in Haskell either
(as they thought "is this experience worthwhile? I won't find a job later").

And thus trying emphatically to improve quality of product by wise choice of the language, the team on other
hand undermines this quality by being unable to get programmers with suitable industrial experience.

<h2 class="section-heading">Positive Case</h2>

about the project when people used gradle instead of java, to be continued...
