---
title: "LOUD: Synthesizing Strongest and Weakest Specifications"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- Kanghee Park
- admin
- Loris D'Antoni

# Author notes (optional)
author_notes:
- "Equal contribution"
- "Equal contribution"

date: "2024-07-11T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
# publishDate: "2023-10-22T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In *Object-oriented Programming, Systems, Languages, and Applications* 2025
publication_short: In *OOPSLA25*

abstract: |
    Specifications allow us to formally state and understand what programs are intended to do. To help one extract useful properties from code, Park et al. recently proposed a framework that given (i) a *quantifier-free* query $\Psi$ posed about a set of function definitions, and (ii) a domain-specific language $\mathcal{L}$ in which each extracted property is to be expressed (we call properties in the language $\mathcal{L}$-properties), synthesizes a set $\{\varphi_1, \ldots , \varphi_n\}$ of $\mathcal{L}$-properties such that each of the $\varphi_i$ is a **strongest $\mathcal{L}$-consequence** for $\Psi$, i.e., $\varphi_i$ is an over-approximation of $\Psi$ and there is no other $\mathcal{L}$-property that over-approximates $\Psi$ and is strictly more precise than $\varphi_i$.

    The framework by Park et al. has two key limitations. First, it only supports quantifier-free query formulas and thus cannot synthesize specifications for queries involving nondeterminism, concurrency, etc. Second, it can only compute $\mathcal{L}$-consequences, i.e., **over-approximations** of the program behavior.

    This paper addresses these two limitations and presents a framework, Loud, for synthesizing strongest $\mathcal{L}$-consequences and **weakest $\mathcal{L}$-implicants** (i.e., under-approximations of the query $\Psi$) for function definitions that can involve *existential quantifiers*.

    We implemented a solver, Aspire, for problems expressed in Loud which can be used to describe and identify sources of bugs in both deterministic and nondeterministic programs,
    extract properties from concurrent programs, and synthesize winning strategies in two-player games.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags: []

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: ''
url_code: 'https://github.com/ebmoon/spyro-sketch/tree/underapprox'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# image:
#   caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
#   focal_point: ""
#   preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
# projects:
# - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---

{{% callout note %}}
Click the *Cite* button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /callout %}}

{{% callout note %}}
Create your slides in Markdown - click the *Slides* button to check out the example.
{{% /callout %}}

Supplementary notes can be added here, including [code, math, and images](https://wowchemy.com/docs/writing-markdown-latex/).
