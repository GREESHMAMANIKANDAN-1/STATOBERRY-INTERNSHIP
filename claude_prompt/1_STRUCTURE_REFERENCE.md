# RAISINS Tutorial — Structural Reference
## Extracted from: Completely Randomised Design (CRD) Tutorial

---

## YAML Front Matter (keep identical for all tutorials)

```yaml
---
title: "[MODULE NAME]"
format:
  html:
    mainfont: "Times New Roman"
    fontsize: 0.90em
    theme: cosmo
    toc: true
    lightbox: true
    number-sections: true
    number-depth: 3
    number-offset: 1
    toc-title: "**TABLE OF CONTENTS**"
    toc-depth: 3
    linkcolor: "purple"
    citations-hover: true
    css: sty.css
---
```

---

## HTML Style Block (keep identical for all tutorials)

```html
<style>
 sup { color: blue; font-size: 0.8em; }
 .affiliations { color: grey; font-size: 0.9em; margin-top: 0.2em; }
</style>
```

---

## Affiliations Line (keep identical for all tutorials)

```
::: affiliations
¹Statoberry LLP, ²Department of Agricultural Statistics, Kerala Agricultural University
:::
```

---

## SECTION STRUCTURE (in order)

### 0. ABSTRACT
- **Type:** Justified paragraph
- **Content:** 4–5 sentences introducing the design, what it does, how RAISINS handles it, what the tutorial covers, and what outputs users can expect (publication-ready tables/plots, multivariate analysis).
- **Key elements to mention:** Design name in bold, RAISINS in bold, mention of MANOVA and PCA.

---

### 1. Introduction `<details>` Block
- **Type:** Collapsible `<details>` element with `<summary>` styled in `#5DADE2`
- **Summary label:** "Introduction [Design Name]"
- **Content:** Historical background of the design (who developed it, when, for what purpose). Uses `.hover-img` CSS class for a scientist's portrait image with popup on hover.
- **Image:** `www/[scientist].webp` — replace for each module if applicable, or omit.

---

### 2. Section: Analysis of Experiments `{#AE}`
- **Type:** Justified paragraph + 1 screenshot
- **Content:** Directs user to RAISINS homepage → Analysis of experiments tab → identifies the specific design being discussed.
- **Screenshot label:** "Analysis of experiment tab"
- **Screenshot file:** `www/intro.webp` → **[REPLACE WITH MODULE SCREENSHOT]**
- **Cross-reference:** `@fig-aov`

---

### 3. Section: [Design Name] `{#C}`
- **Type:** Justified paragraph + collapsible layout diagram
- **Content:** Definition of the design, when it is used, its strengths, and when alternatives are more appropriate.
- **Callout tip:** One-sentence definition of the design.
- **Details block:** Layout diagram explanation. Image: `www/[layout].webp` → **[REPLACE]**

---

### 4. Section: A Working Example `{#W}`
- **Type:** Justified paragraph + 1 screenshot of example dataset
- **Content:** Introduces a hypothetical dataset. Describes: number of treatments, what treatments represent (e.g., varieties), number of replicates, variable names.
- **Screenshot:** `www/[datasetname].webp` → **[REPLACE OR KEEP PLACEHOLDER]**
- **Defines key terms:** "Treatments" and "Variables" in bold.

---

### 5. Section: How to Prepare Your Data? `{#sec-4 .H}`
- **Type:** Justified paragraph + 1 screenshot
- **Content:** Instructions for preparing Excel file for RAISINS upload (single sheet, no blank rows, proper column names). Mentions two options: MS Excel or in-app creation.
- **Screenshot:** `www/CREATEDAT.webp` → **[REPLACE OR KEEP]**

---

### 6. Section: [Design] Analysis Tab Explained `{#AO}`
- **Type:** Justified paragraph + 1 screenshot with annotations
- **Content:** Explains the Analysis tab UI — Browse button, Treatment/Variables selection, Run Analysis button.
- **Screenshot:** `www/sstabs.webp` → **[REPLACE]**
- **Transition note:** Mentions transformation option for non-normal data.

---

