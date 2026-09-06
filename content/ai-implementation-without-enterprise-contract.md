+++
title = "\"AI Implementation\" Doesn't Have to Mean a Six-Figure Vendor Deal"
date = 2026-09-08

[taxonomies]
categories = ["Automation"]
tags = ["small-business", "ai", "implementation"]
+++

Search "AI for small business" and you'll mostly find two kinds of results: consultants
selling a platform subscription, or think-pieces about how AI will transform your
industry in vague, unfalsifiable ways. Neither is aimed at someone who just wants one
specific task to take less time.

<!-- more -->

## The framing problem

"AI implementation," as an industry phrase, usually means: buy a platform, integrate it
across departments, budget for a multi-month rollout and ongoing licensing. That framing
makes sense for a company big enough to have a department dedicated to the rollout. For a
business with twenty employees — or five, or one plus a few seasonal hands — it's the
wrong shape of solution entirely, and it's why so many small business owners have
correctly concluded that "AI" isn't for them yet.

It's not that AI isn't useful at their scale. It's that the *unit of adoption* is wrong.
The unit that actually fits is: one tool, solving one task, that you can turn off without
consequence if it doesn't work out.

## What the smaller unit looks like

A few concrete examples, roughly in order of how much setup they take:

- **A single script using an off-the-shelf model API** to do one narrow task — summarizing
  daily customer emails into a three-line digest, categorizing incoming support requests,
  drafting first-pass replies to routine questions. This is an afternoon of setup, costs
  fractions of a cent per use, and if it doesn't help, you delete the script.
- **A self-hosted open-source model** for anything where sending data to a third-party API
  isn't acceptable (customer PII, financial records, health information). Slower to set up,
  but the ongoing cost is just the electricity to run it, and nothing leaves your network.
- **A small, purpose-built model trained on your own data** — the regression-tree example
  from an earlier post on this blog is exactly this: not "AI" in the platform sense at all,
  just a model that answers one number-guessing question using your own history.

None of these require a vendor relationship, a contract renewal, or a rollout plan. They
require someone willing to spend a few hours getting one thing working.

## The actual risk to manage

The legitimate caution around small-scale AI adoption isn't cost — it's trusting an
unverified output somewhere it can do damage. The mitigation isn't "avoid AI," it's the
same rule that applies to any junior employee doing a new task: **don't let it make an
unreviewed final decision on anything with real consequences.** Have it draft the reply,
not send it. Have it flag the anomaly, not silently correct the books. Once you trust the
narrow thing it's actually doing, expand from there — one task at a time, same as any
other hire you're training up.

## Start smaller than feels serious

If "AI implementation" as a phrase makes your eyes glaze over, that's a reasonable
reaction to how it's usually sold. The version worth actually trying looks less like a
transformation and more like: pick the one task you dread doing every week, spend an
afternoon automating just that, and see if it's actually better. If it is, pick the next
one. That's the whole plan.
