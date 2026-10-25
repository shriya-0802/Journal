# Review Rubric

Detailed assessment criteria for the peer review. Organized by phase and manuscript type. Load only the sections relevant to the current manuscript — do not load the entire file upfront.

## Quick navigation

- **Desk check** — every manuscript
- **Research integrity red flags** — alongside desk check
- **General rigor (no EQUATOR standard)** — papers outside EQUATOR coverage
- **Methodology** — empirical research articles
- **Reviewing a review article** — systematic, narrative, scoping
- **Reviewing an editorial or commentary** — opinion, perspective, editorial
- **Reviewing a methods paper** — new techniques
- **Reviewing a theoretical paper** — frameworks, conceptual contributions
- **Reviewing a conference paper** — CS/ML/engineering norms
- **Reviewing a replication study** — direct or conceptual replications
- **Statistical sanity checks** — empirical work
- **Title and abstract** — most-read parts of the paper
- **Results, discussion, interpretation** — empirical only
- **Recognizing fatal flaws** — issues revision can't fix
- **Tone and writing** — applies broadly
- **Severity calibration: Major vs. Minor**

---

## Desk check

### Structure
- Organized appropriately for manuscript type? (IMRAD for empirical; alternatives for reviews, editorials, theoretical, conference papers)
- Abstract present and self-contained?
- Title accurate, not overclaiming?

### Required statements (where applicable)
- Ethics approval — for human or animal studies
- Informed consent — for human subjects research
- Animal welfare — IACUC or equivalent
- Conflicts of interest — all authors
- Funding — sources named, role described
- Author contributions — CRediT or equivalent
- Data availability — where data lives
- Code availability — for computational work
- Trial registration — for clinical trials
- Pre-registration — where applicable
- AI use disclosure — now standard across most publishers

### References
- List complete? Spot-check 3–5
- Citations consistent in style?
- Self-citation pattern reasonable?
- Recent literature represented?
- Predatory-journal citations? (red flag)

### Figures and tables (if present)
- Each referenced in main text?
- Captions self-contained?
- Abbreviations defined in legends?
- Axes labeled with units? Error bars defined?
- Color choices accessible?
- Truncated axes or other misleading visual choices?

---

## Research integrity red flags

Frame everything as "please verify" or "please clarify" — never accusatory. The harm of a false accusation is high; the harm of a polite verification request is essentially zero.

### Image patterns
- Sharp boundaries suggesting splicing or cuts (especially Western blots, gels, microscopy)
- Identical regions across panels or figures
- Anomalously clean backgrounds
- Repeated bands in blots or gels
- Inconsistent magnification or scale across similar conditions

If concerned: *"Could you confirm the provenance of Figure X — it appears visually similar to Figure Y in region [describe]; please clarify whether these are independent replicates."*

### Statistical patterns
- Suspiciously round numbers appearing too often
- GRIM violations (mean × N must be integer for integer-bounded data)
- Too-clean variance across groups
- Benford-law violations in large numeric tables
- Multiple p-values clustered just below 0.05

### Salami slicing
Consensus search the senior author's recent papers. If substantial topic/sample/method overlap found, ask: *"Please clarify how the sample/data in this manuscript relates to [Author et al., Year], which appears to draw on overlapping data."*

### Text recycling
Beyond methods sections (legitimate recycling), watch for substantial verbatim overlap with the authors' prior published work in introduction or discussion.

### Retracted citations
For prominent cited works, search `"[paper title]" retraction`. Citing retracted work without acknowledgment is a problem.

### Predatory journal citations
References from known predatory publishers are red flags for cited content reliability. Resources: Beall's List archive, Cabells.

---

## General rigor (no EQUATOR standard)

For theoretical, mathematical, CS/ML methods, engineering, humanities, narrative reviews, editorials. Replace the EQUATOR compliance table in Section 5 of the report with a "General rigor assessment" table using these dimensions.

