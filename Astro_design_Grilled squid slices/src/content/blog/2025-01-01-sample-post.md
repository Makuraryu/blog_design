---
title: Sample Post — Markdown & KaTeX Showcase
description: Demonstrates headings, lists, code, tables, images, and math.
pubDate: 2025-01-01
tags: [demo, markdown, math]
heroImage: /images/sample-hero.png
---

# 标题一 / Heading 1

多语言段落，含行内数学 $a^2+b^2=c^2$ 与展示公式：

$$
\sum_{k=1}^n k = \frac{n(n+1)}{2}
$$

## 列表与引用

- 项目 A
- 项目 B
  - 子项

> 引用与 [Astro 文档](https://astro.build/)。

```js
// JavaScript 示例
export const fib = n => n < 2 ? n : fib(n-1) + fib(n-2)
```

| 键 | 值 |
|---:|:---|
| A  | 1  |
| B  | 2  |

![示例图片](/images/sample-hero.png)

对齐环境：

$$
\begin{aligned}
E &= mc^2 \\
F &= ma
\end{aligned}
$$

- [x] 预览样式
- [ ] 发布
