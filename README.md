# Design and Analysis of Algorithms (DAA) -- Practicals

This repository contains Python programs for the **Design and Analysis
of Algorithms (DAA)** laboratory. It includes implementations of sorting
and searching algorithms, heap sort, factorial, dynamic programming
problems, graph traversal, minimum spanning tree algorithms, shortest
paths, and the Travelling Salesperson Problem.

The README provides a summary, conclusion, and time and space complexity
for each practical.

## Table of Contents

1.  [Practical 1 -- Sorting
    Algorithms](#practical-1--sorting-algorithms)
2.  [Practical 2 -- Linear Search and Binary
    Search](#practical-2--linear-search-and-binary-search)
3.  [Practical 3 -- Max Heap Sort](#practical-3--max-heap-sort)
4.  [Practical 4 -- Factorial Using Iteration and
    Recursion](#practical-4--factorial-using-iteration-and-recursion)
5.  [Practical 5 -- Knapsack Using Dynamic
    Programming](#practical-5--knapsack-using-dynamic-programming)
6.  [Practical 6 -- Matrix Chain
    Multiplication](#practical-6--matrix-chain-multiplication)
7.  [Practical 7 -- Making Change
    Problem](#practical-7--making-change-problem)
8.  [Practical 8 -- Graph Traversal Using BFS and
    DFS](#practical-8--graph-traversal-using-bfs-and-dfs)
9.  [Practical 9 -- Prim's Algorithm](#practical-9--prims-algorithm)
10. [Practical 10 -- Kruskal's
    Algorithm](#practical-10--kruskals-algorithm)
11. [Practical 11 -- Floyd--Warshall
    Algorithm](#practical-11--floydwarshall-algorithm)
12. [Practical 12 -- Travelling Salesperson
    Problem](#practical-12--travelling-salesperson-problem)

------------------------------------------------------------------------

## Practical 1 -- Sorting Algorithms

### Summary

In this practical, five different sorting algorithms---Bubble Sort,
Selection Sort, Insertion Sort, Quick Sort, and Merge Sort---were
implemented using Python. Each program takes input elements, sorts them
in ascending order, and displays the sorted array. This practical helps
us understand how different sorting techniques work and how their
performance changes with the size and order of the input data.

### Time and Space Complexity

  -----------------------------------------------------------------------
  Sorting     Best-case time   Average-case     Worst-case      Auxiliary
  algorithm                            time           time          space
  ----------- -------------- -------------- -------------- --------------
  Bubble                O(n)          O(n²)          O(n²)           O(1)
  Sort\*                                                   

  Selection            O(n²)          O(n²)          O(n²)           O(1)
  Sort                                                     

  Insertion             O(n)          O(n²)          O(n²)           O(1)
  Sort                                                     

  Merge Sort      O(n log n)     O(n log n)     O(n log n)           O(n)

  Quick Sort      O(n log n)     O(n log n)          O(n²)       O(log n)
                                                            average; O(n)
                                                               worst-case
                                                                recursion
                                                                    stack
  -----------------------------------------------------------------------

\*Bubble Sort best case is O(n) when the implementation uses an
early-exit check. Without that check, its best-case time is O(n²).

### Conclusion

Through this practical, we learned how different sorting algorithms work
and how they can be implemented in Python. We also understood the
importance of time complexity when comparing algorithm efficiency.
Bubble Sort, Selection Sort, and Insertion Sort are simple to
understand, while Merge Sort and Quick Sort generally perform better on
larger datasets. Overall, this practical helped us understand sorting
techniques, their performance, and how to select a suitable algorithm
for a problem.

------------------------------------------------------------------------

## Practical 2 -- Linear Search and Binary Search

### Summary

In this practical, two important searching techniques---Linear Search
and Binary Search---were implemented using Python. The programs take an
array and a target element as input and search for that element. They
display the position of the element when it is found, or an appropriate
message when it is not found. The practical also compares the time
complexity of both searching methods.

### Time and Space Complexity

  -------------------------------------------------------------------------
  Searching     Best-case time   Average-case     Worst-case      Auxiliary
  algorithm                              time           time          space
  ------------- -------------- -------------- -------------- --------------
  Linear Search           O(1)           O(n)           O(n)           O(1)

  Binary Search           O(1)       O(log n)       O(log n)           O(1)
  (iterative)                                                

  Binary Search           O(1)       O(log n)       O(log n)  O(log n) call
  (recursive)                                                         stack
  -------------------------------------------------------------------------

**Note:** Binary Search works only on sorted data. If the input is not
already sorted, the time required to sort it should be considered
separately.

### Conclusion

Through this practical, we understood how searching algorithms are used
to find a particular element in a collection of data. Linear Search is
simple and can be used on unsorted data, but it may take more time for
large inputs. Binary Search is faster for large sorted arrays because it
repeatedly reduces the search area by half. This practical helped us
understand the difference between the two searching techniques and the
importance of sorting data before applying Binary Search.

------------------------------------------------------------------------

## Practical 3 -- Max Heap Sort

### Summary

In this practical, the Heap Sort algorithm was implemented using a Max
Heap in Python. The program takes elements from the user, builds a Max
Heap, and repeatedly moves the largest element to its correct position
in the array. The heap is adjusted after each removal until all elements
are arranged in ascending order. This practical demonstrates how a heap
data structure can be used to perform sorting.

### Time and Space Complexity

  Operation                       Time complexity
  ----------------------------- -----------------
  Build a Max Heap                           O(n)
  Heapify one node                       O(log n)
  Extract the maximum element            O(log n)
  Complete Heap Sort                   O(n log n)

  Case             Time complexity
  -------------- -----------------
  Best case             O(n log n)
  Average case          O(n log n)
  Worst case            O(n log n)

**Auxiliary space:** O(1) for an iterative, in-place heap sort
implementation. A recursive heapify implementation may use O(log n)
call-stack space.

### Conclusion

Through this practical, we learned how Max Heap Sort works and how the
heap data structure can be used to sort elements efficiently. We
understood how to build a Max Heap, compare parent and child elements,
and repeatedly place the largest element in its correct position.
Overall, this practical improved our understanding of heap operations
and sorting using a tree-based data structure.

------------------------------------------------------------------------

## Practical 4 -- Factorial Using Iteration and Recursion

### Summary

In this practical, the factorial of a number was implemented using two
methods: iteration and recursion. In the iterative method, a loop
multiplies the numbers from 1 up to the given number. In the recursive
method, a function calls itself with a smaller value until it reaches
the base case. Both methods calculate the factorial, and their time and
space requirements can be compared.

### Time and Space Complexity

  Method                  Time complexity   Auxiliary space
  --------------------- ----------------- -----------------
  Iterative factorial                O(n)              O(1)
  Recursive factorial                O(n)   O(n) call stack

### Conclusion

Through this practical, we learned how the same problem can be solved
using both iteration and recursion. The iterative method uses a loop and
requires constant extra space, while the recursive method solves the
problem through repeated function calls and uses additional call-stack
memory. Both methods have O(n) time complexity. This practical helped us
understand the difference between iteration and recursion and compare
their memory requirements.

------------------------------------------------------------------------

## Practical 5 -- Knapsack Using Dynamic Programming

### Summary

In this practical, the 0/1 Knapsack Problem was implemented using
Dynamic Programming. The program takes the weights and values of items,
along with the maximum capacity of the knapsack. It uses a dynamic
programming table to find the maximum value that can be obtained without
exceeding the given capacity. Each item can either be selected once or
not selected.

### Time and Space Complexity

  Approach                                   Time complexity   Auxiliary space
  ---------------------------------------- ----------------- -----------------
  Standard 2D Dynamic Programming                      O(nW)             O(nW)
  Space-optimised 1D Dynamic Programming               O(nW)              O(W)

Here, `n` is the number of items and `W` is the knapsack capacity.

### Conclusion

Through this practical, we learned how Dynamic Programming can be used
to solve the 0/1 Knapsack Problem. We understood how to divide the
problem into smaller subproblems and store previously calculated results
to avoid repeated calculations. The algorithm helps find the maximum
possible value within the given capacity. Overall, this practical
improved our understanding of Dynamic Programming and its use in
optimisation problems.

------------------------------------------------------------------------

## Practical 6 -- Matrix Chain Multiplication

### Summary

In this practical, Matrix Chain Multiplication was implemented using
Dynamic Programming. The program takes the dimensions of a sequence of
matrices and calculates the most efficient order in which they should be
multiplied. It checks different possible positions for splitting the
matrix chain and stores the minimum number of scalar multiplications
required for each subchain.

### Time and Space Complexity

  Operation           Complexity
  ----------------- ------------
  Time complexity          O(n³)
  Auxiliary space          O(n²)

Here, `n` is the number of matrices in the chain.

### Conclusion

Through this practical, we learned how Dynamic Programming can be used
to solve the Matrix Chain Multiplication problem efficiently. We
understood that the order of matrix multiplication affects the total
number of calculations, even though the final product remains the same.
By storing previously calculated results in a table, the algorithm
avoids solving the same subproblems repeatedly. This practical helped us
understand optimal parenthesisation and the use of Dynamic Programming
in optimisation problems.

------------------------------------------------------------------------

## Practical 7 -- Making Change Problem

### Summary

In this practical, the Making Change Problem was implemented using
Dynamic Programming. The program takes a set of coin denominations and a
target amount as input. It uses a dynamic programming array to calculate
the minimum number of coins required to make the given amount. The
program considers the available denominations and stores the best result
for each smaller amount so that it can calculate the result for the
target amount.

### Time and Space Complexity

For the standard minimum-number-of-coins implementation:

  Operation           Complexity
  ----------------- ------------
  Time complexity          O(mA)
  Auxiliary space           O(A)

Here, `m` is the number of coin denominations and `A` is the target
amount.

### Conclusion

Through this practical, we learned how Dynamic Programming can be used
to solve the Making Change Problem. We understood how previously
calculated results can be stored and reused to find the minimum number
of coins required for a target amount. This practical helped us
understand how Dynamic Programming can reduce repeated calculations and
solve problems involving a number of possible combinations.

------------------------------------------------------------------------

## Practical 8 -- Graph Traversal Using BFS and DFS

### Summary

In this practical, Breadth First Search (BFS) and Depth First Search
(DFS) were implemented using Python. The graph is represented using an
adjacency list. BFS uses a queue to visit vertices level by level, while
DFS uses recursion or a stack to explore one path as deeply as possible
before moving to another path. This practical demonstrates two common
methods of traversing a graph.

### Time and Space Complexity

For an adjacency-list representation:

  Algorithm                      Time complexity   Auxiliary space
  ---------------------------- ----------------- -----------------
  Breadth First Search (BFS)            O(V + E)              O(V)
  Depth First Search (DFS)              O(V + E)              O(V)

Here, `V` is the number of vertices and `E` is the number of edges. The
auxiliary space includes the visited structure and the queue or
stack/recursion stack.

### Conclusion

Through this practical, we learned how BFS and DFS work and how they can
be implemented using an adjacency list. BFS is useful for visiting
vertices level by level, while DFS explores one path deeply before
backtracking. We also understood the difference between using a queue in
BFS and recursion or a stack in DFS. Overall, this practical helped us
understand graph representation and graph traversal techniques.

------------------------------------------------------------------------

## Practical 9 -- Prim's Algorithm

### Summary

In this practical, Prim's Algorithm was implemented to find the Minimum
Spanning Tree (MST) of a weighted, undirected graph. The algorithm
starts from a selected vertex and repeatedly chooses the minimum-weight
edge that connects a vertex already included in the MST to a vertex that
has not yet been included. The selected edges are used to connect all
vertices with the minimum total weight.

### Time and Space Complexity

  -----------------------------------------------------------------------
  Implementation                Time complexity           Auxiliary space
  ------------------- ------------------------- -------------------------
  Adjacency matrix                        O(V²)      O(V²) for the matrix
  with simple                                   
  selection                                     

  Adjacency list with                O(E log V)                  O(V + E)
  binary min-heap                               
  -----------------------------------------------------------------------

The complexity depends on the graph representation and the data
structure used to select the minimum-weight edge.

### Conclusion

Through this practical, we learned how Prim's Algorithm is used to find
a Minimum Spanning Tree of a weighted graph. We understood how the
algorithm gradually connects all vertices by selecting the smallest
suitable edge at each step. This practical helped us understand the
greedy approach and how it can be used to minimise the total cost of
connecting the vertices in a graph.

------------------------------------------------------------------------

## Practical 10 -- Kruskal's Algorithm

### Summary

In this practical, Kruskal's Algorithm was implemented to find the
Minimum Spanning Tree of a weighted graph. The algorithm first sorts all
edges in increasing order of weight and then selects edges one by one.
An edge is added to the MST only if it does not create a cycle. The Find
and Union operations are used to identify connected components and avoid
cycles. Finally, the selected edges and their total cost are displayed.

### Time and Space Complexity

  -----------------------------------------------------------------------
  Operation                                                    Complexity
  ------------------------------ ----------------------------------------
  Sorting all edges                                            O(E log E)

  Find and Union operations      Nearly O(1) amortised per operation with
                                  path compression and union by rank/size

  Overall time complexity                                      O(E log E)

  Auxiliary space                  O(V) for Disjoint Set Union, excluding
                                                             edge storage
  -----------------------------------------------------------------------

Here, `V` is the number of vertices and `E` is the number of edges.

### Conclusion

Through this practical, we learned how Kruskal's Algorithm can be used
to find a Minimum Spanning Tree. We understood how sorting edges by
weight and checking for cycles helps build the MST step by step. We also
learned how the Find and Union operations help identify connected
components and prevent cycles. Overall, this practical improved our
understanding of greedy algorithms and minimum spanning trees.

------------------------------------------------------------------------

## Practical 11 -- Floyd--Warshall Algorithm

### Summary

In this practical, the Floyd--Warshall Algorithm was implemented to find
the shortest distances between all pairs of vertices in a weighted
graph. The algorithm uses a distance matrix and repeatedly checks
whether a path through an intermediate vertex gives a shorter distance
between two vertices. The matrix is updated until the shortest distances
between all pairs have been calculated.

### Time and Space Complexity

  Operation           Complexity
  ----------------- ------------
  Time complexity          O(V³)
  Auxiliary space          O(V²)

Here, `V` is the number of vertices in the graph.

### Conclusion

Through this practical, we learned how the Floyd--Warshall Algorithm
finds shortest paths between every pair of vertices in a graph. We
understood how the distance matrix is updated by considering each vertex
as an intermediate vertex. This practical helped us understand Dynamic
Programming and its application to shortest-path problems. The algorithm
can handle negative edge weights, but shortest paths are not
well-defined when a negative-weight cycle is present.

------------------------------------------------------------------------

## Practical 12 -- Travelling Salesperson Problem

### Summary

In this practical, the Travelling Salesperson Problem (TSP) was
implemented to find a minimum-cost tour in which a salesperson visits
every city exactly once and returns to the starting city. The program
uses the given travel costs or distance information to calculate a tour
with minimum total cost. This problem demonstrates how algorithms can be
applied to route planning and optimisation.

### Time and Space Complexity

The complexity depends on the method used in the program:

  -----------------------------------------------------------------------
  Approach                      Time complexity           Auxiliary space
  ------------------- ------------------------- -------------------------
  Brute Force                             O(n!)      O(n) for a recursive
                                                implementation, excluding
                                                             stored input

  Dynamic Programming                O(n² × 2ⁿ)                 O(n × 2ⁿ)
  (Held--Karp)                                  
  -----------------------------------------------------------------------

Here, `n` is the number of cities.

**Note:** Use the row that matches the approach implemented in your
`Travelling salesman.txt` program. The exact complexity cannot be
confirmed from the filename alone.

### Conclusion

Through this practical, we learned how the Travelling Salesperson
Problem can be used to find a low-cost route that visits every city
exactly once and returns to the starting city. We understood that the
problem involves checking different possible routes and selecting the
one with the minimum total cost. This practical helped us understand
combinatorial optimisation and the challenges of solving problems whose
number of possible solutions increases rapidly as the input size grows.

------------------------------------------------------------------------

## Repository Files

The following filenames are based on the files shown in the repository
screenshot. Some practicals contain more than one program.

  -----------------------------------------------------------------------
  Practical                           Files shown
  ----------------------------------- -----------------------------------
  Practical 1 -- Sorting              `Bubblesort.py`,
                                      `selectionsort.py`,
                                      `InsertionSort.py`, `MergeSort.py`,
                                      `QuickSort.py`

  Practical 2 -- Searching            `Linearsearch.py`,
                                      `BinarySearch.py`

  Practical 3 -- Heap Sort            `maxheapsorting`

  Practical 4 -- Factorial            `Factorial_iteration.py`,
                                      `Factorial_Recursive.py`

  Practical 5 -- Knapsack             `knapsack.txt`

  Practical 6 -- Matrix Chain         `chain matrix.txt`
  Multiplication                      

  Practical 7 -- Making Change        `coinchange`

  Practical 8 -- BFS and DFS          `Breadth_first_search.txt`,
                                      `Depth_first_search.txt`

  Practical 9 -- Prim's Algorithm     `prims Algorithm.txt`

  Practical 10 -- Kruskal's Algorithm `kurskal's.txt`

  Practical 11 -- Floyd--Warshall     `FLOYD WARSHAL.py`

  Practical 12 -- Travelling          `Travelling salesman.txt`
  Salesperson                         
  -----------------------------------------------------------------------

**Note:** Filenames are reproduced from the screenshot and may contain
spaces or spelling variations. Check the actual filenames in your
repository before using commands or links.

## How to Run

The `.py` files can generally be run using Python 3:

``` bash
python filename.py
```

Replace `filename.py` with the actual Python filename. For `.txt` files,
first check whether the file contains Python source code or
documentation. If it contains source code, consider renaming it with a
`.py` extension before running it.

## General Notes on Complexity

-   `n` represents the number of input elements or items.
-   `V` represents the number of graph vertices.
-   `E` represents the number of graph edges.
-   `W` represents the knapsack capacity.
-   `m` represents the number of coin denominations.
-   `A` represents the target amount in the Making Change Problem.
-   Space complexity tables describe auxiliary space unless stated
    otherwise.
-   Actual execution time depends on input size, input order,
    implementation, Python version, and computer hardware.
-   The complexity shown is theoretical. Record measured execution times
    separately if your practical requires experimental time analysis.

## Final Conclusion

By completing these practicals, we gained practical knowledge of
important algorithm design techniques, including sorting, searching,
recursion, heaps, Dynamic Programming, greedy algorithms, and graph
traversal. We also learned how to analyse the time and space complexity
of algorithms and compare their efficiency. These experiments helped us
understand how to select suitable algorithms for different computational
problems.
