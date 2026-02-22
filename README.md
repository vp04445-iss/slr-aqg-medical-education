# Systematic Literature Review: Automatic Question Generation for Medical Education

## Project Overview

This repository contains the Systematic Literature Review (SLR) for our team project on **Automatic Question Generation (AQG) for Medical Education**. The review synthesizes nine peer-reviewed studies published between 2019 and 2024, examining ontology-based, NLP-based, and deep learning-based approaches to generating MCQs for clinical and licensing exam preparation.

The document is formatted using the **IEEE LaTeX Conference Template** and was collaboratively authored by a three-member team using Overleaf and synchronized via the Overleaf–GitHub integration.

---

## Repository Structure

```
.
├── literature_review.tex    # Main LaTeX source file (IEEE template)
├── references.bib           # BibTeX bibliography (9 references)
├── literature_review.pdf    # Compiled PDF (final submission)
└── README.md                # This file
```

---

## Topic Summary

**Research Topic:** Automatic Question Generation for Medical Education

**Research Problem:** Manual MCQ authorship for medical licensing exams is time-consuming, inconsistently reproducible, and unable to scale with growing class sizes and assessment frequency requirements.

**Scope of Review:** The SLR covers 9 papers across four databases (IEEE Xplore, PubMed, ACM Digital Library, Google Scholar) using the following key themes:
- Ontology-based MCQ generation
- Transformer-based (BERT, GPT, T5, BART) question generation
- Distractor generation strategies
- Adaptive assessment integration
- Evaluation methodologies for AQG systems

**Key Findings:**
- Transformer-based models have surpassed template-based approaches in fluency and contextual relevance.
- Distractor plausibility remains the most challenging component of medical MCQ generation.
- No unified evaluation standard exists across the field.
- Adaptive integration of AQG into learning systems is critically underexplored.

---

## Team Members

| Member | Articles Reviewed |
|--------|-------------------|
| Member 1 | Leo et al. (2019), Kurdi et al. (2020), Ghanem et al. (2022) |
| Member 2 | Wang et al. (2022), Steuer et al. (2021), Bulut et al. (2023) |
| Member 3 | Bitew et al. (2022), Vachev et al. (2022), Raamadhurai et al. (2019) |

---

## Compiling the Document Locally

### Prerequisites

Ensure you have a full LaTeX distribution installed:

- **Linux/macOS:** [TeX Live](https://www.tug.org/texlive/)
  ```bash
  sudo apt install texlive-full       # Debian/Ubuntu
  brew install --cask mactex          # macOS (Homebrew)
  ```
- **Windows:** [MiKTeX](https://miktex.org/) or [TeX Live](https://www.tug.org/texlive/windows.html)

### Compilation Steps

Clone the repository and compile using `pdflatex` + `bibtex`:

```bash
# 1. Clone the repository
git clone https://github.com/your-team/slr-aqg-medical-education.git
cd slr-aqg-medical-education

# 2. First pass — generates auxiliary files
pdflatex literature_review.tex

# 3. Process bibliography
bibtex literature_review

# 4. Two more passes to resolve citations and references
pdflatex literature_review.tex
pdflatex literature_review.tex
```

The compiled PDF will be saved as `literature_review.pdf`.

### Quick Compile (Latexmk)

If you have `latexmk` installed:

```bash
latexmk -pdf literature_review.tex
```

### Using Overleaf

1. Download the repository as a `.zip` file.
2. Log in to [Overleaf](https://www.overleaf.com).
3. Click **New Project → Upload Project** and upload the `.zip`.
4. Set the compiler to **pdfLaTeX** in the Overleaf settings menu.
5. Click **Recompile**.

---

## Overleaf Integration

This project was developed collaboratively on Overleaf and synchronized to this repository using the **Overleaf–GitHub Sync** feature:

1. In Overleaf, open the project and click **Menu → GitHub**.
2. Select **Push to GitHub** to sync changes to this repository.
3. Use **Pull from GitHub** to receive updates from teammates.

---

## Submission Checklist

- [x] 9 SLR articles reviewed (3 per team member)
- [x] All sections present: Introduction, Methodology, Literature Review, Synthesis & Conclusion
- [x] IEEE template applied with correct bibliography style
- [x] `.tex` source file included
- [x] `.bib` bibliography file included
- [x] Compiled PDF included
- [x] README with compilation steps included
- [x] Repository clean with no extraneous files

---

## Citation Style

All references follow **IEEE citation style** as required by the IEEEtran LaTeX template. The `.bib` file uses standard BibTeX entry types (`@article`, `@inproceedings`) compatible with the `IEEEtran` bibliography style.

---

## Academic Integrity

All reviewed articles are properly cited. Summaries and analyses represent original critical writing by the team. No text has been reproduced from sources without attribution.
