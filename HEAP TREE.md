# Experiment 9(d): Heap Tree

## Aim
To write a Python program to build a heap tree using appropriate Python package and function.

---

## Algorithm

1. Start the program.
2. Import the `heapq` module.
3. Define a function `heaptree()` that takes a list `H` as input.
4. Use `heapq.heapify(H)` to convert the list into a valid heap (min-heap).
5. Print the created heap.
6. End the program.

---

## Program

```
from binarytree import build,heap,Node 
def min_max_heap(L): 
    node=L
    t=build(node)
    for i in t.values:
        print(i,"-->",end="")
    if(t.is_complete):
        print("\nComplete binary tree")
        if(t.is_min_heap):
            print("\nMin heap tree")
        elif(t.is_max_heap):
            print("\nMax heap tree")
    else:
        print("\nNot a Complete binary tree")

```

## OUTPUT
![image](https://github.com/user-attachments/assets/45bb4fde-12a4-4125-b813-ab6f18154895)

## RESULT
The program successfully builds a binary heap tree from the given list. It verifies that the tree is a complete binary tree and correctly identifies whether it is a min-heap or max-heap. The output confirms the heap properties as expected.
