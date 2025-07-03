# 401-Read_05

## 📘 What is a Linked List?
A **Linked List** is a sequence of nodes where each node links to the next.  
Types:
- **Singly** Linked List – each node points to the **next** node.
- **Doubly** Linked List – each node points to **both next and previous** nodes.

### 🔑 Terminology
- **Linked List**: Structure made of connected nodes.
- **Singly**: One reference per node (points to the next).
- **Doubly**: Two references per node (next and previous).
- **Node**: An item in the list containing data and a reference.
- **Next**: Pointer to the next node.
- **Head**: The first node in the list.
- **Current**: Pointer used during traversal (starts at Head).

---

## 🔄 Traversal
Traversal = Moving through a list from node to node.

### ✅ Key Concepts:
- Can't use `for` or `foreach`.
- Use a `while` loop to follow `.next` pointers.
- Start at the **head**.
- Track position using **Current**.
- Stop when `.next` is `null`.

### 💡 Example: Includes(value)
```js
WHILE Current is not NULL
  IF Current.Value == searchValue
    RETURN true
  Current = Current.Next

RETURN false
```

### 🔍 Why It Matters
- Avoids NullReferenceException.
- Lets us safely search through the list.

### 🔢 Big O
- **Time**: O(n) – check each node.
- **Space**: O(1) – no extra memory used.

---

## ➕ Adding a Node

### ✅ Add at the Beginning (O(1))
Steps:
1. Create a new node.
2. Set its `.next` to current `head`.
3. Update `head` to point to the new node.

```js
newNode = new Node
newNode.Value = value
newNode.Next = Head
Head = newNode
```

### ➕ Add Before a Node (O(n))
Steps:
1. Traverse using `Current`.
2. If `Current.Next.Value == targetValue`:
   - `newNode.Next = Current.Next`
   - `Current.Next = newNode`

```js
newNode = new Node
newNode.Value = newValue
newNode.Next = Current.Next
Current.Next = newNode
```

### ⚠️ Be Careful!
- Don’t lose the rest of the list during insert!

### 🔢 Big O
- **Time**: O(n) – you might go through all nodes.
- **Space**: O(1) – no extra space used.

---

## 🖨️ Printing the Linked List

```js
WHILE Current is not NULL
  PRINT Current.Value + " --> "
  Current = Current.Next

PRINT "NULL"
```

- Ends with `"NULL"` to show the list is done.

---

## 🧱 Building the Node Class
- Require a value when creating a new node.

Example: You can't create a node with no value.

---

## 🧠 Summary Table

| Operation           | Loop Used | Starts At | Ends When         | Time Big O | Space Big O |
|---------------------|-----------|-----------|-------------------|------------|-------------|
| Traversal (Includes)| while     | Head      | .Next == null     | O(n)       | O(1)        |
| Add to Beginning    | N/A       | N/A       | N/A               | O(1)       | O(1)        |
| Add Before Node     | while     | Head      | .Next == value    | O(n)       | O(1)        |
| Print Nodes         | while     | Head      | .Next == null     | O(n)       | O(1)        |

---

## 💡 Organizing Data in Code
- Data is everywhere!
- We need ways to **organize** and **use** it well.
- That’s why **data structures** exist.

### 🧰 Common Beginner Data Structures:
- **Variables**: Store one item.
- **Arrays**: Store items in order.
- **Objects/Hashes**: Key-value pairs.

These are just the beginning!

---

## 😵 Why Linked Lists Feel Tricky
- They **look simple**, but are easy to forget.
- Popular in **coding interviews**.
- Knowing when to use them is key.

---

## 📏 What Kind of Structure is a Linked List?

### Linear Data Structures
- Items in a set order (like hopscotch).
- You move one step at a time.
- Examples: Arrays, Linked Lists

### Non-Linear Data Structures
- No fixed order.
- Examples: Trees, Graphs

---

## 🔗 What is a Linked List?
- A **series of nodes**.
- Each node has:
  - A **value**
  - A pointer to the **next node**
- First node = **Head**
- Last node = points to **null**
- You **can’t jump** to the middle — must start at the head.

### 🧠 Metaphors
| Concept          | Metaphor                        |
|------------------|----------------------------------|
| Linear Structure | Row of stepping stones           |
| Linked List      | Treasure hunt with clues         |
| Head             | Starting point                   |
| Null             | End of the list                  |

---

## ✅ Key Takeaways
- Linked Lists store data in steps.
- You move node to node, not by index.
- They get easier with **understanding**, not just memorization.

---

## 😬 Why Linked Lists Feel Confusing (But Aren’t)
- They’re simple — the **when to use them** is the tricky part.
- Common in interviews, but easy to forget if not used regularly.

---

## ⚖️ Intro to Big O

### What is Big O?
A way to measure **how slow or fast** something runs as input grows.

### Think of it like:
> "What happens if I give this function 10... or 10,000 items?"

---

## ⏱️ Common Big O Examples

| Big O  | Meaning                       | Example                       |
|--------|-------------------------------|-------------------------------|
| O(1)   | Constant – always fast        | Add to start of list          |
| O(n)   | Linear – grows evenly         | Traverse entire list          |
| O(n²)  | Exponential – grows fast ⚠️  | Nested loops                  |

**Key**: O(1) = ideal, O(n²) = avoid when possible

---

## 🔗 Linked List vs Array

| Feature                | Linked List         | Array                      |
|------------------------|---------------------|----------------------------|
| Memory layout          | Scattered           | Together in memory         |
| Add at beginning       | Fast (O(1)) ✅       | Slow (O(n)) ❌             |
| Add at end             | Slow (O(n)) ❌       | Fast (if pre-allocated) ✅ |
| Random access          | Slow ❌             | Fast (use index) ✅        |
| Good for...            | Frequent changes     | Fast lookups               |

---

## 🧱 How to Add to a Linked List

### ✅ Insert at Start (O(1))
1. Create new node.
2. Point to current head.
3. Make head point to new node.

### ❗ Insert at End (O(n))
1. Find last node (traverse).
2. Create new node (next = null).
3. Update last node’s next pointer.

---

## 🤔 When to Use Linked Lists
- ✅ You add/remove at the start often.
- ❌ You need fast lookups or indexing.

---

## 🧠 Rule of Thumb
- **Linked List** = great for changing data.
- **Array** = great for finding data.

---

## 🚩 Linked List Tradeoffs

| 👍 Pros                 | 👎 Cons                     |
|-------------------------|-----------------------------|
| Easy to grow/shrink     | Slow search/find            |
| No pre-set memory needed| Can’t jump to middle        |
| Great for insert/remove | Requires full traversal     |

---

## 🔚 Final Thoughts
- Linked Lists are just one tool.
- You don’t have to memorize — just **understand**.
- Knowing when to use them gives you a real advantage!
