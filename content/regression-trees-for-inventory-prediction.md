+++
title = "Predicting What to Order Next Week, With a Regression Tree"
date = 2026-09-07

[taxonomies]
categories = ["Machine Learning"]
tags = ["small-business", "regression-trees", "forecasting", "inventory"]
+++

"Machine learning" and "predictive analytics" get thrown around like they require a data
team and a platform contract. Most of the time, for a single well-defined business
question, they require neither. This is a walkthrough of one of the most approachable
tools for exactly that: the regression tree.

<!-- more -->

## The question, made concrete

Say you run a small bakery, and every Sunday you decide how much flour to order for the
coming week. Order too little and you're turning away customers Thursday afternoon; order
too much and you're throwing out spoiled stock. Right now you're probably guessing based
on gut feel and "how busy did it feel last week" — which works, sort of, until a holiday
or a heat wave throws it off.

A regression tree answers exactly this kind of question: given a few known factors, predict
one number. It doesn't need to be flour — the same shape of problem shows up as "how much
produce to stock," "how many temp staff to schedule," or "how much hay to bale this cutting."

## What data you'd actually need

This is the part that usually gets skipped, and it's the part that matters most: you don't
need a data warehouse. You need a spreadsheet with, for each past week:

- The number you're trying to predict (pounds of flour used, units sold, whatever it is)
- A handful of factors that plausibly affect it: day-of-week mix, season, whether there
  was a local event, recent sales trend, weather if it's weather-sensitive

Twelve months of weekly records — about 52 rows — is enough to get started. You almost
certainly already have most of this in a POS system export or a farm log; the work is
consolidating it, not collecting it from scratch.

## How the tree actually decides

A regression tree works by repeatedly splitting your past data into groups based on the
factor that best separates high-demand weeks from low-demand weeks — then splitting those
groups again — until it reaches small, similar clusters of weeks. Each final cluster gets
a predicted number: the average of what actually happened in weeks like that one.

Concretely, it might learn something like: *is it a summer month?* → if yes, *was there a
local event that week?* → if yes, predict the high end of your range; if no, predict the
seasonal-summer average. No local event, no summer → check the next most useful factor,
and so on. The output isn't a black-box score — you can read the whole decision path in
plain English, which matters when you need to explain to a business partner *why* the
model says to order more flour this week.

## Where this actually pays off

The honest caveat: a regression tree on 52 rows of data won't outperform an experienced
owner's gut feel by a wide margin in a stable business. Where it earns its keep is
consistency and memory — it doesn't forget the odd spike from two Augusts ago, and it
doesn't have an off day. It's also cheap to build and maintain: a single scikit-learn
script, retrained monthly as new weeks of data come in, run on hardware you already own.

That's the pattern worth taking away: this isn't "adopt AI," it's "answer one recurring
number-guessing question a little better than guessing," using a tool simple enough that
you can look at its reasoning and sanity-check it yourself.
