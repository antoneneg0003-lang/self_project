# 🧠 STRATEGY LAYER — ULTRA-EXPANDED (ICPC + Advanced + Research-Level)
(Paradigm is NOT listed here. This is strategy-only. Very large coverage.)

====================================================================
A. PROBLEM INTAKE / FRAMING STRATEGIES
====================================================================

- Constraint-first triage strategy
- Tightest-constraint dominates strategy
- Small-n brute-force detect strategy
- Sample-IO reverse engineer strategy
- Output-shape inference strategy
- Hidden monotonicity hunting strategy
- Hidden convexity hunting strategy
- Hidden subadditivity hunting strategy
- Hidden periodicity hunting strategy
- Hidden symmetry hunting strategy
- Hidden conservation law hunting strategy
- Hidden parity structure hunting strategy
- Hidden matroid/greedy-feasible hunting strategy
- Identify “must-be-sorted” axis strategy
- Identify “must-be-graph” axis strategy
- Identify “must-be-DP” axis strategy
- Identify “must-be-flow/matching” axis strategy
- Identify “must-be-geometry” axis strategy
- Identify “must-be-number-theory” axis strategy
- Identify “must-be-string-index” axis strategy
- Identify online vs offline nature strategy
- Identify incremental updates vs static queries strategy
- Identify “answer is a function of threshold” strategy
- Identify “answer is count of configurations” strategy
- Identify “answer is feasibility” vs “optimization” strategy
- Identify “constructive” vs “decision” vs “enumerative” strategy
- Identify “local to global” structure strategy
- Identify “global invariant” structure strategy
- Identify “graph is sparse/dense” branching strategy
- Identify “tree-like” property strategy
- Identify “planar-like” property strategy
- Identify “bounded degree / bounded value range” strategy
- Identify “bounded alphabet / bounded coordinates” strategy
- Identify “bounded edit distance / bounded k” parameter strategy
- Identify “mod constraint implies modular arithmetic” strategy
- Identify “needs proof before code” strategy

====================================================================
B. CASEWORK / PARTITION STRATEGIES
====================================================================

- Case split by parity strategy
- Case split by sign strategy
- Case split by ordering of key values strategy
- Case split by max/min element location strategy
- Case split by pivot element strategy
- Case split by number of distinct values strategy
- Case split by frequency pattern strategy
- Case split by gcd pattern strategy
- Case split by prime factors pattern strategy
- Case split by bit-length strategy
- Case split by highest set bit strategy
- Case split by modulo class strategy
- Case split by connected components count strategy
- Case split by SCC count strategy
- Case split by tree centroid position strategy
- Case split by diameter endpoints strategy
- Case split by whether graph is bipartite strategy
- Case split by whether solution uses edge/doesn’t use edge strategy
- Case split by whether element is chosen/not chosen strategy
- Case split by whether optimal uses boundary value strategy
- Case split by whether optimal occurs at extreme points strategy
- Case split by “first event” in time-line strategy
- Case split by “last event” strategy
- Case split by “first mismatch” strategy
- Case split by “first crossing” in geometry strategy
- Case split by degenerate vs non-degenerate strategy

====================================================================
C. ENUMERATION / SEARCH STRATEGIES
====================================================================

- Exhaustive enumeration with pruning strategy
- Backtracking with constraint propagation strategy
- Backtracking with ordering heuristic strategy
- Backtracking with fail-fast checks strategy
- Branch-and-bound with upper bound strategy
- Meet-in-the-middle split-by-halves strategy
- Meet-in-the-middle split-by-dimension strategy
- Subset enumeration by increasing size strategy
- Subset enumeration by Gray code strategy
- Enumerate complements instead of subsets strategy
- Enumerate minimal witnesses strategy
- Enumerate maximal feasible sets strategy
- Enumerate boundary candidates only strategy
- Enumerate states of small parameter k strategy
- Enumerate permutations via next_permutation strategy
- Enumerate permutations via factoradic strategy
- Enumerate partitions via DP/recursion strategy
- Enumerate divisors via factorization strategy
- Enumerate submasks strategy
- Enumerate supermasks strategy
- Enumerate pairs via sorting + two pointers strategy
- Enumerate triples via fix-one + two-sum strategy
- Iterative deepening DFS strategy
- IDA* (cost-bounded deepening) strategy
- Bidirectional search strategy
- Multi-source search strategy
- State-space BFS on implicit graph strategy
- Layered expansion with visited compression strategy
- A* with admissible heuristic strategy (rare)
- Beam search heuristic strategy (rare)
- Random-restart search strategy (rare)
- MCMC/annealing heuristic strategy (rare)