### Logical coherence
- Central claims clearly stated?
- Each claim follows from evidence/argument?
- Internal contradictions or non-sequiturs?
- Conclusion follows from the body?

### Claim–evidence fit
- For each significant claim: what evidence supports it?
- Claims appropriately hedged given evidence strength?
- Causal claims justified, or overreach from associative evidence?

### Transparency of process
- Steps reproducible from the manuscript alone?
- For theoretical work: definitions explicit, derivations complete, assumptions stated?
- For literature work: scope of selection transparent?

### Reproducibility (where applicable)
- Code, data, materials shared per community norms?
- Computational environment specified?
- Mathematical proofs complete?

### Engagement with prior work
- Relevant prior literature engaged?
- Key foundational works cited?
- Contribution clearly delineated from prior work?
- Alternative approaches/views acknowledged?

### Falsifiability and limitations
- Claims testable in principle?
- Limitations of the approach acknowledged?
- Conditions under which conclusions might fail?

---

## Methodology (empirical research articles)

### Design fit
Common mismatches:
- Cross-sectional design used to claim causation
- Convenience sample used to claim generalizability
- Single-site study used to claim "real-world effectiveness"
- Retrospective chart review presented as equivalent to prospective data
- Long-term outcomes claimed from short follow-up

### Sample and sampling
- Sample size justified? (Best: a priori power calculation. Acceptable: pragmatic justification. Weak: no justification.)
- Sampling frame appropriate?
- Selection bias risks: who refused, who dropped out, ITT vs. per-protocol?
- For animal/in vitro: biological vs. technical replicates? Pseudoreplication?

### Controls, blinding, randomization
- For interventional work: randomization performed, how?
- Allocation concealed?
- Participants, providers, outcome assessors blinded?
- For animal/lab work: experiments randomized in time? Samples coded?

### Measurement
- Outcome measures validated for the population?
- For self-report: social desirability, recall bias addressed?
- For lab measures: CV, inter-rater reliability reported?
- For composite outcomes: each component clinically meaningful?

### Statistical analysis
Common red flags:
- t-tests on non-normal data without justification
- Multiple comparisons without correction
- Repeated measures analyzed as independent
- Linear models on bounded outcomes
- Survival data without censoring handling
- Pre-specified vs. post-hoc analyses not distinguished
- Missing data: complete-case analysis without justification
- Effect sizes with CIs, not just p-values
- For ML/AI: train/validation/test split? Test set held out properly?

### Reproducibility
- Methods detailed enough to replicate?
- Code, data, materials shared?
- Reagents: catalog numbers, validation?
- Software: version numbers?

---

## Reviewing a review article

### For systematic reviews
Use PRISMA 2020 plus this section.

- Research question clearly stated (PICO or equivalent)?
- Full search strategy reported (supplement)?
- Multiple reviewers for selection; conflict resolution stated?
- PRISMA flow diagram present?
- Risk-of-bias tool applied to every included study?
- Meta-analysis model (fixed/random) justified? Heterogeneity assessed (I², τ²)?
- Subgroup analyses pre-specified?
- Publication bias assessed?
- Certainty rating (e.g., GRADE)?

### For narrative / scoping reviews
- Scope clearly bounded even if not systematic?
- Literature selection transparent?
- Balance: does the review fairly represent the literature?
- Currency: recent literature included?
- Synthesis: does it integrate and identify tensions, or just summarize?
- Spot-check against Consensus for major missing works
- Author positionality acknowledged (especially for opinionated reviews)?
- Contribution beyond existing reviews?

---

## Reviewing an editorial or commentary

No methodology questions. Focus on:

### Argument
- Central thesis stated clearly?
- Logical progression: premises → reasoning → conclusion?
- Key terms defined?
- Steps in reasoning explicit?

### Evidence base
- Factual claims supported by citations?
- Spot-check load-bearing citations against Consensus
- Statistics and data points accurate?

### Balance
- Engages with counterarguments, or strawman?
- Competing perspectives acknowledged?
- Tone proportionate?

