# TODO — representation.tex refinement plan

Three topics are already **explicitly deferred** to future work (Contributions note, §1):
schema/model bootstrapping, identification, and constraint enforcement (cardinality).
The items below are *within* the paper's stated scope and are currently absent or under-specified.

---

## 1. Restore formal body-of-information characteristics (§ Epistemic Properties)

`transitional.tex` defines six crisp properties that justify the algebraic manoeuvres
(removing complemented values, guaranteeing a unique reliability per positor/posit pair, etc.).
`representation.tex` currently collapses them into two informal bullet points.

**Proposed additions** — add proper `\deffy` definitions for:

| Name | What it says | Why it matters |
|---|---|---|
| **Symmetric** | `!(S, p, -c, T)` ≡ `!(S, p̄, c, T)` | Allows removing `not v` in posits in favour of negative certainty |
| **Canonical** | All assertions are over posits without negated values | Storage-friendly normal form |
| **Bounded** | `|c_v + c_v̄| = |c_v + c_v̄|²` (i.e. certainties for a value and its complement lie on the unit boundary) | Constrains the certainty scale to be self-consistent |
| **Exclusive** | No two assertions by the same positor over the same posit differ only in certainty | Prevents lunatic double-assertions |
| **Universal** | All positors agree on the interpretation of appearances | Meaningful disagreement requires shared referents |
| **Comprehensive** | A body that has all five properties above | Assumed throughout the rest of the paper |

The figure `v_and_not_v.pdf` (already referenced) illustrates *bounded* + *symmetric* and can
stay as-is once the definitions are added.

---

## 2. Add the non-contradiction inequality (§ Epistemic Properties or § Bitemporal Dynamics)

The original paper gives a precise test for whether concurrent multi-value assertions by one
positor are self-consistent:

$$\frac{1}{2}\sum_{i=1}^{n}\left[1 - \frac{c_i}{|c_i|}\right] + \sum_{i=1}^{n} c_i \leq 1$$

This is currently completely absent from `representation.tex`.  
Add it with:
- a `\deffy` definition for **non-contradictory**,
- the small worked example from the original (Donna asserting `c=0.25` for fluffy red and
  `c=-0.75` for not-shaved-clean yields LHS = 0.5, well within bounds),
- a note that a *decisive* body is always non-contradictory (single assertion per
  positor/appearance-set implies the sum trivially ≤ 1).

---

## 3. Promote decisive/indecisive to formal definitions

Currently only mentioned as a bullet ("Decisiveness: whether a positor has a single effective
assertion …"). Elevate to a `\deffy` block with the exact wording from the original:

> When multiple assertions by the same positor are in effect for different posits with the same
> appearance set, the positor is **indecisive**; when a single assertion is in effect, the positor
> is **decisive**. A body of information is decisive if no indecisive positor exists in any
> information in effect.

This is needed for the subsumption discussion (3NF is always decisive) and for the future
cardinality section.

---

## 4. Strengthen the "why posits alone are insufficient" passage (§2.1)

The current paragraph is correct but brief. Consider adding:
- The "deck of cards" metaphor (posits cannot self-certify truth — you need an external
  truth-bearer, which is exactly the assertion).
- The precise statement that appearance-time conflicts are unresolvable at the posit level
  because posits are unordered: there is no way to tell which of two same-time posits is the
  "correction" without an outside judgment.

These were footnotes in the original and are good candidates for margin notes if the
document later moves back to a Tufte class.

---

## 5. Expand the Related Work section

The current Related Work is a single paragraph. The original connects to:

- **Philosophy of change** — Bradley ("a bond of identity in differences"), Lombard
  (relational vs. non-relational change), Sider/Black (persistence of identity).
- **Linguistics** — Papafragou ("subjective epistemic modality is time-dependent"),
  Moens & Steedman (culmination / transition to new state).
- **Analytics/fusion** — Smets & Kennes (transferable belief model), Liu & Pan et al.
  (adaptive combination of unreliable sources).
- The *resolve-on-read vs. resolve-on-write* framing (Massaro & Friedman; Lin & Mendelzon)
  is mentioned in the introduction of `representation.tex` but never grounded in related
  work — the connection to information-fusion literature should be made explicit.

A suggested structure for Related Work:
1. Temporal databases (Reichenbach, Snodgrass, SQL:2011, Johnston) — already present ✓
2. Uncertainty and provenance (Benjelloun et al., Dylla et al.) — already present ✓
3. Write-time vs. query-time conflict resolution (Massaro & Friedman; Lin & Mendelzon)
4. Information fusion (Smets & Kennes; Liu et al.)
5. Graph/RDF formalisms (already present ✓)
6. Philosophy & linguistics (Bradley, Lombard, Papafragou) — optional but elevating

---

## 6. Minor / optional

- **Keywords line** in the abstract (the original had a keyword list; useful for indexing).
- **`\classify` command** — the original defined it; not needed now that the classifier
  section is deferred, but may be worth keeping as a stub for future extension.
- The `\assert` macro in `representation.tex` uses `\mathbin{\text{!}}` while the original
  uses `\text{!}`. Verify the spacing renders as intended once the document is compiled.
