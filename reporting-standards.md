# Reporting Standards Reference

This file contains condensed checklists for the reporting standards a peer reviewer should apply during methodology review (Phase 5A of the workflow). Use the standard that matches the study design identified during intake.

## When EQUATOR standards apply (and when they don't)

The EQUATOR Network catalogs reporting guidelines for empirical health and biomedical research. It covers most empirical study designs in health/medicine well. **It does not cover:**

- Theoretical / conceptual papers
- Mathematics
- Most computer science / ML methods papers (which have their own community norms)
- Engineering papers (varies — check the target venue)
- Humanities papers
- Editorials, commentaries, perspectives
- General narrative reviews (though SANRA exists for biomedical narrative reviews)

For papers outside EQUATOR coverage, do **not** force-fit a checklist. Instead, follow Phase 2.2 of the workflow: state plainly that no EQUATOR standard applies, check for community-specific norms, and use the **General rigor assessment** in `review-rubric.md` § "General rigor (no EQUATOR standard)" as the basis for Section 5 of the report.

## Selection guide

| If the study is... | Apply |
|---|---|
| A randomized controlled trial (parallel, cluster, crossover, factorial) | **CONSORT** |
| A systematic review or meta-analysis | **PRISMA 2020** |
| An animal experiment (in vivo) | **ARRIVE 2.0** |
| Observational: cohort, case-control, or cross-sectional | **STROBE** |
| A diagnostic accuracy study | **STARD** |
| Qualitative research | **SRQR** (or **COREQ** for interviews/focus groups) |
| A single or small case series | **CARE** |
| Prediction model development/validation (incl. ML for health) | **TRIPOD** / **TRIPOD-AI** |
| AI intervention in a clinical trial | **CONSORT-AI** |
| Quality improvement | **SQUIRE 2.0** |
| Economic evaluation | **CHEERS** |
| Clinical trial protocol | **SPIRIT** |
| Anything else | Skip and use general rigor rubric |

When in doubt between two standards, pick the one with the better fit and note the alternative in the report.

---

## CONSORT (RCTs) — abbreviated checklist

**Title & abstract**
- Identified as a randomized trial in the title
- Structured abstract with trial design, methods, results, conclusions

**Introduction**
- Scientific background and rationale
- Specific objectives and hypotheses

**Methods**
- Trial design (parallel/crossover/cluster, allocation ratio)
- Eligibility criteria for participants
- Settings and locations of data collection
- Interventions: enough detail for replication
- Outcomes: primary and secondary, pre-specified, with measurement methods
- Sample size calculation and assumptions
- Randomization: sequence generation, allocation concealment, implementation
- Blinding: who was blinded, how
- Statistical methods: primary analysis, subgroup/adjusted analyses

**Results**
- Participant flow diagram (CONSORT diagram)
- Recruitment dates and follow-up period
- Baseline characteristics by group
- Numbers analyzed in each group
- Outcomes & estimation: effect size + precision (CI) for each outcome
- Subgroup/adjusted analyses (pre-specified vs. exploratory)
- Harms: all important adverse events

**Discussion**
- Limitations including sources of bias
- Generalizability
- Interpretation consistent with results

**Other**
- Trial registration number and registry
- Protocol availability
- Funding source and role of funders

---

## PRISMA 2020 (systematic reviews / meta-analyses)

**Title & abstract**
- Identified as a systematic review
- Structured abstract

