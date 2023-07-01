---
---

# Eight Horsers Paradox

**What force produce 8 horses pulling as a single team?** - such a question in some kids book on basics of
physics astonished me greatly.

Author explained, that in situations when multiple horses are joined to pull some heavy load together, their
total pulling force doesn't increase properly (linearly) with the number. He produced some table, supposedly
calculated as a result of some real trials, looking like this:

- 2 horses produce total force of 1.9 times compared to single horse
- 3 produce only 2.6 times
- 4 give just 3.1 (so one horse is almost "waste")
- 5 yield 3.5 (one and half horses lost!)
- 6, 7 and 8 horses barely increase this value (3.7, 3.8, 3.8 correspondingly)

This is explained by horses not pulling synchronously enough and even hindering each other efforts.

**And this works in IT projects too!** Let's have a look at some negative as well as some positive examples.

<h2 class="section-heading">Six men and additional experts</h2>

Experience from "MP" project. When I joined this team, I was the 7-th. Project was conceived as "Start-up",
fusing telecom and blockchain technologies. Besides the full-time members there were part-time "experts", so
it was almost a small army! Despite of this, development was markedly slow and haven't reached production
even after more than year of efforts.

Let's see what the "core team" consisted of:

- Project owner, ideologist and visioner
- Project manager, responsible for hiring the rest of the team and attempting to drive the process
- Cyber-Security Guy - it was anticipated we'll have some degree of fraud from users and he was to prevent this
- IoT specialist - as the project was around certain hardware / telecom solution
- Hardware programmer - to help IoT specialist
- Devops - taking care about infrastructure (servers, clusters, kubernetes, amazon etc)
- Backend programmer - to take care of server-side application collecting data, providing user accounts etc

Still this list lacks some important people: Quality Assurance specialist (or "tester"), Business Analyst, the
person who defines and clarifies the tasks - and Frontend developer (UI, web). Some of them joined later.

**What is wrong with such setup?** Just as the Bible says about Babylon Tower: several people are carrying
single brick instead of one person carrying several bricks. Many calls, few responsibility.

Let's go through the list in order.

Project owner is generally out of question. Entity which exists and couldn't be changed. It is good for product
owner to have background in IT and play role of manager or BA for example. It wasn't the case though.

Manager. Larger companies generally allocate single project manager for 3-4 projects. There are not always enough
work for single manager in single project. Thus it is good for manager to be also BA and QA for example. In this
case manager generally neglected to write tasks requirements so later it sometimes was hard to figure out whether
they are fulfilled by implementation.

Security Guy. In brief, it was premature state for full-time security specialist. It soon appeared that security
issues are overestimated and the fellow was reassigned "to help with backend". Regretfully it wasn't his strongest side. Security too.

IoT specialist and Hardware programmer - why two? because IoT specialist wasn't good in hardware programming.
That's bad, he often had nothing specific to do or was assigned tasks for which he was not exactly capable.

UI developer and UX designer who appeared bit later were separate people. Often developer needed to wait for
designs for several days, because designer was part-time participant.

**To conclude:** it feels like the team was assembled faster than understanding of the project evolved. Also it
often feels difficult to say farewell to members which appear unneeded. In larger company it is possible to
move them to other projects, but it is not the case for start-up.

<h2 class="section-heading">150 heads to do it quickly</h2>

Very different, but also disastrous experience from the "MO" project. I was working for outsourcer company which was approached
by very large client - one of the big international analytics agencies. They wanted some impressive solution to
automate processing of various documents, reports etc - quickly, say in 6 months. This outsourcer in turn was
cool in that they never were afraid of short projects.

They allocated 150 specialists to work on the project (or rather set of subprojects) during the first month.
It soon became a real mess: I myself was made a team-lead of the team which incorporated all people not assigned
to more specific teams yet. Every daily standup I discovered some people left and some new people were added -
and my team soon grew from 3 to about 20 members. Ironically we made certain progress during the first month,
when we were few. But with explosive growth of the "population" work soon converted into numerous calls and
heated debates about what should be done and how.

I left the company soon, but was informed by colleagues the project nevertheless was completed, though it took twice more time than expected and with overall feeling that the amount of work done was adequate for 20-30 people rather than 150. Still the client was less or more satisfied, so it was not a total failure.

<h2 class="section-heading">Positive Cases</h2>

**Microsoft** was started by just two fellows, **Bill Gates** and **Paul Allen**. Of course their first project
was somewhat smaller, but it is worth studying. They learnt that MITS is producing curious and comparatively
small computer "Altair 8800", lacking user-friendly software. Gates contacted MITS claiming they already work
on implementation of BASIC interpreter for this machine. Thus he made sure product can potentially be sold
before it was actually started.

However it is important that while Gates had obvious business skills, he actively participated in development.
Guys cleverly split the work - Paul created emulator of the Altair (they have no real machine) while Gates
worked on interpreter itself (supposedly acquiring and adapting some different version).

The thing was completed in a few weeks. MITS agreed to distribute it. Revenues after year and half totalled
to `$16000` (multiply perhaps by `10` for inflation). Picture of Microsoft staff in two more years shows `11` persons.

Similarly **Apple Inc** was started by two friends, **Steve Jobs** and **Steve Wozniak** who conceived idea of
small home computer, "Apple I". It is in many ways different, particularly because member roles were quit
distinct - Steve W. was hardware guru, while Steve J. besides excellent business and management skills was
always influential in shaping out requirements for company products.

<!--                <h2 class="section-heading">The Final Frontier</h2>
                <a href="#!"><img class="img-fluid" src="assets/img/post-sample-image.jpg" alt="..." /></a> -->

