# 2026-01-01 TIL: Quarto & Typst for High-Quality PDF Reports

## Category: Documentation / Publishing

### Video Reference

[![YouTube](https://img.shields.io/badge/YouTube-Video-red?style=flat-square&logo=youtube)](https://www.youtube.com/watch?v=idgZjnDIS1s)

### Key Takeaways

**Quarto + Typst** is a powerful combination for creating beautiful, data-driven PDF reports with modern tooling.

#### 🔧 What is Quarto?

Quarto is an open-source scientific and technical publishing system that:

- Supports **Python, R, Julia, and Observable JS**
- Renders to multiple formats: PDF, HTML, Word, slides
- Uses Markdown with embedded code chunks
- Replaces/extends R Markdown for cross-language support

#### 📄 What is Typst?

Typst is a modern alternative to LaTeX:

- **Much faster** compilation than LaTeX
- **Simpler syntax** — easier to learn and write
- **Powerful styling** with functions and scripting
- **Native PDF output** with high-quality typography

#### 🤝 Why Combine Them?

| Feature        | Quarto Alone     | Quarto + Typst   |
| -------------- | ---------------- | ---------------- |
| Code execution | ✅               | ✅               |
| PDF rendering  | Via LaTeX (slow) | Via Typst (fast) |
| Styling        | Limited          | Full control     |
| Typography     | Good             | Excellent        |
| Learning curve | Low              | Medium           |

#### 🚀 Basic Workflow

```yaml
# In your .qmd file header
---
title: "My Report"
format:
  typst:
    toc: true
    columns: 1
---
```

````markdown
## Data Analysis

Here's some Python code that generates a plot:

```{python}
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 10, 100)
plt.plot(x, np.sin(x))
plt.title("Sine Wave")
plt.savefig("plot.png")
```
````

The plot shows a beautiful sine wave.

````

### Code / Implementation

Setting up a Quarto + Typst project:

```bash
# Install Quarto (if not already installed)
# Download from https://quarto.org/docs/get-started/

# Create a new Quarto project
quarto create project myreport

# Create a .qmd file with Typst output
cat > report.qmd << 'EOF'
---
title: "Sales Report Q4 2025"
author: "Data Team"
date: today
format:
  typst:
    toc: true
    number-sections: true
    papersize: a4
---

# Executive Summary

This report analyzes Q4 2025 sales performance.

```{python}
#| echo: false
import pandas as pd

data = {
    'Month': ['October', 'November', 'December'],
    'Revenue': [125000, 148000, 189000],
    'Growth': ['12%', '18%', '28%']
}
df = pd.DataFrame(data)
print(df.to_markdown(index=False))
````

# Conclusion

Q4 showed strong growth with December peak.
EOF

# Render to PDF

quarto render report.qmd

````

#### Custom Typst Styling

```typst
// _extensions/custom/typst-template.typ
#let report(title: "", author: "", body) = {
  set page(
    paper: "a4",
    margin: (x: 2.5cm, y: 3cm),
    header: align(right)[#title],
    footer: align(center)[#counter(page).display()]
  )

  set text(font: "Inter", size: 11pt)
  set heading(numbering: "1.1")

  // Title block
  align(center)[
    #text(size: 24pt, weight: "bold")[#title]
    #v(1em)
    #text(size: 14pt)[#author]
  ]

  body
}
````

### Additional Resources

- [Quarto Official Website](https://quarto.org/)
- [Typst Official Website](https://typst.app/)
- [Quarto + Typst Documentation](https://quarto.org/docs/output-formats/typst.html)
- [Original Video](https://www.youtube.com/watch?v=idgZjnDIS1s)
