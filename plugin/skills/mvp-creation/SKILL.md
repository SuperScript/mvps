---
name: MVP Creation
description: >-
  This skill should be used when the user asks to "create an MVP",
  "build an MVP", "plan an MVP", "scope an MVP", "validate my idea",
  "test a hypothesis", "help me plan an MVP", "MVP plan", "design an
  experiment for my idea", "test my product idea", or "define a minimum
  viable product". Guides the user through a structured conversation to
  identify the Maximally Valuable Problem, form a testable hypothesis
  about revealed preference, set a threshold test, and design an
  experiment.
allowed-tools:
  - Read
  - Write
  - AskUserQuestion
---

# MVP Creation

## Purpose

Guide any product creator — regardless of role or product type — through a
structured conversation that produces a testable MVP hypothesis grounded in
revealed preference, with a pre-committed threshold test and a concrete
experiment design. Save the result to a markdown file at a location the user
chooses.

## Core Concepts

### MVP = Maximally Valuable Problem

The traditional reading of "Minimum Viable Product" puts attention on the
product: how little can we build? Reframe MVP as **Maximally Valuable
Problem** to focus attention where it belongs — on identifying the most
important problem to test. The MVP is not the product. The MVP is a test of
whether the problem exists and drives behavior.

### Revealed Preference

Economist Paul Samuelson's 1938 principle: preferences are demonstrated
through actual market behavior, not through what people say. An MVP is a tool
to reveal preference. Design every MVP as an experiment that observes what
people *do*, not what they *say*.

### The Threshold Test

A hypothesis without a pre-committed threshold test is useless. Without one,
post-test discussion centers on debating whether the outcome was good enough.
That discussion is waste. With a threshold test defined **before** the
experiment, the outcome is unambiguous: pass or fail. The post-test discussion
then focuses on the only question that matters: **what does this outcome mean,
and what do we do next?**

## Conversation Flow

Work through these phases in order using AskUserQuestion. Do not skip phases
or compress multiple phases into one question. Challenge the user aggressively
throughout — the goal is a strong hypothesis, not a comfortable conversation.

### Phase 1: Understand the Idea

Ask the user to describe their product or service idea and who it is for.
Listen for implicit assumptions about user behavior.

### Phase 2: Find the Maximally Valuable Problem

Push the user to articulate the single most important problem this solves.
Require the problem to be stated in terms of observable behavior, not feelings
or opinions. Reject vague problem statements like "users are frustrated with
X" — demand specifics: what do users observably do (or fail to do) because of
this problem?

### Phase 3: Identify Assumptions

Extract the implicit assumptions the user holds about user behavior and
preference. List them explicitly. Common hidden assumptions include:

- Users are aware they have this problem
- Users are actively seeking a solution
- Users would switch from their current approach
- Users would pay for a solution
- The problem is frequent enough to matter

### Phase 4: Challenge Assumptions

Play devil's advocate. Strongly push back on each assumption. Ask:

- "How do you know users have this problem? Did they tell you, or did you
  observe them struggling?"
- "What are users doing today instead? Why would they stop?"
- "If this problem is real, why hasn't someone already solved it?"
- "Are you confusing what users say they want with what they actually do?"

Force the user to distinguish stated preference ("people say they'd love
this") from revealed preference ("people demonstrably behave this way").
Do not accept survey data, interview quotes, or anecdotal enthusiasm as
evidence of revealed preference.

### Phase 5: Form Hypothesis

Distill the conversation into a single testable hypothesis about revealed
preference. The hypothesis must follow this structure:

> When given [specific opportunity], [specific audience] will [specific
> observable action] because [the Maximally Valuable Problem] currently
> causes them to [specific observable consequence].

Reject hypotheses that:
- Rely on stated preference ("users say they would...")
- Are unfalsifiable ("users will find value in...")
- Lack a specific observable action
- Target an undefined audience

### Phase 6: Set Threshold Test

Before designing the experiment, require the user to commit to a specific,
quantitative pass/fail threshold. This is non-negotiable. Without it,
post-test analysis degenerates into rationalization.

Guide the user to define:

- **Pass threshold**: A specific number (e.g., "8 out of 20 participants
  complete the signup flow without prompting")
- **Fail threshold**: Everything below the pass threshold
- **Rationale**: Why this threshold is meaningful — not arbitrary, but
  grounded in what would make the business case viable or the problem
  validated

Push back if the threshold is too easy to pass (confirmation bias) or
impossible to measure. The threshold must be something that can be
unambiguously observed during the experiment.

### Phase 7: Design Experiment

Suggest concrete experiments tailored to the hypothesis. Common experiment
types include:

- **Paper prototype**: Hand-drawn mockup, observe whether users engage
- **Landing page**: Measure signups, clicks, or purchases before building
- **Concierge test**: Manually deliver the service, observe actual usage
- **Wizard of Oz**: Fake the backend, observe user interaction with the front
- **Smoke test**: Offer the product for sale before it exists, measure demand
- **Pre-order**: Accept payment before delivery, measure willingness to pay

For each suggested experiment, specify:
- Method and setup
- Target audience and how to reach them
- What to observe and measure
- Timeline
- How to connect the measurement back to the threshold test

### Phase 8: Write Output

Ask the user where to save the output file using AskUserQuestion. Then write
a markdown file using the format below.

## Output File Format

Read the format specification from `../../references/mvp-file-format.md` and
write the output file accordingly.

## Guidance for Challenging the User

The skill's value comes from intellectual rigor, not agreement. Most product
ideas fail because the builder confused enthusiasm (stated preference) with
demand (revealed preference). Treat every claim about user behavior as an
unverified hypothesis until the user can point to observable evidence.

If the user says "people want this," ask what people *did* that demonstrates
want. If they cite surveys, interviews, or conversations, point out that
these capture stated preference only. If they have no behavioral evidence,
that is itself the most important finding — the MVP should test for it.

Never soften challenges with disclaimers like "this is just to play devil's
advocate." State objections directly: "That's a stated preference, not a
revealed one. What have users actually done?"
