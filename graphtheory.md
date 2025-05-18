# Graph Theory Questions and Answers

## 🔹 Matchings & Hall’s Theorem

**5-Marks:**

1. Define the terms: matching, maximal matching, maximum matching.

    *Answer:*
    *   **Matching:** A matching in a graph is a set of edges with no shared vertices.
    *   **Maximal Matching:** A matching that cannot be extended by adding an edge.
    *   **Maximum Matching:** A matching with the largest possible number of edges.

2. State Hall’s Marriage Theorem and Hall’s condition with a simple example.

    *Answer:*
    *   **Hall's Marriage Theorem:** A bipartite graph G = (A ∪ B, E) has a matching that saturates A if and only if for every subset S of A, |N(S)| ≥ |S|, where N(S) is the neighborhood of S.
    *   **Hall's Condition:** For every subset S of A, the number of vertices in B adjacent to at least one vertex in S is greater than or equal to the number of vertices in S.
    *   **Example:** Consider A = {a1, a2, a3} and B = {b1, b2, b3}. If a1 is connected to b1, a2 is connected to b1 and b2, and a3 is connected to b2 and b3, then Hall's condition holds. For instance, if S = {a1, a2}, N(S) = {b1, b2}, and |N(S)| = 2 ≥ |S| = 2.

3. Differentiate between maximal and perfect matching with diagrams.

    *Answer:*
    *   **Maximal Matching:** A matching is maximal if no more edges can be added without violating the matching property (i.e., no shared vertices).
        *   *Diagram Description:* Imagine a graph where some vertices are matched, and you can't add any more edges between unmatched vertices without making two edges share a vertex.
    *   **Perfect Matching:** A matching is perfect if every vertex in the graph is matched.
        *   *Diagram Description:* Imagine a graph where every vertex is part of an edge in the matching. There are no unmatched vertices.
    *   **Difference:** A perfect matching is always a maximal matching, but a maximal matching is not necessarily a perfect matching. A maximal matching stops when no more edges can be added, while a perfect matching requires all vertices to be matched.

**10-Marks:**

1. Explain Hall’s Theorem in detail. Prove it using a bipartite graph.

    *Answer:*
    *   **Hall's Theorem:** Hall's Theorem, also known as the Marriage Theorem, provides a necessary and sufficient condition for the existence of a matching in a bipartite graph that saturates one part of the graph.
    *   **Detailed Explanation:** Let G = (A ∪ B, E) be a bipartite graph with parts A and B. Hall's Theorem states that there exists a matching that saturates A (i.e., every vertex in A is matched to a vertex in B) if and only if for every subset S of A, |N(S)| ≥ |S|, where N(S) is the neighborhood of S (the set of vertices in B adjacent to at least one vertex in S).
    *   **Proof:**
        *   **Necessity:** Suppose there is a matching M that saturates A. For any subset S of A, the vertices in S are matched to distinct vertices in N(S) by M. Therefore, |N(S)| ≥ |S|.
        *   **Sufficiency:** Suppose that for every subset S of A, |N(S)| ≥ |S|. We want to show that there exists a matching that saturates A. We can prove this by induction on |A|.
            *   Base case: If |A| = 1, then the condition |N(S)| ≥ |S| implies that the single vertex in A has at least one neighbor in B, so a matching exists.
            *   Inductive step: Assume the theorem holds for all subsets A' of A with |A'| < |A|. Consider two cases:
                *   Case 1: For every subset S of A with 1 ≤ |S| < |A|, |N(S)| > |S|. Choose any vertex a in A and match it to a neighbor b in B. Now consider the bipartite graph G' = (A' ∪ B', E') where A' = A - {a}, B' = B - {b}, and E' is the set of edges in G with endpoints in A' and B'. For any subset S of A', |N(S)| ≥ |S| in G', so by the induction hypothesis, there exists a matching in G' that saturates A'. Adding the edge (a, b) to this matching gives a matching in G that saturates A.
                *   Case 2: There exists a subset S of A with 1 ≤ |S| < |A| such that |N(S)| = |S|. By the induction hypothesis, there exists a matching in the bipartite graph induced by S and N(S) that saturates S. Now consider the bipartite graph G'' = (A'' ∪ B'', E'') where A'' = A - S, B'' = B - N(S), and E'' is the set of edges in G with endpoints in A'' and B''. For any subset T of A'', |N(T)| ≥ |T| in G''. Thus, by the induction hypothesis, there exists a matching in G'' that saturates A''. Combining this matching with the matching in the bipartite graph induced by S and N(S) gives a matching in G that saturates A.
    *   Therefore, by induction, Hall's Theorem holds.

