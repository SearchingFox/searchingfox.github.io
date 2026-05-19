---
up:
  - "[[Cellular Automata]]"
---
# Abelian sandpile model
- [Abelian sandpile model - Wikipedia](https://en.wikipedia.org/wiki/Abelian_sandpile_model)
## Definition (undirected finite multigraphs)
To generalize the sandpile model from the rectangular grid of the standard square lattice to an arbitrary undirected finite multigraph $G=(V,E)$, a special vertex $s in V$ called the _sink_ is specified that is not allowed to topple. A _configuration_ (state) of the model is then a function $z : V backslash {s} -> NN_0$ counting the non-negative number of grains on each non-sink vertex. A non-sink vertex $v in V backslash { s }$ with $z(v) >= deg(v)$ is unstable; it can be toppled, which sends one of its grains to each of its (non-sink) neighbors:
$$z(v) -> z(v) - deg(v)$$
$$z(u) -> z(u)+1 quad forall u ~ v, u != s$$

The cellular automaton then progresses as before, i.e. by adding, in each iteration, one particle to a randomly chosen non-sink vertex and toppling until all vertices are stable.

The definition of the sandpile model given above for finite rectangular grids $Gamma subset ZZ^2$ of the standard square lattice $ZZ^2$ can then be seen as a special case of this definition: consider the graph $G = (V, E)$ which is obtained from $Gamma$ by adding an additional vertex, the sink, and by drawing additional edges from the sink to every boundary vertex of Γ ![{\displaystyle \Gamma }](https://wikimedia.org/api/rest_v1/media/math/render/svg/4cfde86a3f7ec967af9955d0988592f0693d2b19) such that the [degree](https://en.wikipedia.org/wiki/Degree_(graph_theory)) of every non-sink vertex of $G$ is four. In this manner, also sandpile models on non-rectangular grids of the standard square lattice (or of any other lattice) can be defined: Intersect some bounded subset $S$ of $RR^2$ with $ZZ^2$. [Contract every edge](https://en.wikipedia.org/wiki/Edge_contraction) of $ZZ^2$ whose two endpoints are not in $S sect ZZ^2$. The single remaining vertex outside of $S sect ZZ^2$ then constitutes the sink of the resulting sandpile graph.
