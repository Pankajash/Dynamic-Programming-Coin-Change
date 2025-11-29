# 🤖 Unique Paths DP Visualizer (Offline Version)

A simple and elegant web-based **Dynamic Programming visualizer** that demonstrates the **Unique Paths** problem — showing how a robot can move from the top-left corner to the bottom-right corner of an M × N grid, moving **only down or right**.

This version runs **completely offline**, requires **no API key**, and provides **local explanations** of the dynamic programming logic with **LaTeX math rendering**.

---

## 🚀 Features

- 🧩 **Dynamic Programming Grid Visualization** — See how each cell’s value is computed from its neighbors.
- 📊 **Instant Results** — Calculates total unique paths in real time.
- ✨ **Offline AI Explanation** — A built-in “Explain DP Concept” button provides an educational explanation without any API.
- 🧮 **MathJax Support** — Renders LaTeX equations beautifully.
- 🎨 **Responsive UI** — Built with Tailwind CSS for modern look and feel.

---

## 🧠 Problem Definition

A robot is located at the top-left corner of a grid and can only move **right** or **down**.  
The goal is to determine how many **unique paths** exist to reach the bottom-right corner.

### Dynamic Programming Formula

Base cases:

```math
dp[i][0] = 1, \quad dp[0][j] = 1
