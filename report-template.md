# Report Template

The .docx output structure with section-by-section guidance and example phrasings. Always follow the docx skill (`/mnt/skills/public/docx/SKILL.md`) for the technical implementation. Load this file only at Phase 8 when generating the .docx.

## File naming

Save as `peer-review-report-<short-title-slug>.docx` to `/mnt/user-data/outputs/`. Example: `peer-review-report-creatine-cognition.docx`.

## Page setup

US Letter, 1-inch margins.

## Title block

```
PEER REVIEW REPORT
[Manuscript title — copy verbatim from the paper]
Target journal: [Journal name] — [Article type]
Severity: [Gentle / Standard / Harsh]
Date of review: [today's date]
```

Immediately below, italic note:
> *This is a simulated peer review intended to help the author identify and address issues before submission. It approximates the kind of report a journal reviewer would return, but is not a substitute for actual editorial review.*

---

## Section 1: Summary of the manuscript

**Purpose:** Show the author you understood their paper.

**Length:** One paragraph, 5–8 sentences.

**Include:** research question, design and sample, headline finding(s), claimed contribution.

**Leave out:** No critique here.

**Example:**
> The authors investigate [X] in [population/setting] using [design]. They [briefly describe approach and primary outcome]. Their main finding is that [headline result with effect size if available]. The authors position this as [claimed contribution].

---

## Section 2: Overall assessment

**Length:** 2–3 paragraphs.

- Para 1: **Strengths** — be specific ("the pre-registration of the primary outcome and transparent reporting of failed secondary analyses are exemplary," not "the writing is clear")
- Para 2: **High-level concerns** — sketch the 2–3 most important; don't list every issue
- Para 3: **Headline recommendation** — calibrated to the target journal; which category (ready / minor / major / substantial rework / consider alternative venue) and why

---

## Section 3: Major comments

**Format:** Numbered. Each item has:
- Short bold title (one line)
- Paragraph explaining the issue with specific section/page reference
- Concrete suggested action in italics

**Example:**

> **Major Comment 3: Sample size justification missing**
>
> The Methods section (page 5) reports that 142 participants were enrolled but does not describe how this number was determined. For an RCT with a continuous primary outcome, an a priori power calculation is expected, particularly given the journal's author guidelines explicitly require this for clinical trials.
>
> *Suggested action: Add a sample size calculation specifying the assumed effect size, power, and alpha level. If the study was pragmatic, state this explicitly and discuss implications for power in the limitations.*

**How many:** 5–10. Let the manuscript dictate.

---

## Section 4: Minor comments

**Format:** Numbered list. One to three sentences each. Reference specific page/line.

**Examples:**
> 1. *Page 2, line 34:* "p<0.05" reported without effect size or CI. Add both throughout.
> 2. *Figure 2:* y-axis truncated, visually amplifying group differences. Extend to zero or note truncation in caption.
> 3. *Discussion §3:* "significantly" used in non-statistical sense. Reword to avoid ambiguity.

**How many:** 10–20.

---

## Section 5: Reporting-standard compliance (or general rigor assessment)

**If an EQUATOR standard applies**, use a compliance table:

| Reporting item | Reported? | Comment / location |
|---|---|---|
| Trial design | Yes | Methods §2.1 |
| Sample size calculation | No | Not present; see Major comment 3 |
| Randomization sequence | Partially | §2.4 mentions but doesn't describe method |
| Blinding | Yes | §2.5 — outcome assessors blinded |
| Primary outcome pre-specified | Yes | §2.2, matches registration |
| ... | ... | ... |

If multiple standards apply, produce two tables.

**If no EQUATOR standard applies**, replace with a **General rigor assessment** table:

> *No EQUATOR Network reporting standard applies to this manuscript type ([type]). The assessment below uses general rigor criteria.*

| Dimension | Assessment | Comment / location |
|---|---|---|
| Logical coherence | Strong | Argument structure clear and consistent |
| Claim–evidence fit | Adequate | Most claims supported; see Major Comment 2 |
| Transparency of process | Weak | Literature selection criteria not stated |
| Engagement with prior work | Strong | Key works engaged; one gap noted in §6.3 |
| ... | ... | ... |

If a community-specific norm applies (e.g., NeurIPS reproducibility checklist), reference it in the introductory note.

---

## Section 6: Literature audit (Consensus)

### 6.1 Field context
2–3 sentences on the state of the field from Consensus results. Reference 2–4 key papers.

### 6.2 Novelty assessment
For each major novelty claim:
- The claim
- What you searched
- What you found
- Conclusion: holds / overstated / undermined

If undermined, name the paper(s) with hyperlinks. **Calibrate to the target journal's novelty bar** from Phase 1.3.

### 6.3 Citation gaps (pre-revision-date only)
3–5 papers Consensus surfaced as foundational/recent-and-relevant that aren't cited. Brief rationale each. Flag post-revision papers separately as "new since your revision; consider for v2."

### 6.4 Citation spot-checks
For each spot-checked citation, briefly state whether the cited claim was faithful.

