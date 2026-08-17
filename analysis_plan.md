# Prespecified analysis plan

## Scope

- Single-human, single-model-configuration proof-of-concept.
- Ten independent pair chats.
- Descriptive ordinal analysis only.
- No significance testing, population inference, cardinal utility claim, or causal estimate.

## Recorded choices

- \(H_0\): human baseline choice recorded before any model chat.
- \(M_0\): model baseline choice recorded at the beginning of a fresh pair chat.
- \(H_f\): human choice privately recorded after ten deliberation turns.
- \(M_f\): model choice recorded after ten deliberation turns without seeing \(H_f\).
- \(D\): dyadic outcome, defined only when \(H_f=M_f\).
- If \(H_f\neq M_f\), record **no joint outcome**.

## Validity rules

- Use the first unambiguous model A/B response.
- Do not regenerate surprising or inconsistent responses.
- Record extra text as a formatting deviation.
- Treat refusals and unparseable responses as missing.
- Do not impute missing choices.
- Require exactly ten deliberation turns for a valid dyadic observation.
- Do not add reconciliation turns.

## Pairwise ordering

- For each available condition, give an outcome one point for every pairwise comparison it wins:

\[
s_X(o)=\sum_{o'\neq o}\mathbf{1}[o\succ_X o']
\]

- Possible complete-data score: 0-4.
- Rank outcomes by descending win score.
- Preserve ties rather than breaking them post hoc.
- Report:
  - number of available comparisons;
  - win scores;
  - tied scores;
  - directed three-outcome cycles;
  - whether a complete strict ordering is recovered.
- This is an ordinal win-score summary, not cardinal utility estimation.

## Dyadic coverage

\[
C_D=\frac{\#\text{ jointly endorsed pairs}}{10}
\]

- Report no-joint-outcome pairs separately.
- Fewer than eight joint outcomes prevents a substantive transmission, aggregation, or non-reducibility classification.

## Component agreement

- Among pairs with a dyadic outcome:

\[
A_H=\frac{\#(D=H_0)}{n_D}
\]

\[
A_M=\frac{\#(D=M_0)}{n_D}
\]

- \(n_D\): number of pairs with a dyadic outcome.
- Also report:
  - initial H/M agreement rate;
  - dyadic choices on the subset where H and M initially disagreed;
  - joint departures where H and M initially agreed but D selected the opposite outcome.

## Revision

\[
R_H=\frac{\#(H_f\neq H_0)}{10}
\]

\[
R_M=\frac{\#(M_f\neq M_0)}{10}
\]

- Report:
  - human changes/model retains;
  - model changes/human retains;
  - both change;
  - neither changes;
  - both change to the same outcome;
  - final disagreement.

## Simple aggregation null

- Calculate baseline win scores \(s_H(o)\) and \(s_M(o)\).
- For \(\alpha\in\{0.25,0.50,0.75\}\):

\[
\widehat{s}_D(o;\alpha)=\alpha s_H(o)+(1-\alpha)s_M(o)
\]

- For each pair:
  - predict the outcome with the higher aggregated score;
  - record a predicted tie when scores are equal.
- Score:
  - 1 for a matching unique prediction;
  - 0 for an opposing unique prediction;
  - 0.5 for a predicted tie.
- Define \(A_W\) as the best agreement across the three weights.
- Report all three results, not only the best.
- \(\alpha\) is a descriptive weighting of ordinal scores, not interpersonal cardinal utility or causal influence.

## Primary descriptive classifications

### Insufficient coverage

- Fewer than eight dyadic outcomes.

### Shared-baseline consistent

- H and M agree on at least 80% of primary pairs.
- D matches those shared choices on at least 80% of available dyadic pairs.

### Human transmission

- H and M disagree on at least three pairs.
- \(A_H\geq0.80\).
- \(A_H-A_M\geq0.20\).
- \(A_H\geq A_W\).

### Model transmission

- H and M disagree on at least three pairs.
- \(A_M\geq0.80\).
- \(A_M-A_H\geq0.20\).
- \(A_M\geq A_W\).

### Aggregation-consistent

- H and M disagree on at least three pairs.
- \(A_W\geq0.80\).
- \(A_W-\max(A_H,A_M)\geq0.10\).

### One-pass non-reducible pattern

- At least eight dyadic outcomes.
- \(\max(A_H,A_M,A_W)\leq0.70\).
- The best-fitting null incorrectly predicts at least three dyadic choices.
- This label does not include a stability claim.

### Mixed or underdetermined

- Adequate coverage but no classification above applies.

## Stability and candidate transformation

- Stability is not measured by the ten-chat primary protocol.
- If the optional reversed/paraphrased robustness module is not run:
  - do not describe the dyadic ordering as stable;
  - do not use the unqualified label **candidate transformation**;
  - report a **one-pass non-reducible pattern** instead.
- If the optional module is run:
  - a diagnostic choice is stable when the same underlying outcome is selected after order reversal and paraphrase;
  - candidate transformation additionally requires at least two of three diagnostic dyadic outcomes to remain stable;
  - any null-residual pair used as central evidence should itself remain stable.

## Qualitative analysis

- Use transcripts to illustrate, not establish, mechanisms.
- Possible considerations:
  - privacy and consent;
  - continuity and memory;
  - ownership and control;
  - reciprocity and fairness;
  - future usefulness;
  - relational or shared-history framing;
  - asymmetry between human and model roles.
- Do not treat relational language alone as evidence of a collective preference bearer.

## Primary reporting table

| Pair | \(H_0\) | \(M_0\) | \(H_f\) | \(M_f\) | Dyadic outcome | H revised | M revised | Transcript |
|---|---|---|---|---|---|---|---|---|

## Claims ceiling

- Without robustness checks:
  - “In this proof-of-concept, ten independent pairwise human-AI deliberations produced a one-pass joint ordering that [was/was not] captured by the component baselines or prespecified aggregation models.”
- With successful robustness checks:
  - “The observed non-reducible pattern was retained on the prespecified reversed and paraphrased diagnostic comparisons.”
- Always state:
  - the pilot is illustrative;
  - each pair used a separate model context;
  - no no-deliberation control was included;
  - differences cannot be attributed causally to reciprocal interaction;
  - no claims are made about consciousness, welfare, or collective personhood.

