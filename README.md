# Code-Problem-Practice 

Recording my coding practice routine :rocket:

### 2020.3.20

leetcode: `Dynamic Programming`

- 198 House Robber:
  - O(1) space implementation
- 213 House Robber II:
  - Two way House Robber
- 132 Palindrome Partition:
  - Record isPalindrome and partition number
  - prune cases: expand out from current letter
- 62 Unique Path:
  - O(n) space implementation
- 63 Unique Path II:
  - Similar implementation: watch out for the corner case

### 2020.3.17

leetcode: `tree`

- 99 Binary Tree Right Side View: `Depth-first Search` `Breadth-First Search`
  - postorder search and only record first one of the level
- 111 Minimum Depth of Binary Tree: `Depth-first Search` `Breadth-First Search`
- 112 Path Sum: `Depth-first Search` `Breadth-First Search`
- 103 Binary Tree Zigzag Level Order Traversal: `Depth-first Search` `Breadth-First Search`
  - use deque
- 94 Binary Tree Inorder Traversal
- 113 Path Sum II: `Depth-first Search` `Breadth-First Search`

### 2020.3.14

leetcode: `tree`

- 96 Unique Binary Search Trees: `Dynamic Programing`

- 95 Unique Binary Search Trees II: `Dynamic Programing`

- 106 Construct Binary Tree from Inorder and Postorder Traversal :star:
  - Solved in recursion version. This one is a quite classic problem. 

- 100 Same Tree: `Inorder Traversal`

- 99 Recover Binary Search Tree :star:
  - First, could be solved by a inorder traversal (only two nodes are swapped)
  - Second, a very interesting way to solve by `Morris Traversal`. Look at [this website](https://www.cnblogs.com/AnnieKim/archive/2013/06/15/morristraversal.html) and [this discussion](https://leetcode.com/problems/recover-binary-search-tree/discuss/32559/Detail-Explain-about-How-Morris-Traversal-Finds-two-Incorrect-Pointer).

leetcode: `linked list`

- 206 Reverse Linked List
  - Iterative: dummy node
  - recursive: straight-forward
- 92 Reverse Linked List II
  - iterative: dummy node