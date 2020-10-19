# about Graph Convolutional Networks(GCN)
[sourse1](https://medium.com/analytics-vidhya/getting-the-intuition-of-graph-neural-networks-a30a2c34280d)
[source2](https://medium.com/@BorisAKnyazev/tutorial-on-graph-neural-networks-for-computer-vision-and-beyond-part-1-3d9fada3b80d)

#### keywords or unmentiond useful further material:
[Spektral](https://spektral.graphneural.network/) a Python library for Graph Neural Networks based on Keras and Tensorflow 2 developed by Daniele Grattarola.

## what is a graph?
we represent a graph by its vertxes and its links between vertexes, so a graph is represented by G(v, r)
#### directed VS undirected graphs
how the edges link the nodes allws us t o distinguish between a __directed__ vs __undirected__ graph.\\

#### complete graph
where each node is connected to all other nodes.

## one way of thinking:
how can those graphs be shaped into features to be fed into the Neural Networks?

### Adjacency matrix (A)
An adjacency matrix is a (N, N) matrix filled with either 0 or 1, where N is the total number of nodes.
Matrix element $A_{ij}$ Aᵢⱼ is 1 if an edge exists between node i and j.
