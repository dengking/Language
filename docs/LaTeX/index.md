# LaTeX

## Keep left justifying 

Sure! If you want to left-justify three formulas in LaTeX, you can use several methods. Here are three common approaches:

### Method 1: Using the `fleqn` Option

You can set the `fleqn` option in the document class to make all equations left-aligned by default.

```latex
\documentclass[fleqn]{article}
\usepackage{amsmath}

\begin{document}

\begin{equation}
C_n = \frac{1}{n+1} \binom{2n}{n}
\end{equation}

\begin{equation}
C_{n+1} = \sum_{i=0}^{n} C_i C_{n-i}
\end{equation}

\begin{equation}
C_n = \frac{(2n)!}{(n+1)!n!}
\end{equation}

\end{document}
```

### Method 2: Using the `align` Environment

You can use the `align` environment from the `amsmath` package and place an alignment marker `&` before each equation to left-align them.

```latex
\documentclass{article}
\usepackage{amsmath}

\begin{document}

\begin{align}
& C_n = \frac{1}{n+1} \binom{2n}{n} \\
& C_{n+1} = \sum_{i=0}^{n} C_i C_{n-i} \\
& C_n = \frac{(2n)!}{(n+1)!n!}
\end{align}

\end{document}
```

### Method 3: Using the `flalign` Environment

The `flalign` environment also allows for left-aligned equations and provides more flexibility with spacing.

```latex
\documentclass{article}
\usepackage{amsmath}

\begin{document}

\begin{flalign}
& C_n = \frac{1}{n+1} \binom{2n}{n} & \\
& C_{n+1} = \sum_{i=0}^{n} C_i C_{n-i} & \\
& C_n = \frac{(2n)!}{(n+1)!n!} &
\end{flalign}

\end{document}
```

### Method 4: Using the `multline` Environment

The `multline` environment is another option for left-aligning multiple lines of equations.

```latex
\documentclass{article}
\usepackage{amsmath}

\begin{document}

\begin{multline}
C_n = \frac{1}{n+1} \binom{2n}{n} \\
C_{n+1} = \sum_{i=0}^{n} C_i C_{n-i} \\
C_n = \frac{(2n)!}{(n+1)!n!}
\end{multline}

\end{document}
```

Each of these methods will left-align your equations. Choose the one that best fits your document's formatting needs.



If you want to left-justify and number multiple equations in LaTeX, you can use the `align` environment from the `amsmath` package. This environment allows you to align equations at specific points and automatically numbers each row.

Here is an example of how to left-justify and number three equations:

```latex
\documentclass{article}
\usepackage{amsmath}

\begin{document}

\begin{align}
C_n &= \frac{1}{n+1} \binom{2n}{n} \\
C_{n+1} &= \sum_{i=0}^{n} C_i C_{n-i} \\
C_n &= \frac{(2n)!}{(n+1)!n!}
\end{align}

\end{document}
```

### Explanation:

1. **Document Class and Package**:
   - `\documentclass{article}`: Specifies the document class.
   - `\usepackage{amsmath}`: Imports the `amsmath` package, which provides the `align` environment.

2. **Align Environment**:
   - `\begin{align} ... \end{align}`: The `align` environment is used to align multiple equations.
   - `&`: The ampersand `&` is used to specify the alignment point. In this case, it aligns the equations at the equals sign `=`.
   - Each equation is written on a new line, and LaTeX automatically numbers each line.

### Output:

The output will be three left-justified equations, each with its own number:

1. \( C_n = \frac{1}{n+1} \binom{2n}{n} \)
2. \( C_{n+1} = \sum_{i=0}^{n} C_i C_{n-i} \)
3. \( C_n = \frac{(2n)!}{(n+1)!n!} \)

This method ensures that your equations are neatly aligned and numbered, making them easy to read and reference.



## Represent Z

In LaTeX, you can represent the set of integers, commonly denoted by \( \mathbb{Z} \), using the `amsmath` package. The `amsmath` package provides a convenient way to use blackboard bold characters, which are often used to denote sets like the integers, real numbers, and complex numbers.

Here is how you can represent \( \mathbb{Z} \) in LaTeX:

### Using `amsmath` and `amssymb` Packages

1. **Document Class and Packages**:
   - `\documentclass{article}`: Specifies the document class.
   - `\usepackage{amsmath}`: Imports the `amsmath` package.
   - `\usepackage{amssymb}`: Imports the `amssymb` package, which provides the `\mathbb` command.

2. **Using `\mathbb{Z}`**:
   - `\mathbb{Z}`: Represents the set of integers.

Here is a complete example:

```latex
\documentclass{article}
\usepackage{amsmath}
\usepackage{amssymb}

\begin{document}

The set of integers is denoted by \( \mathbb{Z} \).

\end{document}
```

### Explanation:

- `\usepackage{amsmath}`: Loads the `amsmath` package, which is essential for many mathematical typesetting features.
- `\usepackage{amssymb}`: Loads the `amssymb` package, which provides the `\mathbb` command.
- `\mathbb{Z}`: The command to produce the blackboard bold letter \( \mathbb{Z} \), representing the set of integers.

### Output:

The output will be:

```
The set of integers is denoted by ℤ.
```

This method ensures that you can correctly and consistently represent the set of integers in your LaTeX documents.

## Infer(推导出)

In LaTeX, you can represent the logical inference symbol (often denoted as \( \Rightarrow \) or \( \vdash \)) using various commands provided by the `amsmath` package. Here are a few ways to represent logical inference:

### Using `\Rightarrow`

The `\Rightarrow` command produces a double-lined right arrow, which is commonly used to denote logical implication or inference.

```latex
\documentclass{article}
\usepackage{amsmath}

\begin{document}

If \( A \) then \( B \): \( A \Rightarrow B \).

\end{document}
```

### Using `\vdash`

The `\vdash` command produces a turnstile symbol, which is often used in formal logic to denote syntactic entailment.

```latex
\documentclass{article}
\usepackage{amsmath}

\begin{document}

From \( A \), infer \( B \): \( A \vdash B \).

\end{document}
```

### Using `\implies`

The `\implies` command is another way to denote logical implication, provided by the `amsmath` package.

```latex
\documentclass{article}
\usepackage{amsmath}

\begin{document}

If \( A \) then \( B \): \( A \implies B \).

\end{document}
```

### Using `\Longrightarrow`

The `\Longrightarrow` command produces a longer double-lined right arrow, which can be used for emphasis or in contexts where a longer arrow is visually preferable.

```latex
\documentclass{article}
\usepackage{amsmath}

\begin{document}

If \( A \) then \( B \): \( A \Longrightarrow B \).

\end{document}
```

### Example with Multiple Inference Symbols

Here is a complete example that demonstrates the use of different inference symbols:

```latex
\documentclass{article}
\usepackage{amsmath}

\begin{document}

Logical implication using different symbols:

\begin{itemize}
    \item If \( A \) then \( B \): \( A \Rightarrow B \).
    \item From \( A \), infer \( B \): \( A \vdash B \).
    \item If \( A \) then \( B \): \( A \implies B \).
    \item If \( A \) then \( B \): \( A \Longrightarrow B \).
\end{itemize}

\end{document}
```

### Explanation:

- `\Rightarrow`: Produces \( \Rightarrow \), a double-lined right arrow.
- `\vdash`: Produces \( \vdash \), a turnstile symbol.
- `\implies`: Produces \( \implies \), another form of logical implication.
- `\Longrightarrow`: Produces \( \Longrightarrow \), a longer double-lined right arrow.

Each of these commands can be used depending on the specific context and notation preferences in your document.