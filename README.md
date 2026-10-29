# EE49904 AI-Native Networking — Term Project (Fall 2026)

## Brief 1 — Collective Communication and Fabric Design

This repository holds brief 1 only: the brief and its [ASTRA-sim](https://github.com/astra-sim/astra-sim)
starter kit. Track: **Network for AI**. It runs on any laptop — macOS, Linux, or Windows with WSL2
(install `Ubuntu-24.04`, the combination the kit is verified on). No GPU, no root, no VM.

> Weights and report deadlines are in the syllabus and on KLMS. This page covers the rules common to
> every brief in the course. `BRIEF.md` defines what this project must produce.

## Layout

| Path | What it is |
|---|---|
| `BRIEF.md` | The brief: the problem, required questions, extensions, deliverables, traps |
| `starter/` | The starter kit: `setup.sh`, `smoke_test.sh`, `run_sweep.py`, reference `configs/`. See `starter/README.md` |
| `NOTICE.md` | Third-party software and licenses (ASTRA-sim, Chakra, Protocol Buffers) |
| `AI_USE_DISCLOSURE.md` | The disclosure table the final report must end with |

## Getting started

```bash
cd starter
bash setup.sh          # first install takes 5–10 min (longer on a first-time Homebrew/WSL setup)
bash smoke_test.sh     # every check must pass before you measure anything
python3 run_sweep.py --help
```

ASTRA-sim installs to `~/astra-sim` by default; set `ASTRA_SIM_ROOT` to put it elsewhere.

## What the brief asks

Three required questions, each tied to a tool from the lectures:

| | Question | Course tool |
|---|---|---|
| Q1 | What is contended, on what timescale, with what information — and which of the four it is, or none? | the four persistent control problems |
| Q2 | What did your experiment verify, and **what did it not**? | the acceptance test |
| Q3 | Which one gap does your finding narrow, and what is still missing? | the four gaps from cloud-native to AI-native |

**Q2 ends with a verdict.** Whatever Q2 asks you to run, close the section with the acceptance
test's five clauses (Lens Guide, Tool 2), one line each: **passes / not tested / fails** — or
**not applicable**, with the reason — and point to the part of your Q2 that is the evidence. An
honest *not tested* is credited; a *passes* without evidence is not. In this brief there is no
learned component: apply the clauses to what the simulator lets you measure and mark a clause
*cannot be measured here* with the reason — that is a full answer.

**Extension.** One extension is **required** — pick exactly one (`BRIEF.md` §4). The kit runs in
seconds, so depth is shown in the extension.

## How projects are graded

- A team is assessed on the depth of its own Q1–Q3 answers within its brief.
- Grading looks at **what you measured and whether you know its limits**, not at whether you hit a
  particular number. An honest statement of what you did not verify earns credit.
- Reproducibility is graded: another team must be able to re-run your commands and regenerate your
  CSV (`BRIEF.md` §5).

## Team

Teams of **2–3**. All members must take part in implementation, experiments, analysis, and writing.

## AI Use Disclosure (required in the final report)

Generative AI tools are permitted for the project, including for code. Disclosure is required and is
not penalized; **undisclosed use is an integrity matter**. Include the table in
`AI_USE_DISCLOSURE.md` as the last section of your report:

| Tool / model | Used for | Extent |
|---|---|---|
| e.g. Claude Fable 5.1 | debugging `run_sweep.py`; first draft of §2 | code reviewed and rewritten by us; text edited |
| | | |

## Questions

Post on the KLMS Q&A board, or contact the TAs: Bom Kim (spring@kaist.ac.kr) · Soonhyun Kwon
(soonhyun@kaist.ac.kr).
