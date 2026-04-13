# Custom Data Structures in Java

This project provides custom implementations of fundamental data structures without using `java.util` collections (except `Iterator`). It includes:

- **MyArrayList** – a dynamic array implementation of the `MyList` interface.
- **MyLinkedList** – a doubly‑linked list implementation of the `MyList` interface.
- **MyStack** – LIFO stack built on `MyArrayList`.
- **MyQueue** – FIFO queue built on `MyLinkedList`.
- **MyMinHeap** – min‑heap (priority queue) built on `MyArrayList`.
- **Console Menu** – interactive CLI for testing all structures.

All classes are generic and operate on objects that implement `Comparable` when ordering is required.

---

## Project Structure

| File | Description |
|------|-------------|
| `MyList.java` | Core interface defining common list operations. |
| `MyArrayList.java` | Array‑based list with dynamic resizing. |
| `MyLinkedList.java` | Doubly‑linked list with efficient head/tail operations. |
| `MyStack.java` | Stack implementation using `MyArrayList`. |
| `MyQueue.java` | Queue implementation using `MyLinkedList`. |
| `MyMinHeap.java` | Min‑heap (binary heap) using `MyArrayList`. |
| `Main.java` | Interactive console menu for testing. |

---

## Design Choices

### Why `MyArrayList` for `MyStack`?
- Push and pop operations at the end of an array list are **amortized O(1)**.
- No overhead of node objects → memory efficient.

### Why `MyLinkedList` for `MyQueue`?
- Enqueue at the tail and dequeue from the head are **O(1)** operations.
- `MyArrayList` would require shifting elements on dequeue (O(n)).

### Why `MyArrayList` for `MyMinHeap`?
- A binary heap is naturally represented as an **array**.
- Parent/child index calculations are O(1).
- Dynamic resizing is handled automatically.

---

## How to Compile and Run

1. Place all `.java` files in the same directory.
2. Compile with:
   ```bash
   javac *.java
