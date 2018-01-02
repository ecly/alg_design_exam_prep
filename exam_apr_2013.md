Algorithm Design - Exam April 4th 2013 
# 1
- Zompf
- Sort decreasing order - pick coins from start to end or till the value of the the coin is less than the exchange rate.
- n log n

# 2
- Crisis
- Vertices Banks, Edges: Dependencies, Graph is directed | a-\>b | b depends on a
- BFS - identify connected component
- O(m) | #nodes <= 2m because at most 2 new nodes per line.

# 3
- Neighbours
-   OPT(0) = 0
    OPT(1) = val(1)
    OPT(K) = max(OPT(k-1), OPT(k-2)+val(k))
-   Time = O(n), Space = O(n)
    Time recurrence relation: T(k) = 1+T(k-1)+T(k-2)

# 4
- Lockout 
-   Bipartite matching graph layout | n nodes on the left | m nodes on right
    S connected to children with capacity 1, parents connected to t with their capacity.
    Connected whildren with parents based on the preferences.
-   Use Ford-Fulkerson which has running time BFS(m+n) * Capacity | Represent it based on given parameters.
    O(n^2m)

# 5
- It is not a decision problem as we are not answering yes/no. - If we want it as a decision problem.
    Can all the children be taken care of? ---- Is MaxFlow == N?
- Certificate is the output of an execution that we can use to verify the correctness of the solution.
-   Every child has a host
    Hosts do not exceed the capacity.
    No host/child preferences are broken.
    -- This n*m preferences, check for n children. O(n*(n*m))

# 6
- Stacks (P1)
- P2 <= P1 (Reduce an NP-hard problem to our problem) | Subset sum problem. Where the sum we're aiming for is (total sum/2)
- P2 <= P1 - We want to reduce SS to Stack - SS <=p Stacks - such that if we find a polynomial time solution for Stacks, we would solve SS.
    Which means we would solve NP-hardness.
-   Add an extra coin with value of the total sum and Stacks will put that coin in one stack, and the rest in the other.
    If it then returns true then we've won.
