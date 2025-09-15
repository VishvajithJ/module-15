# Experiment 9(b): Binary Search Tree

## Aim
To write a Python program to build a Binary Search Tree (BST) using a built-in function.

---

## Algorithm

1. Start the program.
2. Import the `Node` class from the `binarytree` module.
3. Define a function `_build_bst_from_sorted_values()` to build a BST recursively from a sorted list.
4. Define a function `left_subtree()` to print the values in the left subtree of the BST.
5. Accept input from the user for the number of elements.
6. Read the elements into a list.
7. Sort the list.
8. Build the BST by calling `_build_bst_from_sorted_values()` with the sorted list.
9. Print the postorder traversal of the BST.
10. Print the left subtree values.
11. Check and print whether the built tree is a Binary Search Tree.
12. End the program.

---

## Program

```
#@title Default title text
from binarytree import Node
def _build_bst_from_sorted_values(sorted_values):
    
    if len(sorted_values) == 0:
        return None
    mid_index = len(sorted_values) // 2
    root = Node(sorted_values[mid_index])
    root.left = _build_bst_from_sorted_values(sorted_values[:mid_index])
    root.right = _build_bst_from_sorted_values(sorted_values[mid_index + 1 :])  
    return (root)

def right_subtree(l):
  print("Right Subtree : ")
  for i in l[2].values:
    print(i,"-->",end="")
  return 

a=[]
size=int(input())
for i in range(0,size):
  val=int(input())
  a.append(val)
x=sorted(a)


l=_build_bst_from_sorted_values(x)
print("Postorder :",l.postorder)
right_subtree(l)
print("\nIs this a Binary Search Tree? ",l.is_bst)


```

## OUTPUT

![image](https://github.com/user-attachments/assets/22ed85cd-a87f-4c08-b9b6-0465d094c146)

## RESULT
The program correctly builds a Binary Search Tree from the input values, displays its postorder traversal, and confirms that the tree is a valid BST
