# Efficiency Cases: Worst, Best, and Average

When analyzing algorithms, the performance often depends on the **nature** of the input, not just the size. We analyze three specific cases.

---

## 1. Worst Case Analysis (Big-O)

*   **Definition:** The maximum number of steps the algorithm takes for an input of size $N$.
*   **Significance:** It gives us an **upper bound guarantees** that the algorithm will never take longer than this. This is the most critical metric for software reliability.
*   **Example (Linear Search):**
    *   Searching for an element that is **not present** or is at the **very last position**.
    *   We must check all $N$ elements.
    *   Complexity: $O(N)$.

---

## 2. Best Case Analysis (Big-Omega $\Omega$)

*   **Definition:** The minimum number of steps the algorithm takes for an input of size $N$.
*   **Significance:** It shows the potential optimal performance, though often less useful for general guarantees.
*   **Example (Linear Search):**
    *   Searching for an element that is at the **first position**.
    *   We find it in 1 step.
    *   Complexity: $\Omega(1)$.

---

## 3. Average Case Analysis (Big-Theta $\Theta$)

*   **Definition:** The expected number of steps over all possible inputs of size $N$.
*   **Significance:** Useful when worst-case inputs are rare (e.g., Quicksort worst case is $O(N^2)$ but average is $O(N \log N)$).
*   **Example (Linear Search):**
    *   On average, the element might be in the middle.
    *   We check $N/2$ elements.
    *   Complexity: $\Theta(N)$ (Constants like $1/2$ are ignored).

---

## Visual Comparison

| Algorithm | Best Case | Average Case | Worst Case |
| :--- | :--- | :--- | :--- |
| **Linear Search** | $O(1)$ | $O(N)$ | $O(N)$ |
| **Insertion Sort** | $O(N)$ | $O(N^2)$ | $O(N^2)$ |
| **Quick Sort** | $O(N \log N)$ | $O(N \log N)$ | $O(N^2)$ |
