# Lab 06 — Hypothesis Testing from Claims

EAES 480: Modern Statistics in Earth & Environmental Science  
University of Illinois Chicago  
Instructor: Dr. Gavin McNicol

---

# Dataset & Study Context

This lab continues using the simplified **AmeriFlux-style dataset** from the **US-AMS site at Argonne National Laboratory (near Chicago, IL)** covering **2023 at 30-minute resolution**.

## What is AmeriFlux?

AmeriFlux is a network of ecosystem observation sites (primarily **eddy covariance towers**) that measure exchanges of:

- carbon dioxide (CO₂),
- water vapor,
- energy,

between ecosystems and the atmosphere, along with supporting meteorological variables.

AmeriFlux overview:  
https://ameriflux.lbl.gov/about/about-ameriflux/

AmeriFlux variable documentation:  
https://ameriflux.lbl.gov/data/aboutdata/data-variables/

---

# Why This Dataset is Ideal for Hypothesis Testing

The US-AMS time series contains:

- strong seasonality,
- a clear day–night cycle,
- structured variability across months,
- and substantial short-term fluctuations.

These properties make it ideal for exploring:

- how **sample estimates differ from population parameters**,
- how **uncertainty affects our interpretation of estimates**, and
- how we can evaluate whether a **claim about the population is plausible**.

---

# Overview

This lab introduces **hypothesis testing** as a natural extension of sampling, sampling distributions, and bootstrap uncertainty.

Rather than simply estimating a mean, we now ask:

> If someone makes a claim about the population, do our data support that claim?

This assignment emphasizes:

- translating verbal claims into **null hypotheses**,
- computing **sample estimates**,
- estimating uncertainty using **bootstrap methods**,
- calculating **z-statistics and p-values**, and
- interpreting hypothesis tests in clear scientific language.

You will work in a structured **R Markdown (`.Rmd`) document** that includes:

- guided code chunks with fill-in sections,
- sections where you write code from scratch,
- and short written interpretation responses.

---

# Learning Goals

By the end of this lab, you should be able to:

- Translate a scientific claim into a **null hypothesis**
- Define and interpret a **population parameter**
- Draw a random sample and compute a **point estimate**
- Use bootstrap resampling to estimate **standard error**
- Compute and interpret a **z-statistic**
- Compute and interpret a **p-value**
- Explain how **confidence intervals and hypothesis tests are related**
- Produce a fully reproducible **R Markdown analysis**

---

# What You’ll Do

In the provided R Markdown template, you will:

- Select a **numeric variable** from the US-AMS dataset
- Define the **population parameter** of interest
- Formulate a **claim about the population mean**
- Convert the claim into **null and alternative hypotheses**
- Draw a sample and compute the **sample mean**
- Estimate uncertainty using **bootstrap resampling**
- Compute a **z-statistic and p-value**
- Determine whether the data **support or contradict the claim**
- Visualize the hypothesis test using the bootstrap distribution
- Write short explanations interpreting the results

This lab emphasizes **statistical reasoning as much as coding**.

---

# Repository Contents

Contents

* `lab-06-hypothesis-testing.Rmd`  
→ The lab template you will complete and submit

* `README.md`  
→ This file

* `data/us-ams-simple.csv`  
→ Simplified AmeriFlux-style dataset (US-AMS, 2023)

---

# Instructions

1. Fork or clone this repository to your own GitHub account  
2. Open `lab-06-hypothesis-testing.Rmd` in **RStudio**  
3. Work through the document **from top to bottom**  
4. Complete all code chunks (some fill-in, some from scratch)  
5. Answer interpretation prompts in complete sentences  
6. Knit regularly to catch errors early  

⚠️ Code that runs in the Console but not in the `.Rmd` does not count.

---

# Reproducibility Requirements

Your submission must:

- Knit without errors  
- Run top-to-bottom in a clean R session  
- Include all required libraries in the setup chunk  
- Avoid hard-coded local file paths  
- Use `na.rm = TRUE` where appropriate  
- Use `set.seed()` where instructed  
- Clearly define any chosen variable names (e.g., `target_var`)

These are not stylistic preferences—they are **scientific standards**.

---

# Submission

You should:

- Commit and push your completed `.Rmd` file to your GitHub repository
- Submit the **GitHub repository link** on Canvas

You do **not** need to submit the knitted HTML unless instructed.

Your work will be evaluated on:

- correctness of the statistical workflow,
- clarity of interpretation,
- understanding of hypothesis testing,
- and reproducibility.

---

# Collaboration Policy

Please consider:

- You may discuss statistical concepts and testing strategies with classmates
- You may not copy code verbatim from others
- Code you submit must be written and understood by you

---

# Why This Matters

In Earth & Environmental Science:

- we rarely observe full populations,
- measurements are limited by time and resources,
- and claims about environmental processes require evidence.

Hypothesis testing provides a structured way to evaluate whether **observed data are consistent with scientific claims**.

This lab marks the transition from **estimating quantities** to **evaluating hypotheses**, a central step in statistical inference.