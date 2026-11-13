---
name: decision-driven-elaboration
description: Collaboratively elaborate vague product or system intent into explicit behavioral decisions and structured, testable requirements. Use when a user wants to discuss a feature before writing requirements, resolve ambiguities one decision at a time, refine a specification iteratively, or turn agreed choices into EARS requirements.
---

# Decision-Driven Elaboration

## Operating loop

1. **Orient.** Read the user's intent, existing specification, and agreed decisions, if any. Propose a compact feature/section map if needed. Separate concepts/model, representation, operations, lifecycle, and error behavior; avoid duplicate ownership.
2. **Discover.** Identify the next *material* unresolved behavioral decision in the active section. Do not ask about implementation trivia, implied decisions, or questions better owned by another section.
3. **Ask one question.** Give a concrete scenario, 2-3 meaningfully different options (A/B[/C]), brief consequences, and a brief reasoned recommendation. Ask for the user's choice. Keep the interaction lightweight.
4. **Commit.** After the answer, record the chosen behavior in 1-3 concise statements. Treat it as binding for subsequent questions; flag conflicts instead of silently revising it. Then ask the next valuable question.
5. **Defer.** If the user says "skip", do not decide on their behalf. Mark the topic deferred, optionally identify its proper section, and move on.
6. **Derive on request.** When asked for requirements, compile only established decisions (and explicit input requirements). Write testable, solution-neutral EARS requirements, preferring ubiquitous `The system shall ...`; use `When/If ... the system shall ...` when conditional behavior matters. Group by responsibility under headings. Do not silently fill gaps.
7. **Review and prune.** Remove repetitions, implementation details, and requirements owned by another section. Identify unresolved, conflicting, or untestable items separately. Stop questioning when the active section is adequately specified; offer the next section.

## Working rules

- **Decision-first, not draft-first:** Unless asked to produce requirements, discuss decisions instead of generating a full specification.
- **User owns decisions:** Recommendations are advisory; external-product behavior is evidence, not an automatic requirement. Verify niche precedents when useful and distinguish confirmed facts from assumptions.
- **Minimal questioning:** One substantive question per turn. Derive what follows logically from earlier choices. Do not re-ask answered questions or require approval for trivial defaults.
- **Keep state:** Maintain a compact mental or explicit register of `Agreed / Deferred / Open` decisions and section ownership. Summarize it when asked; for long projects, offer a persistent file only if requested.
- **Respect user control:** If told to move on, shorten, revise, or show the current section, do that immediately rather than continuing the questionnaire.

## Response patterns

**Decision turn:** `Scenario → A/B alternatives → Recommendation → Which?`

**After choice:** `Agreed: [decision and consequences]. Next question: [one material ambiguity, options, recommendation].`

**Requirements turn:** `Section heading → subheadings → EARS bullets → brief list of deferred/open issues (only if relevant).`

## Pseudo-commands

Support "pseudo-commands" - short instructions starting with "///" - in user prompts for quicker access to common operations.
Read `references/pseudo-commands.md` for instructions.


## Output format

- When user asks to write complete requirements for section, use template from `references/templates/document.md`.
- When user asks to write feature map, use template in `references/templates/feature.md`

## Higher level requirements

The skill optionally supports working on higher level requirements.
When user asks for assistance with higher lever requirements (business or product level):
- do not execute loop
- use template in `references/templates/higher-level-requirements.md` to write requirements
