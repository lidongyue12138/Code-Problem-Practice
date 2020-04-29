# Code-Problem-Practice 

Recording my coding practice routine :rocket:

### 2020.4.29

leetcode: `math`

- [268. Missing Number](https://leetcode.com/problems/missing-number)
  - XOR'ing a number by itself results in 0
  - XOR is commutative and associative
- [273. Integer to English Words](https://leetcode.com/problems/integer-to-english-words)
- [1073. Adding Two Negabinary Numbers](https://leetcode.com/problems/adding-two-negabinary-numbers):star:
  - Interesting! 
  - Change from add from binary numbers 

### 2020.4.28

leetcode: `Binary Search`

- [74. Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix)

  - Don't treat it as a 2D matrix, just treat it as a sorted list

- [981. Time Based Key-Value Store](https://leetcode.com/problems/time-based-key-value-store)

  - This is new. We need to write a class first.
  - Hash map + map: lower_bound
  - Use binary search :star:

- [50. Pow(x, n)](https://leetcode.com/problems/powx-n) :star:

  - Watch out for processing `n<0`

    ```
    double myPow(double x, int n) {
        if (n==0) return 1;
        if (n<0) return 1/x * myPow(1/x, -(n+1));
        return (n%2) ? myPow(x*x, n/2)*x:myPow(x*x, n/2);
    }
    ```

  - Bit manipulation

- [69. Sqrt(x)](https://leetcode.com/problems/sqrtx)

  - Newton's method: 

    ![{x}_{{k+1}}={\frac  {1}{2}}\left(x_{k}+{\frac  {n}{x_{k}}}\right),\quad k\geq 0,\quad x_{0}>0.](https://wikimedia.org/api/rest_v1/media/math/render/svg/6c5fdaf147463d73eb69b6a9d85d97b2e1d9a6ce)

  - Binary search: watch out for edge cases (fastest)

### 2020.4.26

leetcode: `Binary Search`

- [4. Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays):star:

  - Binary Search: median number index property
    - Search in the short array
    - edge cases solved by adding imaginary nodes (smart)

- [35. Search Insert Position](https://leetcode.com/problems/search-insert-position)

  - Easy binary search problem

    ```
    if (nums[mid] >= target) hi = mid;
    else lo = mid + 1;
    ```

- [34. Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array) 

  - Binary search for the left and right boundary (2 pass) :star: (a trick to make mid bias to the right)
  - Another way to search right bound: search left bound for `target + 1`

- [744. Find Smallest Letter Greater Than Target](https://leetcode.com/problems/find-smallest-letter-greater-than-target)

  - Find right bound

- [153. Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array)

  - Remember:

    ```c++
    int findMin(vector<int>& nums) {
            int lo = 0, hi = nums.size() - 1, mid;
            
            while (lo < hi) {
                mid = (lo + hi) >> 1;
                
                if (nums[mid] > nums[hi]) lo = mid + 1; // compare with right one
                else hi = mid; 
            }
            return nums[lo];
        }
    ```

  - Another way

    ```C++
    int findMin(vector<int> &num) {
            int start=0,end=num.size()-1;
            
            while (start<end) {
                if (num[start]<num[end])
                    return num[start];
                
                int mid = (start+end)/2;
                
                if (num[mid]>=num[start]) {
                    start = mid+1;
                } else {
                    end = mid;
                }
            }
            
            return num[start];
        }
    ```

- [162. Find Peak Element](https://leetcode.com/problems/find-peak-element)
  - find the peak only on its right elements( cut the array to half)
  - Tricky one: because search we can always get a solution by searching the local maximum side

### 2020.4.23

leetcode: `array` `Binary Search`

- [704. Binary Search](https://leetcode.com/problems/binary-search)
  - Typical Solution
  - Difference of `l < r` and `l <= r`
    - first should be right open interval
    - second should be right closed interval

- [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array) :star:
  - Find the smallest one
  - Perform normal binary search
- [81. Search in Rotated Sorted Array II](https://leetcode.com/problems/search-in-rotated-sorted-array-ii)
  - Handle special condition where `nums[left] == nums[mid]`

### 2020.4.14

leetcode: `array`

- [1. Two Sum](https://leetcode.com/problems/two-sum)
  - Hash Map: record indexes:star:
  - Sorted two-sum search problem (more complex)
- [15. 3Sum](https://leetcode.com/problems/3sum) :star:
  - Classic
  - Sort + Decompose to two sum problem
- [16. 3Sum Closest](https://leetcode.com/problems/3sum-closest)
  - Similar to 15
  - Add conditional codes for a few specific cases (faster).
- [923. 3Sum With Multiplicity](https://leetcode.com/problems/3sum-with-multiplicity)
  - Hash map

leetcode: `backtracking`

- [77. Combinations](https://leetcode.com/problems/combinations)
  - iterative
  - recursive
  - backtrack
- [78. Subsets](https://leetcode.com/problems/subsets)
  - recursive
  - iterative
  - bit manipulation

### 2020.4.12

leetcode: `array`

- [18. 4Sum](https://leetcode.com/problems/4sum)
  - attention on how to eliminate repeated one
  - fast 2-pointer to solve 2-sum, and recursion to reduce the N-sum to 2-sum
- [169. Majority Element](https://leetcode.com/problems/majority-element) 
  - [this solution collection](https://leetcode.com/problems/majority-element/discuss/51612/C%2B%2B-6-Solutions) 
  - Hash Table
  - Sort
  - Moore Voting Algorithm:star:
  - Bit Manipulation

### 2020.4.11

leetcode: `array`

- [55. Jump Game](https://leetcode.com/problems/jump-game): 
  - Record maximum reach of jump
- [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water)
  - Two pointer: how to traverse all possible feasible solutions? (Pruning)

### 2020.4.4

leetcode: `daily challenge`

- [283. Move Zeroes](https://leetcode.com/problems/move-zeroes)
  - scan once, move non-zero to the front

leetcode: `graph`

- [133. Clone Graph](https://leetcode.com/problems/clone-graph)
  - learn to write BFS/DFS to traverse a graph
  - In this problem, **avoid copying the same node for multiple times** (mapping from an original node to its copy)
- [207. Course Schedule](https://leetcode.com/problems/course-schedule)
  - **topological sort** to detect circle, we first transform it to the adjacency-list representation. 
- [289. Game of Life](https://leetcode.com/problems/game-of-life) :star:
  - Simulation problem
  - In place solution: use 2nd-bit as change number (genius)

### 2020.4.3

leetcode: `daily challenge`

- [136. Single Number](https://leetcode.com/problems/single-number)
  - O(n) solution use XOR

- [202. Happy Number](https://leetcode.com/problems/happy-number)
  - Floyd Cycle detection algorithm
  - Use set to detect cycle
- [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray)

### 2020.3.31

leetcode: `Linked List`

- [2. Add Two Numbers](https://leetcode.com/problems/add-two-numbers)

  - Linked List add two number

- [23. Merge k Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists) :star:

  - Construct on merge two sorted list

  - Merge two adjacent lists every iteration

    ```
    I agree with @cqnkxy.
    
    During 1st iteration, we merge two lists(every list is N) into one, this will make K down to K / 2.
    
    During 2nd iteration, we merge two lists(every list is 2N) into one, this will make K / 2 down to k /4.
    
    During 3rd iteration, we merge two lists(every list is 4N) into one, this will make K / 4 down to k /8.
    
    And so forth...
    
    I think when we merge two lists, the complexity is O(list1.length) + O(list2.length).
    
    So the total complexity is:
    
    (2N) * (K / 2) + 
    (4N) * (K / 4) + 
    (8N) * (K / 8) + 
    .............. + 
    (2^logK*N) * (K / (2 ^logK)) 
    
    = logK*KN
    ```

  - Priority-queue or Heap

    - priority_queue<Type, Container, Functional> 

      default Functional is < 

      ```C++
      struct compare {
          bool operator()(const ListNode* l, const ListNode* r) {
              return l->val > r->val; // output minimum one
          }
      };
      ```

    - Heap in C++: Maximum Heap

      ```C++
      static bool heapComp(ListNode* a, ListNode* b) {
              return a->val > b->val;
      }
      ```

    - [Heap in C++ STL | make_heap(), push_heap(), pop_heap(), sort_heap(), is_heap, is_heap_until()](https://www.geeksforgeeks.org/heap-using-stl-c/)

- [1171. Remove Zero Sum Consecutive Nodes from Linked List](https://leetcode.com/problems/remove-zero-sum-consecutive-nodes-from-linked-list) :star:

  - **Intuition**

      ```
      Assume the input is an array.
      Do you know how to solve it?
      Scan from the left, and calculate the prefix sum.
      Whenever meet the seen prefix,
      remove all elements of the subarray between them.
      ```
      
      ![image](https://assets.leetcode.com/users/hamlet_fiis/image_1566705933.png)
      
      ![image](https://assets.leetcode.com/users/hamlet_fiis/image_1566705946.png)

- [817. Linked List Components](https://leetcode.com/problems/linked-list-components)

  - use set or list to record appearance

    ```C++
    unordered_set<int> setG (G.begin(), G.end());
    
    ... setG.count(head->val) ... // appearance
    ... setG.erase(...) ... // delete
    ```

- [445. Add Two Numbers II](https://leetcode.com/problems/add-two-numbers-ii)

  - If no reverse: stack:star:

- [83. Remove Duplicates from Sorted List](https://leetcode.com/problems/remove-duplicates-from-sorted-list)

### 2020.3.30

leetcode: `Linked List`

- [61. Rotate List](https://leetcode.com/problems/rotate-list)

  - Find the tail and reconnect
  - Use the circle list

- [25. Reverse Nodes in k-Group](https://leetcode.com/problems/reverse-nodes-in-k-group)

  - Reverse Node classical code block (use frequently)

    ```Python
    # Not using dummy node
    prev, cur, nxt = None, head, head
    while cur:
        nxt = cur.next
        cur.next = prev
        prev = cur
        cur = nxt
    return prev    
    ```

  - recursive solution

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