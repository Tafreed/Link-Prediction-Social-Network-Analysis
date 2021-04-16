# **Link-Prediction-Social-Network-Analysis**

### 5 Different Types of Link Prediction (Python Code)



- *Jaccard’s Coefficient*. The Jaccard Coefficient, also known as Jaccard index or Jaccard similarity coefficient, is a statistic measure used for comparing similarity of sample sets. It is usually denoted as J(x,y) where x and y represent two different nodes in a network. In link prediction, all the neighbours of a node are treated as a set and the prediction is done by computing and ranking the similarity of the neighbour set of each node pair. This method is based on Common Neighbours method and its complexity is also O(Nk^2) . The mathematical expression of this method is as follows  

<p align="center">
  <a href="https://www.codecogs.com/eqnedit.php?latex=\LARGE&space;\left\lvert&space;\frac{&space;\Gamma(x)&space;\cap&space;\Gamma&space;(y)}{&space;\Gamma(x)&space;\cup&space;\Gamma&space;(y)}&space;\right\rvert" target="_blank"><img src="https://latex.codecogs.com/svg.latex?\LARGE&space;\left\lvert&space;\frac{&space;\Gamma(x)&space;\cap&space;\Gamma&space;(y)}{&space;\Gamma(x)&space;\cup&space;\Gamma&space;(y)}&space;\right\rvert" title="\LARGE \left\lvert \frac{ \Gamma(x) \cap \Gamma (y)}{ \Gamma(x) \cup \Gamma (y)} \right\rvert" /></a>
</p>

- *Preferential Attachment*. Due to the assumption that the node with high degree is more likely to get new links, preferential attachment was introduced as a prediction method. The degree of both nodes in a pair needs to be considered for the prediction. Same as common neighbours, this is also a basic prediction method which is usually used as a baseline to measure the performance of other prediction methods. This method will calculate similarity score for each pair of nodes within the network rather than only the neighbour of nodes; thus the complexity of preferential attachment is O(N^2K^2) . This method can be expressed as

$$
\mid\Gamma(x)\mid   \ast   \mid\Gamma (y)\mid
$$

- *Adamic Adar Index*. It was initially designed to measure the relation between personal home pages. As shown in, the more friends has, the lower score it will be assigned to. Thus, the common neighbour of a pair of nodes with few neighbours contributes more to the Adamic/Adar score (AA) value than this with large number of relationships. In real-world social network, it can be interpreted as follows: if a common acquaintance of two people has more friends, then it is less likely that he will introduce the two people to each other than in the case when he has only few friends. It shows good results in predicting the friendship according to personal homepage and Wikipedia Collaboration Graph, but in the experiment of predicting author collaboration, it shows a poor accuracy prediction. It is another method that is based on common neighbour; the complexity is also the O(Nk^2). It is calculated as

$$
\sum_{z \in  \Gamma (x)  \cap  \Gamma {y)}} \frac{1}{log\mid\Gamma(z)\mid}
$$

- *Cosine Similarity*. The idea of this method is based on the dot product of two vectors. It is often used to compare documents in text mining. For each pair of nodes with common neighbours, this method will perform a vector multiplication and thus the complexity is . In network prediction problem, this method is expressed as

$$
\frac{\mid\Gamma(x)\mid \mid\Gamma(y)\mid}{\mid\mid\Gamma(x)\mid\mid  \ast  \mid\mid\Gamma(y)\mid\mid}
$$

- *Resource Allocation Index*. Among a number of similarity-based methods to predict missing links in a complex network, Research Allocation Index performs well with lower time complexity. It is defined as a fraction of a resource that a node can send to another through their common neighbours.

  
  $$
  \sum_{z \in  \Gamma (x)  \cap  \Gamma {y)}} \frac{1}{\mid\Gamma(z)\mid}
  $$
  

[Check Reference here](https://www.hindawi.com/journals/sp/2015/172879/)

