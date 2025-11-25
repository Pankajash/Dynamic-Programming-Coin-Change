## 🚀 Unique Paths DP Visualizer

This project is an interactive web-based tool that visualizes and explains the **Unique Paths** problem using Dynamic Programming (DP). A robot starts at the top-left corner of an `M x N` grid and can only move either down or right at any point. The goal is to find the number of unique paths the robot can take to reach the bottom-right corner.

The tool provides:
* An input interface to define the grid dimensions (M rows, N columns).
* A calculated total number of unique paths.
* A step-by-step visualization of the DP table, showing the number of paths to reach each cell.
* An AI-generated explanation of the Dynamic Programming concept for this problem, including base cases and recurrence relation, powered by the Gemini API.

### 🤖 Problem Statement: Unique Paths

Imagine a robot on an `M x N` grid. The robot is initially located at the `(0, 0)` cell (top-left corner). It wants to reach the `(M-1, N-1)` cell (bottom-right corner). The robot can only move either **down** or **right** at any point in time. The task is to determine the total number of unique paths the robot can take to reach its destination.

### ✨ Dynamic Programming Approach

This problem exhibits optimal substructure and overlapping subproblems, making it a perfect candidate for Dynamic Programming.

1.  **Define the DP State:** Let `dp[i][j]` represent the number of unique paths to reach the cell at row `i` and column `j`.

2.  **Base Cases:**
    * For any cell in the first row `(0, j)`, there's only one way to reach it (by moving right `j` times). So, `dp[0][j] = 1`.
    * For any cell in the first column `(i, 0)`, there's only one way to reach it (by moving down `i` times). So, `dp[i][0] = 1`.
    * The starting cell `(0, 0)` has `1` path to itself.

3.  **Recurrence Relation:** For any other cell `(i, j)` where `i > 0` and `j > 0`, the robot can reach it either from the cell directly above `(i-1, j)` (by moving down) or from the cell directly to its left `(i, j-1)` (by moving right).
    Therefore, the total number of unique paths to reach `(i, j)` is the sum of the unique paths to these two cells:
    $$dp[i][j] = dp[i-1][j] + dp[i][j-1]$$

4.  **Final Result:** The answer is the value stored in the bottom-right cell of the DP table: `dp[M-1][N-1]`.

### 🚀 How to Use

1.  **Open the `index.html` file** in your web browser. (Assuming your code is saved as `index.html`)
2.  **Enter Grid Dimensions:** Use the "Rows (M)" and "Columns (N)" input fields to specify the size of your grid.
3.  **Calculate & Visualize:** Click the "Calculate Paths & Visualize" button.
    * The total number of unique paths will be displayed.
    * A grid visualization will appear, showing the `dpTable` where each cell `(i, j)` contains `dp[i][j]`. The start cell (0,0) and end cell (M-1, N-1) are highlighted.
4.  **Get AI Explanation:** Click the "✨ Explain DP Concept" button to receive a detailed, AI-generated explanation of the Dynamic Programming approach to this problem, including the base cases and recurrence relation.

### 🌐 Technology Stack

* **HTML:** Structure of the web page.
* **CSS (Tailwind CSS):** Modern, utility-first styling for a responsive and clean UI.
* **JavaScript:** Implements the Dynamic Programming algorithm, handles user input, updates the DOM for visualization, and interacts with the Gemini API for explanations.
* **Gemini API:** Provides intelligent, contextual explanations of the DP concept upon user request.
* **MathJax:** Renders LaTeX equations beautifully within the AI explanation output.

### ⚙️ Local Setup

1.  **Save the Code:** Save the provided HTML content as `index.html` (or any `.html` file).
2.  **Get a Gemini API Key:**
    * Visit [Google AI Studio](https://aistudio.google.com/).
    * Generate an API Key.
    * **Replace `const apiKey = "";`** in the JavaScript section of the `index.html` file with your actual API key: `const apiKey = "YOUR_GEMINI_API_KEY";`.
3.  **Open in Browser:** Simply open the `index.html` file with your web browser. No local server is required.

### 💡 Example

If you input `Rows = 3` and `Columns = 7`, the tool will calculate that there are `28` unique paths, and you will see the DP table filled accordingly.
`

### 🤝 Contribution

Feel free to fork this repository, suggest improvements, or fix bugs. This project is a great way to understand and visualize Dynamic Programming.