====================================================================
D. GREEDY SELECTION / ORDERING STRATEGIES
====================================================================

- Sort-and-scan greedy strategy
- Greedy by earliest deadline strategy
- Greedy by earliest finish time strategy
- Greedy by smallest start time strategy
- Greedy by largest weight/benefit strategy
- Greedy by smallest cost strategy
- Greedy by best ratio strategy (careful) 
- Greedy by marginal gain strategy
- Greedy by marginal loss strategy
- Greedy by feasibility-first strategy
- Greedy by maintain invariants strategy
- Greedy by local exchange improvability strategy
- Greedy with priority queue “active set” strategy
- Greedy with monotonic stack strategy
- Greedy with monotonic queue strategy
- Greedy with DSU “merge when possible” strategy
- Greedy with union-find for intervals strategy
- Greedy with sweep line events strategy
- Greedy with offline sorting by key strategy
- Greedy with lazy deletions strategy
- Greedy by “take forced moves first” strategy
- Greedy by “kill biggest threat” strategy
- Greedy by “pack smallest first” strategy
- Greedy by “pack largest first” strategy
- Greedy by “fill gaps” strategy
- Greedy by “match extremes” strategy
- Greedy by “pair nearest” strategy
- Greedy by “pair farthest” strategy
- Greedy by “most constrained variable first” strategy
- Greedy by “least constraining value” strategy

====================================================================
E. DIVIDE & CONQUER / DECOMPOSITION STRATEGIES
====================================================================

- Divide by midpoint in index space strategy
- Divide by median in value space strategy
- Divide by pivot element strategy
- Randomized pivot partition strategy
- Divide by centroid (tree) strategy
- Divide by separator (graph) strategy (rare)
- Divide by blocks (sqrt blocks) strategy
- Divide by bit (MSB splitting) strategy
- Divide by time/queries (offline) strategy
- Divide by dimension (2D/3D) strategy
- Divide-and-conquer on answer space strategy
- Divide-and-conquer DP optimization strategy
- CDQ on inversions/dominance strategy
- CDQ on time (updates/queries) strategy
- D&C over convolution ranges strategy
- Split into independent components strategy
- Condense SCC then solve DAG strategy
- Decompose into biconnected components strategy
- Block-cut tree solve strategy
- SPQR tree solve strategy (rare)
- Tree centroid decomposition solve strategy
- Heavy-light decomposition solve strategy
- DSU-on-tree (small-to-large) strategy
- Rerooting decomposition strategy
- Tree flattening via Euler tour strategy

====================================================================
F. BINARY SEARCH / PARAMETRIC STRATEGIES
====================================================================

- Binary search on feasibility strategy
- Binary search on minimal maximum (minimax) strategy
- Binary search on maximal minimum strategy
- Binary search on threshold count strategy
- Binary search on monotone DP/greedy check strategy
- Parallel binary search strategy (offline)
- Parametric search with dynamic structure strategy (advanced)
- Ternary search on unimodal function strategy
- Discrete ternary / hill-climb strategy
- Fractional binary search (precision) strategy
- Search on Lagrange multiplier (rare)
- Aliens trick (Lagrangian DP) strategy (advanced)

====================================================================
G. DP STATE DESIGN STRATEGIES
====================================================================

