# 21Oct-datenstruktur: Important Points

## Goals of this Lesson

After this lesson, you can:

1. distinguish arrays, `Map`/objects, `Set`, stacks, queues, and linked lists by their basic ideas and typical uses.
2. explain the LIFO principle of a stack and describe why a stack can be implemented with an array.
3. implement and use a simple JavaScript stack with `push()`, `pop()`, `peek()`, `isEmpty()`, and `size()`.
4. explain the steps of a linear search and find a value or record in an array.
5. describe how Bubble Sort compares and swaps neighboring values, and implement the algorithm in JavaScript.
6. classify the approximate runtime and memory usage of simple operations using `O(1)`, `O(n)`, and `O(n²)`.

## Understanding Questions

1. How do arrays, `Map`/objects, and `Set` differ in the way they organize or look up data?
2. What does LIFO mean, and which values does a stack return after `push("A")`, `push("B")`, `push("C")`, followed by two calls to `pop()`?
3. Why does `peek()` access `this.items[this.items.length - 1]`, and how does the example class handle an empty stack?
4. How does the return value of `linearSearch()` differ from that of `findUserById()` when no match is found?
5. Why is Bubble Sort inefficient for large lists, and how does `[...array]` affect additional memory usage and the original array?