### 7. Section: Transformation `{#sec-6 .T}`
- **Type:** Justified paragraph + 1 screenshot + 3 sub-explanations
- **Content:** When and why to use Log, Square Root, and Arcsine transformations. Definitions of each.
- **Screenshot:** `www/trans.webp` → **[REPLACE OR KEEP]**
- **Blockquote:** "After choosing the appropriate transformation proceed to @sec-7 for analysis."

---

### 8. Section: Analysis Results `{#sec-7 .AR}`
- **Type:** Justified paragraph + 2 tables with screenshots + interpretation subsections
- **Content:**
  - **Table 1 — ANOVA Summary:** F-test result. Screenshot: `www/res1.webp` → **[REPLACE]**
    - Collapsible ANOVA table explanation
    - Interpretation subsection `### Interpretation from @fig-100`
  - **Table 2 — Detailed tabular result with multiple comparisons:** Screenshot: `www/Result2.webp` → **[REPLACE]**
    - Collapsible overview of parameters (Treatments, Response Variable, Post-hoc grouping, F stat, p value, CD, SE, MSE, CV%, Cohen's F)
    - Interpretation subsection `### Interpretation from @fig-101`
    - 2 callout-tip boxes (one on Tukey's HSD/DMRT, one on Cohen's f)

---

### 9. Section: Multiple Comparison Tests `{#sec-8 .MCT}`
- **Type:** Collapsible intro + justified paragraphs
- **Content:** What is a post-hoc test (collapsible). Then explains LSD, Tukey's HSD, DMRT — with formulas for LSD.
- **Screenshot:** `www/CUSRES.webp` → **[REPLACE]**
- **Collapsible:** Full post-hoc test details (LSD formula, HSD explanation, DMRT explanation)
- **"Which post-hoc test to use?" paragraph** comparing the three options.

---

### 10. Section: Summary Stats `{#SUM}`
- **Type:** Justified paragraph + 1 table screenshot + collapsible parameter descriptions + interpretation
- **Content:** How to access Summary Stats tab. Table shows Mean, SD, SE, Min/Max, CV, Skewness, Kurtosis per treatment.
- **Screenshot:** `www/summary_stat.webp` → **[REPLACE]**
- **Collapsible:** Definitions of all statistical metrics in the table.
- **Interpretation subsection** `### Interpretations from @fig-102`

---

### 11. Section: Individual ANOVA `{#IA}`
- **Type:** Justified paragraph + 2 table screenshots + collapsible + 2 interpretation subsections
- **Content:** How to get individual ANOVA tables per variable. Shows F-stat, CD, CV%, MSE, SE(m), SE(d).
- **Screenshot 1 (Table 4):** `www/INDIVIDUAL ANOVA.webp` → **[REPLACE]**
- **Screenshot 2 (Table 5):** `www/summary_abc.webp` → **[REPLACE]**
- **Collapsible:** Definitions of CD, CV%, MSE, SE(m), SE(d) with formulas.

---

### 12. Section: Basic Plots `{#BP}`
- **Type:** Justified paragraph + interactive hover grid of 5 plots
- **Content:** How to access Basic Plots tab. Mentions gear icon for customization, download options (PNG 300dpi, JPEG, TIFF, PDF, SVG).
- **Subsection:** "Customizing plots" — screenshot of settings panel: `www/customize.webp` → **[REPLACE]**
- **Plot grid (2-column CSS grid):** 5 plots with hover-reveal descriptions:
  1. Box plot — `www/box.webp` → **[REPLACE]**
  2. Violin plot — `www/violin.webp` → **[REPLACE]**
  3. Bar plot — `www/bar.webp` → **[REPLACE]**
  4. Mean Value Plot — `www/mean.webp` → **[REPLACE]**
  5. Connected line plot — `www/connect.webp` → **[REPLACE]**

---

### 13. Section: Advanced Plots `{#AP}`
- **Type:** Justified paragraphs + 5 individual plot screenshots with descriptions
- **Content:** Overview of advanced plots. Each with a bolded title, screenshot, and paragraph explanation.
  1. Summary Plot — `www/plot summary.webp` → **[REPLACE]**
  2. Advanced Raincloud Plot — `www/advanced_raincloud.webp` → **[REPLACE]**
  3. QQ Plot — `www/qq_plot.webp` → **[REPLACE]**
  4. Rain Cloud Plot — `www/raincloud_plot.webp` → **[REPLACE]**
  5. Distribution Plot — `www/distri.webp` → **[REPLACE]**

---

### 14. Section: AI Interpretation `{#AI}`
- **Type:** Justified paragraph + 1 screenshot
- **Content:** Describes RAISINS AI Assistant — summarizes results, identifies significant differences, suggests next steps.
- **Screenshot:** `www/ai.webp` → **[REPLACE OR KEEP]**

---

### 15. Section: Multivariate `{#MUL}`
- **Type:** Justified paragraphs + 7 screenshots
- **Content:** Multivariate analysis — MANOVA + PCA. Explains:
  - How to navigate to Multivariate tab
  - MANOVA table interpretation
  - Eigen Values / PCA variance explained
  - Scree plot
  - Loadings table and interpretation
  - PCA Biplot interpretation
  - Scaled Index Score with cutoff selector
- **Screenshots (in order):**
  1. Multivariate tab: `www/MultiTAB.webp` → **[REPLACE]**
  2. MANOVA Results: `www/MAN2.webp` → **[REPLACE]**
  3. PCA Index Score: `www/MAN3.webp` → **[REPLACE]**
  4. Scree Plot: `www/CRD_Scree_Plot*.webp` → **[REPLACE]**
  5. Loadings: `www/MAN4.webp` → **[REPLACE]**
  6. Biplot: `www/BiplotPCA*.webp` → **[REPLACE]**
  7. Index Score: `www/MAN5.webp` + `www/Indexplot*.webp` → **[REPLACE]**

---

### 16. Section: Preparing Your Data `{#PRE}`
- **Type:** Quote + numbered list
- **Content:** Motivational quote about data quality. Two options: MS Excel or RAISINS app.

---

### 17. Section: Preparing Data in MS Excel `{#EX}`
- **Type:** Justified paragraph + 2 format screenshots + 2 collapsible blocks
- **Content:** Column-based format instructions, file format (CSV preferred), naming rules.
- **Screenshots:** `www/P1.webp`, `www/P2.webp` → **[REPLACE OR KEEP]**
- **Collapsibles:** Dataset Creation Rules, How to Save as CSV in MS Excel.

---

### 18. Section: Creating Dataset in RAISINS `{#CR}`
- **Type:** Justified paragraph + bullet list + 1 screenshot
- **Content:** How to use Create Data Tab — select Treatments, Replications, Characters, click Create.
- **Screenshot:** `www/CREATEDAT.webp` → **[KEEP — same UI]**

---

### 19. Section: Model Datasets `{#M}`
- **Type:** Short justified paragraph + 1 screenshot
- **Content:** Users can download model datasets from the Datasets tab to test the app.
- **Screenshot:** `www/modeldata.webp` → **[KEEP — same UI]**

---

### 20. Section: FAQ's `{#F}`
- **Type:** Short paragraph + 1 screenshot
- **Content:** Points user to FAQs tab within the app.
- **Screenshot:** `www/FAQ TAB.webp` → **[KEEP — same UI]**

---

### 21. Section: View Data `{#U}`
- **Type:** Short paragraph + 1 screenshot
- **Content:** View Data as diagnostic tool — Health Check on upload, validates column types and formatting.
- **Screenshot:** `www/view data.webp` → **[KEEP — same UI]**

---

## RECURRING STYLE RULES

| Element | Rule |
|---|---|
| All body text | `{style="text-align: justify;"}` |
| Collapsible blocks | `<details>` + `<summary style="color: #5DADE2">` |
| Callout tips | `::: callout-tip` with `####` heading |
| Section IDs | Short uppercase abbreviations in `{#ID}` |
| Screenshot captions | Short descriptive labels |
| Cross-references | `@fig-XXX` and `@sec-X` throughout |
| Plot hover grid | CSS `.plot-container` + `.plot-description` + JS `showDescription/hideDescription` |
| Formulas | LaTeX in `$$...$$` blocks |
| Image folder | All images in `www/` subfolder |
| Screenshot placeholder | `![Caption](www/SCREENSHOT_PLACEHOLDER.webp){#fig-XX fig-align="center"}` |
