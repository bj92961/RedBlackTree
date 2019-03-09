# RedBlackTree
Implement red black tree in Python

Red-Black Tree is a special Binary Search Tree(BST). In a red-black tree, each node has to follow four rules below:
1). Every node is either red or black.
2). Root node is black
3). There are no two adjacent red nodes (A red node cannot have a red parent or red child).
4). Every path from a node (including root) to any of its descendant NULL node has the same number of black nodes. 

1. Add
	When we add a new node to tree, this new node is always set to RED. If its parent is black, we are done. If its parent
	is red, rule 3 is broken. We need to fix it. 
  
2. Delete
  Deletion is a bit complicated. We assume node x is to be deleted. If x has two children, then we need to find a leaf node
  to replace it, that is to say x is becoming a leaf node. In the end, we are sure x is either a leaf node or a node with
  one child only. If x and its parent have different color, we can safely remove x without violating any rule. If x and
  its parent are same color(double black), we need to solve the double black issue.

Function is_valid_red_black_tree is for testing. It helps us check if our tree is valid or not at any time. 
