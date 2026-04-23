---
title: "{{ replace .File.ContentBaseName "-" " " | title }}"
date: {{ .Date }}
tags: ["keyword 1", "keyword 2", "keyword 3"]
author: ["Author Name"]
description: "Book description for search engines (less than 155 characters)"
summary: "Book summary for list page (less than 265 characters)"
cover:
    image: "{{ .File.ContentBaseName }}.png"
    alt: "{{ replace .File.ContentBaseName "-" " " | title }}"
    relative: true
editPost:
    URL: "https://publisher-or-book-page.example.com"
    Text: "Publisher"
showToc: false
disableAnchoredHeadings: false

---

---

#### Description

Add a concise description of the book here.

---

#### Praise

> Add an endorsement or review blurb here.

---

#### View

+ [Chapter 1](chapter1.pdf)
+ [Chapter 2](chapter2.pdf)
+ [Chapter 3](chapter3.pdf)

---

#### Excerpt

Add a short excerpt, summary passage, or introductory text here.

---

#### Citation

Author Name. {{ dateFormat "2006" .Date }}. *{{ replace .File.ContentBaseName "-" " " | title }}*. City, Country: Publisher. https://example.com/book.

```latex
@book{key,
author = {Author Name},
year = {{ dateFormat "2006" .Date }},
title = { {{ replace .File.ContentBaseName "-" " " | title }} },
publisher = {Publisher},
address = {City, Country},
url = {https://example.com/book}}
```
