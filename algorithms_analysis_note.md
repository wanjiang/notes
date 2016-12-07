#Dynamic Programming
- Identify recursive properties
  - Solve iteratively
  - Use Bottom-up approach
- Dynamic Programming Algorithms
  - Fibonacci Sequence
  ```
  F(n) = n,             if n<2
       = F(n-1)+F(n-2), otherwise
  ```
    - Divide-and-conquer Algoritm
      - Recursion Tree
      - Time complexity T(n)=1.5^n
    - Dynamic Programming
      - Time complexity? 
    
  - Binomial Coefficient
    - C(n,k) = C(n-1,k) + C(n-1,k-1)
    - Divide-and-conquer vs dynamic programming

  - 0/1 Knapsack
    - greedy approach
    - divide and conquer
    - dynamic programming

  - Matrix Chain Multiplication
    - Given a chain of matrics A1,A2,A3,...,An and dimensions d0,d1,...,dn
      where Ai is a di-1xdi matix, determine the best order in which to 
      carry out the matix multiplication in a way that minimizes the number of
      scalar multiplications.
    - Brute force
    - Greedy approach
    - Dynamic programming
      - find the recursive property of the solution to a problem and solve it
        iteratively
        ```
        value(i,j) = min{value(i,k)+value(k,j)+di-1*dk*dj}
        ```
      - bottom-up approach
        - start with the smallest problem, store solutions in an array or table
        ```
        n by n table
        value(i,i) = 0
        value(i,i+1)
        ```
        ```
        output:
        value[n,n]
        K[n,n]
        ```
        - look up the solutions to smaller problems

  - Floyd's Algorithm for All Pairs Shortest Paths
    - Given an edge-weighted directed graph, compute the shortest paths from
      each vetex to each of the other vertices.
    - how many different paths?
    - how many pairs of vertices?
    - O(?)

#Greedy Approach
- Very efficient if locally optimal choices lead to globally optimal solution
- Algorithms
  - Kruskal's Minimum Spanning Tree
  - Prim's Minimum Spanning Tree
  - Dijkstra's Shortest Path
  - Scheduling Problems
  - Optimal Merge Pattern
  - Huffman Code


#Searching Problems
- Binary and Sequential Search algorithms
- Finding Maximum
  - Lower bound in Maximum Problem
    - Simple recursive O(n-1)
      ```
      W(n) = 0,        n=1
           = W(n-1)+1, n>1
      ```
    - Divide and conquer O(n-1)
      ```
      W(n) = 0,        n=1
           = 2W(n/2)+1,n>1
      ```
  - (n-1) elements have to lose in a comparison, each produces at most one loser

- Finding Maximum and Minimum
  - B(n)=(n-1) if array is ordered, W(n)=(2n-2)
  - Divide and conquer O(3n/2-2)

    ```
    Assume n>=2
    if n=2
      compare s[l] and s[u] => max, min
    else
      maxmin(S,l,m,max1,min1)
      maxmin(S,m+1,u,max2,min2)
      max=larger(max1,max2)
      min=smaller(min1,min2)
    ```

    ```
    W(n) = 1,         n=2
         = 2W(n/2)+2, n>2
    ```

  - Lower bound on Maximum and Minimum
    - Labeling argument n/2+(n-2)
      - label each element as
      ```
      N: has not been compared
      W: has won one or more comparison(s)
      L: has lost one or more comparison(s)
      W/L: has won and lost
      N     W  one element
      N     WL n-2 elements
      N     WL
      .
      .
      .     WL
      N     L  one element
      need 1+2(n-2)+1=(2n-2) lable changes
      ```
      ```
      Types of comparisons:(N,N),(N,W),(W,W),...(L,W)
      Only type (N,N) guarantees 2 label changes
      There are n/2 comparisons of (N,N) which makes 2(n/2)=n label changes
      We need additional 2n-2-n=(n-2) lable changes, which requires (n-2) more 
      comparisons
      ```

#Comparison
- Recursion tree vs decision tree
  - MergeSort, Fib(8)

#Fundamentals
- Time vs Storage
  - time means CPU cycles and storage means memory
- instance vs solution
- recursion tree (P31)


#Search Algorithms
- Binary search
- Sequential Search


#Fundamentals
- Basic Programming Model
  - Basic structure Java
    - Primitive data types
    - Statements
    - Arrays
    - Strings
    - Input/output sets
    - Data abstraction
- Data Abstraction
- Bags, Queues, and Stacks
- Analysis of Algorithms