- DP by prefix length strategy
- DP by suffix length strategy
- DP by interval [l,r] strategy
- DP by subsequence endpoints strategy
- DP by last choice strategy
- DP by count of chosen elements strategy
- DP by remaining capacity/resource strategy
- DP by current balance (stack depth) strategy
- DP by bitmask of used items strategy
- DP by subset partition strategy
- DP by connected component mask strategy (rare)
- DP by “number of ways” counting strategy
- DP by “minimum cost” optimization strategy
- DP by “feasibility boolean” strategy
- DP by “expected value” strategy
- DP by “probability distribution” strategy
- DP on DAG topological order strategy
- DP on tree postorder strategy
- DP on tree with parent state strategy
- DP on tree rerooting strategy
- DP on tree with heavy child reuse strategy
- DP on digits (digit DP) strategy
- DP on positions with tight/loose flags strategy
- DP on automaton states strategy (string DP)
- DP on parity/bit states strategy
- DP on compressed coordinates strategy
- DP with meet-in-the-middle state split strategy
- DP with BFS as shortest path on state graph strategy
- DP with monotone queue optimization strategy
- DP with convex hull trick optimization strategy
- DP with divide-and-conquer optimization strategy
- DP with Knuth optimization strategy
- DP with SMAWK/Monge optimization strategy (advanced)
- DP with bitset acceleration strategy
- DP with SOS transform strategy
- DP with subset convolution strategy
- DP with inclusion–exclusion integration strategy
- DP with “store only last layer” rolling strategy
- DP with “store sparse states only” strategy

====================================================================
H. DP CORRECTNESS / STRUCTURE STRATEGIES
====================================================================

- Prove optimal substructure strategy
- Prove overlapping subproblems strategy
- Identify monotone opt index strategy
- Identify quadrangle inequality strategy (Knuth)
- Identify Monge array property strategy
- Identify convex hull maintainable lines strategy
- Identify monotonic queue applicable cost form strategy
- Identify bitset convolution applicable transitions strategy
- Identify linear recurrence form strategy
- Identify Markov property strategy
- Identify independence enabling factorization strategy
- Decompose state into independent components strategy

====================================================================
I. GRAPH MODELING STRATEGIES (GENERAL)
====================================================================

- Model entities as nodes strategy
- Model constraints as edges strategy
- Model states as nodes (state graph) strategy
- Layered graph construction strategy
- Time-expanded graph strategy
- Difference constraints graph strategy
- Build bipartite graph from constraints strategy
- Build flow network from capacity constraints strategy
- Build circulation with demands from lower bounds strategy
- Convert “minimize max” to shortest path/flow strategy
- Convert “choose items with conflicts” to matching/flow strategy
- Convert “feasible ordering” to topological constraints strategy
- Convert “equivalence relations” to DSU strategy
- Convert “minimum removals” to max matching/min vertex cover strategy
- Convert “min cut” interpretation strategy
- Dualize via max-flow min-cut reasoning strategy
- Use residual graph reachability strategy
- Use potentials for reduced costs strategy (min cost flow)
- Condense SCC to DAG strategy
- Use bridges/articulation to split problem strategy
- Convert tree to rooted tree strategy
- Use LCA to answer path constraints strategy
- Use HLD to support path queries strategy
- Use centroid decomposition to support distance queries strategy
- Use virtual tree for subset-of-nodes queries strategy

====================================================================
J. SPECIFIC GRAPH STRATEGY FAMILIES
====================================================================

- Connectivity via DSU strategy
- Offline connectivity via rollback DSU strategy
- Dynamic connectivity via divide&conquer on time strategy (advanced)
- Shortest path with nonnegative weights strategy
- Shortest path with 0/1 weights strategy
- Shortest path with small integer weights strategy
- Shortest path with negative edges strategy
- Detect negative cycle strategy
- Multi-source shortest path strategy
- All-pairs shortest path on small n strategy
- MST via sorting edges strategy
- Second-best MST reasoning strategy
- Minimum arborescence modeling strategy (rare)
- Maximum matching modeling strategy
- Min vertex cover in bipartite via maxflow strategy
- Min path cover in DAG via matching strategy
- Edge-disjoint paths via flow strategy
- Node-splitting to model vertex capacities strategy
- Lower-bound edges -> demands transform strategy
- Min-cost flow via potentials strategy
- Gomory-Hu tree for all-pairs mincut strategy (rare)
- Dominator tree for flow/CFG-like constraints strategy (rare)

