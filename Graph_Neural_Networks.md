1. Youtube, Graph Convolutional Neural Networks, https://www.youtube.com/watch?v=Mf-mIRF3ao8 ,AI learns(GCN) structure(Graph) of data points. Irregular data structures. Adjacency Matrix in graph. Node classification: use label nodes to predict unable nodes. Graph classification: predict information about new graphs, based on labeled graphs. CNN: spatial invariance properties. Graph-Shifted Signal: idea from the DSP field, linear shift invariant filter can be represented as a polynomial of shifts.Youtube Linear Filters: https://www.youtube.com/watch?v=WeNpd_YEF6I ,blur filters, sharper filter. ECE course: Linearity, Shift Invariance: https://www.youtube.com/watch?v=xhDGX8nHAdg

GNN Tools: PyTorch Geometric, Graph Nets(TensorFlow), Deep Graph(easy for beginners)

2. Youtube, Graph Network, Siraj Raval. https://www.youtube.com/watch?v=bA261BF0bdk ,Simple intuitive introduction of GNN, Sample neighbourhood —> Aggregate feature information from neighbours —> Predict graph context and label using aggregated information.

3. CS224W: Machine Learning with Graphs Stanford/Fall 2019

Official Website: http://web.stanford.edu/class/cs224w/index.html

Youtube Channel: https://www.youtube.com/watch?v=dD6LRgw_2mQ&list=PL1OaWjIc3zJ4xhom40qFY5jkZfyO5EDOZ&index=1

Lecture 1: Properties of Networks and Random Graph Models

Degree distribution, path, distance, the consequence in directed graphs: distance is not symmetric. Diameter: the maximum (shortest path) distance between any pair of nodes in a graph. Average path length. Clustering coefficient(for undirected graphs, how connected are i’s neighbours to each other? Average clustering coefficient, very useful for social networks), size of the largest connected component: largest set where any two vertices can be joined by a path(largest component=giant component). Random Graph Model( G_np: undirected graph on n nodes where each edge (u, v) appears i.i.d with probability p, G_nm: undirected graph with n nodes, and m edges picked uniformly at random), expansion alpha. In real world social network: high clustering coefficient and low diameter.(graph model with high clustering coefficient and high diameter introduces randomness(shortcuts with probability), which is the Watts Strogatz Model —> high clustering coefficient and low diameter). 

Kronecker Graph Model: Generating large realistic graphs. A recursive model of network structure. Kronecker product. Kronecker graph is obtained by growing sequence of graphs by iterating the Kronecker product over the initiator matrix K_1. Stochastic Kronecker Graphs: probability matrix. Fast Kronecker generator algorithm. 
