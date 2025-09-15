# Experiment 9(a): Binary Tree (Float Values)

## Aim
To write a Python program to build a binary tree with a root, left, and right node using float values.

---

## Algorithm

1. Start the program.
2. Import the `Node` class from the `binarytree` module.
3. Create a root node using the `Node` class and input a floating-point value for the root.
4. Create left and right child nodes for the root using floating-point values.
5. Convert the binary tree to a list.
6. Print the list of nodes.
7. End the program.

---

## Program

```
from binarytree import Node,build
l=[]
for i in range(0,3):
    a=input()
    l.append(a)
root=Node(l[0])
root.left=Node(l[1])
root.right=Node(l[2])

print("List of nodes :",list(root))

```

## OUTPUT
![image](https://github.com/user-attachments/assets/e54ef15b-2d39-45a7-abe6-03172d6a962e)

## RESULT
The program successfully creates a binary tree with float values as nodes, prints the tree as a list of nodes, and confirms the correct construction of the binary tree
