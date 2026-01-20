# Time and Space Complexity Analysis

Complexity analysis is the primary way to measure the efficiency of an algorithm. We don't measure time in "seconds" (because that depends on hardware); instead, we measure how the **number of operations** grows as the **input size ($N$)** grows.

---

## 1. Time Complexity

**Time Complexity** quantifies the amount of time taken by an algorithm to run as a function of the length of the input.

### Why not measure in seconds?
*   Different computers have different speeds.
*   The same computer takes different times based on background processes.
*   We need a hardware-independent metric.

### How to Calculate?
We count the **elementary operations** (additions, comparisons, assignments, etc.).

**Example 1: Linear Loop ($O(N)$)**
```cpp
// Runs N times
for(int i = 0; i < N; i++) {
    print(i); // O(1) operation
}
```
Total operations $\approx c \cdot N$. Complexity: **Linear**.

**Example 2: Nested Loops ($O(N^2)$)**
```cpp
// Outer runs N times
for(int i = 0; i < N; i++) {
    // Inner runs N times
    for(int j = 0; j < N; j++) {
        print(i, j);
    }
}
```
Total operations $\approx N \times N$. Complexity: **Quadratic**.

---

## 2. Space Complexity

**Space Complexity** quantifies the amount of memory (RAM) used by an algorithm to execute and produce the result.

**Space Complexity = Auxiliary Space + Input Space**

*   **Input Space:** Space to store the input data (e.g., array of size $N$).
*   **Auxiliary Space:** Extra space or temporary space used by the algorithm.

Usually, when we talk about space complexity in interviews, we refer to **Auxiliary Space**.

**Example 1: Using Variables ($O(1)$)**
```cpp
int sum(vector<int> arr) {
    int total = 0; // O(1) space
    for(int x : arr) total += x;
    return total;
}
```
We only used `total` and loop variable `x`. The space doesn't grow with $N$.

**Example 2: Using an Array ($O(N)$)**
```cpp
vector<int> copyArray(vector<int> arr) {
    vector<int> newArr(arr.size()); // O(N) space
    // ... copy ...
    return newArr;
}
```
We created a new container proportional to the input size.
