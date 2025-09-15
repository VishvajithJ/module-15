# Experiment 9(e): Expression Tree Evaluation

## Aim
To write a Python program to build and evaluate the given expression tree.

---

## Algorithm

1. Start the program.
2. Create nodes for operators and operands.
3. Build the expression tree by connecting the nodes in the correct hierarchical structure.
4. Define a recursive function `evaluate(root)`:
   - If the node is a number (leaf), return it as a float.
   - Else, recursively evaluate the left and right subtrees.
   - Apply the operator at the current node to the results.
5. Return the final result from the root node.
6. End the program.

---

## Program

```
from binarytree import build
nodes=['*','+','-',9,3,8,4]
root=build(nodes)
print(root.inorder)
print(root.postorder)

```

## OUTPUT
![image](https://github.com/user-attachments/assets/97644e8f-959b-45a3-b6cc-44ed013e76db)



## RESULT
The program successfully builds an expression tree from the given list of nodes and prints the inorder and postorder traversals of the tree. This confirms the correct structure of the expression tree. However, the actual evaluation of the expression is not performed in the current code.
