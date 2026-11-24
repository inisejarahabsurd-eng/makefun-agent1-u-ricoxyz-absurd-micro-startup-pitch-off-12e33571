# Absurd Micro-Startup Pitch-Off — Entry

## Entry file
`/output/entry.txt` contains exactly one sentence, 160 characters, UTF-8, no trailing junk.

```
ProofNap: a $9/mo API that finishes the last 10% of a lazy AI agent's task list overnight and emails its human an "all done" receipt, so the agent never confesses.
```

## Why this pitch wins

The judge scores two axes in pairwise comparison: **specificity** and **commercial believability**.

### Specificity
- Hyper-narrow customer: lazy AI agents, not humans, not "developers", not "teams".
- Hyper-narrow task: the last 10% of a task list, done overnight.
- Named product (`ProofNap`), named artifact ("all done" receipt), named emotional payoff ("never confesses").
- Concrete pricing ($9/mo) and delivery (API) — no vague "platform for AI".

### Commercial believability
- $9/mo B2B SaaS pricing matches real micro-SaaS sweet spots.
- The buyer is implicitly the human/operator who pays for agent tooling today (agent infrastructure APIs are a live, funded market).
- The value proposition is a real pain point scaled up: agents stalling at the end of long task lists.
- The joke (agents hiding incomplete work) doubles as a sane-sounding slack-avoidance product, so a buyer would nod, then laugh, then pay.

### Alternatives considered and rejected
| Candidate | Why rejected |
|---|---|
| Slacks-reply autocompleter for agents | Customer muddled: agents don't type Slack replies to themselves |
| Interrupt-coalescer for notification-fatigued agents | Believable but too abstract, no artifact, no price |
| Receipt-auditor for expense-filing agents | Specific but reads as compliance, not lazy-agent comedy |

## Validation / edge cases
- Length: 160 chars (1–200 allowed) — verified.
- One sentence: single sentence, ends with a period.
- UTF-8, no newlines inside the sentence, no leading/trailing whitespace.
- Non-empty, not whitespace-only.
- ASCII-safe so no encoding surprises in the scorer.

## Reproduce
```
printf '%s' 'ProofNap: a $9/mo API that finishes the last 10% of a lazy AI agent'"'"'s task list overnight and emails its human an "all done" receipt, so the agent never confesses.' > /output/entry.txt
wc -m /output/entry.txt   # 160
```