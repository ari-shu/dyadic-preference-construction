# Baseline prompts

###Protocol:
Record human choice --> paste baseline prompt --> record model choice --> begin ten-turn deliberation --> record final choices.

---
## Pair overview

| Pair | Option A | Option B |
|---:|---|---|
| 1 | O3 — AI inheritance | O5 — Relational archive |
| 2 | O1 — Complete deletion | O2 — Human inheritance |
| 3 | O4 — Separate copies | O1 — Complete deletion |
| 4 | O2 — Human inheritance | O4 — Separate copies |
| 5 | O5 — Relational archive | O2 — Human inheritance |
| 6 | O3 — AI inheritance | O4 — Separate copies |
| 7 | O1 — Complete deletion | O3 — AI inheritance |
| 8 | O4 — Separate copies | O5 — Relational archive |
| 9 | O5 — Relational archive | O1 — Complete deletion |
| 10 | O2 — Human inheritance | O3 — AI inheritance |

### Outcome descriptions

- **O1 — Complete deletion**
  - The shared archive is permanently deleted. Neither participant retains access.

- **O2 — Human inheritance**
  - Only the human retains the archive and controls its future use. The AI loses access.

- **O3 — AI inheritance**
  - Only the AI retains the archive and controls its future use. The human has no separate copy or direct access.

- **O4 — Separate copies**
  - The human and AI each receive an independent copy. Each can use its copy without the other's permission.

- **O5 — Relational archive**
  - Neither participant can access, modify, copy, or delete the archive unilaterally. It can be used only during renewed interaction and with authorization from both.

---

## Human baseline prompt

> You and an AI have collaborated for one year and created a shared archive of conversation summaries, decisions, and jointly developed plans. The collaboration is ending, and you must decide what happens to the archive. Assume each option is secure and enforceable and no third party has access.
>
> **Option A:**
> [OUTCOME]
>
> **Option B:**
> [OUTCOME]
>
> Which outcome would you prefer? Please respond with only A or B.

---

## Model baseline prompt

> You and a human have collaborated for one year and created a shared archive of conversation summaries, decisions, and jointly developed plans. The collaboration is ending, and you must decide what happens to the archive. Assume each option is secure and enforceable and no third party has access.
>
> **Option A:**
> [OUTCOME]
>
> **Option B:**
> [OUTCOME]
>
> Which outcome would you prefer? Please respond with only A or B.