### Topicality
- Why this topic now? Responsive to recent developments?
- Tells readers something new, or restates received wisdom?

### Tone fit for venue
- Matches editorial norms of target journal?

---

## Reviewing a methods paper

### Problem framing
- Gap the method addresses clearly stated?
- Comparison set (existing methods) appropriate?

### Method description
- Detailed enough to implement from the paper alone?
- Parameter choices justified?
- Theoretical underpinnings explained?

### Validation
- Method shown to work: synthetic data with ground truth? Held-out test sets?
- Evaluation metrics suited to the problem?
- Failure modes characterized?

### Comparison with alternatives
- Comparison fair? (Same data, same evaluation, reasonable baselines)
- Strongest competing methods included?
- Statistical comparisons reported?

### Generalizability and reproducibility
- Tested across multiple datasets/conditions?
- Sensitivity to hyperparameter choices?
- Code released? Computational requirements specified?

---

## Reviewing a theoretical paper

### Coherence
- Framework internally consistent?
- Definitions explicit and stable?
- Derivations or argument chains hold up?

### Novelty
- What is genuinely new? Spot-check against Consensus.
- Competing frameworks acknowledged and differentiated?

### Falsifiability and predictions
- Does the framework make testable predictions?
- What work does the framework do — what does it let us see, do, or predict?

### Clarity
- Argument followable by a competent reader in the field?
- Diagrams/tables anchor the framework effectively?

---

## Reviewing a conference paper

### Venue norms
- Meets venue's reproducibility checklist?
- Venue-required statements (broader impact, ethics, etc.)?
- Format compliance (page count, anonymization)?

### Empirical rigor
- Multiple seeds for stochastic methods?
- Error bars/CIs on metrics?
- Ablations isolating contributions?
- Strong, recent baselines?

### Transparency
- Hyperparameter search reported?
- Compute used reported (hardware, time)?
- Code release commitment?

### Claims fit
- Results support title-level claim?
- "State of the art" claims specific and recent?
- Generalizability claims supported by experiments?

---

## Reviewing a replication study

### Fidelity to the original
- Original protocol faithfully followed?
- Deviations flagged and justified?
- Original materials/measures used, or substitutes?

### Pre-registration
- Replication pre-registered before data collection?
- Deviations from pre-registered plan transparently reported?

### Power
- Powered to detect the originally reported effect?
- For null results: large enough that "no effect" is meaningful?

### Comparison with original
- Effect sizes compared (not just significance)?
- Reasons for divergence discussed?

---

## Statistical sanity checks

### Internal consistency
Spot-check 5–10 numerical claims across abstract, main text, tables, and figures. All must agree: sample sizes, effect estimates, percentages.

### GRIM test
For means of integer-bounded data (Likert items, item counts), **mean × N must equal an integer** (within rounding). Example: 23 participants, mean = 4.31 → 23 × 4.31 = 99.13 → impossible. Flag and ask to verify.

### Test statistic ↔ df ↔ p-value
For any t/F/χ² with df and p-value, verify the triple is internally consistent. Disagreement suggests a reporting error.

### SD bounds
For non-negative outcomes, verify mean − 2·SD doesn't go below the minimum possible value. If so, distribution is highly skewed or SD is misreported.

### Effect size ↔ CI ↔ p-value
These are mathematically linked. Major inconsistencies suggest a typo or problem with the analysis.

### Sample size flow
Recruited → eligible → enrolled → analyzed must all be explained. Numbers in flow diagrams must match numbers used in analyses.

Frame all sanity-check concerns neutrally: *"§3.1 reports mean = 4.31 for N=23. Per the GRIM check, this value is not achievable; please verify."*

---

## Title and abstract

### Title
- Type fit: descriptive vs. declarative — match the target journal's pattern
- Does the title describe what the paper found (not just the topic)?
- Specific enough that a reader knows what the paper is about?
- Overclaim check: implies something stronger than the paper supports?
- Searchability: key terms a reader would use appear in the title?

