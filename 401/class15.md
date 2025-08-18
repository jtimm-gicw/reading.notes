# 401-Read_15

## Questions

Think of a tree in computer science like a real tree turned upside-down:
Root → The very top point (like the trunk base) where everything starts.

Branches → Connections (edges) leading to other points.

Nodes → The points themselves (could be the root, middle points, or ends).

Leaves → The very end points with nothing growing out of them.

It’s called a tree because:
*It starts from one root.*
It branches out into multiple paths.
Each branch can have more branches, but they never loop back into themselves.


In code terms:
**A tree is a way of storing data where each piece of data (a node) can link to child nodes below it.**


*This structure makes it easy to:*
Search for things
Organize information
Represent relationships (like a family tree, folder system, or game map)


*So in short:*
A tree is like a family chart for your data — starting from one “ancestor” and branching out to “descendants” in a clear, connected way.
🌳 Trees in Computer Science – Notes

1. Common Terminology
Node – A component that contains:
- A value (data)
- References (links) to other nodes

Root – The very first node in the tree (starting point)

K – The maximum number of children a node can have

Binary Tree → K = 2

Left / Right – In binary trees, the two possible children

Edge – Connection (link) between a parent and child node

Leaf – A node with no children

Height – Number of edges from the root to the furthest leaf


2. Traversals
*Why Traverse?*
Search for a node
Print contents
Process each node in a specific order




*Depth-First Traversal (DFS)*
Explore as far down a branch as possible before backtracking.
Commonly implemented with recursion (uses the call stack).


**Types:**
Pre-order → root → left → right
In-order → left → root → right
Post-order → left → right → root


**DFS Pseudocode:**
*Pre-order*
OUTPUT root.value
preOrder(root.left)
preOrder(root.right)

*In-order*
inOrder(root.left)
OUTPUT root.value
inOrder(root.right)

*Post-order*
postOrder(root.left)
postOrder(root.right)
OUTPUT root.value

*Output:*
Inorder Traversal: 10 20 30 100 150 200 300
Preorder Traversal: 100 20 10 30 200 150 300
Postorder Traversal: 10 30 20 150 300 200 100

*Breadth-First Traversal (BFS)*
Visits level-by-level, starting from the root.
Uses a queue instead of recursion.


**Pseudocode:**
enqueue(root)
while queue is not empty:
    node = dequeue()
    OUTPUT node.value
    enqueue(node.children)

Output example: A, B, C, D, E, F

3. Binary Trees vs. K-ary Trees
**Binary Tree**
Max 2 children per node (left & right)
No specific ordering by default


*Adding a node:*
Use BFS to find the first available child spot


*K-ary Tree*
Max K children per node


BFS traversal works similarly, but loop through all children instead of just left/right

4. Big O Complexity
*Binary Tree*
Insert/Search → O(n) (may need to visit every node)

Space (BFS insertion) → O(w) where w = tree’s max width

Perfect binary tree width: 2^(h-1)

Height h ≈ log(n)


**Binary Search Tree (BST)**
*Nodes ordered:*
Left subtree < root < right subtree

*Search/Insert:*
O(h) → height of tree


*Balanced tree:* O(log n)
Worst case (unbalanced): O(n)
Space (search) → O(1)



5. Searching a BST
Compare target with current node:


If smaller → go left


If larger → go right


*Repeat until:*

Match found
Or leaf reached with no match
Example search for 15:
Compare with 23 → go left
Compare with 8 → go right
Compare with 16 → go left
Found 15

6. Summary Table
Concept
Description
Data Structure Used
Node
Value + references
—
Root
First node
—
Edge
Parent → child link
—
Leaf
No children
—
DFS Traversal
Depth-first visiting order
Recursion (stack)
BFS Traversal
Level-order visiting order
Queue
Binary Tree
Max 2 children
Tree
K-ary Tree
Max K children
Tree
BST
Ordered binary tree
Tree


