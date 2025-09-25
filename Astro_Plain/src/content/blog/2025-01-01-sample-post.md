---
title: Sample Post — Markdown & KaTeX Showcase
description: A quick tour of headings, lists, code, tables, images, and math.
pubDate: 2025-01-01
tags: [demo, markdown, math]
heroImage: /images/sample-hero.png
---

# Heading 1

## Heading 2

### Heading 3

Paragraph with inline math: $e^{i\pi}+1=0$. Display math:

$$
\int_{-\infty}^{\infty} e^{-x^2} \, dx = \sqrt{\pi}
$$

- Unordered item A
- Unordered item B
  - Nested item

1. Ordered one
2. Ordered two

> Blockquote with emphasis and a link to [Astro](https://astro.build/).

```ts
// Code fence with TypeScript
interface Point { x: number; y: number }
const len = ({x, y}: Point) => Math.hypot(x, y)
```

| Column | Value |
|-------:|:------|
| A      | 1     |
| B      | 2     |

Image example (place asset under `public/images`):

![Sample Image](/images/sample-hero.png)

KaTeX aligned equations:

$$
\begin{aligned}
\nabla \cdot \vec{E} &= \frac{\rho}{\varepsilon_0} \\
\nabla \cdot \vec{B} &= 0
\end{aligned}
$$

Task list:
- [x] Build
- [ ] Preview