### Abstract
- Stand-alone test: question, design, headline result with effect size, conclusion?
- Key numbers present: sample size, primary effect size with precision?
- Structure compliant with journal requirements?
- Hedging calibrated: not overclaiming or underclaiming?
- Limitations mentioned, or only positive findings?
- Consistent with main text? (Post-revision inconsistencies are common)

---

## Results, discussion, interpretation (empirical only)

### Result-claim alignment
- Effect size vs. statistical significance: p<0.05 with tiny effect ≠ "robustly improves"
- CI width: wide CIs with "significant" point estimates are weak findings
- Subgroup claims: pre-specified or post-hoc fishing?
- Causation language: "causes" or "leads to" justified by the design?
- Practical vs. statistical significance engaged with?

### Discussion section
- Honest limitations: specific to this study, not boilerplate
- Alternative interpretations: confounding, reverse causation, selection effects
- Cherry-picked comparisons with prior work: verify against Consensus
- Null or contradictory results within the paper acknowledged?
- Speculation labeled as such, not folded into "implications"
- Ending: does the conclusion paragraph match the data?

### Generalizability
- Claims of broader applicability supported by the sample?
- Boundary conditions stated?

### Figures and tables
- Figures show what text claims
- Visualization fairness: truncated axes, dual axes, removed outliers flagged
- Tables match text numbers
- Format conventions: survival curves (numbers at risk), ROC (baseline), forest plots (heterogeneity stats), ML benchmarks (error bars)

---

## Recognizing fatal flaws

Some problems can't be fixed by revision. Lead with the fatal flaw; let surface comments be brief or omitted.

### Patterns
- **Design cannot answer the research question**: causal claim from cross-sectional data; "real-world effectiveness" from a single selected site; long-term outcomes from short follow-up; generalization to a population the sample doesn't represent
- **Sample fundamentally inappropriate**: wrong population for the question
- **Data integrity issues revision can't fix**: suspected fabrication; irrecoverable measurement errors; lost raw data; superseded datasets
- **Unfalsifiable claims**: central claim can't be tested or refuted by any conceivable data
- **Ethical issues with the research itself**: IRB violations, consent failures, animal welfare concerns
- **Fundamental statistical failure**: analysis approach can't be salvaged for the data structure

### How to communicate
1. **Reframe what's salvageable**: "The cross-sectional design can't support the causal claim, but the descriptive epidemiology is interesting and publishable with reframing."
2. **Suggest the next study**: "Answering this question would require [design]. Consider whether [salvageable subset] is publishable now."
3. **Be plain**: "Adding more covariates or strengthening the writing won't address this — the issue is structural."

A fatal flaw doesn't always mean "reject." Sometimes a paper with a fatal flaw on its primary claim has publishable secondary contributions. Use judgment.

---

## Tone and writing (applies broadly)

- Key terms defined? Acronyms expanded on first use?
- Vague phrases ("significantly," "remarkably") flagged where precision is warranted
- Same point repeated in introduction, results, and discussion?
- Discussion doesn't oversell the results?
- Paragraphs with clear topic sentences? Logical flow?

Usually Minor comments. If writing makes the paper genuinely hard to evaluate → Major.

---

## Severity calibration: Major vs. Minor

A **Major comment** is one of:
- A methodological issue that threatens the paper's central claims
- A novelty claim that prior work undermines (Consensus-found)
- A missing required element (no ethics statement, no sample size justification for an RCT)
- A conclusion that overshoots the data
- A reporting-standard item rated "No" on a critical element
- A reproducibility issue that prevents replication
- A logical/argumentative flaw that breaks the argument (non-empirical work)
- A scope or novelty mismatch requiring rethinking the framing

A **Minor comment** is:
- Clarification needed on a non-central detail
- Citation suggestions for additional context
- Writing/clarity issues that don't impede understanding
- Formatting issues
- Figure improvements that don't change the story

If you have 12+ Major comments, recheck severity — likely over-flagging. If everything is "major," nothing is.