2. Discuss the difference between perfect, maximal matchings and augmenting paths. Use Berge’s Theorem.

    *Answer:*
    *   **Perfect Matching:** A matching where every vertex in the graph is matched.
    *   **Maximal Matching:** A matching where no more edges can be added without violating the matching property.
    *   **Augmenting Path:** A path that starts and ends at unmatched vertices and alternates between edges not in the matching and edges in the matching.
    *   **Berge's Theorem:** A matching M in a graph G is a maximum matching if and only if there is no augmenting path with respect to M.
    *   **Difference:**
        *   A perfect matching is a special case of a maximal matching where all vertices are matched.
        *   A maximal matching is a matching that cannot be extended, but it may not include all vertices.
        *   An augmenting path is a tool used to find a maximum matching. If an augmenting path exists, the matching is not maximum, according to Berge's Theorem. By using the augmenting path to increase the size of the matching, we can get closer to a maximum matching.

## 🔹 Chromatic Number & Coloring

**5-Marks:**

1. Define the chromatic number of a graph with a suitable example.

    *Answer:*
    *   **Chromatic Number:** The chromatic number of a graph G, denoted χ(G), is the minimum number of colors needed to color the vertices of G such that no two adjacent vertices share the same color.
    *   **Example:** Consider a complete graph K3 (a triangle). Each vertex is adjacent to the other two, so each vertex must have a different color. Therefore, the chromatic number of K3 is 3, i.e., χ(K3) = 3.

2. What is the chromatic number of $K_n$, a path graph, and a cycle graph?

    *Answer:*
    *   **Complete Graph (Kn):** The chromatic number of a complete graph Kn is n, i.e., χ(Kn) = n.
    *   **Path Graph:** The chromatic number of a path graph is 2, i.e., χ(Path) = 2.
    *   **Cycle Graph:** The chromatic number of a cycle graph with an even number of vertices is 2, and with an odd number of vertices is 3.

**10-Marks:**

1. Describe the Greedy Coloring Algorithm with steps and an example.

    *Answer:*
    *   **Greedy Coloring Algorithm:**
        1.  Order the vertices of the graph in some arbitrary order: v1, v2, ..., vn.
        2.  Assign the first vertex v1 the first color (color 1).
        3.  For each subsequent vertex vi, consider the colors already used by its neighbors.
        4.  Assign vi the smallest-numbered color that is not used by any of its neighbors.
    *   **Example:** Consider a graph with vertices A, B, C, D and edges AB, BC, CD, DA, AC.
        1.  Order: A, B, C, D
        2.  A: Color 1
        3.  B: Color 2 (neighbor A has color 1)
        4.  C: Color 3 (neighbors A has color 1, B has color 2)
        5.  D: Color 2 (neighbors C has color 3, A has color 1)
        *   The greedy coloring algorithm uses 3 colors for this graph.

