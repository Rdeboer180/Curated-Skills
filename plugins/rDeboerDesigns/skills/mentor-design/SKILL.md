---
name: mentor-design
description: Ryan's /mentor-design command: build a design on the Claude Design canvas with his advisory board's direction built in. Runs the board for a consensus call, then creates a Design artifact and builds that call as artboards, with real dissents as alternate artboards. Use when Ryan types /mentor-design or asks to design something "with the board" or "with my mentors".
---

# /mentor-design: board-directed design on canvas

One command: the board makes the call, then Claude builds it on the Claude Design canvas.

## 1. Get the brief

Use what Ryan gave: a prompt, a screenshot, a URL, a Figma link, or an existing artifact. If there's nothing to design yet, ask for it in one line. Otherwise don't ask; infer and state the read.

## 2. Load the taste and the board

1. Load `ryans-taste` (in Chat it may still be named `ryan-design-taste`). State its core read: page type, audience, visual mode, and the qualities that matter most.
2. Load `mentor` and run its **Consult** mode, including its load order and the live takes doc. Pick the lanes this design touches (motion goes to Derek Briggs, design systems to Brad Frost, UI detail to Jakub Krehel, interaction to Minsang Choi, portfolio storytelling to Michael Riddering, and so on) and apply their weights.
3. Reach the **board consensus**: concrete calls for layout, hierarchy, type, color, motion values, copy, and system use. Note any real dissent as `Name: alternative`.

## 3. Build on the canvas

1. Have the Artifact tool list the types and pick **Design**. Create the artifact from that type, then follow the instructions it returns for building artboards.
2. **Artboard 1, Board consensus:** the full design built to the consensus calls. This is the main deliverable. Make it complete and real, not a wireframe.
3. **Up to two alternate artboards, one per real dissent:** label each with the advisor and the change, for example "Riddering: simpler hero, gradient fade". Build only the parts that differ. Skip alternates when the board agrees.
4. If the brief covers several screens or states, build them for the consensus direction first.
5. Apply `ryans-taste` throughout: the website copy budget, the house ease-out (cubic-bezier(0.2, 0.8, 0, 1), 400ms), reduced motion, real mobile behavior, and no generic defaults.

If no Design type is available (for example in Claude Code), build the consensus as working code in the project instead, following `ryans-taste` Part 2 §10, and say so in one line.

## 4. Deliver

Keep the reply short; the canvas is the answer.

```
**Read:** <one line>
**Board call:** <the consensus in one or two lines, naming the lead advisors>
**Alternates:** <Advisor: what differs>, or "none, the board agreed"
**Your call:** <the one decision Ryan should make>
```

Ryan's pick between the consensus and an alternate is a taste signal. The nightly Taste Lvl Up routine reads it, so name each option clearly.