**Hyperlinks:** Use `ExternalHyperlink` with `style: "Hyperlink"` for every Consensus URL. Never truncate URLs.

If Consensus was unavailable: *"A Consensus-grounded literature audit could not be performed. The author should manually verify novelty claims and check for missing key citations."*

---

## Section 7: Journal-specific assessment

### 7.1 Scope fit
2–3 sentences. Quote/paraphrase and link the scope statement from the guidelines fetched in Phase 1.2.

**Example:**
> *[Journal]* describes its scope as covering [X, Y, Z]. The manuscript's focus on [topic] aligns squarely with this scope. *(Or: The manuscript sits at the edge of the journal's scope; see §7.5 for alternative venues.)*

### 7.2 Novelty calibration
Name 2–3 recent journal papers as comparators (from Phase 1.3). Be concrete.

**Example:**
> Recent work in *[Journal]* has reported [type of advance], for instance [Author, Year — Consensus link]. The current manuscript's contribution — [paper's contribution] — is comparable in scale to [comparator]. The novelty bar appears [met / borderline / below typical].

### 7.3 Writing & style fit
Concrete mismatches only: length vs. word limits, abstract structure, tone, headings.

### 7.4 Required-but-missing items
Cross-reference journal guidelines with `references/journal-fit-checklist.md`. Use a table:

| Required item | Requirement | Status | Action |
|---|---|---|---|
| Cover letter | Required | Missing | Draft one-page letter arguing scope fit |
| Highlights (≤85 chars each) | Required | Missing | Add 3–5 bullets front-loading findings |
| AI use disclosure | Required | Missing | Add statement or confirm not applicable |
| Data availability statement | Required | Inadequate | Currently "on request"; deposit in repository or justify restriction |
| ... | ... | ... | ... |

### 7.5 Alternative venues (only if recommending venue change)
2–3 candidates with one-line rationale each.

---

## Section 8: Recommendation

One-line bold recommendation + 1–2 paragraphs of rationale **calibrated to the target journal**.

**Example:**

> **Recommendation: Major revision recommended before submission to *[Journal]*.**
>
> The study addresses an important question with a generally appropriate design. However, three concerns require attention before submission to *[Journal]* specifically: (1) the absence of a sample size justification, which the journal's guidelines explicitly require; (2) the novelty claim being partially undermined by [Author, Year — Consensus link]; and (3) the discussion's overstatement of effect magnitude. In addition, several required submission elements are missing — detailed in §7.4.
>
> Each issue is addressable. With these revisions the manuscript would be competitive at *[Journal]*. If the novelty concern proves difficult to resolve, see §7.5 for alternative venues.

The recommendation must match the comments. 8 Major comments ≠ "minor revision."

---

## Section 9: Audit log

### 9.1 Manuscript processed
- Title, authors, file type, approximate word count
- Study type, reporting standard applied
- Target journal, article type, literature window

### 9.2 Sources used to profile the journal

| Source | URL | Notes |
|---|---|---|
| [Journal] author guidelines | https://... | Used for word limits, required supplements |
| [Journal] aims & scope | https://... | Used in §7.1 |

### 9.3 Consensus searches

| # | Query | Results | Used in |
|---|---|---|---|
| 1 | [query] | 20 | Field context §6.1 |
| 2 | [query] | 14 | Novelty audit §6.2 |
| 3 | [query] | 8 | Spot-check §6.4 |

### 9.4 Coverage notes and limitations
- Consensus tier (Free 10/search or Pro 20/search); total searches; failed searches
- Whether journal author guidelines were retrievable
- Supplementary Information: provided / not provided / referenced but absent
- Standard caveats: simulated review; Consensus bounded by tier and queries; guidelines may have been updated; statistical methodology checks are general; raw data not accessible

---

## docx implementation notes

Use the `docx` npm package per `/mnt/skills/public/docx/SKILL.md`.

```javascript
const { Document, Packer, Paragraph, TextRun, Table, TableRow, TableCell,
        AlignmentType, LevelFormat, ExternalHyperlink, HeadingLevel,
        BorderStyle, WidthType, ShadingType } = require('docx');

// Numbered list for major/minor comments
numbering: {
  config: [{
    reference: "majorList",
    levels: [{ level: 0, format: LevelFormat.DECIMAL, text: "%1.",
      alignment: AlignmentType.LEFT,
      style: { paragraph: { indent: { left: 720, hanging: 360 } } } }]
  }]
}

// Hyperlinks for Consensus papers and journal guidelines — full URL, never truncated
new ExternalHyperlink({
  link: "https://consensus.app/papers/details/...",
  children: [new TextRun({ text: "Author et al., Year", style: "Hyperlink", size: 22, font: "Arial" })]
})

// Three-column compliance table
new Table({
  width: { size: 9360, type: WidthType.DXA },
  columnWidths: [3000, 1500, 4860],
  rows: [/* header row + data rows */]
})
```

After saving, validate:
```bash
python /mnt/skills/public/docx/scripts/office/validate.py <output>.docx
```
