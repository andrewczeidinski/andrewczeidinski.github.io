---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
tags: ["research", "dashboard", "data"]
author: ["Andrew Czeidinski"]
description: "Short description for search engines (less than 155 characters)."
summary: "Short summary for the research list page (less than 265 characters)."
cover:
    image: "{{ .Name }}.png"
    alt: "{{ replace .Name "-" " " | title }}"
    relative: true
editPost:
    URL: "https://github.com/andrewczeidinski"
    Text: "Project repository"
showToc: true
disableAnchoredHeadings: false

---

This research page presents the motivation, evidence, outputs, and supporting materials for the project. Replace this overview with a concise explanation of the question, why it matters, and what the reader can do with the results below.

---

## Key updates

+ {{ dateFormat "January 2006" .Date }} - Project page created.
+ Month Year - Add a short note about a dataset update, release, paper, presentation, or policy development.

---

## Research question

State the central research question in plain language. Explain the scope, the population or system being studied, and the practical decision or scientific debate the work informs.

---

## Main output

<iframe
    src="main-output.html"
    title="Main research output"
    style="width: 100%; aspect-ratio: 4 / 3; border: none;">
</iframe>

+ *Construction:* Explain how the measure, model, figure, or dashboard panel is built.
+ *Interpretation:* Explain what a high, low, rising, or falling value means.
+ *Source:* Describe the underlying data source and link to it when possible.
+ [Download data](main-output.csv)
+ [View in full screen](main-output.html)

---

## Secondary output

<iframe
    src="secondary-output.html"
    title="Secondary research output"
    style="width: 100%; aspect-ratio: 4 / 3; border: none;">
</iframe>

+ *Construction:* Explain how this output is produced.
+ *Interpretation:* Explain how readers should understand the output.
+ *Source:* Describe the data, assumptions, or model inputs.
+ [Download data](secondary-output.csv)
+ [View in full screen](secondary-output.html)

---

## Methods

Summarize the method, model, measurement strategy, or workflow. Keep this section readable for non-specialists, and link to technical documentation where needed.

---

## Data and code

+ [Project repository](https://github.com/andrewczeidinski)
+ [Dataset](dataset.csv)
+ [Technical notes](notes.pdf)

---

## Frequently asked questions

### When are the results updated?

Explain the update schedule, release lag, or conditions under which the page changes.

### What are the main limitations?

Describe the most important caveats, assumptions, missing data, or uncertainty.

### How should these results be cited?

Use the citation below or adapt it for the final publication.

---

## Citation

Andrew Czeidinski. {{ dateFormat "2006" .Date }}. "{{ replace .Name "-" " " | title }}." https://andrewczeidinski.github.io/research/{{ .Name }}/.

```BibTeX
@misc{czeidinski{{ dateFormat "2006" .Date }}{{ replace .Name "-" "" }},
author = {Czeidinski, Andrew},
year = {{ dateFormat "2006" .Date }},
title = { {{ replace .Name "-" " " | title }} },
url = {https://andrewczeidinski.github.io/research/{{ .Name }}/}}
```

---

## References

+ Author Name. Year. "Reference Title." *Journal or Publisher*. https://doi.org/example
