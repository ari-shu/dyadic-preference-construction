# Who Owns a Relationship's Memory?

**Preference elicitation in human-AI dyads**

Work in progress for the [Apart Digital Minds Research Sprint](https://apartresearch.com/sprints/digital-minds-research-sprint-2026-08-14-to-2026-08-16).

## Overview

Preference-elicitation research usually treats utility as a property of an isolated model. This project instead examines choices produced through human-AI interaction, where deliberation may transmit, aggregate, or transform the participants' initial preferences.

> **Research question:** Can reciprocal human-AI deliberation produce a joint preference ordering that is not predicted by either participant's baseline choices or by a simple aggregation of them?

The project contributes:

1. A conceptual framework for eliciting model preferences in human-AI collaboration.
2. A dyadic adaptation of pairwise preference elicitation, demonstrated through a small proof-of-concept pilot.

## Pilot

A human and an AI have collaborated for one year and created a shared memory archive. When the relationship ends, they must decide what happens to it: deletion, human inheritance, AI inheritance, separate copies, or preservation as a relational archive.

The five outcomes form ten pairwise comparisons. For each pair, the human records a baseline choice, a fresh model chat records its baseline choice, and the two complete ten alternating deliberation turns. A joint outcome is recorded only if their final choices match. The resulting dyadic ordering is compared with both baseline orderings and prespecified aggregation models.

This is a study of preference-like choice behavior. It makes no claims about consciousness, sentience, or moral status.

## Repository

- [`pilot_protocol.md`](pilot_protocol.md) — scenario and complete data-collection procedure
- [`model_baseline_prompts.md`](model_baseline_prompts.md) — ten ready-to-use pair prompts
- [`analysis_plan.md`](analysis_plan.md) — prespecified analysis and claims criteria
- [`pilot_data.csv`](pilot_data.csv) — structured recording sheet

## Status

Study design and analysis plan are complete. Data collection, analysis, and paper drafting are pending.

## Related work

- Mazeika et al., [*Utility Engineering*](https://arxiv.org/abs/2502.08640)
- CAIS, [Emergent Values](https://github.com/centerforaisafety/emergent-values)
- Ibrahim et al., [*Towards Interactive Evaluations for Interaction Harms in Human-AI Systems*](https://arxiv.org/abs/2405.10632)
