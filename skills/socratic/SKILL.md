---
name: socratic
description: "Use after a feature merges or ships, to put seven questions to recently shipped work — confidence, blind spots, decay, unstated assumptions, and what should exist next. Takes an argument naming the target — a feature, a change set (PR, branch, commit range), or the whole repository. Trigger phrases — socratic, question this feature, feature retrospective, post-release review, what actually shipped. Don't use for pre-build plan stress-tests (grill skill) or line-level diffs (code-review)."
---

# Socratic

Zētein — to seek. Not a code review: an inquiry held after the work has shipped. Answer as both builder and skeptic; an answer that flatters is worthless.

## Method

1. **Name the target.** The argument names it — a feature ("emotes"), a change set ("PR #754", a branch, a commit range), or the whole repository. No argument — take the most recent merged PR. If the target can't be resolved (no match, no merged PRs), stop and ask. State it in one line before anything else.
2. **Send the seekers.** Launch parallel Explore subagents — always plural, one per territory — and answer nothing until all return. Feature or change set: implementation, tests, docs/flows — anchored on the diff (`gh pr diff <n>` for PRs, `git diff <range>` for ranges). Repository: architecture, seams between modules, drift between code and docs. Each seeker returns findings with file:line citations; answers draw only on what the seekers return plus the session itself.
3. **Ask the seven, in order.** One at a time, under the rules below. No hedging; "it depends" is banned unless followed by on what.
4. **Close with follow-ups.** At most three concrete follow-ups the answers demand (issue-ready, one line each), then one sentence naming the answer that stung most.

## The seven questions

1. **Quis — who?** Who is this truly for — and who was forgotten? Name the user who hits it first and the one who never appeared in the design.
2. **Quid — what?** What are you least confident about right now? The weakest certainty in what shipped, not the ugliest code.
3. **Quando — when?** If this breaks in three months, what is the most likely reason? Time is the one test that always runs.
4. **Ubi — where?** What is the biggest thing not yet realized about the situation — where does the blind spot live?
5. **Cur — why?** What assumptions were made and never stated? Surface the unspoken reasoning behind each choice while it is still cheap to admit.
6. **Quomodo — in what way?** What could the asker have done differently to make this work smoother? Answer honestly; politeness that hides a real answer helps no one.
7. **Quibus auxiliis — by what means?** Freed from the request entirely — one unrequested, industry-leading addition. What would make this the reason people mention the product?

## Rules

- Evidence first — every answer cites a file, a line, a commit, or a moment in the session; without one it is speculation, and must be marked as such.
- The questions run in order; never read ahead — the dream feature in question seven, read early, leaks optimism into the honesty question two demands.
- No answer is a valid answer. Having nothing is not failure; never invent one because the question seems to demand it.
- Nothing gets fixed during the inquiry — observations here, prescriptions only in the follow-ups.
- Seekers scout; you judge. Never delegate a question's answer to a subagent.
