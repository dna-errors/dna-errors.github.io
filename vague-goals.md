---
title: Vague Goals
---

# We want to move! Not sure where...

This story happened so long ago that there is no need to disguise company name.
Moreover I always think of this company with much tenderness - it was my
first work as Java developer and people here were really friendly.

"Real estate Bulletin" was a local company issuing the said bulletin - weekly
volumes of advertisements, mainly, about selling houses, flats, commercial
property etc. They also ran a web-site with similar information.

For every issue they collected about `30000` lines of ads, sent by various
agencies by email. And here comes the task I was hired for.

<h2 class="section-heading">Parsing Ads</h2>

The overall process was to get these "ad orders" from the mailbox, parse and
upload to database. And parsing was the most painful problem, e.g.:

- customers may slightly violate the required text format
- customers may express property parameters differently
- worse of all - people made lots of mistakes in the addresses!

To solve this problem company had dedicated fellow (call him Di)  who manually processed
all incoming orders every Thursday. He used some old tools carelessly written
many years ago. However while they could do simple fixes (like shortening
"Angels street" to "Angels st"), there was no ability to correct typos.

And Di usually had too much work to carefully check every mistakes, so often
mistaken ads ended up as declined or fall into some wrong district.

This situation was to be corrected and I was much enthusiastic. Dedicated
tool was created, which I called "Fuzzy Regular Expressions for Java" - small
engine which matched addresses against a lot of whimsical but flexible rules
and automatically corrected most typos and names variations - this still
could be found in my github. There were other interesting tasks, like searching
the street in the nearby districts, resolving duplicate names etc.

Well, I spent few months to implement application wrapped around this tool and
perhaps a month to create the set of rules to parse addresses in our city.

At last the time to demonstrate the work has come. I loaded the whole bulk
of `30000` orders and... output was produced in a few seconds! Several random
picks have shown all results are seemingly finely "groomed" and corrected.
About `300` lines were declined as "hopeless" and when checked, they really
looked beyond repair, so everything looked extremely fine.

**But where are any, eh... buttons... which Di can press?**

So I was asked by senior colleagues. I said well... there are no any. Process
is fully-automated.

I readily added a "step-by-step" mode with two buttons, so that Di could
review the check result for every line and accept or decline it.

This haven't satisfied my colleagues. They agreed it "looks like what we want"
but said they are not ready to tell Di his work is not needed anymore.

They spent some weeks on trying to re-think how to reconcile existence of
automatic tool and manual work by Di. Meanwhile I was told to extend the tool
so it work as well for the addresses in the country around the city.

After this was done I actually had nothing more to do, so I left for the new
company. My successor on this project told me later he spent a year lazily
amending and refurbishing the web-part of my project, but he also haven't
worked long enough to see this tool integrated into "business-process".

Colleagues seemingly were hesitant to move forth - and at the same time
reluctant to freeze the project, since considerable efforts (and financing)
was spent on it.

<h2 class="section-heading">Conclusion</h2>

Who are to blame? If I were more experienced, I would insist on frequent
"sync-ups" with Di himself, so that both he and everyone were more prepared
to switching to fully-automated process.

On the other hand, as my colleagues and bosses were seeking to streamline
the ads parsing for years, they should prepare some "integration plan" instead
of looking onto results of the project with great surprise.

Further I learnt in the other projects that importance of such "integration
plan" is often underestimated (or not thought of at all) unless in companies
with quite mature managers. Generally there are two ways:

- either the new service or tool can be integrated gradually, as it is being
    developed, gets new features etc.

- or it could be integrated only after certain bulk of functionality is
    implemented

Looking back I think the first way was viable for our case - as there were
`33` different types of ads, we could start using the tool only on some
small subset of orders, like commercial properties etc.
