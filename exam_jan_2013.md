**Algorithm Design - Exam Jan 23th 2013**
# 1
- n*m
- T(n)=T(n-1)+T(n-2)
- T(0)=c

# 2
- Pioneer
- Read input and sort land by price increasingly. Pick as many from start of list as possible.
- nlog(n)

# 3
- Cheap travel
- Airports are vertices, connections are edges and prices are weights on the edges
- Dijkstra
- In original parameters: O(n log(n))

# 4
- Area
-   k = #area, C = budget
    OPT(0,C) = 0      OPT(k,0) = 0 
    OPT(k,C) = max{vk + OPT(k-1, C-Ck), OPT(k-1,C)}
- O(kC), space = k**2

# 5
- Rounding
-   Network flow - connect each floating point number to all the integers it can be rounded to. Connect *s* to all floats and,
    connect all integers to *t*
-   If max flow != n | print impossible
- Running time = Ford Fulkerson (bounded in original parameters)

# 6
- yes
- eg. list of edges in the spanning tree
-   bfs to check that the spanning tree is acyclic and connected 
    check if k vertices are only listed once in the spanning tree

# 7
- P1 = Leaves (unsolved by other questions)
- P2 = Hamiltonian Path
- P2 <=p P1
- 
HP(G) {
    k=2
    Lesves(G,k)
}
