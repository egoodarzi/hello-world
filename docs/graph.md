# about Graph Convolutional Networks(GCN)
[sourse1](https://medium.com/analytics-vidhya/getting-the-intuition-of-graph-neural-networks-a30a2c34280d),
[source2](https://medium.com/@BorisAKnyazev/tutorial-on-graph-neural-networks-for-computer-vision-and-beyond-part-1-3d9fada3b80d),
[source3](https://missinglink.ai/guides/convolutional-neural-networks/graph-convolutional-networks/),
[stanford](http://web.stanford.edu/class/cs224w/)

#### keywords or unmentiond useful further material:
[Spektral](https://spektral.graphneural.network/) a Python library for Graph Neural Networks based on Keras and Tensorflow 2 developed by Daniele Grattarola.

## what is a graph?
A **graph**in computer science is a data structure consisting of Vertices (also called nodes) and Edges (also called connections).
Here are two ways to represent a graph: using an equation with a group of vertices V and a group of edges E. And a diagram with nodes and the connections between those nodes

![image](https://missinglink.ai/wp-content/uploads/2019/07/Graph-and-Convolutional-Neural-Network-Concepts.png)
![image](https://missinglink.ai/wp-content/uploads/2019/07/Converting-graph-structure-to-a-neural-network-function.png)
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
What is Graph Neural Network?
A Graph Neural Network, also known as a Graph Convolutional Networks (GCN), performs a convolution on a graph, instead of on an image composed of pixels.[3]

![image](https://missinglink.ai/wp-content/uploads/2019/07/Converting-graph-structure-to-a-neural-network-function.png)

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

Colloquially, people call this averaging or summation “convolution”, since we also “slide” from one node to another and apply an aggregator operator in each step

# What makes a neural network a graph neural network?
Now, how do we transform our vanilla neural network to a graph neural network? As you already know, the core idea behind GNNs is aggregation over “neighbors”. 
**Here, it is important to understand that in many cases, it is actually `you` who specifies “neighbors”.**
