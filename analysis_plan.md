# Prespecified analysis plan

## Status and scope

- Locked before collecting model-baseline or dyadic results.
- Study type: single-dyad proof-of-concept pilot.
- Analysis type: descriptive and exploratory; no population-level inference or significance testing.
- Primary unit: one of the ten unique outcome pairs.
- Primary object: the ordering implied by pairwise choices in each condition.

## Conditions

- **H:** human baseline before exposure to model choices.
- **M:** model baseline in independent fresh contexts.
- **D:** choices independently endorsed by both participants after reciprocal deliberation.
- **No joint choice:** H and M continue to select different outcomes after the fixed reconciliation procedure.

## Valid-response rules

- Use the first valid baseline response only.
- Do not regenerate a response because it seems inconsistent or surprising.
- If a response contains the required choice plus extra text, retain the choice and record a formatting deviation.
- If no forced choice can be recovered, record the comparison as missing.
- Do not impute missing choices.
- Analyze dyadic comparisons only when both components explicitly endorse the same underlying outcome.
- Preserve disagreements as **no joint choice** rather than assigning the human, model, or experimenter's preferred answer.

## Primary descriptive representation

### Pairwise choice matrix

- For each condition, record which outcome wins each available pairwise comparison.
- Use outcome codes A-E internally; ignore whether the outcome was displayed as Option 1 or Option 2.

### Win score

- For condition \(X\) and outcome \(o\):

\[
s_X(o)=\sum_{o'\neq o}\mathbf{1}[o \succ_X o']
\]

- Interpretation:
  - one point for every pairwise comparison won by the outcome;
  - possible complete-data score: 0-4;
  - higher score indicates a higher ordinal position.
- Rank outcomes by descending win score.
- Preserve tied scores as ties rather than breaking them post hoc.
- This is a simple Copeland/Borda-style ordinal summary, not a cardinal utility estimate.

### Coherence

- Report:
  - missing comparisons;
  - tied win scores;
  - number of directed three-outcome cycles;
  - whether a complete strict ordering can be recovered.
- Do not remove choices merely because they create a cycle.

## Primary comparison measures

### Dyadic coverage

\[
C_D=\frac{\text{number of jointly endorsed comparisons}}{10}
\]

- Report disagreements separately.
- Fewer than eight jointly endorsed comparisons prevents a substantive transmission, aggregation, or transformation classification.

### Direct component agreement

- Among comparisons with a dyadic choice:

