# Asymptotic Notations: Big-O, $\Omega$, and $\Theta$

Asymptotic notations are mathematical tools to describe the running time of an algorithm in terms of the input size $N$ as $N \to \infty$.

---

## 1. Big-O Notation ($O$) - The Upper Bound

Describes the **Worst Case** scenario. It puts a limit on the growth from above.

*   **Definition:** $f(n) = O(g(n))$ if there exist constants $c$ and $n_0$ such that $f(n) \le c \cdot g(n)$ for all $n \ge n_0$.
*   **Meaning:** The algorithm will not grow faster than $g(n)$.
*   **Example:** If $f(n) = 3n + 5$, then $f(n) = O(n)$.

---

## 2. Omega Notation ($\Omega$) - The Lower Bound

Describes the **Best Case** scenario. It puts a limit on the growth from below.

*   **Definition:** $f(n) = \Omega(g(n))$ if there exist constants $c$ and $n_0$ such that $f(n) \ge c \cdot g(n)$ for all $n \ge n_0$.
*   **Meaning:** The algorithm will take *at least* this much time.
*   **Example:** If $f(n) = 3n + 5$, then $f(n) = \Omega(n)$ (It grows at least linearly).

---

## 3. Theta Notation ($\Theta$) - The Tight Bound

Describes the **Average/Exact Case**. It sandwiches the function between an upper and lower bound.

*   **Definition:** $f(n) = \Theta(g(n))$ if there exist constants $c_1, c_2$ and $n_0$ such that $c_1 \cdot g(n) \le f(n) \le c_2 \cdot g(n)$.
*   **Meaning:** The algorithm grows exactly at the rate of $g(n)$.
*   **Example:** If $f(n) = 3n + 5$, then $f(n) = \Theta(n)$.

---

## Common Complexity Classes (Ordered Better to Worse)

1.  **$O(1)$** - Constant Time (Access array index)
2.  **$O(\log N)$** - Logarithmic Time (Binary Search)
3.  **$O(N)$** - Linear Time (Simple Loop)
4.  **$O(N \log N)$** - Linearithmic Time (Merge Sort, Heap Sort)
5.  **$O(N^2)$** - Quadratic Time (Bubble Sort, Nested Loops)
6.  **$O(2^N)$** - Exponential Time (Recursive Fibonacci)
7.  **$O(N!)$** - Factorial Time (String Permutations)
