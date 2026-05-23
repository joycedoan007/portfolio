---
title: How I think about complexity budgets
date: "2025-04-08"
readTime: 9 min read
description: Every feature has a complexity cost. Most teams pay it without knowing the price.
notionUrl: https://joycedoan.notion.site/complexity-budgets
---

Complexity is the one resource that products accumulate naturally and spend unconsciously. You don't decide to make something complicated. You decide to add one more option, one more edge case, one more configuration toggle — and complexity is what's left when you add them all up.

The teams that build clean, usable software aren't the ones that have fewer ideas. They're the ones that know how much complexity they can afford and are disciplined about spending it.

## Every feature has a cost

The cost of a feature isn't just engineering time. It's the cognitive tax it levies on every user who encounters it — whether or not they use it. A setting buried in a menu still needs to be parsed and discarded by the user who opens that menu. An optional field still asks a question that most users have to answer with "I don't know what this is."

This cost compounds. A product with fifty features requires users to maintain a mental model of fifty things that might affect their experience. A product with ten features requires ten. The ten-feature product isn't half as useful — it's often twice as usable, because the user's attention is free to go to the task rather than the interface.

The metaphor I find useful is budgeting. Every product has a complexity budget — an amount of cognitive load it can impose before users start dropping off or making errors. Features are purchased from this budget. The question before adding any feature isn't just "is this useful?" but "is this worth the budget it costs?"

## How to audit your current budget

Most teams don't know what they're spending. To find out, you have to do the uncomfortable work of looking at your product through fresh eyes.

Walk through the product as a new user would. Every time you have to stop and decide something — which of these options to choose, what this label means, whether this action is reversible — mark it down. These are budget draws. By the end of the walkthrough you have a rough map of where complexity lives.

Do the same with support tickets and user research. Confusion concentrates around complexity. If the same screen generates 30% of your confusion-related support tickets, you know where your biggest budget overspend is.

The audit isn't about identifying everything to cut. It's about making the costs legible so that future decisions are made with full information.

## The compounding problem

Complexity compounds in ways that aren't immediately visible. A feature added today interacts with every feature that already exists and every feature that will be added in the future. The tenth option in a list isn't ten times as complex as the first option — it makes the list itself harder to scan, introduces potential conflicts with other options, and adds to the maintenance burden of every future change.

The worst version of this is the "just one more thing" pattern. Each individual addition seems small. The cumulative effect is a product that feels heavy and hard to learn. Users describe it as "bloated" or "overwhelming" — words that capture the felt sense of too much complexity without pointing to any particular cause.

The only defense is considering interactions, not just individual features. Before adding something new, ask: how does this interact with what already exists? Does it create new combinations the user has to understand? Does it make the existing mental model harder to maintain?

## When to say no

Saying no to a feature request is uncomfortable. The request is usually well-intentioned, the use case is usually real, and the person asking is usually frustrated by the current limitation. None of that changes the analysis.

The right frame is: how many users benefit from this feature, and how much does it cost every user who doesn't need it? If 5% of users need a feature and the other 95% pay a small tax for it, the math often doesn't work — especially as you add more features with similar profiles.

Some features justify their complexity cost through outsized impact on the users who need them, or through being hidden deeply enough that they don't tax non-users. Most features can't make this argument honestly if you try to make it explicitly. The default should be no. The burden of proof should be on the feature to justify its complexity cost, not on the team to justify saying no.
