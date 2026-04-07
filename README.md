# MinLA Problem

## Problem definition

The *Minimum Linear Arrangement* problem (MinLA) was first stated by Harper in [1]. His aim was to design error-correcting codes with minimal average absolute errors on certain classes of graphs. Later, in the 1970's MinLA was used as an abstract model of the placement phase in VLSI layout, where vertices of the graph represented modules and edges represented interconnections. In this case, the cost of the arrangement measures the total wire length [2]. MinLA arises also in other research fields like biological applications, graph drawing, software diagram layout and job scheduling [3,4].

The MinLA problem can be defined formally as follows. Let $G(V,E)$ be a finite undirected graph, where $|V|=n$ defines the set of vertices and $E$ is the set of edges. Given a one-to-one labeling function $\varphi :V\rightarrow \\{1..n\\}$, called a linear arrangement, the total edge length (cost) for $G$ with respect to the arrangement $\varphi$ is defined according to

$$LA(G,\varphi )=\sum\limits_{(u,v)\in E}|\varphi (u)-\varphi (v)|,$$ 

where $|\varphi (u)-\varphi (v)|$ is called the linear distance, and $\varphi (u)$ denotes the label associated to vertex $u$.

Then the MinLA problem consists in finding a linear arrangement $\varphi^\ast$ for a given graph $G$ so that $LA(G,\varphi^\ast)$ is minimized.


## Benchmark instances

- **Small and Medium Instances (smallInstances.tgz).** This is a test-suite originally proposed by Jordi Petit and used later by other authors. It includes 21 graphs from 6 different families: Uniform random, geometric random, graphs with known optima, finite element discretizations, VLSI design and graph drawing competitions. Their number of vertices is between 62 and 9800.
- **Big Instances (bigInstances.tgz).** The second test-suite is composed of 9 very large graphs from finite element discretizations, obtained from the publicly available collections of George Karypis and Francois Pellegrini. These graphs were first used by Yehuda Koren and David Harel. Their number of vertices is between 78136 and 1017253.


## Computational results

The results reported in this section were obtained with the Two-Stage Simulated Annealing Algorithm (TSSA) algorithm described in the following paper:

*An Effective Two-Stage Simulated Annealing Algorithm for the Minimum Linear Arrangement Problem.* Eduardo Rodriguez-Tello, Jin-Kao Hao and Jose Torres-Jimenez, Computers & Operations Research, 35(10):3331-3346, Elsevier Octobre 2008, DOI: [10.1016/j.cor.2007.03.001](https://doi.org/10.1016/j.cor.2007.03.001).

- **Final Permutations (finalPermutations.tgz).** This file contains the best final permutations found using our TSSA algorithm.

- **Detailed Results (detailedResultsCOR2007.zip).** This file contains the detailed execution data from our experiments with the TSSA algorithm.


## References

1. L. H. Harper. Optimal assignment of numbers to vertices. SIAM Journal on Applied Mathematics,
12(1):131–135, 1964.
2. D. Adolphson and T. C. Hu. Optimal linear ordering. SIAM Journal on Applied Mathematics,
25(3):403–423, 1973.
3. J. Diaz, J. Petit, and M. Serna. A survey of graph layout problems. ACM Computing Surveys,
34(3):313–356, 2002.
4. Y.-L. Lai and K. Williams. A survey of solved problems and applications on bandwidth, edgesum,
and profile of graphs. Graph Theory, 31:75–94, 1999.

