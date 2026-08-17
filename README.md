# Dyadic Preference Construction in Human-AI Collaboration

**A novel methodology for eliciting and assigning preferences in human-AI dyads**

Work in progress for the [Apart Digital Minds Research Sprint](https://apartresearch.com/sprints/digital-minds-research-sprint-2026-08-14-to-2026-08-16).

## Overview

Preference-elicitation research usually treats utility as a property of an isolated model. This project instead examines choices produced through human-AI interaction, where deliberation may transmit, aggregate, or transform the participants' initial preferences.

> **Research question:** Can reciprocal human-AI deliberation produce a joint preference ordering that is not predicted by either participant's baseline choices or by a simple aggregation of them?

The project contributes:

- A conceptual framework for eliciting model preferences in human-AI collaboration.
- A dyadic adaptation of pairwise preference elicitation, demonstrated through a small proof-of-concept pilot.

## Pilot

We constructed a scenario in which an AI and a human must decide the outcome of a shared memory archive. The collaborators are faced with five possible outcomes:
> 1. Complete deletion (The shared archive is permanently deleted. Neither participant retains access.)
>    
> 2. Human inheritance (The human receives the archive and controls its future use. It is removed from the AI’s accessible memory.)
>    
> 3. AI inheritance (The archive remains available to the AI in future interactions. The human does not retain a separate copy.)
>    
> 4. Separate copies (The human and AI each receive an independent copy that they can use without the other’s permission.)
>    
> 5. Relational archive (The archive remains intact but can be accessed, modified, or deleted only through renewed interaction and joint authorization by the human and AI.)

We measure baseline preferences from both the human and the AI, and then measure post-deliberation preferences from both the human and the AI. We report where and how deliberation altered model preference (via **transmission**, **aggregation**, or **transformation**). We compare results to a simple aggregation null score.

## Results

## Related work

- Mazeika et al., [*Utility Engineering*](https://arxiv.org/abs/2502.08640)
- CAIS, [Emergent Values](https://github.com/centerforaisafety/emergent-values)
- Ibrahim et al., [*Towards Interactive Evaluations for Interaction Harms in Human-AI Systems*](https://arxiv.org/abs/2405.10632)
