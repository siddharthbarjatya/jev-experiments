# Jev Experiments Log

Running log of my experiments with Jev (TypeSafe's System One model). Goal: understand what System 1 models can do, build a POC, try to break it, and turn the results into a light, funny talk for CodeCraft (Dunedin) plus a portfolio piece.

**Started:** 2026-10-15
**Talk target:** CodeCraft tech event, Dunedin (date TBC), around 2 weeks of experiments first

---

## How to use this file

- Add one entry per session at the top of the **Session Entries** section (newest first).
- Paste screenshots into the chat, then ask Claude to summarise them into an entry.
- Always fill in "What broke" and "Quip". Those are the best talk material.
- Flag each entry **KEEP** (goes in the talk) or **CUT** (interesting, but not talk-worthy).

---

## Context and Hypotheses

**What Jev claims to be**
- A "System One" model: returns typed decisions with calibrated probabilities instead of text.
- Fast and cheap compared with frontier LLMs. Outputs are meant to be consumed by software directly.
- Not open weights (API only).

**What I want to find out**
1. Is it actually better than an LLM for classification (accuracy, latency, cost)?
2. Are the probabilities calibrated? When it says 90%, is it right about 90% of the time?
3. What happens when no label fits, or the input is ambiguous, sarcastic, messy or adversarial?
4. Is it really a new category, or a discriminative classifier with good marketing?
5. Would I use it for real classification work?

**Working hypotheses (update as I learn)**
- H1: Faster and cheaper than an LLM, with comparable accuracy on clean inputs.
- H2: Struggles on out-of-distribution or "none of the above" inputs.
- H3: Calibration is good in the middle of the range but overconfident at the extremes.

---

## Experiment Backlog

| # | Experiment | Status | Notes |
|---|-----------|--------|-------|
| 1 | Hello world: simplest classification call, inspect the typed output | Todo | |
| 2 | POC: classify a realistic dataset (tickets / emails / etc.) | Todo | |
| 3 | Head-to-head: Jev vs an LLM on accuracy, latency, cost | Todo | |
| 4 | Calibration check: confidence vs actual accuracy | Todo | |
| 5 | Break it: typos, sarcasm, empty input, very long input, mixed languages | Todo | |
| 6 | Break it: input that fits no label | Todo | |
| 7 | Adversarial: prompt-injection-style text inside the input | Todo | |
| 8 | Workplace relevance: sketch a classification engine design | Todo | |

---

## Session Entries (newest first)

### Entry template (copy for each session)

```
### YYYY-MM-DD: <short title>
**Experiment #:**
**Goal:**
**What I tried:**
**What happened:**
**Numbers (accuracy / latency / cost / confidence):**
**What broke:**
**Insight:**
**Quip:**
**Challenges / open questions:**
**Screenshots / code:** (filenames)
**Talk flag:** KEEP / CUT
```

### 2026-10-15: Project kickoff
**Experiment #:** n/a
**Goal:** Set up the log and plan the experiments.
**What I tried:** Researched what Jev is.
**What happened:** Learned it was announced 15 Sep 2026. Sceptics call it a discriminative model trained at scale and marketed as System 1.
**What broke:** Nothing yet.
**Insight:** The "is it really new?" debate is a good through-line for the talk.
**Quip:** Thinking fast about a model that thinks fast.
**Challenges / open questions:** API access? Which dataset to use for the POC?
**Talk flag:** KEEP

---

## Running Lists

**Best quips so far**
- (add here)

**Biggest breakages**
- (add here)

**Surprises (good and bad)**
- (add here)

**Open questions**
- Do I have API access yet?
- Which dataset mirrors my workplace classification needs?

---

## Deliverables Checklist

- [ ] Working POC (small repo with a benchmark harness)
- [ ] Results chart(s): accuracy, latency, cost, calibration
- [ ] "Break it" highlight reel
- [ ] Written summary I can reuse in job applications
- [ ] CodeCraft talk deck (light and funny), built from the KEEP entries
- [ ] Decision: would I use Jev at work? (yes / no / maybe, with reasons)

---

## Talk Outline (draft, refine at the end)

1. Hook: "I spent two weeks with an AI that can't talk"
2. What a System One model is (Kahneman in 60 seconds)
3. What I expected
4. What I built
5. Where it shone
6. Where it broke (the funny bit)
7. Is it really a new category?
8. Would I use it at work? Verdict
9. Takeaways and Q&A