====================================================================
K. STRING / TEXT STRATEGIES
====================================================================

- Prefix-function/KMP modeling strategy
- Z-function modeling strategy
- Rolling hash compare strategy
- Double hash collision-avoid strategy
- Suffix array for ordering substrings strategy
- LCP use for range queries strategy
- Suffix automaton for distinct substrings strategy
- Aho-Corasick for multi-pattern strategy
- Palindromic tree for palindrome decomposition strategy
- Manacher for palindrome radius strategy
- Minimal rotation / Booth strategy
- String DP with automaton states strategy
- Edit-distance style DP strategy
- Periodicity / border exploitation strategy
- Small alphabet bitset trick strategy
- Offline queries on strings via suffix structure strategy

====================================================================
L. DATA-STRUCTURE-DRIVEN STRATEGIES
====================================================================

- Maintain prefix aggregates strategy
- Maintain difference array under range updates strategy
- Coordinate compression strategy
- Sweep-line with ordered set strategy
- Event sorting + active structure strategy
- Fenwick for prefix sums under updates strategy
- Segment tree for range query/update strategy
- Lazy propagation strategy
- Implicit segment tree for sparse coords strategy
- Persistent segment tree for offline kth/order stats strategy
- Treap/BBST for sequence operations strategy
- Implicit treap for splits/merges strategy
- Li Chao for dynamic line container strategy
- Convex hull trick lines sorted strategy
- Sparse table for static RMQ strategy
- DSU on tree for subtree query aggregation strategy
- Mo’s algorithm reorder queries strategy
- Mo’s with modifications strategy (advanced)
- Bitset as compressed DP state strategy
- Wavelet tree for k-th in range strategy (advanced)
- Merge sort tree for offline 2D queries strategy

====================================================================
M. OFFLINE / QUERY REORDERING STRATEGIES
====================================================================

- Sort queries by right endpoint strategy
- Sort by left endpoint strategy
- Sort by time in updates strategy
- Offline prefix processing strategy
- Offline sweep line by coordinate strategy
- Offline divide & conquer on time strategy
- Parallel binary search on answers strategy
- Mo’s ordering strategy
- CDQ dominance offline strategy
- Sort + BIT for inversion-like counts strategy
- Coordinate compress + offline events strategy
- Offline rebuild in blocks (sqrt rebuild) strategy

====================================================================
N. MATHEMATICAL STRATEGIES (NUMBER THEORY)
====================================================================

- Reduce problem modulo M strategy
- Normalize negative modulo strategy
- Precompute factorials/inverses strategy
- Use gcd structure to simplify strategy
- Use prime factorization to convert multiplicative constraints strategy
- Use SPF sieve for many factorizations strategy
- Enumerate divisors to transform constraints strategy
- Convert to CRT system strategy
- Use Euler totient for cycle length strategy
- Use Fermat for inverse mod prime strategy
- Use extended Euclid for inverse mod composite strategy
- Use Möbius inversion to invert sums strategy
- Use divisor-sum convolution strategy
- Use multiplicative function decomposition strategy
- Use discrete log reduction strategy (rare)
- Use primitive roots to parameterize residues strategy (rare)
- Use NTT when convolution under mod prime is needed strategy (advanced)

====================================================================
O. MATHEMATICAL STRATEGIES (COMBINATORICS)
====================================================================

- Count by direct construction strategy
- Count by complement strategy
- Count by casework partition strategy
- Count via inclusion–exclusion strategy
- Count via DP-on-structure strategy
- Count via recurrences strategy
- Count via bijection strategy
- Count via double counting strategy
- Count via symmetry quotient strategy (Burnside) 
- Count via Polya enumeration strategy (rare)
- Use Catalan templates strategy
- Use Stirling/Bell templates strategy (rare)
- Use generating functions to encode counts strategy
- Use convolution to combine independent choices strategy
- Use subset convolution strategy (advanced)
- Use binomial transform strategy (advanced)

