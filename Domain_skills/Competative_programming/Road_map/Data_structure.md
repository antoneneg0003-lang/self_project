# 🧱 DATA STRUCTURES — EXHAUSTIVE CATALOG (Deep Hierarchical Learning Map)

====================================================================
LEVEL 0 — FOUNDATIONAL IDEA
====================================================================

- Data Structure
  - Primitive / Atomic Types
  - Abstract Data Types (Logical Models)
  - Concrete Implementations
  - Specialized / Domain-Specific Structures


====================================================================
LEVEL 1 — ABSTRACT DATA TYPES (Logical Layer)
====================================================================

- Collection ADTs
  - Container
  - Iterable
  - Sequence
    - List
    - Tuple (Product Type)
  - Set
    - Multiset / Bag
  - Map / Dictionary
    - Multimap

- Restricted Access ADTs
  - Stack (LIFO)
  - Queue (FIFO)
    - Deque
    - Priority Queue
      - Min Priority Queue
      - Max Priority Queue
    - Double-ended Priority Queue

- Partitioning ADT
  - Disjoint Set (Union-Find)

- Hierarchical ADTs
  - Tree
  - Heap (Priority-based Tree)
  - Graph


====================================================================
LEVEL 2 — LINEAR / SEQUENTIAL STRUCTURES
====================================================================

- Array-Based Structures
  - Static Array
  - Dynamic Array (Vector)
  - Multi-dimensional Array
    - 2D Array
    - 3D Array
  - Jagged Array
  - Sparse Array
  - Circular Array
  - Circular Buffer
  - Bit-Level Arrays
    - Bit Array
    - Bitset
    - Bitmap
    - Bitfield
  - Memory Layout Variants
    - Dope Vector
    - Iliffe Vector
    - Hashed Array Tree

- String / Text Sequences
  - Immutable String
  - Mutable String Buffer
  - Rope (Tree-backed string)

- Linked Structures
  - Linked List
    - Singly Linked List
    - Doubly Linked List
    - Circular Linked List
    - XOR Linked List
  - Unrolled Linked List
  - Skip List
    - Deterministic Skip List
    - Randomized Skip List
  - Self-organizing List
  - Association List
  - Zipper (Functional Navigation)

- Text Editor Structures
  - Gap Buffer
  - Piece Table
  - Rope (repeated because multi-category)


====================================================================
LEVEL 3 — HASH-BASED STRUCTURES
====================================================================

- Hash Table
  - Collision Handling
    - Separate Chaining
    - Open Addressing
      - Linear Probing
      - Quadratic Probing
      - Double Hashing
      - Robin Hood Hashing
      - Cuckoo Hashing
  - Perfect Hashing
    - Static Perfect Hashing
    - Dynamic Perfect Hashing

- Hash Variants
  - Hash Map
  - Hash Set
  - Hash Multiset
  - Hash Array Mapped Trie (HAMT)
  - Ctrie (Concurrent HAMT)

- Probabilistic Hash Structures
  - Bloom Filter
  - Cuckoo Filter
  - Quotient Filter

- Streaming / Sketch Structures
  - Count-Min Sketch
  - HyperLogLog
  - MinHash
  - Locality Sensitive Hashing (LSH)


====================================================================
LEVEL 4 — TREE STRUCTURES
====================================================================

- Basic Trees
  - Binary Tree
    - Full
    - Complete
    - Perfect
    - Threaded
  - General Tree
    - Left-Child Right-Sibling Representation

--------------------------------------------------

- Binary Search Trees (Ordered Trees)
  - Basic BST
  - Self-Balancing BST
    - AVL Tree
    - Red-Black Tree
    - AA Tree
    - WAVL Tree
    - Scapegoat Tree
    - Splay Tree
    - Treap
    - Zip Tree
    - Weight-Balanced Tree

--------------------------------------------------

