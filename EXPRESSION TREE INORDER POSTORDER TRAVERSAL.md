# Experiment 9(c): Expression Tree – Inorder and Postorder Traversal

## Aim
To write a Python program to build the following expression tree and print the inorder and postorder traversal.


---

## Algorithm

1. Begin the program.
2. Import the necessary modules (`build`, `Node`) from the `binarytree` package.
3. Define a list `x` representing the binary tree in pre-order format.
4. Use the `build()` function to construct the expression tree from the list.
5. Print the inorder traversal of the expression tree using `.inorder`.
6. Print the postorder traversal of the expression tree using `.postorder`.
7. End the program.

---

## Program

```
class Node:
    def __init__(self, val, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right

def isLeaf(node):
    return node.left is None and node.right is None
 
def process(op, x, y):
    if op == '+':
        return x + y
    if op == '-':
        return x - y
    if op == '*':
        return x * y
    if op == '/':
        return x / y
 
def evaluate(root):
    if root is None:
        return 0
    if isLeaf(root):
        return float(root.val)
    x=evaluate(root.left)
    y=evaluate(root.right)
    return (process(root.val,x,y))
root=Node('+')
root.left=Node('*')
root.right=Node('/')
root.left.left=Node('-')
root.left.right=Node('5')
root.right.left=Node('21')
root.right.right=Node('7')
root.left.left.left=Node('10')
root.left.left.right=Node('5')
print("The value of the expression tree is",evaluate(root))
```

## OUTPUT
![image](https://github.com/user-attachments/assets/28f8c089-8ac3-4994-bce9-4401678e348b)

## RESULT
The program builds the expression tree and calculates its value correctly. The output is as expected, so the program works well.


