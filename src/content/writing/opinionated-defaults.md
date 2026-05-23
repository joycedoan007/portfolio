---
title: The case for opinionated defaults
date: "2025-08-20"
readTime: 6 min read
description: Configurability is a debt instrument. Defaults are the principal payment.
notionUrl: https://joycedoan.notion.site/opinionated-defaults
---

There's a specific kind of product meeting where someone says "we should let users configure this" and everyone nods. Configuration feels like generosity. You're not forcing a choice on the user — you're respecting that they might want something different. You're being flexible.

The problem is that configurability has a cost that never shows up in the meeting. It shows up later, when users open a settings panel and don't know what any of the options mean, or when a new user has to make fifteen decisions before they can do the thing they came to do.

## Defaults encode intent

A default is a statement. It says: in the absence of other information, this is the right choice for most people in most situations. A good default is one where the design team has done the work of figuring out what "most people in most situations" actually means and committed to it.

A bad default is one where the team didn't want to make a decision, so they picked something arbitrary, or worse, left it up to the user at the cost of an extra decision on first run.

The best defaults are invisible. Users don't notice them because they're already doing the right thing. The worst defaults are the ones that generate the most first-run friction and the most support tickets about "how do I change X back to how it was."

## Configurability as a debt instrument

When you make something configurable, you're taking out a debt. The debt is this: you now have to maintain every configuration variant, test every configuration combination, and document every option. And you have to do this for every version, forever.

This debt is often worth taking on. There are genuine cases where users have legitimately different needs, and configuration is the right answer. Notification preferences. Color themes. Keyboard shortcuts. These are worth the debt because the variation in user needs is real and significant.

But most configurability doesn't come from this honest analysis. It comes from not wanting to commit to a default, from hedging against hypothetical user complaints, from wanting to appear flexible without the work of figuring out what the right answer actually is.

The discipline is to treat every configuration option as debt and ask whether the return justifies the interest payments. Often it doesn't. And in those cases, the right move is to pick an opinionated default and ship it.

## How to set good defaults

A good default comes from understanding actual usage, not hypothetical preferences. Look at what users do when you give them a choice. If 90% of users choose option A, A should be the default — or better, the only option.

This requires having usage data, which requires having shipped something and watched how people use it. Early in a product's life you won't have this, so you have to make your best guess and commit to being wrong and updating. That's fine. Defaults can be changed. The important thing is to have one.

When you don't have data, ask what decision minimizes harm for the most users. A default that causes a small problem for 10% of users is better than a forced choice that delays everyone. You can tell the 10% how to change it. You can't give back the time the forced choice cost the 90%.

## When user control is right

None of this means configuration is bad. It means configuration should be earned by demonstrating that the variance in user needs is real enough to justify the cost.

The cases where user control is genuinely worth it are usually the ones where getting it wrong has real consequences for the user. A default time zone is harmless to change if wrong — unless you're a scheduling tool, in which case a wrong default causes missed meetings. A default notification frequency is easy to adjust — unless notifications are the main reason the user opened the product.

The tell is whether users would feel wronged by the default, not just inconvenienced. If the wrong default causes genuine harm, configuration is probably worth the cost. If it just requires one setting change to fix, you have a fine default and a forgettable support ticket.

Make the important decisions for your users. Let them override the things that matter to them personally. The discipline is knowing which is which.
