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

   **Answer:** Imagine organizing your toys. An **array** is a row of toys. Each place has a number, starting at **0**, so you can find a toy by its place. A **Map/object** is like boxes with labels: use a label, like `"teddy"`, to find the matching value. A **Set** is a collection with no repeats: add `"ball"` twice, and it still keeps just one `"ball"`.

2. What does LIFO mean, and which values does a stack return after `push("A")`, `push("B")`, `push("C")`, followed by two calls to `pop()`?

   **Answer:** **LIFO means "Last In, First Out."** Think of a pile of plates. The last plate you put on top is the first one you take off. After adding `"A"`, then `"B"`, then `"C"`, the first `pop()` removes and returns **`"C"`**. The second removes and returns **`"B"`**. Only `"A"` remains.

3. Why does `peek()` access `this.items[this.items.length - 1]`, and how does the example class handle an empty stack?

   **Answer:** `peek()` means "Look at the top without taking it away." Computers number array places starting at **0**. With three toys, the places are **0, 1, 2**. So **3 − 1 = 2** gives the last toy's place. That is why we use `this.items.length - 1`. In this example, an empty stack makes both `peek()` and `pop()` return **`undefined`**, meaning "There's nothing here!"

4. How does the return value of `linearSearch()` differ from that of `findUserById()` when no match is found?

   **Answer:** Both look through items one by one, like searching for a toy. If nothing matches, `linearSearch()` returns **`-1`**, meaning "I couldn't find its place." `findUserById()` returns **`null`**, meaning "I couldn't find that person." Both mean "not found," but use different signals.

5. Why is Bubble Sort inefficient for large lists, and how does `[...array]` affect additional memory usage and the original array?

   **Answer:** Imagine putting numbered blocks in order. Bubble Sort checks two blocks beside each other and swaps them if they are in the wrong order. It keeps going through the row until everything is sorted. With lots of blocks, this can mean lots and lots of checking! The work can grow roughly like the number of blocks multiplied by itself. We call this **`O(n²)`**, where `n` is the number of items.

   `[...array]` makes a **new list**. Sorting that new list leaves the original list's order unchanged. But another list needs extra space. More items mean more extra space: **`O(n)`**.