**Methods**
- Eligibility criteria (PICO or equivalent)
- Information sources (databases, registers, dates last searched)
- Full search strategy (typically in supplement)
- Selection process: how many reviewers, conflict resolution
- Data extraction process
- Risk-of-bias assessment tool (e.g., RoB 2, ROBINS-I)
- Effect measures (RR, OR, MD, SMD)
- Synthesis methods: grouping, model (fixed/random), heterogeneity, sensitivity analyses
- Reporting bias assessment (funnel plot, Egger's)
- Certainty assessment (e.g., GRADE)

**Results**
- PRISMA flow diagram
- Study characteristics table
- Risk-of-bias results per study
- Results of individual studies and syntheses
- Heterogeneity findings
- Certainty findings

**Other**
- Registration (PROSPERO) and protocol
- Funding, conflicts of interest

---

## ARRIVE 2.0 (animal experiments)

**Essential 10**
1. Study design: groups, experimental unit
2. Sample size: N per group, justification
3. Inclusion/exclusion criteria: pre-specified
4. Randomization: how groups were assigned
5. Blinding: at allocation, intervention, outcome assessment
6. Outcome measures: primary and secondary
7. Statistical methods: appropriate for design
8. Experimental animals: species, strain, sex, age, weight, source
9. Experimental procedures: when, where, how, frequency
10. Results: descriptive stats + effect sizes with precision

Note: many animal studies fail on items 2 (sample size justification), 4 (randomization), and 5 (blinding).

---

## STROBE (observational studies)

**Title & abstract**: study design indicated; balanced summary.

**Introduction**: scientific background, specific objectives.

**Methods**
- Study design clearly stated (cohort/case-control/cross-sectional)
- Setting, locations, dates
- Participants: eligibility criteria, sources, selection methods
- Variables: outcomes, exposures, confounders — clearly defined
- Data sources and measurement methods
- Bias: efforts to address potential sources
- Study size: how arrived at
- Quantitative variables: how handled in analysis
- Statistical methods: confounding control, subgroup/interaction analyses, missing data handling
- For cross-sectional: sampling strategy

**Results**
- Participant flow numbers at each stage
- Descriptive data: characteristics, exposures, missing data
- Main results: unadjusted AND confounder-adjusted estimates with CI
- Other analyses: subgroups, interactions, sensitivity

**Discussion**
- Key results
- Limitations including direction and magnitude of potential bias
- Interpretation considering objectives, limitations, similar studies
- Generalizability

**Other**: funding source.

---

## STARD (diagnostic accuracy)

Key items:
- Index test and reference standard fully described
- Eligibility criteria and recruitment
- Index test blind to reference standard (and vice versa)
- Time interval between index test and reference standard
- Estimates of diagnostic accuracy with CIs (sensitivity, specificity, predictive values, likelihood ratios)
- Handling of indeterminate results, missing data
- Flow diagram of participants

---

## SRQR / COREQ (qualitative research)

Common items:
- Theoretical framework and methodological orientation
- Researcher characteristics and reflexivity (especially COREQ)
- Sampling strategy and rationale; saturation
- Data collection methods, setting, duration
- Recording, transcription, field notes
- Analytic approach (coding, theme derivation, software)
- Trustworthiness: triangulation, member checking, inter-coder agreement
- Quotations to support themes

---

## CARE (case reports)

- Patient information (de-identified): demographics, primary concern
- Clinical findings, timeline, diagnostic assessment, therapeutic intervention, follow-up
- Discussion of strengths/limitations, takeaway lessons
- Patient perspective and informed consent

---

## TRIPOD / TRIPOD-AI (prediction models)

- Source of data, study design, eligibility criteria
- Outcome definition and measurement
- Predictors: definition, measurement, blinding to outcome
- Sample size considerations
- Missing data handling
- Statistical methods including model specification and validation strategy
- Performance measures: discrimination (AUC), calibration, clinical utility
- For TRIPOD-AI: fairness across subgroups, train/validation/test split, code/model availability

---

## How to use these in the report

1. Identify which standard applies during intake (Phase 0).
2. Load only the relevant section from this file.
3. During Phase 5A, check the manuscript against each item.
4. In Section 6 of the report, produce a compliance table:

| Item | Reported? | Comment |
|---|---|---|
| Sample size calculation | Partially | Stated in Methods §2.3 but no power assumption given |
| Randomization sequence | No | Allocation method not described |

5. Items rated "No" or "Partially" become Major or Minor comments depending on severity.
