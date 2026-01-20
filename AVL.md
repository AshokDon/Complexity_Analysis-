# AVL Tree

**AVL Tree** (Adelson-Velsky and Landis) is a self-balancing Binary Search Tree (BST) where the difference between heights of left and right subtrees cannot be more than 1 for all nodes.

**Balance Factor** ($BF$) = Height(LeftSubtree) - Height(RightSubtree)
$BF \in \{-1, 0, 1\}$.

---

## 1. Rotations

To restore balance, we use rotations:

1.  **Left Rotation (LL Case):**
    *   Right child moves up, Node moves down-left.
2.  **Right Rotation (RR Case):**
    *   Left child moves up, Node moves down-right.
3.  **Left-Right Rotation (LR Case):**
    *   Left child does left rotation, then Node does right rotation.
4.  **Right-Left Rotation (RL Case):**
    *   Right child does right rotation, then Node does left rotation.

**Time Complexity:**
*   Search: $O(\log N)$
*   Insert: $O(\log N)$
*   Delete: $O(\log N)$

---

## Implementation (Rotation Logic)

<details>
<summary><b>C++ Snippet</b></summary>

```cpp
struct Node {
    int key, height;
    Node *left, *right;
};

int height(Node *N) {
    if (N == NULL) return 0;
    return N->height;
}

Node* rightRotate(Node *y) {
    Node *x = y->left;
    Node *T2 = x->right;
    
    // Rotation
    x->right = y;
    y->left = T2;
    
    // Update heights
    y->height = max(height(y->left), height(y->right)) + 1;
    x->height = max(height(x->left), height(x->right)) + 1;
    
    return x;
}

Node* leftRotate(Node *x) {
    Node *y = x->right;
    Node *T2 = y->left;
    
    // Rotation
    y->left = x;
    x->right = T2;
    
    // Update heights
    x->height = max(height(x->left), height(x->right)) + 1;
    y->height = max(height(y->left), height(y->right)) + 1;
    
    return y;
}
```
</details>
