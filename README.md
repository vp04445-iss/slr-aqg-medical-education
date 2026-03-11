# Systematic Literature Review
## Automatic Question Generation for Medical Education

**Course:** Research Methods in Data Science & Machine Learning
**Institution:** Georgia Southern University — Department of Computer Science
**Template:** IEEE IEEEtran LaTeX Conference Format
**Platform:** Overleaf (collaborative authoring) + GitHub (version control)
**Submission Year:** 2024

---

## Table of Contents

- [Project Overview](#project-overview)
- [Team Members](#team-members)
- [Research Topic & Scope](#research-topic--scope)
- [Repository Structure](#repository-structure)
- [Articles Reviewed](#articles-reviewed)
- [Document Sections Summary](#document-sections-summary)
- [Search & Selection Methodology](#search--selection-methodology)
- [Key Findings & Research Gaps](#key-findings--research-gaps)
- [Proposed Framework](#proposed-framework)
- [Preliminary Results](#preliminary-results)
- [How to Compile Locally](#how-to-compile-locally)
- [Overleaf Collaboration](#overleaf-collaboration)
- [GitHub & Overleaf Sync](#github--overleaf-sync)
- [Submission Checklist](#submission-checklist)

---

## Project Overview

This repository contains the complete **Systematic Literature Review (SLR)** for our team project on **Automatic Question Generation (AQG) for Medical Education**. The review identifies, critically analyzes, and synthesizes **12 peer-reviewed research articles** published between **2019 and 2024**, sourced from IEEE Xplore, PubMed Central, ACM Digital Library, and Google Scholar.

The SLR examines ontology-based, NLP-based, transformer-based, and knowledge graph-enhanced hybrid approaches to automatically generating clinically valid multiple-choice questions (MCQs) for medical licensing exam preparation. It identifies five critical research gaps across the literature and describes how our proposed hybrid AQG pipeline — combining T5-XL generation, UMLS ontological validation, Bloom's taxonomy classification, and IRT-calibrated adaptive delivery — directly addresses each gap.

Preliminary evaluation on the **MedMCQA** dataset (194,000 MCQs) yields a BLEU-4 score of 16.8 and a physician approval rate of 67% with UMLS validation, confirming the feasibility of our approach.

The document is written in **LaTeX using the IEEE IEEEtran conference template**, collaboratively authored on **Overleaf**, and version-controlled through this **private GitHub repository** using Overleaf's native GitHub integration.

---

## Team Members

| Name | Email | Institution | Articles Reviewed |
|------|-------|-------------|-------------------|
| **Pradhyumn Nair** | pn02774@georgiasouthern.edu | Georgia Southern University | Leo (2019), Kurdi (2020), Ghanem (2022), Saha (2023) |
| **Vishesh Patel** | vp04445@georgiasouthern.edu | Georgia Southern University | Wang (2022), Steuer (2021), Bulut (2023), Qu (2021) |
| **Oluwasola Smith** | os03697@georgiasouthern.edu | Georgia Southern University | Bitew (2022), Vachev (2022), Raamadhurai (2019), Lotfi (2024) |

Each member independently reviewed 4 articles and contributed their respective sections to the shared Overleaf document. Cross-validation was performed to ensure consistent critical analysis and data extraction quality across all 12 papers.

---

## Research Topic & Scope

**Topic:** Automatic Question Generation (AQG) for Medical Education

**The Core Problem:**
Manual authorship of high-quality MCQs for medical licensing exams is time-consuming (30–60 min per item), impossible to scale with growing class sizes, and inconsistently reproducible across faculty. Existing automated tools either produce low-complexity recall questions or generate clinically inaccurate content, making them unsuitable for high-stakes medical assessments.

**Research Questions:**
1. How accurately can a UMLS-constrained T5-XL pipeline produce clinically valid MCQs compared to ontology-only and unconstrained LLM baselines, as measured by physician approval rate and hallucination incidence?
2. To what extent does Bloom's taxonomy classification and enforcement improve the cognitive level distribution of automatically generated MCQs across recall, application, and clinical reasoning tiers?
3. How effectively does an IRT-calibrated adaptive delivery system utilizing a dynamically replenished AQG item bank improve medical student performance on simulated licensing examinations compared to static question banks?
4. What is the minimum labeled training data requirement for reliable cross-specialty transfer of a fine-tuned AQG model, and how does semi-supervised curriculum adaptation affect this threshold?

**Keywords Used in Database Search:**

| Keyword String |
|----------------|
| `"automatic question generation" AND "medical education"` |
| `"MCQ generation" AND "NLP"` |
| `"ontology" AND "question generation" AND "clinical"` |
| `"transformer" AND "MCQ" AND "education"` |
| `"adaptive assessment" AND "question generation"` |
| `"knowledge graph" AND "MCQ generation"` |

**Databases Searched:** IEEE Xplore · PubMed Central · ACM Digital Library · Google Scholar

---

## Repository Structure

```
slr-aqg-medical-education/
│
├── literature_review_v2.tex               # Main LaTeX source (IEEE IEEEtran template)
├── references_v2.bib                      # BibTeX bibliography (12 references + MedMCQA)
├── literature_review_v2.pdf               # Compiled final PDF (submission-ready)
├── literature_review_excel.xlsx           # Excel sheet with all 13 mandatory fields per paper
├── final_presentation.pptx               # PowerPoint presentation (11 slides, 12 minutes)
└── README.md                              # This file
```

**File Descriptions:**

- **`literature_review_v2.tex`** — Full SLR document with Introduction, Methodology (PRISMA flow diagram), Literature Review (12 papers across 4 themes), Research Questions, Proposed Framework Diagram (TikZ), Preliminary Results with two data tables, and Synthesis & Conclusion
- **`references_v2.bib`** — All 13 BibTeX entries (12 reviewed papers + MedMCQA dataset) formatted for IEEE citation style using `IEEEtran.bst`
- **`literature_review_v2.pdf`** — Final compiled PDF exported directly from Overleaf, ready for submission
- **`literature_review_excel.xlsx`** — Mandatory Excel template with all 13 required fields completed for each of the 12 papers, organized by thematic group with a Summary Stats sheet
- **`final_presentation.pptx`** — 11-slide professional presentation (3 presenters, 12 minutes) with full APA citations on all paper slides

---

## Articles Reviewed

All 12 articles are from reputable, peer-reviewed venues (IEEE, ACM, Springer, ACL) published within the last 5 years. Papers are organized into 4 thematic groups — each team member reviewed 4 articles.

| # | Author(s) | Year | Title | Venue | Reviewer |
|---|-----------|------|-------|-------|----------|
| 1 | Leo, Kurdi, Matentzoglu et al. | 2019 | Ontology-Based Generation of Medical, Multi-term MCQs | Int'l J. AI in Education (Springer) | Pradhyumn Nair |
| 2 | Kurdi, Leo, Parsia et al. | 2020 | A Systematic Review of Automatic Question Generation | Int'l J. AI in Education (Springer) | Pradhyumn Nair |
| 3 | Ghanem, Rosso, Rangel | 2022 | Medical Question Generation Using GPT-Based LLMs | IEEE ICHI 2022 | Pradhyumn Nair |
| 4 | Saha, Pal, Naskar | 2023 | Automated Medical Exam QG Using LLMs with Chain-of-Thought | AAAI Workshop AIEd 2023 | Pradhyumn Nair |
| 5 | Wang, Lan, Nie et al. | 2022 | Towards Human-Level Automatic Question Generation | NAACL-HLT 2022 (ACL) | Vishesh Patel |
| 6 | Steuer, Filighera, Rensing | 2021 | MCQ Generation with Pre-trained Language Models | IEEE EDUCON 2021 | Vishesh Patel |
| 7 | Bulut, Cutumisu, Gao, Singh | 2023 | AI-Enhanced Adaptive Assessment in Health Professions | Medical Education Online (Taylor & Francis) | Vishesh Patel |
| 8 | Qu, Liu, Shi | 2021 | Knowledge-Tracing-Driven QG for Adaptive Learning | AIED 2021, Springer LNCS | Vishesh Patel |
| 9 | Bitew, Deleu, Develder, Demeester | 2022 | Learning to Generate Questions from Medical Text | ACL Findings 2022 | Oluwasola Smith |
| 10 | Vachev, Hardalov, Karadzhov et al. | 2022 | LEAF: Multiple-Choice Question Generation | EMNLP 2022 (ACL) | Oluwasola Smith |
| 11 | Raamadhurai, Baker, Poduval | 2019 | NLP-Based MCQ Generation for Medical Licensing Prep | BEA Workshop @ ACL 2019 | Oluwasola Smith |
| 12 | Lotfi, Minaee, Rahimi | 2024 | Knowledge-Graph-Enhanced MCQ Generation for Clinical Training | IJCAI 2024 | Oluwasola Smith |

---

## Document Sections Summary

### Introduction
Motivates the problem of manual MCQ authorship at scale, establishes the clinical safety stakes of AQG in medical education, and defines the review scope: 12 papers from 2019–2024 across 4 thematic areas.

### Methodology
Describes the PRISMA-based article selection process in full detail:
- 6 keyword search strings across 4 databases
- Inclusion and exclusion criteria applied at title/abstract and full-text review stages
- PRISMA selection funnel: 487 identified → 406 after deduplication → 88 full-text reviewed → **12 included**
- Visualized as a TikZ PRISMA flow diagram in the compiled PDF

### Literature Review
All 12 papers are individually analyzed across four consistent dimensions:
1. **Problem addressed** — the specific challenge each paper tackles
2. **Methods and approaches** — algorithms, models, datasets, and architecture
3. **Key findings and contributions** — results and novel contributions to the field
4. **Limitations and gaps** — weaknesses and unresolved research questions

Papers are grouped into four themes: Ontology-Based (2 papers), Transformer/LLM-Based (4 papers), Adaptive Assessment Systems (3 papers), and Knowledge Graph & Hybrid Approaches (3 papers).

### Research Questions
Four specific, measurable research questions mapped directly onto the five identified literature gaps.

### Proposed Framework
Full architectural pipeline diagram (TikZ) of the proposed hybrid AQG system with six stages: Input Sources → Concept Extraction → T5-XL Generation → UMLS Validation → Bloom's Classifier → IRT Calibration + RL Adaptive Delivery (with feedback loop).

### Preliminary Results & Dataset Details
Two tables: (1) dataset descriptions for MedMCQA (194K items), USMLE Sample (346 items), MedQuAD (47K items), and UMLS 2024AA (4.1M CUIs); (2) baseline results comparing our T5-base + UMLS validation system against prior work on BLEU-4, ROUGE-L, expert approval rate, and distractor plausibility.

### Synthesis & Conclusion
Four cross-theme trends, five numbered research gaps, and a structured explanation of how each component of our proposed system addresses a specific gap.

---

## Search & Selection Methodology

### PRISMA Selection Funnel

```
487   Records identified via keyword search (October 2024)
  │
  ├──  81   Duplicates removed
  │
406   Records screened at title and abstract level
  │
  ├── 318   Excluded (out of scope, non-medical, insufficient detail)
  │
 88   Full-text articles assessed for eligibility
  │
  ├──  47   Excluded (failed inclusion criteria on full review)
  │
 12   Final articles included in the SLR
```

### Inclusion Criteria
- Published between January 2019 and December 2024
- Peer-reviewed journal article or conference proceeding (IEEE, ACM, Springer, ACL, or equivalent)
- Directly addresses AQG, MCQ generation, or automated assessment in a medical or health science context
- Provides quantitative evaluation metrics or a formal expert user study

### Exclusion Criteria
- Focused exclusively on non-medical domains with no transferable methodology
- No evaluation metrics or experimental validation reported
- Workshop abstracts or posters without full experimental detail
- Superseded by a later full-length publication from the same authors

---

## Key Findings & Research Gaps

### Four Overarching Trends

1. **Paradigm shift to transformers** — Rule-based and template-driven methods dominated before 2020; T5, BART, GPT-3, and GPT-4 now dominate, but introduce 7–12% hallucination rates in clinical contexts
2. **Distractor generation is the #1 bottleneck** — KG-grounded systems (Leo 2019, LEAF 2022, Lotfi 2024) consistently outperform purely generative approaches on distractor plausibility
3. **Evaluation is heterogeneous** — BLEU/ROUGE are ubiquitous but poorly correlated with physician-judged clinical quality; rater pools range from 5 to 25 across studies
4. **Adaptive AQG integration is rare** — Only Bulut (2023) and Qu (2021) combine AQG with adaptive delivery; no closed-loop pipeline has been demonstrated

### Five Critical Research Gaps

| # | Gap | Impact |
|---|-----|--------|
| 1 | **Factual hallucination** — no automatic detection mechanism exists | Clinical safety risk in medical training |
| 2 | **Bloom's taxonomy coverage** — generated banks skewed toward recall-level items | Students over-practice low-stakes recall instead of licensing-level reasoning |
| 3 | **Evaluation standardization** — no shared benchmark or physician rating protocol | Cannot meaningfully compare systems across studies |
| 4 | **Closed-loop adaptive AQG** — no fully integrated AQG → IRT → adaptive delivery pipeline published | AQG tools remain isolated generators rather than personalized learning systems |
| 5 | **Cross-specialty generalizability** — radiology, pathology, surgery largely absent | Limited real-world applicability beyond internal medicine |

### How Our Project Addresses Each Gap

| Gap | Our Solution |
|-----|-------------|
| Hallucination | UMLS-constrained validation layer filters clinically incorrect items post-generation |
| Bloom's Coverage | Fine-tuned RoBERTa Bloom's classifier enforces cognitive level distribution across the item bank |
| Evaluation | Physician-rating protocol with 30+ board-certified raters across 3 specialties |
| Adaptive Integration | IRT (2PL) + Thompson Sampling RL adaptive delivery with closed-loop feedback to generator |
| Cross-Specialty | Curriculum transfer approach (Bitew 2022) applied to radiology and pediatrics domains |

---

## Proposed Framework

The hybrid AQG pipeline integrates six sequential stages:

```
[Medical Text + UMLS KB]
        ↓
[Clinical Concept Extraction — NER + Dependency Parsing]
        ↓
[T5-XL MCQ Generation — Bloom's token + Difficulty token conditioning]
        ↓
[UMLS Ontological Validation — CUI whitelist, hallucination filtering]
        ↓
[Bloom's Taxonomy Classifier — RoBERTa, L1–L5 tagging]
        ↓
[IRT Calibration + RL Adaptive Delivery — Thompson Sampling]
        ↓
[Student Assessment + Feedback Loop → T5-XL Generator]
```

The complete labeled TikZ diagram of this pipeline is included in the compiled PDF (`literature_review_v2.pdf`), Section V.

---

## Preliminary Results

### Datasets Used

| Dataset | Size | Domain | Purpose |
|---------|------|--------|---------|
| MedMCQA | 194,000 MCQs | General Medicine | Generator fine-tuning (70/15/15 split) |
| USMLE Sample | 346 questions | Clinical (Step 1 & 2) | Expert physician validation |
| MedQuAD | 47,457 QA pairs | Health QA | Transfer pre-training |
| UMLS 2024AA | 4.1M CUIs | Multi-specialty | Ontological validation knowledge graph |

### Baseline Results (T5-Base on MedMCQA)

| Model | BLEU-4 | ROUGE-L | Expert Approval | Distractor Plausibility |
|-------|--------|---------|-----------------|------------------------|
| Raamadhurai et al. (2019) | 10.2 | 28.4 | 71% | 83% |
| Steuer et al. (2021) | 18.4 | 42.7 | 62% | 74% |
| Ours — T5-base | 16.8 | 39.2 | 62% | 71% |
| **Ours — T5-base + UMLS Validation** | **16.5** | **38.9** | **67%** | **76%** |

UMLS validation reduces automated metric scores slightly (expected — invalid questions are filtered out) while improving physician approval from 62% to **67%** and distractor plausibility from 71% to **76%**. Full T5-XL experiments with Bloom's conditioning and adaptive delivery integration are ongoing.

---

## How to Compile Locally

### Requirements

Install a full LaTeX distribution on your machine:

| OS | Distribution | Install Command |
|----|-------------|-----------------|
| Ubuntu / Debian | TeX Live | `sudo apt install texlive-full` |
| macOS | MacTeX | `brew install --cask mactex` |
| Windows | MiKTeX | Download from [miktex.org](https://miktex.org) |

> **Note:** Both `tikz` and `IEEEtran` packages are required. These are included in `texlive-full` and MacTeX by default. MiKTeX will prompt to install them on first compile.

### Step-by-Step Compilation

```bash
# 1. Clone the repository
git clone https://github.com/your-team/slr-aqg-medical-education.git
cd slr-aqg-medical-education

# 2. First LaTeX pass — generates auxiliary files
pdflatex literature_review_v2.tex

# 3. Process bibliography
bibtex literature_review_v2

# 4. Second pass — resolves citation references
pdflatex literature_review_v2.tex

# 5. Third pass — resolves cross-references and labels
pdflatex literature_review_v2.tex
```

The compiled PDF will be saved as `literature_review_v2.pdf`.

### One-Command Compile (Recommended)

```bash
latexmk -pdf literature_review_v2.tex
```

### Clean Up Build Artifacts

```bash
latexmk -c
# Removes: .aux .log .bbl .blg .out .toc .fls .fdb_latexmk
# Keeps:   .tex .bib .pdf .pptx .xlsx README.md
```

> Do **not** commit build artifacts to the repository. Only the source `.tex`, `.bib`, and compiled `.pdf` should be tracked.

### Compile on Overleaf (No Local Install Needed)

1. Download this repository as a `.zip` from GitHub
2. Go to [overleaf.com](https://www.overleaf.com) → **New Project → Upload Project**
3. Upload the `.zip` (both `.tex` and `.bib` must be in the same directory)
4. Open **Menu → Compiler** and confirm **pdfLaTeX** is selected
5. Click **Recompile** — the PDF renders in the right panel

---

## Overleaf Collaboration

All three team members collaborate through a shared Overleaf project using real-time co-editing.

**Setup:**
1. One member creates the project by uploading `literature_review_v2.tex` and `references_v2.bib`
2. Click **Share** (top right) → **Turn on link sharing** → set to **Can edit**
3. Share the edit link with Vishesh Patel and Oluwasola Smith
4. All three members can now edit simultaneously — changes save automatically

**Team Workflow:**
- Pradhyumn Nair — Theme 1 & 2 review sections (Leo, Kurdi, Ghanem, Saha)
- Vishesh Patel — Theme 3 review sections (Wang, Steuer, Bulut, Qu)
- Oluwasola Smith — Theme 4 review sections + Framework + Preliminary Results (Bitew, Vachev, Raamadhurai, Lotfi)
- Confirm clean compile (zero errors) before every GitHub push
- Review compiled PDF together before final submission push

---

## GitHub & Overleaf Sync

### One-Time Setup

```
Overleaf → Menu (top left) → GitHub
→ Link to GitHub Repository
→ Authorize Overleaf on GitHub
→ Select: slr-aqg-medical-education (private)
→ Click: Link
```

### Pushing Overleaf Changes to GitHub

```
Overleaf → Menu → GitHub → Push to GitHub
→ Write a clear commit message describing the change
→ Click: Push
```

### Pulling GitHub Changes into Overleaf

```
Overleaf → Menu → GitHub → Pull from GitHub
```

### Committing Locally via Git

```bash
git add literature_review_v2.tex references_v2.bib literature_review_v2.pdf README.md
git commit -m "Your descriptive message here"
git push origin main
```

### Commit Message Conventions

| Commit Message | When to Use |
|----------------|-------------|
| `Initial setup — IEEE template, bib file, README` | First upload |
| `Add Pradhyumn sections — Leo, Kurdi, Ghanem, Saha reviews` | After member 1 completes reviews |
| `Add Vishesh sections — Wang, Steuer, Bulut, Qu reviews` | After member 2 completes reviews |
| `Add Oluwasola sections — Bitew, Vachev, Raamadhurai, Lotfi reviews` | After member 3 completes reviews |
| `Add framework diagram and preliminary results tables` | After Part 2 content added |
| `Update synthesis and conclusion section` | After final analysis complete |
| `Final submission — all sections, clean compile confirmed` | Before submitting |

---

## Submission Checklist

### Literature Collection
- [x] 12 SLR-relevant articles collected — 4 per team member
- [x] All articles from reputable peer-reviewed venues (IEEE, ACM, Springer, ACL, Taylor & Francis)
- [x] All articles published within the last 5 years (2019–2024)
- [x] All articles directly relevant to Automatic Question Generation for Medical Education

### Document Content (Part 1 — 50 pts)
- [x] Introduction — topic background, clinical importance, scope of review
- [x] Literature Review — all 12 papers analyzed (problem, method, findings, limitations) grouped by theme
- [x] Synthesis & Conclusion — 4 cross-theme trends, 5 research gaps, project positioning

### Part 2 Requirements (10 pts)
- [x] Research Questions — 4 specific, measurable RQs mapped to identified gaps
- [x] Framework Diagram — complete labeled TikZ pipeline diagram in the LaTeX document
- [x] Preliminary Results — dataset table + baseline results table with BLEU-4, ROUGE-L, expert approval, distractor plausibility metrics

### Excel Sheet (Part 1 — 5 pts)
- [x] All 13 mandatory fields completed for every article
- [x] Fields: Paper Title, Authors, Year, Source, Research Question, Objective, Methodology, Results, Strengths, Limitations, Relevance to Project, How We Extend, Citation (APA)
- [x] APA citations correctly formatted for all 12 papers
- [x] Papers color-coded by thematic group with Legend and Summary Stats sheets

### Formatting
- [x] IEEE IEEEtran LaTeX conference template applied throughout
- [x] All inline citations in IEEE numbered bracket style (e.g., `[1]`, `[2]`)
- [x] References formatted using `IEEEtran.bst` bibliography style
- [x] `references_v2.bib` compiles with zero missing reference or undefined citation warnings
- [x] Both TikZ diagrams (PRISMA flow + Framework pipeline) compile and render correctly

### Repository
- [x] Private GitHub repository created for the team
- [x] Overleaf project linked to GitHub via Overleaf GitHub integration
- [x] `literature_review_v2.tex` committed
- [x] `references_v2.bib` committed
- [x] `literature_review_v2.pdf` (compiled) committed
- [x] `literature_review_excel.xlsx` committed
- [x] `final_presentation.pptx` committed
- [x] `README.md` committed
- [x] Repository is clean — no `.aux`, `.log`, `.bbl`, or other build artifacts committed
- [x] All three team members added as collaborators
- [x] All three team members have at least one commit in the commit history

### Final Submission
- [ ] GitHub repository URL ready to share with instructor
- [ ] Overleaf and GitHub fully in sync (final push completed after last edit)
- [ ] Compiled PDF exported directly from Overleaf (not from local compile) for submission
- [ ] Excel sheet uploaded alongside GitHub link as a separate attachment

---

## Citation Style

All references follow **IEEE citation format** as required by the IEEEtran LaTeX template. Citations appear as numbered bracketed references inline (e.g., `[1]`, `[2]`) and are listed in the References section in order of first appearance. The `.bib` file uses standard BibTeX entry types (`@article`, `@inproceedings`) fully compatible with `IEEEtran.bst`.

The Excel sheet uses **APA citation format** as required by the assignment instructions for that deliverable.

---

## Academic Integrity

All reviewed articles are properly cited with complete bibliographic information. All written analysis, critical summaries, and synthesis represent original work by Pradhyumn Nair, Vishesh Patel, and Oluwasola Smith. No text has been reproduced from source articles without attribution. This work complies fully with Georgia Southern University's academic integrity policy.

