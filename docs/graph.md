# about Graph Convolutional Networks(GCN)
[sourse1](https://medium.com/analytics-vidhya/getting-the-intuition-of-graph-neural-networks-a30a2c34280d)
[source2](https://medium.com/@BorisAKnyazev/tutorial-on-graph-neural-networks-for-computer-vision-and-beyond-part-1-3d9fada3b80d)

#### keywords or unmentiond useful further material:
[Spektral](https://spektral.graphneural.network/) a Python library for Graph Neural Networks based on Keras and Tensorflow 2 developed by Daniele Grattarola.

## what is a graph?
we represent a graph by its vertxes and its links between vertexes, so a graph is represented by G(v, r)

examples are: chemical molecular structure, documents citation networks, ...
#### directed VS undirected graphs
how the edges link the nodes allws us t o distinguish between a __directed__ vs __undirected__ graph.

undirected graph is equal to bi-directional graph.
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

# Graph Neural Networks vs Convolutional Neural Networks (CNN)
Interestingly, images can also be seen as a complete graph, where:
- Each __node__ represents each __pixel__.
- __Node feature__ represents the __pixel value__.
- __Edge feature__ represents __the Euclidean distance between each pixel__. The closer 2 pixels are to each other, the larger the edge values.

##-------------------------------##
## permutation invariance
max or sum pooling are permutation invariant, i.e. they will pool the same value from a spatial region even if you randomly shuffle all pixels inside that region.

the dot product ins not permutation invariant, simply because X₁W₁+X₂W₂ ≠X₂W₁+X₁W₂.

**Nodes are a set, and any permutation of this set does not change it. Therefore, the aggregator operator that people apply should be permutation-invariant.**  The most popular choices are averaging [(GCN, Kipf & Welling, ICLR, 2017)](https://arxiv.org/abs/1609.02907) and summation [(GIN, Xu et al., ICLR, 2019)](https://arxiv.org/abs/1810.00826) of all neighbors, i.e. sum or mean pooling, followed by projection by a trainable vector W. See [Hamilton et al., NIPS, 2017](https://arxiv.org/abs/1706.02216) for some other aggregators.
![image](https://miro.medium.com/max/700/1*r91KCqXWXm3ltrixv_kUcA.png)


