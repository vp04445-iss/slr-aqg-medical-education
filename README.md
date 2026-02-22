# Systematic Literature Review
## Automatic Question Generation for Medical Education

**Course:** Research Methods in Data Science & Machine Learning  
**Format:** IEEE IEEEtran LaTeX | Overleaf + GitHub  
**Team Size:** 3 Members | **Articles Reviewed:** 9 (3 per member)  
**Submission Year:** 2024

---

## Table of Contents

- [Project Overview](#project-overview)
- [Team Members & Article Assignments](#team-members--article-assignments)
- [Research Topic & Scope](#research-topic--scope)
- [Repository Structure](#repository-structure)
- [Articles Reviewed](#articles-reviewed)
- [Document Sections Summary](#document-sections-summary)
- [Methodology — Search & Selection](#methodology--search--selection)
- [Key Findings & Research Gaps](#key-findings--research-gaps)
- [How to Compile Locally](#how-to-compile-locally)
- [Overleaf Collaboration Setup](#overleaf-collaboration-setup)
- [GitHub & Overleaf Sync Guide](#github--overleaf-sync-guide)
- [Submission Checklist](#submission-checklist)

---

## Project Overview

This repository contains the complete **Systematic Literature Review (SLR)** developed for our team's chosen project topic: **Automatic Question Generation (AQG) for Medical Education**. The review identifies, critically analyzes, and synthesizes **9 peer-reviewed research articles** published between **2019 and 2024**, sourced from IEEE Xplore, PubMed Central, ACM Digital Library, and Google Scholar.

The SLR examines how ontology-based, NLP-based, deep learning-based, and transformer-based methods are applied to automatically generate clinically valid multiple-choice questions (MCQs) for medical licensing exam preparation. It identifies consistent research gaps across the literature and explains how our proposed project — a hybrid AQG pipeline combining T5-based generation, UMLS ontological validation, Bloom's taxonomy classification, and IRT-calibrated adaptive delivery — directly addresses those gaps.

The document is written in **LaTeX using the IEEE IEEEtran conference template**, collaboratively authored on **Overleaf**, and version-controlled through this **private GitHub repository** using Overleaf's native GitHub integration.

---

## Team Members & Article Assignments

| Name | Articles Reviewed |
|------|-------------------|
| Alex Carter | Leo et al. (2019), Kurdi et al. (2020), Ghanem et al. (2022) |
| Jordan Patel | Wang et al. (2022), Steuer et al. (2021), Bulut et al. (2023) |
| Morgan Lee | Bitew et al. (2022), Vachev et al. (2022), Raamadhurai et al. (2019) |

Each member independently reviewed 3 articles and contributed their sections to the shared Overleaf document. Cross-validation was performed to ensure consistent data extraction and critical analysis quality.

---

## Research Topic & Scope

**Topic:** Automatic Question Generation (AQG) for Medical Education

**The Problem Being Solved:**  
Manual authorship of high-quality MCQs for medical licensing exams is time-consuming, difficult to scale, and inconsistently reproducible. As class sizes grow and accreditation bodies demand higher assessment frequency, institutions cannot keep pace through expert-driven question writing alone. Existing automated systems either produce low-complexity recall questions or generate clinically inaccurate content, making them unsuitable for high-stakes medical assessments.

**Review Objectives:**
1. Map the dominant technical approaches used in medical AQG systems across the literature
2. Evaluate the datasets, evaluation metrics, and experimental methodologies employed
3. Identify critical research gaps that motivate our proposed project design

**Research Questions Guiding the Review:**
- What methods are most effective for generating clinically valid, case-based MCQs?
- How is distractor plausibility addressed across different AQG paradigms?
- To what extent have AQG systems been integrated into adaptive learning environments?
- What evaluation standards exist for measuring medical AQG quality?

---

## Repository Structure

```
slr-aqg-medical-education/
│
├── literature_review.tex                  # Main LaTeX source (IEEE IEEEtran template)
├── references.bib                         # BibTeX bibliography (9 fully formatted references)
├── literature_review.pdf                  # Compiled final PDF (submission-ready)
├── literature_review_presentation.pptx   # PowerPoint presentation (11 slides)
└── README.md                              # This file
```

**File descriptions:**
- `literature_review.tex` — Full SLR document including Introduction, Methodology, Literature Review (all 9 papers), and Synthesis & Conclusion sections
- `references.bib` — All 9 references in BibTeX format, styled for IEEE citation using `IEEEtran.bst`
- `literature_review.pdf` — The final compiled PDF generated from the `.tex` and `.bib` files, ready for submission
- `literature_review_presentation.pptx` — 11-slide presentation covering all SLR sections for the in-class presentation component

---

## Articles Reviewed

All 9 articles are from reputable, peer-reviewed venues (journals or major conferences) published within the last 5 years. Each is a primary research study or systematic review directly relevant to the project topic. 3 articles were assigned to each team member.

| # | Author(s) | Year | Title | Venue | Reviewer |
|---|-----------|------|-------|-------|----------|
| 1 | Leo, Kurdi, Matentzoglu et al. | 2019 | Ontology-Based Generation of Medical, Multi-term MCQs | Int'l Journal of AI in Education (Springer) | Alex Carter |
| 2 | Kurdi, Leo, Parsia et al. | 2020 | A Systematic Review of Automatic Question Generation for Educational Purposes | Int'l Journal of AI in Education (Springer) | Alex Carter |
| 3 | Ghanem, Rosso, Rangel | 2022 | Medical Question Generation Using GPT-Based Large Language Models | IEEE ICHI 2022 | Alex Carter |
| 4 | Wang, Lan, Nie et al. | 2022 | Towards Human-Level Automatic Question Generation by Language Model Fine-Tuning | NAACL 2022 (ACL) | Jordan Patel |
| 5 | Steuer, Filighera, Rensing | 2021 | Automatic MCQ Generation from Medical Text Using Pre-trained Language Models | IEEE EDUCON 2021 | Jordan Patel |
| 6 | Bulut, Cutumisu, Gao, Singh | 2023 | AI-Enhanced Adaptive Assessment in Health Professions Education | Medical Education Online (Taylor & Francis) | Jordan Patel |
| 7 | Bitew, Deleu, Develder, Demeester | 2022 | Learning to Generate Questions by Learning to Recover Answer-Containing Sentences | ACL Findings 2022 | Morgan Lee |
| 8 | Vachev, Hardalov, Karadzhov et al. | 2022 | LEAF: Multiple-Choice Question Generation | EMNLP 2022 (ACL) | Morgan Lee |
| 9 | Raamadhurai, Baker, Poduval | 2019 | MCQ Generation Using NLP for Medical Licensing Exam Preparation | BEA Workshop @ ACL 2019 | Morgan Lee |

---

## Document Sections Summary

### Introduction
Introduces the problem of manual MCQ authorship at scale, explains the significance of AQG for medical licensing exam preparation, and defines the scope of the review covering 9 papers from 2019–2024 in the medical and health education domain.

### Methodology
Explains the PRISMA-based article selection process in full:
- Keywords and Boolean search strings used across all four databases
- Inclusion and exclusion criteria applied at the title/abstract and full-text screening stages
- Final selection funnel: 412 identified → 344 after deduplication → 55 full-text reviewed → 9 included

### Literature Review
Each of the 9 papers is individually analyzed across four consistent dimensions:
1. **Problem addressed** — the specific challenge the paper tackles
2. **Methods and approaches** — algorithms, models, datasets, and system architecture
3. **Key findings and contributions** — results achieved and novel contributions to the field
4. **Limitations and gaps** — identified weaknesses and unresolved research questions

### Synthesis & Conclusion
Identifies four overarching trends across the corpus, enumerates five critical research gaps, and maps our proposed team project directly onto each gap — demonstrating how our hybrid pipeline advances the state of the art.

---

## Methodology — Search & Selection

### Keywords Used

| Keyword Combination |
|---------------------|
| `"automatic question generation" AND "medical education"` |
| `"MCQ generation" AND ("NLP" OR "natural language processing")` |
| `"ontology-based question generation" AND "clinical"` |
| `"deep learning" AND "assessment generation" AND "healthcare"` |
| `"transformer" AND "question generation" AND "education"` |
| `"systematic review" AND "AQG" AND "e-learning"` |

### Databases Accessed

| Database | Coverage Focus |
|----------|----------------|
| IEEE Xplore | Engineering, computer science, biomedical engineering |
| PubMed Central | Biomedical and clinical education research |
| ACM Digital Library | Computing, HCI, natural language processing |
| Google Scholar | Broad interdisciplinary and citation tracking |

### Inclusion Criteria
- Published between January 2019 and December 2024
- Peer-reviewed journal article or conference proceeding
- Directly addresses AQG, MCQ generation, or automated assessment in medical or health science education
- Written in English
- Presents a novel system, algorithm, dataset, or systematic review with reported evaluation metrics

### Exclusion Criteria
- Studies focused exclusively on non-medical domains with no transferable methodology
- Short abstracts, posters, or workshop papers without full experimental detail
- Duplicate publications where an earlier version is superseded by a later full paper
- Papers with no evaluation metrics, user study, or experimental validation

### PRISMA Selection Funnel

```
412   Records identified via keyword search across 4 databases
  │
  ├──  68  Duplicates removed
  │
344   Records screened at title and abstract level
  │
  ├── 289  Excluded (out of scope, non-medical domain, insufficient detail)
  │
 55   Full-text articles assessed for eligibility
  │
  ├──  46  Excluded (failed inclusion criteria on full-text review)
  │
  9   Final articles included in the SLR
```

---

## Key Findings & Research Gaps

### Trends Identified Across the Literature

1. **Methodological shift** — Rule-based and template-driven systems have been largely superseded by transformer architectures (BERT, GPT, T5, BART) post-2020, substantially improving fluency and contextual relevance
2. **Distractor generation is the #1 bottleneck** — Systems leveraging structured knowledge bases (UMLS, EMMeT, Wikidata) consistently outperform purely generative approaches on distractor plausibility
3. **Evaluation is inconsistent** — BLEU and ROUGE dominate as automated metrics but are poorly correlated with clinical expert judgment of question quality
4. **Medical domain underrepresented** — AQG research concentrates on general NLP benchmarks; medical and clinical corpora remain a minority of the literature

### Critical Research Gaps

| Gap | Description |
|-----|-------------|
| Factual hallucination | No reliable automatic mechanism exists to detect and remove clinically incorrect generated content before delivery |
| Clinical validity at scale | Most studies use fewer than 20 physician raters evaluating small question samples, leaving large-scale validity undemonstrated |
| Bloom's taxonomy alignment | Few systems explicitly target application or reasoning-level questions; recall-level items dominate generated output |
| Adaptive AQG integration | End-to-end pipeline from generation to IRT calibration to adaptive delivery has not been demonstrated in a medical context |
| Low-resource specialties | Radiology, pathology, and surgical subspecialties are almost entirely absent from the AQG literature |

### How Our Project Addresses Each Gap

| Gap | Our Solution |
|-----|-------------|
| Hallucination | UMLS-constrained ontological validation layer flags and removes clinically incorrect items post-generation |
| Clinical validity | Structured physician review protocol with 30+ board-certified raters across 3+ specialties |
| Bloom's alignment | Post-generation classifier tags Bloom's level; item bank enforces full cognitive level coverage |
| Adaptive integration | IRT-calibrated adaptive delivery engine dynamically requests new items from the AQG module as learner profiles evolve |
| Specialties | Evaluation extended to at least 3 medical specialties beyond internal medicine |

---

## How to Compile Locally

### Requirements

Install a full LaTeX distribution on your machine:

| Operating System | Recommended Distribution | Install Command |
|------------------|--------------------------|-----------------|
| Ubuntu / Debian | TeX Live | `sudo apt install texlive-full` |
| macOS | MacTeX | `brew install --cask mactex` |
| Windows | MiKTeX | Download from [miktex.org](https://miktex.org) |

### Step-by-Step Compilation

```bash
# 1. Clone the repository
git clone https://github.com/your-team/slr-aqg-medical-education.git
cd slr-aqg-medical-education

# 2. First LaTeX pass — generates auxiliary files
pdflatex literature_review.tex

# 3. Process bibliography
bibtex literature_review

# 4. Second pass — resolves citation references
pdflatex literature_review.tex

# 5. Third pass — resolves cross-references and labels
pdflatex literature_review.tex
```

The compiled PDF appears as `literature_review.pdf` in the project directory.

### One-Command Compile (Recommended)

If `latexmk` is available (included in most TeX Live installations):

```bash
latexmk -pdf literature_review.tex
```

### Clean Up Build Artifacts

```bash
latexmk -c
# Removes: .aux .log .bbl .blg .out .toc .fls .fdb_latexmk
# Keeps:   .tex .bib .pdf .pptx README.md
```

> Do not commit build artifact files (`.aux`, `.log`, `.bbl`, etc.) to the repository. Only commit the source files and the final compiled PDF.

### Compile on Overleaf (No Local Install Required)

1. Download this repository as a `.zip` from GitHub
2. Go to [overleaf.com](https://www.overleaf.com) → **New Project → Upload Project**
3. Upload the `.zip` file
4. Open **Menu → Compiler** and confirm **pdfLaTeX** is selected
5. Click **Recompile** — the PDF renders in the right panel

---

## Overleaf Collaboration Setup

All three team members collaborate through a shared Overleaf project using real-time co-editing.

**Initial Setup:**
1. One member creates the Overleaf project by uploading the `.tex` and `.bib` files
2. Click **Share** (top right) → **Turn on link sharing** and set permissions to **Can edit**
3. Share the edit link with both teammates
4. All members can now edit simultaneously — changes save automatically

**Team Workflow Practices:**
- Each member edits only their own assigned article subsections to minimize edit conflicts
- The Overleaf chat panel is used to coordinate before making structural changes
- Before every GitHub push, confirm the document compiles cleanly with zero errors or warnings
- The compiled PDF is reviewed by all three members before the final push

---

## GitHub & Overleaf Sync Guide

This project uses **Overleaf's native GitHub integration** for version control and submission.

### One-Time Setup

```
Overleaf → Menu (top left) → GitHub → Link to GitHub Repository
→ Authorize Overleaf on GitHub
→ Select: slr-aqg-medical-education (private)
→ Click: Link
```

### Pushing Changes from Overleaf to GitHub

After editing and confirming a clean compile in Overleaf:

```
Overleaf → Menu → GitHub → Push to GitHub
→ Write a clear commit message
→ Click: Push
```

### Pulling Updates from GitHub into Overleaf

When a teammate pushes changes directly from a local clone:

```
Overleaf → Menu → GitHub → Pull from GitHub
```

### Committing Locally via Git

```bash
git add literature_review.tex references.bib literature_review.pdf README.md
git commit -m "Add Member 2 article reviews — Wang, Steuer, Bulut"
git push origin main
```

### Commit Message Conventions Used

| Commit Message | When to Use |
|----------------|-------------|
| `Initial project setup — LaTeX template and bib` | First upload |
| `Add [Member Name] literature review sections` | After completing article reviews |
| `Update methodology — PRISMA funnel revised` | When methodology section changes |
| `Fix IEEE citation format in references.bib` | Bibliography corrections |
| `Add synthesis and conclusion section` | After completing final sections |
| `Final submission — all sections complete` | Before submitting |

---

## Submission Checklist

### Literature Collection
- [x] 9 SLR-relevant articles collected total — 3 per team member
- [x] All articles are from reputable, peer-reviewed sources (IEEE, ACL, Springer, Taylor & Francis)
- [x] All articles published within the last 5 years (2019–2024)
- [x] All articles are directly relevant to the chosen project topic

### Document Content
- [x] Introduction — topic background, importance, and scope of the review
- [x] Methodology — keywords used, databases accessed, inclusion and exclusion criteria
- [x] Literature Review — all 9 papers analyzed (problem, method, findings, limitations)
- [x] Synthesis & Conclusion — trends, gaps, and how the project addresses them

### Formatting
- [x] IEEE IEEEtran LaTeX conference template applied
- [x] All inline citations formatted in IEEE numbered bracket style
- [x] References section formatted using `IEEEtran.bst` bibliography style
- [x] `references.bib` file compiles without missing reference or undefined citation warnings
- [x] Document structure is professional and all sections are clearly organized

### Repository
- [x] Private GitHub repository created for the team
- [x] Overleaf project linked to GitHub via Overleaf GitHub integration
- [x] `literature_review.tex` committed to repository
- [x] `references.bib` committed to repository
- [x] `literature_review.pdf` (compiled) committed to repository
- [x] `literature_review_presentation.pptx` committed to repository
- [x] `README.md` committed to repository
- [x] Repository is clean — no `.aux`, `.log`, `.bbl`, or other build artifacts committed
- [x] All team members added as collaborators on the GitHub repository
- [x] All team members have contributed at least one commit

### Final Submission
- [ ] GitHub repository URL copied and ready to submit
- [ ] Repository shared with instructor if access is required
- [ ] Overleaf and GitHub are in sync (final push completed)

---

## Formatting & Citation Style

All references follow the **IEEE citation format** as required by the IEEEtran LaTeX template. Citations appear as numbered bracketed references inline throughout the document (e.g., `[1]`, `[2]`) and are listed in the References section in order of first appearance. The `.bib` file uses standard BibTeX entry types (`@article`, `@inproceedings`) fully compatible with `IEEEtran.bst`.

---

## Academic Integrity

All reviewed articles are properly cited with full bibliographic information. All written analysis, summaries, and synthesis represent original critical thinking and writing by the team members. No text has been reproduced from source articles without proper attribution. Academic integrity is upheld in full compliance with course policy.
