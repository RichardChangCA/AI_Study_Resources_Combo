1. Youtube, Graph Convolutional Neural Networks, https://www.youtube.com/watch?v=Mf-mIRF3ao8 ,AI learns(GCN) structure(Graph) of data points. Irregular data structures. Adjacency Matrix in graph. Node classification: use label nodes to predict unable nodes. Graph classification: predict information about new graphs, based on labeled graphs. CNN: spatial invariance properties. Graph-Shifted Signal: idea from the DSP field, linear shift invariant filter can be represented as a polynomial of shifts.Youtube Linear Filters: https://www.youtube.com/watch?v=WeNpd_YEF6I ,blur filters, sharper filter. ECE course: Linearity, Shift Invariance: https://www.youtube.com/watch?v=xhDGX8nHAdg

GNN Tools: PyTorch Geometric, Graph Nets(TensorFlow), Deep Graph(easy for beginners)

2. Youtube, Graph Network, Siraj Raval. https://www.youtube.com/watch?v=bA261BF0bdk ,Simple intuitive introduction of GNN, Sample neighbourhood —> Aggregate feature information from neighbours —> Predict graph context and label using aggregated information.

3. CS224W: Machine Learning with Graphs Stanford/Fall 2019

Official Website: http://web.stanford.edu/class/cs224w/index.html

Video: http://snap.stanford.edu/class/cs224w-videos-2019/

Youtube Channel: https://www.youtube.com/watch?v=dD6LRgw_2mQ&list=PL1OaWjIc3zJ4xhom40qFY5jkZfyO5EDOZ&index=1

<b>Lecture 1: Properties of Networks and Random Graph Models</b>

Degree distribution, path, distance, the consequence in directed graphs: distance is not symmetric. Diameter: the maximum (shortest path) distance between any pair of nodes in a graph. Average path length. Clustering coefficient(for undirected graphs, how connected are i’s neighbours to each other? Average clustering coefficient, very useful for social networks), size of the largest connected component: largest set where any two vertices can be joined by a path(largest component=giant component). Random Graph Model( G_np: undirected graph on n nodes where each edge (u, v) appears i.i.d with probability p, G_nm: undirected graph with n nodes, and m edges picked uniformly at random), expansion alpha. In real world social network: high clustering coefficient and low diameter.(graph model with high clustering coefficient and high diameter introduces randomness(shortcuts with probability), which is the Watts Strogatz Model —> high clustering coefficient and low diameter). 

Kronecker Graph Model: Generating large realistic graphs. A recursive model of network structure. Kronecker product. Kronecker graph is obtained by growing sequence of graphs by iterating the Kronecker product over the initiator matrix K_1. Stochastic Kronecker Graphs: probability matrix. Fast Kronecker generator algorithm. 

<b>Lecture 2 Motifs and Structural Roles in Networks:</b>

Motifs:Subnetworks, negative significance: under-representation, positive significance: over-representation, network significance profile, Network motifs:”recurring, significant patterns of interconnections”, Pattern: small induced subgraph, Recurring: Found many times(i.e. with high frequency), Significant: more frequent than expected(i.e. in randomly generated networks), Significance of a Motif: Subgraphs that occur in a real network much more often than in a random network have functional significance. Z score captures statistical significance of motif. Network significance profile(SP) is a vector of normalized Z-scores. Significance profile emphasizes relative significance of subgraphs and generally, larger networks display higher Z-scores. Configuration Model: Generate a random graph with a given degree sequence k_1, k_2, …, k_N. Switching configuration model. Graphlets: connected non-isomorphic subgraphs. Graphlet degree vector(GDV): a vector with the frequency of the node in each orbit position, uses graphlets to obtain a node-level subgraph metric and counts #(graphlets) that a node touches.  Automorphism orbit takes into account the symmetries of a subgraph. Graphlet degree vector provides a measure of a node’s local network topology. Finding size-k motifs and graphlets requires: enumerating all size-k connected subgraphs and counting #(occurrences of each subgraph type). Just knowing if a certain subgraph exists in a graph is a hard computational problem(NP-complete) and computation time grows exponentially as the size of the motif and graphlet increases, so feasible motif size is usually small(2 to 8). ESU(Exact Subgraph Enumeration) ESU tree. Graph Isomorphism: Graphs G and H are isomorphic if there exists a bijection f:V(G)—>V(H){high computational complexity} such that: Any two nodes u and v of G are adjacent in G iff f(u) and f(v) are adjacent in H.

Structural Roles in Networks: Roles(A group of nodes with similar structural properties), Communities/Groups(A group of nodes that are well-connected to each other), Structural equivalence(Nodes u and v are structural equivalent if they have the same relationships to all other nodes). RoIX: Automatic discovery of nodes’ structural roles in networks, Recursive feature extraction(Aggregate features of a node and use them to generate new recursive features).

4. Medium, An Illustrated Guide to Graph Neural Networks(GNN) https://medium.com/dair-ai/an-illustrated-guide-to-graph-neural-networks-d5564a551783
