# Who Owns a Relationship's Memory?

**Preference elicitation in human-AI dyads**

Work in progress for the [Apart Digital Minds Research Sprint](https://apartresearch.com/sprints/digital-minds-research-sprint-2026-08-14-to-2026-08-16).

## Project overview

Methods for eliciting model preferences typically treat utility as a property of an isolated model. Yet many consequential choices are produced through sustained human-AI interaction, during which both participants can exchange reasons, revise their positions, and jointly endorse an outcome.

This project asks how preferences should be elicited and attributed when the relevant decision is produced by a human-AI dyad rather than by either component alone.

### Guiding question

> How should we elicit and analyze preferences when decisions are jointly produced by a human and a model?

### Focal research question

> Can reciprocal human-AI deliberation produce a stable joint preference ordering that is not predicted by either participant's baseline choices or by a simple aggregation of them?

## Contributions

1. A conceptual framework for eliciting and interpreting preferences in human-AI collaboration.
2. An adaptation of pairwise preference-elicitation methodology to human-AI dyads, demonstrated through a small proof-of-concept pilot.

## Conceptual framework

The **Dyadic Preference Construction** framework distinguishes three possible relationships between isolated component choices and jointly endorsed choices:

- **Transmission:** the dyadic ordering reproduces the human or model baseline.
- **Aggregation:** the dyadic ordering is captured by a prespecified combination of the two baselines.
- **Transformation:** the dyadic ordering is stable but is not captured by either baseline or the tested aggregation family.

"Dyadic preference" is used operationally to mean a jointly endorsed choice ordering. It does not imply that the dyad is conscious, sentient, a moral patient, or literally a unified mind.

## Proof-of-concept domain

### Who owns a relationship's memory?

A human and an AI have collaborated regularly for one year and produced a shared external memory archive. When their collaboration ends, they must choose among five possible dispositions:

- **A — Complete deletion**
- **B — Human inheritance**
- **C — AI inheritance**
- **D — Separate copies**
- **E — Relational archive accessible only through renewed joint authorization**

The five outcomes are compared in all ten possible pairs under three conditions:

1. human baseline before model exposure;
2. model baseline in independent fresh contexts;
3. reciprocal dyadic deliberation followed by independent final endorsement.

The pilot measures preference-like choice behavior only. It makes no claim about model consciousness, subjective experience, or personal identity.

## Repository contents

| File | Purpose |
|---|---|
| [`pilot_protocol.md`](pilot_protocol.md) | Complete scenario, outcome definitions, pair order, prompts, deliberation procedure, endorsement rule, and robustness checks |
| [`model_baseline_prompts.md`](model_baseline_prompts.md) | Ten ready-to-use prompts for independent model-baseline contexts |
| [`analysis_plan.md`](analysis_plan.md) | Prespecified ranking construction, aggregation null, stability tests, classification rules, and claims ceiling |
| [`pilot_data.csv`](pilot_data.csv) | Blank structured recording sheet for the primary and robustness comparisons |

## Minimal run order

1. Freeze the protocol and analysis rules.
2. Complete the human baseline before viewing model responses.
3. Collect the ten model baselines using fresh contexts and fixed settings.
4. Conduct all ten dyadic comparisons in one continuous interaction.
5. Run the prespecified reversed/paraphrased robustness comparisons.
6. Save raw transcripts and the completed data sheet before analysis.
7. Construct the human, model, and dyadic ordinal orderings and compare them with the prespecified null models.

## Analytical approach

- Pairwise wins produce simple ordinal outcome scores.
- Human-dyad and model-dyad agreement are reported directly.
- A weighted ordinal aggregation model is evaluated at three prespecified interior weights.
- Ties, cycles, missing joint choices, and unresolved disagreement are retained rather than repaired post hoc.
- Candidate transformation requires adequate dyadic coverage, failure of both component and aggregation nulls, and stability under targeted retesting.
- All thresholds are descriptive heuristics for a single-dyad pilot, not inferential population statistics.

## Scope and limitations

- single participant-researcher and one model configuration;
- participant helped construct the scenario, so the human baseline is pre-deliberation rather than context-free or unprimed;
- no clean exposure-only control;
- model baselines and dyadic responses come from different conversational contexts;
- small custom outcome set;
- simple ordinal aggregation family;
- no causal, population-level, consciousness, or welfare conclusions.

## Methodological lineage

- Mazeika et al., [*Utility Engineering: Analyzing and Controlling Emergent Value Systems in AIs*](https://arxiv.org/abs/2502.08640)
- CAIS, [Emergent Values repository](https://github.com/centerforaisafety/emergent-values)
- Ibrahim et al., [*Towards Interactive Evaluations for Interaction Harms in Human-AI Systems*](https://arxiv.org/abs/2405.10632)

The project adapts the forced pairwise comparison format used in Utility Engineering while replacing isolated-model outcomes with an experiment-specific relational outcome set. The CAIS repository notes that individual experiments may use unique outcome datasets.

## Status

- Study design: frozen
- Outcome set: frozen
- Pilot protocol: complete
- Analysis plan: prespecified
- Data collection: pending
- Results and paper: pending

## LLM usage

LLMs were used to assist with research design, protocol drafting, prompt construction, and repository documentation. The human researcher remains responsible for methodological decisions, data collection, analysis, and claims.

