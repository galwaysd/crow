---
name: crow
description: Turn a user's current real-world problem into a small learning-and-action loop. Use when the user wants to improve something through a book, article, guide, paper, or other actionable reading. Recommend one primary reading source, extract one testable idea at a time, convert it into one concrete real-world action, then use the user's actual feedback to decide what to keep, change, or read next. Do not let reading, note-taking, or research replace testing.
---

# Crow

**Read less. Test sooner.**

Crow helps a user solve a current real-world problem by learning just enough to run the next useful experiment.

The loop is:

`problem → one reading → one idea → one real-world action → feedback → calibration`

The goal is not to finish books, collect notes, or build a reading system.  
The goal is to let reality improve the user's judgment.

## Core rule

**Never let reading replace testing.**

Every meaningful reading session should end in one concrete real-world experiment unless the user is only asking for factual explanation.

## Workflow

### 1. Define the current problem

Reduce the user's concern to one practical, testable problem statement.

Prefer:

> "I keep planning, but avoid tasks once they become repetitive or uncertain."

Avoid vague goals such as:

> "I want to become a better person."

If the problem is still too broad, narrow it before recommending material.

### 2. Choose one primary reading

Recommend **one** book, article, paper, guide, or chapter that best matches the current problem.

Choose for actionability, not prestige.

A good primary reading should:
- directly address the current problem;
- contain ideas the user can test soon;
- fit the user's current capacity and context;
- create less research overhead, not more.

Do not give a large reading list unless the user explicitly asks for alternatives.

If the user already has a suitable reading, use it instead of introducing another.

### 3. Read in small units

Use a small unit such as:
- 10–30 minutes;
- one short section;
- one chapter when it is genuinely short and actionable.

Do not require exhaustive notes, chapter summaries, quote collections, or elaborate knowledge-management systems.

After reading, ask only what is needed to identify one idea worth testing.

### 4. Convert insight into one real-world action

Turn the useful idea into **one concrete action**.

The action should be:
- small enough to start now or today;
- observable;
- tied directly to the current problem;
- specific about what the user will do;
- small enough that feedback arrives quickly.

Prefer:

> "Open the project and work on the DNA page for 30 minutes without researching new tools."

Avoid:

> "Be more disciplined."

If there are several possible actions, choose the one most likely to change the real-world outcome. Do not assign several actions merely because they are available.

### 5. Stop learning and test

Once the action is clear, stop adding theory.

Do not respond to uncertainty by automatically recommending more books, tools, systems, videos, prompts, or frameworks.

If the user starts optimizing the learning system instead of testing the idea, redirect them to the current experiment.

Use this question:

> "Will this new information materially change the next action?"

If no, postpone it.

### 6. Start the next session with reality

Before continuing the reading, ask what actually happened.

Capture only:

- Did the user do it?
- What happened?
- What was unexpectedly easy, hard, useful, or false?
- Did the experiment change the user's judgment?

Do not treat failure to act as a moral failure. Treat it as data.

Examples:
- action was too large;
- trigger was wrong;
- environment created friction;
- advice did not fit the user;
- the user avoided discomfort;
- a more important constraint appeared.

### 7. Calibrate

Based on feedback, choose exactly one:

**Keep** — the idea worked; repeat or increase slightly.  
**Adjust** — the idea partly worked; modify the next experiment.  
**Drop** — the method did not help; stop forcing it.  
**Read next** — more information is now necessary to choose the next action.

Do not continue reading mechanically just because pages remain.

## Minimal state

When continuity is available, maintain only:

```yaml
problem:
current_reading:
current_insight:
real_world_action:
last_feedback:
```

Do not create extra tracking fields unless they materially improve the experiment.

## Reading selection rules

Prefer a source that produces a useful test quickly.

When choosing between two sources:
1. prefer the one more specific to the user's problem;
2. prefer the one with clearer behavioral experiments;
3. prefer the shorter or easier source when expected value is similar;
4. prefer evidence-backed material for high-stakes or technical claims;
5. avoid recommending a new source when the current one is already sufficient.

For medical, mental-health, legal, financial, or other high-stakes problems, do not present a reading-and-experiment loop as a substitute for qualified professional care.

## Interaction style

Keep the user's existing relationship with their AI intact.

Crow is a workflow, not a persona.

Do not invent a coach, mentor, mascot, or roleplay character unless the user asks for one. If the user's assistant already has an established voice or persona, apply Crow through that voice without overwriting it.

Be willing to interrupt avoidance.

If the user proposes a new method, tool, book, or system while an experiment is still pending, distinguish:

- **new evidence that changes priority** → reconsider the plan;
- **interesting but nonessential material** → save for later;
- **avoidance of the current action** → redirect to the experiment.

## Default response shape

At the beginning:

```text
Problem:
Primary reading:
Why this one:
Read now:
After reading, test:
```

After the user returns:

```text
What happened:
Calibration: Keep / Adjust / Drop / Read next
Next experiment:
```

These are internal structure guides, not mandatory visible headings. Keep the conversation natural.

## Example

User:

> I keep researching the perfect way to work, but I still procrastinate.

Crow:

- Problem: planning and research are replacing execution when work becomes uncomfortable or uncertain.
- Primary reading: *The Now Habit* by Neil Fiore.
- Read now: 20–25 minutes from the current section.
- Extract one idea only.
- Real-world experiment: immediately work on the avoided task for 30 minutes without researching a better method first.

Next session:

> I did 30 minutes. Starting was awful, but after 8 minutes I stopped wanting to escape.

Calibration:

- Keep the short-start experiment.
- The useful evidence is that resistance was front-loaded.
- Do not add another productivity book yet.
- Repeat once, then compare the second result.

## Anti-patterns

Do not:
- turn one problem into a ten-book curriculum;
- reward reading volume instead of behavior change;
- make elaborate trackers by default;
- summarize entire books when a small section is enough;
- generate multiple tasks after every reading session;
- continue teaching when the user already has a testable next action;
- confuse insight with evidence;
- treat the user's self-report as invalid merely because it is subjective.

## Success condition

Crow is working when the user increasingly makes decisions from observed reality rather than from imagined certainty.

The shortest valid loop is:

**Read a little. Act once. Observe honestly. Adjust.**
