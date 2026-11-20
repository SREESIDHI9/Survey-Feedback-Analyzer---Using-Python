# Survey-Feedback-Analyzer - Using-Python
Python tool that adds user survey entries, cleans messy feedback text, counts keywords, computes average ratings and longest comments, extracts unique words, and ranks responses by rating.

## Project Overview
This project builds a Python-based text and rating feedback analysis tool using core programming constructs—dictionaries of lists, loops, conditionals, string manipulation, user-defined functions, `zip()`, and `sorted()`. Starting from preloaded survey responses, it supports adding new user entries, normalizing messy text, counting keyword appearances, summarizing ratings and vocabulary, and ranking feedback by score.

## Objective
* Collect and append new survey feedback entries (`Name`, `Feedback`, and `Rating` from 1–5) with automatic `S_No` increments onto a preloaded dictionary of lists
* Clean raw feedback text by stripping punctuation (`.`, `,`, `!`, `?`), collapsing extra whitespace, trimming leading/trailing spaces, and converting text to lowercase
* Implement a reusable `count_word_in_feedbacks(word)` function to measure case-insensitive word occurrences across feedback entries
* Compute summary metrics including overall average rating, longest comment by word count, unique vocabulary list, and descending rating-based sorting.

## Dataset Description
* **Structure (`feedback_data`):** A Python dictionary of lists containing four keys: `S_No` (integer IDs), `Name` (respondent names), `Feedback` (free-text comments), and `Rating` (numeric ratings on a 1–5 scale).
* **Initial & Appended Records:** Starts with 10 preloaded entries (`S_No` 1–10: Ravi, Meera, Sam, Anu, Raj, Divya, Arjun, Kiran, Leela, Nisha) and supports appending additional entries starting at `S_No` 11 (e.g., an 11th entry for `G.one` / `G.ONE` with rating `5`).
* **Text Characteristics:** Raw entries include capitalization variations, punctuation marks (`!`, `,`, `.`, `?`), extra spaces, and mixed sentiment phrases ranging from strong praise to dissatisfaction.

## Workflow
* **Step 1 — Preloaded Feedbacks:** Initialized the `feedback_data` dictionary of lists with 10 baseline survey records.
* **Step 2 — Add More Feedbacks:** Prompted the user for the number of additional entries, collected `Name`, `Feedback`, and `Rating` (`1–5`), auto-assigned sequential `S_No` values, and appended each entry to `feedback_data`.
* **Step 3 — Text Cleaning:** Iterated through `feedback_data['Feedback']` to remove `.`, `,`, `!`, and `?`, convert strings to lowercase, and normalize spacing via `.split()` and `' '.join()`.
* **Step 4 — Word Count Insights:** Defined `count_word_in_feedbacks(word)` and queried feedback counts for `"good"`, `"poor"`, and `"excellent"`.
* **Step 5 — Final Summary, Insights & Sorting:** Printed the cleaned `feedback_data` dictionary, calculated the average rating, identified the longest comment by word count, extracted sorted unique words using a `set`, and sorted entries from highest to lowest rating using `zip()` and `sorted()`.

## Key Findings
* **Rating Performance:** Across the 11 recorded feedbacks in the notebook run, ratings range from 1 to 5 with an average rating of **3.55** (4 five-star, 2 four-star, 2 three-star, 2 two-star, and 1 one-star entry).
* **Keyword Mentions:** After text cleaning, `"good"` appears in **3** feedbacks, `"poor"` appears in **2** feedbacks, and `"excellent"` appears in **1** feedback.
* **Longest Comment:** The longest comment is `"poor response and poor handling of issue"` at **7 words** (paired with a rating of 1).
* **Vocabulary Breadth:** All cleaned feedbacks together contain **33 unique words** (e.g., *service*, *support*, *experience*, *care*, *food*, *ambience*, *response*, *handling*, *issue*, *satisfied*).

## Business & Policy Recommendations
* **Address Service & Issue Handling Friction:** Because the lowest rating (`1`) and longest comment (`"poor response and poor handling of issue"`) highlight response and issue-handling gaps—alongside `"poor support not happy"` at rating `2`—establish clear SLA response targets and follow-up loops for unresolved tickets.
* **Reinforce High-Impact Service Pillars:** Leverage positive drivers seen in 4- and 5-star entries (`good food and good ambience`, `good support quick service`, `excellent care excellent staff`, `very good service`) as operational benchmarks.
* **Convert Neutral/Moderate Ratings:** Follow up with mid-tier respondents (`3` ratings such as `"satisfied but could be better"` and `"okay okay"`) to identify specific improvements that lift scores to 4 or 5.

## Tools Used, Tech Stack & Libraries
* **Programming Language:** Python 3 (core built-ins: `dict`, `list`, `set`, `str`, `int`, `len()`, `sum()`, `zip()`, `sorted()`, `input()`, `print()`)
* **Environment & Tooling:** Jupyter Notebook (`.ipynb`), IPython kernel
* **Version Control & Documentation:** Git, GitHub, Markdown (`README.md`)

## Repository Structure
```text
survey-feedback-analyzer/
├── README.md
├── ModuleEndAssignment.ipynb
└── docs/
    └── Module End Assignment 3_Python Fundamentals - Survey Feedback Analyzer (1).pdf
```

---

**Author:** Sree Sidhi
