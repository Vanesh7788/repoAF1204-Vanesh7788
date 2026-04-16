# AF1204 Individual Portfolio
Vanesh Kumar
BSc Accounting and Finance | City St Georges, University of London (Bayes Business School)
Module: AF1204 Introduction to Data Science and AI Tools

---

## Live Portfolio

https://vanesh7788.github.io/repoAF1204-Vanesh7788/

---

## About This Project

Built using Marimo, a reactive Python notebook framework, and deployed to GitHub Pages
as a WebAssembly (WASM) application. Demonstrates data literacy skills across Weeks 1 to 8
of AF1204.

The portfolio takes a sector-level and company-level exploration approach to the S&P 500
dataset, focusing on the relationship between firm size (market capitalisation),
credit health (Altman Z-Score), and borrowing cost. This is distinct from a purely
cross-sectional or time-series angle.

---

## Portfolio Structure

| Tab | Content | Key Skills |
|-----|---------|-----------|
| Profile | Two-column CV layout with CV download | Markdown, base64, mo.hstack |
| Sector Dashboard | Aggregated sector metrics embedded in mo.md() dashboard | Weeks 3, 4 |
| Company Explorer | Scatter with continuous colour + sunburst hierarchical chart | Weeks 3, 4, self-exploration |
| Research | ESG keyword bar, Z-Score histogram, LLM prompt builder | Weeks 7, 8 |
| Background | Written narrative about background and interests | Week 1 |

---

## Technical Skills Demonstrated

- Week 1: Markdown formatting and narrative writing
- Week 2: Altman Z-Score distress and safe zone thresholds, financial health logic
- Week 3: px.bar grouped horizontal chart, px.histogram, px.sunburst, px.scatter
- Week 4: mo.ui.dropdown, mo.ui.slider, reactive filtering, mo.hstack two-column layout, WASM deployment, mo.md() dashboard embedding with mo.as_html()
- Week 6: Winsorisation, missing value handling, data cleaning pipeline
- Week 7: Web scraping pipeline — Playwright, PyMuPDF, pytesseract, recursive URL crawling, df_DL.csv ledger
- Week 8: Structured prompt template, Temperature and Top P hyperparameter control, RAG via grounding context, structured multi-section output format
- Self-exploration: px.scatter with continuous RdYlGn colour scale, px.sunburst hierarchical breakdown, top-N company selection with groupby().apply(), Blues sequential colour mapping

---

## Design Choices

Profile tab uses a two-column hstack layout — a different structural approach
from standard vertical stacking. The Sector Dashboard uses the mo.md() embedding
pattern from the Week 4 dashboard template. The Company Explorer uses a continuous
colour gradient (cost of debt as colour intensity) rather than categorical sector
colours, asking a different analytical question: do financially healthier firms
tend to be larger? The CV is embedded as a base64-encoded DOCX with no external
file dependency.

---

## Project Structure

```
repoAF1204-[username]/
├── MyPortfolio.py    Main Marimo notebook
├── index.html        WASM export for GitHub Pages
└── README.md         This file
```

---

## How to Run Locally

```bash
pip install marimo pandas plotly pyarrow
marimo edit MyPortfolio.py
```

## How to Export for GitHub Pages

```bash
marimo export html-wasm MyPortfolio.py -o index.html --mode run
git add .
git commit -m "Export portfolio as WASM HTML for GitHub Pages deployment"
git push
```

---

Data source: S&P 500 financial dataset (Z-Score and Cost of Debt) provided by the
module lecturer via GitHub Gist. Built with Python, Marimo, pandas, Plotly.
Deployed via GitHub Pages WebAssembly.
