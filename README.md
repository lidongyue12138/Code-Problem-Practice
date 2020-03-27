# Code-Problem-Practice 

Recording my coding practice routine :rocket:

### 2020.3.27

leetcode: `Linked List`

- [21. Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists)

  - iterative solution: base solution

    ```c++
    cur->next = (l1) ? l1:l2;
    ```

  - recursive solution

- [86. Partition List](https://leetcode.com/problems/partition-list)

  - Two pointer approach: simple and intuitive
  - my own solution: first submission (complicated thought)

- [109. Convert Sorted List to Binary Search Tree](https://leetcode.com/problems/convert-sorted-list-to-binary-search-tree)

  - Recursion:
    - two pointer approach for finding out the middle element of a linked list :star:
  - Recursion + Conversion to Array :star:
  - Inorder Simulation

- [24. Swap Nodes in Pairs](https://leetcode.com/problems/swap-nodes-in-pairs)

  - classical swap problem: use dummy node

- [143. Reorder List](https://leetcode.com/problems/reorder-list) 

  - logic == 206 + 92 

- [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list) :star:

  standard code block

  ```C++
  ListNode *tmp = pre->next;
  pre->next = cur->next;
  cur->next = cur->next->next;
  pre->next->next = tmp;
  ```

- [92. Reverse Linked List II](https://leetcode.com/problems/reverse-linked-list-ii) :star:

### 2020.3.24

leetcode: `Dynamic Programming`

- 332 Coin Change
  - Dynamic Programming
  - DFS search (pruning out unnecessary situations): much faster :star:
- 413 Arithmetic Slices
- 221 Maximal Square :star:
  - brute force search (my solution)
  - Dynamic Programming
- 64 Minimum Path Sum :star:
- 85 Maximal Rectangle :star:
  - similar to 221 (but solution is totally different)
  - similar to 84: histogram square
- 85 Maximal Rectangle :star:
  - Search left and right
  - use stack :star:
- 70 Climbing Stairs
  - `Fibonacci array`
- 53 Maximum Subarray :star:
  - classical subarray sum problem: O(n) time, O(1) space
- 121 Best Time to Buy and Sell Stock :star:
  - transform to 53 problem
  - intuitive solution: record minimum price

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