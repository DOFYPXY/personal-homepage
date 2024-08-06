---
title: "Synthesizing Efficient Memoization Algorithms"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- Yican Sun
- admin
- Yingfei Xiong

# Author notes (optional)
# author_notes:
# - "Equal contribution"
# - "Equal contribution"

date: "2023-10-22T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2023-10-22T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In *Object-oriented Programming, Systems, Languages, and Applications*
publication_short: In *OOPSLA23*

abstract: In this paper, we propose an automated approach to finding correct and efficient memoization algorithms from a given declarative specification. This problem has two major challenges (i) a memoization algorithm is too large to be handled by conventional program synthesizers; (ii) we need to guarantee the efficiency of the memoization algorithm. To address this challenge, we structure the synthesis of memoization algorithms by introducing the local objective function and the memoization partition function and reduce the synthesis task to two smaller independent program synthesis tasks. Moreover, the number of distinct outputs of the function synthesized in the second synthesis task also decides the efficiency of the synthesized memoization algorithm, and we only need to minimize the number of different output values of the synthesized function. However, the generated synthesis task is still too complex for existing synthesizers. Thus, we propose a novel synthesis algorithm that combines the deductive and inductive methods to solve these tasks. To evaluate our algorithm, we collect 42 real-world benchmarks from Leetcode, the National Olympiad in Informatics in Provinces-Junior (a national-wide algorithmic programming contest in China), and previous approaches. Our approach successfully synhesizes 39/42 problems in a reasonable time, outperforming the baselines.

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
url_code: ''
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
