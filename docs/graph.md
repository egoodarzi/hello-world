# about Graph Convolutional Networks(GCN)
[sourse1](https://medium.com/analytics-vidhya/getting-the-intuition-of-graph-neural-networks-a30a2c34280d)
[source2](https://medium.com/@BorisAKnyazev/tutorial-on-graph-neural-networks-for-computer-vision-and-beyond-part-1-3d9fada3b80d)

#### keywords or unmentiond useful further material:
[Spektral](https://spektral.graphneural.network/) a Python library for Graph Neural Networks based on Keras and Tensorflow 2 developed by Daniele Grattarola.

## what is a graph?
we represent a graph by its vertxes and its links between vertexes, so a graph is represented by G(v, r)

examples are: chemical molecular structure, documents citation networks, ...
#### directed VS undirected graphs
how the edges link the nodes allws us t o distinguish between a __directed__ vs __undirected__ graph.\\

#### complete graph
where each node is connected to all other nodes.

## one way of thinking:
how can those graphs be shaped into features to be fed into the Neural Networks?

### Adjacency matrix (A)
An adjacency matrix is a (N, N) matrix filled with either 0 or 1, where N is the total number of nodes.
Matrix element $A_{ij}$ is 1 if an edge exists between node i and j.

### Node attribute matrix (X)
this matrix represents the features or attributes of each node. 
If there are N nodes and the size of node attributes is F, then the shape of this matrix is (N, F).

### Edge attributes matrix (E)
If the size of edge attributes is S and the number of edges available is n_edges, 
the shape of this matrix is (n_edges, S).

## - Graph Neural Networks Data Modes
### batch mode
in this setting, the number of the graphs we have will be as many as the number of the observations, example: classify chemical molecules
### single mode
we will only have 1 big graph consisting of all the observations as the nodes. example: classify documents within a document citation network.