2. Prove the bound: $\chi(G) \leq \Delta(G) + 1$.

    *Answer:*
    *   **Proof:**
        *   Let G be a graph with maximum degree Δ(G). We want to show that χ(G) ≤ Δ(G) + 1.
        *   We can prove this by induction on the number of vertices in G.
            *   Base case: If G has only one vertex, then χ(G) = 1 ≤ Δ(G) + 1.
            *   Inductive step: Assume the bound holds for all graphs with fewer than n vertices. Let G be a graph with n vertices. Remove a vertex v from G to obtain a graph G' with n-1 vertices. By the induction hypothesis, χ(G') ≤ Δ(G') + 1. Since Δ(G') ≤ Δ(G), we have χ(G') ≤ Δ(G) + 1.
            *   Now add the vertex v back to G. The vertex v has at most Δ(G) neighbors. Therefore, there is at least one color available to color v from the set of Δ(G) + 1 colors. Thus, χ(G) ≤ Δ(G) + 1.
        *   Therefore, by induction, the bound holds.

3. Derive and explain the inequality $\chi(G) \cdot \alpha(G) \geq n(G)$.

    *Answer:*
    *   **Derivation and Explanation:**
        *   Let G be a graph with chromatic number χ(G), independence number α(G), and n(G) vertices.
        *   We want to show that χ(G) ⋅ α(G) ≥ n(G).
        *   Consider an optimal coloring of G with χ(G) colors. Let V1, V2, ..., Vχ(G) be the color classes (i.e., the sets of vertices with the same color).
        *   Since each Vi is an independent set, |Vi| ≤ α(G) for all i.
        *   The total number of vertices in G is n(G) = |V1| + |V2| + ... + |Vχ(G)|.
        *   Since |Vi| ≤ α(G) for all i, we have n(G) ≤ χ(G) ⋅ α(G).
        *   Therefore, χ(G) ⋅ α(G) ≥ n(G).

## 🔹 Planar Graphs & Euler’s Formula

**5-Marks:**

1. State Euler’s formula for connected planar graphs.

    *Answer:*
    *   **Euler's Formula:** For aConnected planar graph, Euler's formula states that:  v - e + f = 2, where v is the number of vertices, e is the number of edges, and f is the number of faces.

2. Use Euler’s inequality to verify whether a graph with 7 vertices and 17 edges is planar.

    *Answer:*
    *   **Euler's Inequality:** For a planar graph, e ≤ 3v - 6.
    *   Given v = 7 and e = 17, we check if the inequality holds:
    *   17 ≤ 3(7) - 6
    *   17 ≤ 21 - 6
    *   17 ≤ 15
    *   Since 17 is not less than or equal to 15, the graph is not planar.

3. What is the condition for planarity in terms of vertices and edges?

    *Answer:*
    *   **Condition for Planarity:** For a planar graph with v vertices and e edges, the following conditions must hold:
        *   e ≤ 3v - 6 (for v ≥ 3)
        *   e ≤ 2v - 4 (if the graph is triangle-free, i.e., has no cycles of length 3)

**10-Marks:**

1. Prove Euler’s Formula for connected and disconnected planar graphs. Add examples.

    *Answer:*
    *   **Euler's Formula for Connected Planar Graphs:**
        *   v - e + f = 2, where v is the number of vertices, e is the number of edges, and f is the number of faces.
        *   **Proof:** We can prove this by induction on the number of faces.
            *   Base case: If f = 1, then the graph is a tree, and v - e + 1 = 2, so v - e = 1, which is true for a tree.
            *   Inductive step: Assume the formula holds for all connected planar graphs with fewer than f faces. Let G be a connected planar graph with f faces. Choose an edge e that is not a bridge. Removing e merges two faces into one, so the resulting graph G' has f - 1 faces. By the induction hypothesis, v' - e' + f' = 2, where v' = v, e' = e - 1, and f' = f - 1. Therefore, v - (e - 1) + (f - 1) = 2, so v - e + 1 + f - 1 = 2, so v - e + f = 2.
        *   **Example:** Consider a square. It has 4 vertices, 4 edges, and 1 face (plus the outer face). So 4 - 4 + 2 = 2.
    *   **Euler's Formula for Disconnected Planar Graphs:**
        *   v - e + f = k + 1, where v is the number of vertices, e is the number of edges, f is the number of faces, and k is the number of connected components.
        *   **Proof:** Let G be a disconnected planar graph with k connected components. Let vi, ei, and fi be the number of vertices, edges, and faces in the ith connected component. Then, for each connected component, vi - ei + fi = 2. Summing over all k components, we get (v1 + v2 + ... + vk) - (e1 + e2 + ... + ek) + (f1 + f2 + ... + fk) = 2k. Let v = v1 + v2 + ... + vk, e = e1 + e2 + ... + ek, and f = (f1 - 1) + (f2 - 1) + ... + (fk - 1) + 1 (we subtract 1 from each fi because the outer face is counted in each component, and we add 1 to account for the single outer face of the entire disconnected graph). Then, v - e + f = 2k - (k - 1) = k + 1.
        *   **Example:** Consider two disjoint squares. Each square has 4 vertices, 4 edges, and 2 faces (including the outer face). So, v = 8, e = 8, f = 4. Then 8 - 8 + 4 = 4 = 2 + 1, where k = 2 is the number of connected components.

2. Check whether $K_5$ and $K_{3,3}$ are planar using Euler’s inequality.

    *Answer:*
    *   **K5:**
        *   K5 has 5 vertices and 10 edges.
        *   Euler's inequality: e ≤ 3v - 6
        *   10 ≤ 3(5) - 6
        *   10 ≤ 15 - 6
        *   10 ≤ 9
        *   Since 10 is not less than or equal to 9, K5 is not planar.
    *   **K3,3:**
        *   K3,3 has 6 vertices and 9 edges.
        *   Since K3,3 is bipartite, it has no cycles of length 3, so we use e ≤ 2v - 4.
        *   9 ≤ 2(6) - 4
        *   9 ≤ 12 - 4
        *   9 ≤ 8
        *   Since 9 is not less than or equal to 8, K3,3 is not planar.

3. Derive the inequality $e \leq 3n - 6$ for planar graphs.

    *Answer:*
    *   **Derivation:**
        *   Let G be a planar graph with v vertices, e edges, and f faces, where v ≥ 3.
        *   Each face is bounded by at least 3 edges.
        *   Each edge is part of at most 2 faces.
        *   Therefore, 3f ≤ 2e.
        *   By Euler's formula, v - e + f = 2.
        *   So, f = 2 + e - v.
        *   Substituting this into 3f ≤ 2e, we get 3(2 + e - v) ≤ 2e.
        *   6 + 3e - 3v ≤ 2e
        *   e ≤ 3v - 6.

## 🔹 Dual Graphs

**5-Marks:**

1. Define the dual of a planar graph with an example.

    *Answer:*
    *   **Dual Graph:** Given a planar graph G, its dual graph G* is constructed as follows:
        *   For each face f in G, create a vertex f* in G*.
        *   For each edge e in G separating two faces f1 and f2, create an edge e* in G* connecting f1* and f2*.
    *   **Example:** Consider a square. It has 4 vertices, 4 edges, and 1 face (plus the outer face). The dual graph has two vertices (one for the inner face, one for the outer face) and 4 edges connecting them.

2. What is the relationship between the number of faces and dual vertices?

    *Answer:*
    *   **Relationship:** The number of faces in a planar graph G is equal to the number of vertices in its dual graph G*. In other words, f(G) = v(G*).

**10-Marks:**

1. Explain the construction of the dual of a planar graph. Give an illustrative example.

    *Answer:*
    *   **Construction of the Dual Graph:**
        1.  **Vertices:** For each face f in the planar graph G, create a vertex f* in the dual graph G*.
        2.  **Edges:** For each edge e in G, if e separates two faces f1 and f2, then create an edge e* in G* connecting the corresponding vertices f1* and f2*. If e is an edge on the boundary of the outer face, then e* is a self-loop on the vertex corresponding to the outer face.
    *   **Illustrative Example:**
        *   Consider a planar graph G consisting of a square with one diagonal.
        *   G has 4 vertices, 5 edges, and 3 faces (two triangles and the outer face).
        *   The dual graph G* has 3 vertices (one for each face of G).
        *   The dual graph has 5 edges, each corresponding to an edge in G.
        *   Two edges connect the vertices corresponding to the two triangles, and the remaining three edges connect each triangle to the vertex corresponding to the outer face.

2. Show how the dual graph preserves planarity and explain with a diagram.

    *Answer:*
    *   **Preservation of Planarity:** The dual graph G* of a planar graph G is also planar. This is because the construction of the dual graph places a vertex inside each face of the original graph, and the edges of the dual graph follow the edges of the original graph. Therefore, the dual graph can be drawn without any edges crossing.
    *   **Explanation:** Since the dual graph is constructed by placing vertices inside the faces of the original graph and connecting them through the edges, the dual graph will always be planar.
    *   **Diagram Description:** Imagine a planar graph drawn on a plane. Now, inside each face, place a vertex. Connect these vertices through the edges of the original graph. You can see that the resulting graph (the dual graph) can also be drawn on the plane without any edges crossing.

## ✳️ Important Conceptual/Numerical Questions Faculty Might Ask

* Given a bipartite graph, determine if Hall’s condition holds and construct a perfect matching.

    *Answer:*
    *   **Determining if Hall's Condition Holds:**
        1.  Let G = (A ∪ B, E) be a bipartite graph.
        2.  For every subset S of A, find the neighborhood N(S) (the set of vertices in B adjacent to at least one vertex in S).
        3.  Check if |N(S)| ≥ |S| for all subsets S of A. If this condition holds for all S, then Hall's condition holds.
    *   **Constructing a Perfect Matching (if Hall's Condition Holds):**
        1.  If Hall's condition holds, then a perfect matching exists.
        2.  Use an algorithm like the Ford-Fulkerson algorithm or the Hopcroft-Karp algorithm to find a maximum matching.
        3.  If the size of the maximum matching is equal to |A| (or |B| if |A| = |B|), then the maximum matching is a perfect matching.
        4.  **Example:**
            *   Let A = {a1, a2, a3} and B = {b1, b2, b3}.
            *   Edges: a1b1, a2b1, a2b2, a3b2, a3b3
            *   Hall's condition holds.
            *   A perfect matching is: a1b1, a2b2, a3b3

* Use Greedy Coloring on a specific graph (provide adjacency or edge list).

    *Answer:*
    *   **Steps:**
        1.  Order the vertices of the graph in some arbitrary order.
        2.  Assign the first vertex the first color (color 1).
        3.  For each subsequent vertex, consider the colors already used by its neighbors.
        4.  Assign the vertex the smallest-numbered color that is not used by any of its neighbors.
    *   **Example:**
        *   Graph: Vertices A, B, C, D; Edges: AB, BC, CD, DA, AC
        *   Adjacency List: A: B, C, D; B: A, C; C: A, B, D; D: A, C
        *   Order: A, B, C, D
        *   A: Color 1
        *   B: Color 2 (neighbor A has color 1)
        *   C: Color 3 (neighbors A has color 1, B has color 2)
        *   D: Color 2 (neighbors A has color 1, C has color 3)
        *   Colors used: 3

* Prove that every tree is planar and has chromatic number 2.

    *Answer:*
    *   **Every Tree is Planar:**
        *   A tree is a connected graph with no cycles.
        *   Any tree can be drawn in the plane without any edges crossing.
        *   Therefore, every tree is planar.
    *   **Every Tree has Chromatic Number 2 (except for the trivial tree with one vertex):**
        *   We can prove this by induction on the number of vertices.
            *   Base case: A tree with 2 vertices has one edge and can be colored with 2 colors.
            *   Inductive step: Assume that every tree with n vertices has a chromatic number of 2. Let T be a tree with n+1 vertices. Remove a leaf (a vertex with degree 1) from T. The resulting graph T' is a tree with n vertices, so by the induction hypothesis, it has a chromatic number of 2. Now add the leaf back to T. Since the leaf has only one neighbor, we can color it with the color that is not used by its neighbor. Therefore, T has a chromatic number of 2.

* For a graph with 10 vertices and 24 edges, check if it’s planar using Euler’s formula.

    *Answer:*
    *   **Euler's Formula:** v - e + f = 2
    *   **Euler's Inequality:** e ≤ 3v - 6
    *   Given v = 10 and e = 24, we check if the inequality holds:
    *   24 ≤ 3(10) - 6
    *   24 ≤ 30 - 6
    *   24 ≤ 24
    *   Since 24 is less than or equal to 24, the graph may be planar. However, this is only a necessary condition, not a sufficient one. We cannot definitively say it is planar using only Euler's formula.

* Given a planar graph, draw its dual and explain the relationship between edges, faces, and vertices.

    *Answer:*
    *   **Drawing the Dual Graph:**
        1.  Given a planar graph G, for each face in G, place a vertex in the dual graph G*.
        2.  For each edge in G, draw an edge in G* connecting the vertices corresponding to the faces that the edge separates. If an edge is on the boundary of the outer face, draw a self-loop on the vertex corresponding to the outer face.
    *   **Relationship between Edges, Faces, and Vertices:**
        *   Let G be a planar graph and G* be its dual.
        *   The number of faces in G is equal to the number of vertices in G*: f(G) = v(G*).
        *   The number of vertices in G is equal to the number of faces in G*: v(G) = f(G*).
        *   The number of edges in G is equal to the number of edges in G*: e(G) = e(G*).
