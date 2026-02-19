🧮 Matrix Chain Multiplication – Web Implementation

A simple and interactive web-based implementation of the Matrix Chain Multiplication (MCM) problem using Dynamic Programming.

This project calculates the minimum number of scalar multiplications required to multiply a chain of matrices.

📌 Problem Statement

Given a sequence of matrices, determine the most efficient way to multiply them together.

Matrix multiplication is associative, meaning:

(A × B) × C ≠ A × (B × C)  (in terms of cost)


Different parenthesizations can lead to different computation costs.
The goal is to minimize the total number of scalar multiplications.

🚀 Features

Modern Glassmorphism UI

Input validation

Error handling

Dynamic Programming implementation

Instant calculation

Step-based mathematical explanation (added)

🛠️ Technologies Used

HTML5

CSS3

JavaScript (ES6)

Dynamic Programming

🧠 Algorithm Explanation

The algorithm uses a DP table to store minimum multiplication costs.

Recurrence Relation:
𝑚
[
𝑖
]
[
𝑗
]
=
min
⁡
(
𝑚
[
𝑖
]
[
𝑘
]
+
𝑚
[
𝑘
+
1
]
[
𝑗
]
+
𝑝
[
𝑖
]
×
𝑝
[
𝑘
+
1
]
×
𝑝
[
𝑗
+
1
]
)
m[i][j]=min(m[i][k]+m[k+1][j]+p[i]×p[k+1]×p[j+1])

Where:

p[] → array of matrix dimensions

m[i][j] → minimum cost from matrix i to j

k → partition index

📊 Example Calculation
🔢 Input:
10,20,30,40

🧩 Matrices Formed:

A1 = 10 × 20

A2 = 20 × 30

A3 = 30 × 40

🔍 Possible Parenthesizations

Since there are 3 matrices, only 2 ways exist:

🟢 Case 1: (A1 × A2) × A3
Step 1: Multiply A1 × A2

Cost:

10 × 20 × 30 = 6000


Resulting matrix = 10 × 30

Step 2: Multiply Result × A3

Cost:

10 × 30 × 40 = 12000

✅ Total Cost:
6000 + 12000 = 18000

🔴 Case 2: A1 × (A2 × A3)
Step 1: Multiply A2 × A3

Cost:

20 × 30 × 40 = 24000


Resulting matrix = 20 × 40

Step 2: Multiply A1 × Result

Cost:

10 × 20 × 40 = 8000

❌ Total Cost:
24000 + 8000 = 32000

🏆 Final Comparison
Parenthesization	Cost
(A1A2)A3	18000 ✅
A1(A2A3)	32000
🎯 Final Output
Minimum Multiplications: 18000


Because 18000 < 32000, the optimal multiplication order is:

(A1 × A2) × A3

⏱️ Complexity Analysis

Time Complexity: O(n³)

Space Complexity: O(n²)

▶️ How to Run

Clone or download the repository.

Open the HTML file in any browser.

Enter matrix dimensions (comma separated).

Click Compute.

View the minimum multiplication cost instantly.

🎓 Learning Outcomes

Understanding Dynamic Programming

Optimization problems

Algorithm implementation in JavaScript

Time & Space complexity analysis

Mathematical reasoning in DAA

👨‍💻 Author

Abhishek Akhand
B.Tech – AI & Data Science (2nd Year)
