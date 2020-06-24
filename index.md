---
mathjax: true
published: true
---

# Greetings

In this post I am going to introduce you to TDA and how to use it as an anomaly detection tool. 

## Main Problem

$k-$Nearest Neighbor algorithms ($k-$NN) are widely used for anomaly detection regardless their high sensibility to changes in scale parameter $k$. This shortcoming, here named 
Local-Global Duality, occurs independently to the way nearest neighbors are selected. Topological description of data sets by persistent homology leads to a new model for 
anomaly detection where the multi scale nature of the topological featuring brought by homology persistence solves Local-Global Duality for single anomalies. The proposed 
anomaly detection model leans on the comparison between noteworthy topological changes inducted by single point extractions and the relative topological variation inherent 
to the data set. The relevant changes are measured using the Bottleneck Distance to compare persistent diagrams associated to deformations in data when a single point is 
removed. The proposed model and some $k-$NN algorithms  are compared in some experiments.

## Local-Global Duality

$k-$NN algorithms look for a ``familiar`` behavior in nearby points 



Los algoritmos tipo $k-$NN parten del principio de \textbf{similaridad por comportamiento próximo.} Para calcular la escala de anomalía en un punto $x\in X$, se escogen $k$ registros cercanos $N_k(x)=\{x_1, \dots x_k \}$ de acuerdo a alguna métrica $d$. Sobre este conjunto se caracterizará el comportamiento de $x$ de tal forma que la escala de anomalía representa qué tanto difiere $x$ del comportamiento de sus vecinos. Esta caracterización se hace mediante distintos métodos: comparación de distancias, conteo, comparación de costos, construcción de cadenas, entre otros.  \\ 

Los métodos tipo $k-$NN se ejecutan en tres tiempos: selección de parámetros, medición de anomalía y decisión de anomalía. Por ejemplo, los modelos que solamente de basan en comparar distancias como $k$-NN y $k^{th}$-NN cumplen con este esquema. Una vez fijado $k \in \mathbb{N}$, cada punto $x \in X$ es asociado a su respectivo conjunto de vecinos $N_k(x)$. Luego, a partir de cada conjunto  se genera una marca de anomalía mediante una determinada medición: el algoritmo $k$-NN asigna a cada punto $x$ la cantidad \\ 
