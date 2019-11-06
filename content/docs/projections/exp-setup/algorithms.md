# Algorithms

**PCA** - A technique for dimensionality reduction that performs a linear mapping of the data to a lower-dimensional space maximizing the variance of the data in the low-dimensional representation. We created a wrapper that around the scikit-learn implementation that offers two usage modes: Strategy 1 (pca_s1) computes PCA independently for each timestep. Strategy 4 (pca_s4) works by grouping all timesteps and computing PCA once. The terminology was borrowed from the dt-SNE paper.

**t-SNE** - This method converts the nD distances between data points to joint probabilities and tries to minimize the Kullback-Leibler divergence between the joint probabilities of the low-dimensional mD embedding and the high-dimensional nD data. This usually results in good neighborhood preservation. Our implementation is based off the scikit-learn implementation and the perplexity is set as default (30).

**dt-SNE** - This method extends t-SNE to deal with dynamic data by adding a stability term (lambda) to the cost function.

**Autoencoders** - In the context of dimensionality reduction, we take a (usually) hourglass-shaped neural network and train it to reconstruct the input. After training, the middle layer acts as a compact (latent) representation of the original data. The middle layer has to have a number of neurons equivalent to the dimensionality of the space we want to project out data into. We tested four different "types" of autoencoders:

|       |                                                        |                                                                        |
|------:|:-------------------------------------------------------|:-----------------------------------------------------------------------|
|    AE | _Dense autoencoders_                                   | Fully connected layers.                                                |
|  C2AE | _Convolutional autoencoders_                           | Used only on the image-based datasets.                                 |
|   VAE | _Variational autoencoders with fully connected layers_ | trying to get better internal representations by avoiding overfitting. |
| C2VAE | _Variational autoencoders with convolutional layers_   | possibly better of both worlds regarding input reconstruction ability. |

We experiment with different optimizers, architectures, training routines, etc. To decode the names to understand the number of layers, neurons per layer, epochs of training, etc.


The notebooks/script associated with each run can be found at https://github.com/EduardoVernier/dynamic-projections/tree/master/Models. Information about replication and tests with new datasets can be found in the [Replication]({{< ref "/docs/projections/replication.md" >}}) section.
