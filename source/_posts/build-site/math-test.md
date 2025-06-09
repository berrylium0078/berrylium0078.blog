---
title: Test Page for Math Fomulas
date: 2025-06-06 23:19:41
categories: "build site"
excerpt: "This blog uses MathJax v3.2 as math display engine. It supports macro definition, equation labeling, and the physics extension pack"
tags:
---

$\KaTeX\quad\LaTeX\quad\TeX$

$$
\begin{cases}
\frac{\partial\mathcal{D}}{\partial t} \quad & = \quad \nabla\times\mathcal{H},   & \quad \text{(Loi de Faraday)} \\[5pt]
\frac{\partial\mathcal{B}}{\partial t} \quad & = \quad -\nabla\times\mathcal{E},  & \quad \text{(Loi d'Ampere)}   \\[5pt]
\nabla\cdot\mathcal{B}                 \quad & = \quad 0,                         & \quad \text{(Loi de Gauss)}   \\[5pt]
\nabla\cdot\mathcal{D}                 \quad & = \quad 0.                         & \quad \text{(Loi de Colomb)}
\end{cases}
$$

### Line Breaks

They must appear inside certain environments.

$1\\2$
`$1\\2$`

$\displaylines{1\\2}$
`$\displaylines{1\\2}$`

$\begin{aligned} 1\\2 \end{aligned}$
`$\begin{aligned} 1\\2 \end{aligned}$`

### Defining Macros

{% note orange fa-warning %}
When the characters `{` and `#` appear together, all following content will be discarded due to a [Hexo bug](https://github.com/hexojs/hexo/issues/5301#issuecomment-1735550123)
{% endnote %}

$\newcommand{\water}{H_2O} \def\wate{H_2O}\def\liminfty#1{\lim_{ #1\to\infty}}$
$\water,\wate,\liminfty n$

```markdown
$\newcommand{\water}{H_2O} \def\wate{H_2O}\def\liminfty#1{\lim_{ #1\to\infty}}$
$\water,\wate,\liminfty n$
```

### Equation Labeling

$\begin{equation}1\end{equation}$
$\begin{equation}1\label{asd.sdsd}\end{equation}$
$$2\tag{b}\label{l2}$$
$\ref{asd.sdsd},\ref{l2}$

```md
$\begin{equation}1\end{equation}$
$\begin{equation}1\label{asd.sdsd}\end{equation}$
$$2\tag{b}\label{l2}$$
$\ref{asd.sdsd},\ref{l2}$
```

{% note yellow fa-lightbulb %}
You must define am equation label before referencing it.
{% endnote %}

{% note green fa-lightbulb %}
The hyper link for labeled equation is `{postURL}#mjx-eqn%3A{label}` --- where spaces are replaced with underscores --- according to the [MathJax3.2 Documentation](https://docs.mathjax.org/en/v3.2-latest/input/tex/extensions/tagformat.html)
{% endnote %}

### Enabling Extension Packs

_colorv2_:

$\color{red}{red\color{ #0000ff}{blue}}$

`$\color{red}{red\color{ #0000ff}{blue}}$`

_physics_:

$\eval{\sin x}_0^\pi$

`$\eval{\sin x}_0^\pi$`

_setoptions_:

$\setOptions[physics]{arrowdel=true} \grad \setOptions[physics]{arrowdel=false} \grad$

`$\setOptions[physics]{arrowdel=true} \grad \setOptions[physics]{arrowdel=false} \grad$`

Note: _require_ and _autoload_ will not work properly --- avoid using them.
