---
title: When AI helps, and when it gets in the way
date: "2025-11-10"
readTime: 12 min read
description: A field guide to confidence, declines, and the difference between a copilot and a clippy.
notionUrl: https://joycedoan.notion.site/when-ai-helps
---

Every few months someone ships a product with AI in it and calls it a copilot. Sometimes it's genuinely useful. Sometimes it's a suggestions dropdown with a language model behind it, dressed up in the language of collaboration. The word copilot has done a lot of work in the last two years and it's starting to show the strain.

The question I keep coming back to isn't whether to use AI in a product. It's when AI actually helps the user — and when it gets in the way.

## The confidence problem

The fundamental challenge with AI-generated output is that it's non-deterministic in ways that feel deterministic. A user asks the system to draft something, and it produces text that looks authoritative, formatted correctly, and plausible. Whether it's accurate is a different question. The interface rarely makes that distinction clear.

This creates a confidence problem. Users either over-trust the output — they copy it without review because it looked right — or they develop blanket suspicion and stop using the feature entirely. Neither is good. The goal is calibrated confidence: the user should have an accurate sense of how much to trust any given response.

Designing for calibrated confidence means building interfaces that communicate uncertainty, show sources, and invite scrutiny. It means not hiding the model's reasoning. It means building verification into the workflow rather than treating output as final.

## Designing for non-deterministic output

Traditional UI design assumes determinism. A button does what the label says. A form field accepts the type it specifies. A chart shows the data it's given. The designed output matches the expected output.

AI breaks this contract. The same input can produce different outputs. The user's intent and the system's interpretation can diverge in ways that are hard to anticipate. The UI has to handle not just success states but ambiguous states — situations where the output is technically correct but not what the user wanted.

This requires new patterns. Confidence indicators that map to actual model uncertainty, not just vibes. Undo stacks that are output-level, not keystroke-level. Multiple-options patterns where the model proposes and the user selects rather than the model deciding. These aren't just nice-to-haves — they're the infrastructure for trust.

## The copilot vs Clippy distinction

The reason Clippy failed isn't that it offered suggestions. It's that it couldn't tell when suggestions were welcome. It interrupted constantly, regardless of context. It made the computer feel like it was watching you.

The copilot model — the one that actually works — is about waiting to be invoked. It's about having a clear mental model of when to help and when to stay out of the way. GitHub Copilot works partially because code completion is a natural invocation point: you pause after a function signature, and that pause is a signal. The help arrives when it's appropriate.

For AI features in other products, the invocation point is harder to find. If you're building a writing tool, when does the user want a suggestion? If you're building a data tool, when does the user want an interpretation? Getting this wrong in either direction — too eager or too passive — makes the feature feel broken even when the model is performing well.

## When AI should decline

One of the most underrated AI interface design decisions is the decline state. When the model isn't confident, when the input is ambiguous, when the task falls outside reliable territory — what happens?

Most products treat the decline as a failure state to be minimized. The result is systems that hallucinate rather than admit uncertainty, or that produce low-quality output rather than refuse. This is the wrong tradeoff.

A well-designed decline teaches the user something. It narrows the space of what the system can do, which makes the remaining space more reliable. "I can't help with X" is useful information. It lets the user adjust their approach or go elsewhere. Confident silence — the system doing nothing when it shouldn't try — is better than tentative action that produces noise.

## Graceful failure

When AI does fail — and it will — the question is how gracefully it fails and what path it leaves for recovery. A failure mode that destroys work or leaves the user in an unrecoverable state is a design bug, regardless of whether it was caused by AI or deterministic code.

Graceful failure for AI features means preserving user agency throughout the output cycle. The user's original content should never be silently replaced. Suggestions should be additive and reversible. The system should make it easy to say "no, not that" without losing what you had.

This is partly a philosophical commitment and partly an interface architecture decision. The interface should treat AI output as one possible path, not the only path. The user is always the final editor.
