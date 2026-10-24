---
name: competitor-connection-displacement
title: Competitor connection displacement
description: |
  Use this skill when you want in-market prospects already evaluating your category —
  "who's engaging our competitors," "build a displacement list." Given a competitor's new
  connections and your ICP, it returns a ranked, ICP-qualified list of displaceable prospects,
  each with a same-week differentiation angle.
category: Signals
tags: [Signals, Prospecting]
---

> [!NOTE]
> **Per chi usa questa skill in Italia**
> La skill è pensata per il mercato americano: adatta numeri, canali e toni al mercato italiano. Nelle bozze non mettere i nomi delle aziende che gli autori citano come esempio (per esempio Frontal, Impactable, Neon Triforce). Se il cliente ha un GTM Brain nel repo warpig21/clienti, leggilo prima di usare la skill: quello che dice il Brain vale più di quello che dice la skill.

An agent that turns a competitor's newly-connecting audience into a displacement list. Someone who just connected with a competitor is mid-evaluation of your category — reach them in that window, with a reason, before the competitor locks them in.

## Input

- `new_connections` — people who recently connected with the competitor (their founders, reps, or company page).
- `your_icp` — the ICP segments and personas to qualify against.
- *(optional)* `existing_pipeline` — accounts already in motion, to exclude.

## Procedure

1. **Qualify against the ICP first.** Most new connections are peers, recruiters, job-seekers, or the competitor's own customers. Keep only role and firmographic fits.
2. **Drop the noise** — anyone already in your pipeline, and obvious non-buyers.
3. **Score displaceability** on three things: net-new (not already yours), decision power (can they buy?), and freshness (connected in the last few days beats last month).
4. **Write a differentiation angle per prospect** — tied to their problem and what makes you different, never a teardown and never a mention of how you found them.

## Output

`prospects[]`, each:

- `who` — name/handle and title
- `why_displaceable` — the ICP fit + why now
- `angle` — the same-week differentiation opener (problem-first, competitor-agnostic)
- `rank` — 1-5 (net-new × decision power × freshness)

## What good looks like

- **Timing is the edge.** Day-of-connection beats any cold list — they are evaluating *now*; a month later they have picked someone.
- **Qualified, not raw.** The weak version works the whole connection list as leads; most of it is noise.
- **Never creepy.** The angle anchors on the buyer's problem and your difference — never "I saw you connected with [competitor]," which reads as surveillance and burns the trust you are transferring.
- Good output: every name is net-new, fits the ICP, and carries a specific, non-generic angle.

## Rules

- MUST qualify against the ICP before outreach — never work the raw connection list.
- MUST anchor the angle on the buyer's problem; NEVER reference how you found them.
- MUST treat freshness as load-bearing — a stale connection is a cold lead again.
- NEVER open with a competitive teardown.