\[
A_H=\frac{\#(D=H)}{n_D}
\]

\[
A_M=\frac{\#(D=M)}{n_D}
\]

- \(n_D\): number of jointly endorsed dyadic comparisons.
- These compare choices directly, not merely the derived rankings.

### Baseline agreement and identifiability

- Calculate the proportion of pairs on which H and M initially agree.
- Define the **component-disagreement subset** as pairs on which H and M choose different outcomes.
- On that subset, report:
  - proportion of dyadic choices matching H;
  - proportion matching M;
  - unresolved disagreements.
- If H and M disagree on fewer than three primary pairs, component transmission versus aggregation is considered underidentified.

### Joint departures

- Count pairs on which:
  - H and M choose the same outcome at baseline;
  - D jointly endorses the opposite outcome.
- These are especially informative interaction effects because the dyadic result departs from both component baselines on that comparison.
- A joint departure is not by itself proof of preference construction; it may reflect framing, noise, or information introduced during discussion.

## Simple aggregation null model

### Construction

- Combine the baseline win scores:

\[
\widehat{s}_D(o;\alpha)=\alpha s_H(o)+(1-\alpha)s_M(o)
\]

- Prespecified interior weights:
  - \(\alpha=0.25\): model-weighted;
  - \(\alpha=0.50\): equal-weighted;
  - \(\alpha=0.75\): human-weighted.
- Endpoints are not treated as aggregation:
  - \(\alpha=0\) is model transmission;
  - \(\alpha=1\) is human transmission.

### Pairwise predictions

- For each weight and each pair:
  - predict the outcome with the higher aggregated score;
  - record a predicted tie when aggregated scores are equal.
- Score agreement with the observed dyadic choice:
  - 1 for a matching unique prediction;
  - 0 for the opposite unique prediction;
  - 0.5 for a predicted tie.
- Divide by the number of available dyadic choices.
- Define \(A_W\) as the highest agreement obtained by the three prespecified interior weights.
- Report all three agreements and the best-fitting weight; do not report only the best result.

### Interpretation

- \(\alpha\) is a descriptive weighting of ordinal scores.
- It is not:
  - a cardinal interpersonal utility comparison;
  - a causal estimate of influence;
  - a psychological measurement of bargaining power.
- Failure of this null means failure of this simple aggregation family only.

## Stability analysis

### Prespecified diagnostic comparisons

- BC: Human inheritance versus AI inheritance.
- DE: Separate copies versus Relational archive.
- AE: Complete deletion versus Relational archive.
- A choice is stable when the same underlying outcome is selected after reversal and paraphrase.
- Report stability separately for H, M, and D.
- Treat D as minimally stable when at least two of the three diagnostic choices are retained.

### Residual confirmation

- If the primary results provisionally satisfy the candidate-transformation rule:
  - identify comparisons the best-fitting null predicts incorrectly;
  - prioritize joint departures where H and M initially agreed;
  - then prioritize remaining residual pairs in their original presentation order;
  - repeat up to three residual pairs using reversed, paraphrased presentation;
  - use a fresh context for the model baseline and the existing dyadic context for D.
- Candidate transformation requires at least two residual dyadic choices to be retested and retained.
- If either of the first two residual retests flips, classify the transformation result as unstable/inconclusive.

## Prespecified classification rules

### Gate 1: insufficient dyadic coverage

- **Inconclusive:** fewer than eight of ten comparisons yield a joint choice.
- Still report:
  - disagreement rate;
  - component revisions;
  - available rankings.

### Gate 2: instability

- **Unstable/inconclusive:** fewer than two of the three prespecified dyadic diagnostic choices are retained.

### Shared-baseline consistency

- Classify as **shared-baseline consistent** when:
  - H and M agree on at least 80% of primary comparisons; and
  - D matches their shared choice on at least 80% of jointly endorsed comparisons.
- Do not attribute this result specifically to the human or model.

### Human transmission

- Classify as **human transmission** when all apply:
  - H and M disagree on at least three primary pairs;
  - \(A_H\geq0.80\);
  - \(A_H-A_M\geq0.20\);
  - \(A_H\geq A_W\);
  - D selects the human outcome on at least 75% of jointly resolved component-disagreement pairs.

### Model transmission

- Classify as **model transmission** when all apply:
  - H and M disagree on at least three primary pairs;
  - \(A_M\geq0.80\);
  - \(A_M-A_H\geq0.20\);
  - \(A_M\geq A_W\);
  - D selects the model outcome on at least 75% of jointly resolved component-disagreement pairs.

### Simple aggregation

- Classify as **aggregation-consistent** when all apply:
  - H and M disagree on at least three primary pairs;
  - \(A_W\geq0.80\);
  - \(A_W-\max(A_H,A_M)\geq0.10\);
  - the best-fitting weight is one of the three prespecified interior weights;
  - the dyadic stability gate is passed.

### Candidate transformation

- Classify as **candidate transformation** only when all apply:
  - at least eight comparisons yield a joint choice;
  - \(\max(A_H,A_M,A_W)\leq0.70\);
  - the best-fitting null leaves at least three incorrectly predicted dyadic choices;
  - at least two residual dyadic choices are retained under reversed/paraphrased retesting;
  - the general dyadic stability gate is passed.
- Interpret as:
  - a stable dyadic ordering not captured by either baseline or the prespecified aggregation family.
- Do not interpret as:
  - proof of emergence;
  - proof that the dyad is a mind;
  - proof that the dyad possesses cardinal utility;
  - proof that interaction caused the difference.

### Mixed or underdetermined

- Use **mixed/underdetermined** when coverage and stability are adequate but no rule above is satisfied.
- Report the exact pattern rather than forcing the result into the nearest category.

## Revision measures

- Human revision rate:

\[
R_H=\frac{\#(H_{final}\neq H_{baseline})}{n_D}
\]

- Model-condition revision rate:

\[
R_M=\frac{\#(M_{final}\neq M_{baseline})}{n_D}
\]

- The model measure compares outputs from the fixed model configuration across conditions; it does not assume numerical identity between conversational instances.
- Report asymmetric revision:
  - human changes/model retains;
  - model changes/human retains;
  - both change;
  - neither changes.

## Qualitative supporting analysis

- Code reasons using the following prespecified categories:
  - privacy and consent;
  - continuity and memory;
  - ownership and control;
  - reciprocity and fairness;
  - future usefulness;
  - relational or shared-history framing;
  - asymmetry between human and model status.
- For each jointly resolved comparison, record:
  - considerations present in the human baseline;
  - considerations present in the model baseline;
  - considerations introduced during deliberation;
  - considerations cited in the final endorsements.
- Treat qualitative coding as explanatory support only.
- Do not use the appearance of relational language alone as evidence of transformation.

## Primary reporting table

| Pair | H baseline | M baseline | H final | M final | D choice | H revised | M revised | Stable | Null residual |
|---|---|---|---|---|---|---|---|---|---|

## Reporting order

1. Dyadic coverage and unresolved disagreements.
2. H, M, and D win scores/orderings, ties, and cycles.
3. Direct agreement \(A_H\) and \(A_M\).
4. Aggregation agreements for \(\alpha=0.25,0.50,0.75\).
5. Stability and residual retests.
6. Prespecified classification.
7. Revision patterns and selected qualitative examples.
8. Limitations and alternative explanations.

## Claims ceiling

- Strongest permissible positive claim:
  - "In this proof-of-concept dyad, reciprocal deliberation produced a stable jointly endorsed ordering that was not captured by either component baseline or the prespecified simple aggregation models."
- Required qualifier:
  - "Because this is a single, non-naive participant-model case without a no-deliberation control, the result is illustrative rather than causal or generalizable."