- Multiway Search Trees
  - B-Tree
    - B+
    - B*
  - 2–3 Tree
  - 2–3–4 Tree
  - (a,b)-Tree
  - Bε-Tree
  - Fractal Tree
  - LSM Tree
  - Buffer Tree

--------------------------------------------------

- Heap Structures
  - Binary Heap
    - Min Heap
    - Max Heap
  - d-ary Heap
  - Binomial Heap
  - Fibonacci Heap
  - Pairing Heap
  - Leftist Heap
  - Skew Heap
  - Soft Heap
  - Weak Heap
  - Brodal Queue
  - Interval Heap
  - Min-Max Heap

--------------------------------------------------

- Trie / Prefix Trees
  - Trie
  - Compressed Trie
  - Patricia Trie
  - Radix Tree
  - Binary Trie
  - Persistent Trie
  - Judy Array
  - X-fast Trie
  - Y-fast Trie
  - van Emde Boas Tree

--------------------------------------------------

- Range Query Trees
  - Segment Tree
    - Lazy Segment Tree
    - Persistent Segment Tree
    - Dynamic Segment Tree
    - 2D Segment Tree
    - Segment Tree Beats
  - Fenwick Tree
    - 1D BIT
    - 2D BIT
  - Interval Tree
  - Range Tree
  - Priority Search Tree
  - Cartesian Tree
  - Order Statistic Tree
  - Merge Sort Tree
  - Sparse Table
  - Disjoint Sparse Table
  - Li Chao Tree

--------------------------------------------------

- String Index Trees
  - Suffix Tree
    - Generalized Suffix Tree
  - Suffix Array
    - Compressed Suffix Array
  - FM-Index
  - Wavelet Tree
  - Palindromic Tree (Eertree)

--------------------------------------------------

- Spatial Trees
  - k-d Tree
  - Quadtree
  - Octree
  - R-Tree
    - R+
    - R*
  - BSP Tree
  - VP-Tree
  - BK-Tree
  - Cover Tree
  - M-Tree

--------------------------------------------------

- Dynamic Trees
  - Link-Cut Tree
  - Euler Tour Tree
  - Top Tree


====================================================================
LEVEL 5 — GRAPH STRUCTURES
====================================================================

- Graph Representations
  - Adjacency List
  - Adjacency Matrix
  - Edge List
  - CSR Representation
  - Implicit Graph

- Graph Variants
  - Directed Graph
  - Undirected Graph
  - Weighted Graph
  - Multigraph
  - Hypergraph
  - DAG

- Graph Decomposition Trees
  - Dominator Tree
  - Gomory-Hu Tree
  - SPQR Tree

- Decision Diagrams
  - BDD
  - ZDD
  - AIG


====================================================================
LEVEL 6 — PERSISTENT / FUNCTIONAL / SUCCINCT
====================================================================

- Persistent Structures
  - Persistent Array
  - Persistent Segment Tree
  - Persistent Trie
  - Persistent DSU
  - Fully Persistent BST

- Functional Structures
  - Finger Tree
  - Zipper

- Succinct Structures
  - Rank/Select Bitvector
  - Wavelet Tree
  - FM-Index
  - Elias-Fano Encoding


====================================================================
LEVEL 7 — ADVANCED SYSTEM STRUCTURES
====================================================================

- Cache-Oblivious Structures
  - Cache-Oblivious B-Tree
  - Funnel Heap
  - COLA

- Concurrent Structures
  - Lock-Free Stack
  - Lock-Free Queue
  - Concurrent Hash Map
  - Non-blocking Skip List

- Distributed Structures
  - Distributed Hash Table
  - Chord
  - Kademlia
  - Merkle Tree
  - CRDT

- Computational Geometry Structures
  - Half-Edge Structure
  - Winged-Edge Structure
  - BVH
  - BIH

- Compiler / Logic Structures
  - Abstract Syntax Tree
  - Parse Tree
  - Expression Tree
  - Decision Tree
  - E-Graph