====================================================================
P. MATHEMATICAL STRATEGIES (PROBABILITY)
====================================================================

- Use linearity of expectation strategy
- Use indicator variables strategy
- Use conditional expectation strategy
- Use law of total probability strategy
- Use Bayes decomposition strategy
- Use Markov property strategy
- Use DP for expected steps strategy
- Use absorbing Markov chain strategy (advanced)
- Use random walk symmetry strategy
- Use coupling/comparison reasoning strategy (rare)

====================================================================
Q. MATHEMATICAL STRATEGIES (LINEAR ALGEBRA)
====================================================================

- Model constraints as linear equations strategy
- Use Gaussian elimination feasibility strategy
- Use rank to detect uniqueness strategy
- Use xor-basis over GF(2) strategy
- Use matrix exponentiation for transitions strategy
- Use linear recurrence + exponentiation strategy
- Use determinant-based counting strategy (rare)
- Use Kirchhoff matrix-tree theorem strategy (rare but WF)
- Use min-plus matrix multiplication awareness strategy (rare)

====================================================================
R. MATHEMATICAL STRATEGIES (GEOMETRY)
====================================================================

- Replace geometry with vector operations strategy
- Use orientation (ccw) as primitive strategy
- Segment intersection via orientation strategy
- Use convex hull + queries strategy
- Use rotating calipers for diameter/width strategy
- Use sweep line for intersections strategy
- Use half-plane intersection strategy (advanced)
- Use point-in-polygon winding/ray strategy
- Use polygon area shoelace strategy
- Use Minkowski sum for distance/containment strategy (advanced)
- Use coordinate transform to simplify constraints strategy
- Use integer geometry to avoid eps strategy
- Use eps and robust comparisons strategy
- Use angle sorting strategy
- Use projection/dot to compare distances strategy

====================================================================
S. CONSTRUCTIVE STRATEGIES
====================================================================

- Build output directly from constraints strategy
- Build from extremes inward strategy
- Build greedily while maintaining invariants strategy
- Build by reverse process (undo operations) strategy
- Build minimal witness then extend strategy
- Build maximal then prune strategy
- Build by local patching strategy
- Build by “pairing” strategy
- Build by “cycle stitching” strategy (graphs)
- Build by “component merging” strategy
- Build by “balancing counts” strategy

====================================================================
T. PROOF-DRIVEN / CORRECTNESS STRATEGIES
====================================================================

- Exchange argument strategy
- Cut argument strategy
- Invariant maintenance strategy
- Monovariant descent strategy
- Extremal principle strategy
- Minimal counterexample strategy
- Induction on size/steps strategy
- Potential method strategy
- Amortized accounting strategy
- Symmetry argument strategy
- Uniqueness argument strategy
- Lower bound argument strategy
- Feasibility + minimality constructive proof strategy

====================================================================
U. RANDOMIZATION / PROBABILISTIC ALGO STRATEGIES
====================================================================

- Random shuffle to avoid worst-case strategy
- Random hashing to avoid hacks strategy
- Monte Carlo estimate strategy
- Las Vegas retry-until-correct strategy
- Random pivot partition strategy
- Random sampling to reduce candidates strategy
- Randomized balancing trees strategy
- Randomized rounding awareness strategy (rare)

====================================================================
V. ADVANCED / RESEARCH-LEANING STRATEGIES
====================================================================

- Persistent structure to time-travel queries strategy
- Rollback DSU for offline dynamics strategy
- Retroactive DS reasoning strategy (rare)
- Cache-oblivious layout strategy (rare)
- Algebraic transform acceleration strategy (FWT/NTT/FFT)
- Information-theoretic lower bound strategy
- Decision-tree complexity reasoning strategy
- Planar duality strategy (rare)
- Parametric flow strategy (rare)
- Kinetic structure reasoning strategy (rare)
- Submodular optimization awareness strategy (rare)
- Matroid greedy applicability-check strategy (rare but appears)
- Divide & conquer + FFT polynomial multiplications strategy (advanced)
- Bitset convolution / FWT XOR-AND-OR strategy (advanced)
