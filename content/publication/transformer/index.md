---
title: "LOUD: Synthesizing Strongest and Weakest Specifications"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- admin
- Dominic Kennedy
- Yuyou Fan
- Ben Greenman
- John Regehr
- Loris D'Antoni


# Author notes (optional)
author_notes:
- "Equal contribution"
- "Equal contribution"

date: "2026-04-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2026-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In *Symposium on Principles of Programming Languages* 2026
publication_short: In *POPL26*

abstract: |
    Static analyses play a fundamental role during compilation: they discover facts that are true in all executions of the code being compiled, and then these facts are used to justify optimizations and diagnostics.
    
    Each static analysis is based on a collection of **abstract transformers** that provide abstract semantics for the concrete instructions that make up a program.

    It can be challenging to implement abstract transformers that are sound, precise, and efficient---and in fact both LLVM and GCC have suffered from miscompilations caused by unsound abstract transformers.
    
    Moreover, even after more than 20 years of development, LLVM lacks abstract transformers for some instructions in its intermediate representation (IR).

    We developed NiceToMeetYou: a program synthesis framework for abstract transformers that are aimed at the kind of non-relational integer abstract domains that are heavily used by today's production compilers.
    
    It exploits a simple but novel technique for breaking the synthesis problem into parts: each of our transformers is the meet of a collection of simpler, sound transformers that are synthesized such that each new piece fills a gap in the precision of the final transformer. 
    
    Our design point is bulk automation: no sketches are required, and formal semantics for IR instructions were previously created using an SMT dialect of MLIR. Each of our synthesized transformers is provably sound, and some of them are more precise than those provided by LLVM

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
url_code: 'https://github.com/Hatsunespica/xdsl-smt/tree/synth_transfer/xdsl_smt'
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
