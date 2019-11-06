---
weight: 2
title: "Videos and Trails"
---

# Videos and Trails


{{< expand "1. cartolastd - 696 observations - 19 timesteps - 17 dimensions - 5 classes" "..." >}}
The dataset was scrapped from the Brazilian fantasy soccer platform Cartola and represents the second turn of the 2017 championship. The scrapper source can be found at https://github.com/henriquepgomide/caRtola. To make the dataset smoother, the dimensions were cumulatively averaged.
{{< youtube id="SKcRJRXL5cg" >}}
![](https://github.com/EduardoVernier/dynamic-projections/blob/master/Plots/Figs/trails-cartolastd.png?raw=true)
{{< /expand >}}

{{< expand "2. cifar10cnn - 1000 observations - 30 timesteps - 10 dimensions - 10 classes" "..." >}}
I took the example CNN available at the keras website (https://keras.io/examples/cifar10_cnn/) and looked at the output of the last layer after each epoch for 1000 images of the validation set. After 30 epochs the CNN had an accuracy of 0.6950.
{{< youtube id="jaoB6aJVG4s" >}}
![](https://github.com/EduardoVernier/dynamic-projections/blob/master/Plots/Figs/trails-cifar10cnn.png?raw=true)
{{< /expand >}}

{{< expand "3. esc50 - 320 observations - 108 timesteps - 128 dimensions - 8 classes" "..." >}}
Sound samples of 8 classes (brushing_teeth, chainsaw, crying_baby, engine, laughing, rain, siren, wind) compressed to 128 frequencies and smoothed over time. Collected from https://github.com/karoldvl/ESC-50 by K. J. Piczak.
{{< youtube id="FZEpRadyAN0" >}}
![](https://github.com/EduardoVernier/dynamic-projections/blob/master/Plots/Figs/trails-esc50.png?raw=true)
{{< /expand >}}

{{< expand "4. fashion - 1000 observations - 10 timesteps - 784 dimensions (28x28 pixels) - 10 classes" "..." >}}
100 images from each class (T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot) were selected and added decreasing amounts of noise.
{{< youtube id="IXicmZ5h8yI" >}}
![](https://github.com/EduardoVernier/dynamic-projections/blob/master/Plots/Figs/trails-fashion.png?raw=true)
{{< /expand >}}

{{< expand "5. gaussians - 2000 observations - 10 timesteps - 100 dimensions - 10 classes" "..." >}}
Dataset from Rauber et. al's dt-sne paper. “We create the multivariate Gaussians dataset specifically as a controlled experiment for dynamic t-SNE. Firstly, we sample 200 observations from each of 10 distinct (isotropic) 100-dimensional multivariate Gaussian distributions with variance 0.1. We combine the resulting 2000 observations into a single dataset D[1]. Each multivariate Gaussian has a distinct mean, which is chosen uniformly between the standard basis vectors for R 100 . Given D[t], the dataset D[t + 1] is created as follows. Each observation x[t + 1] ∈ D[t + 1] corresponds to an observation x[t] ∈ D[t] moved 10% of the remaining distance closer to the mean of its corresponding multivariate Gaussian. In simple terms, each of the 10 clusters becomes more compact as t increases. We consider T = 10 datasets.”
{{< youtube id="8RcAyrBywdw" >}}
![](https://github.com/EduardoVernier/dynamic-projections/blob/master/Plots/Figs/trails-gaussians.png?raw=true)
{{< /expand >}}

{{< expand "6. nnset - 80 observations - 30 timesteps - 8070 dimensions - 8 classes" "..." >}}
This dataset represents the internal states (weights and biases) of a set of neural networks learning to classify MNIST with same architecture but using different optimizers, batch sizes, training data sizes. There doesn't seem to be a clear class separation in this dataset.
{{< youtube id="rcdcES9Ei8k" >}}
![](https://github.com/EduardoVernier/dynamic-projections/blob/master/Plots/Figs/trails-nnset.png?raw=true)
{{< /expand >}}

{{< expand "7. qtables - 180 observations - 40 timesteps - 1200 dimensions - 9 classes" "..." >}}
Each observation is an agent learning to move a car up a hill using the reinforcement learning algorithm Q-learning. The classes represent variations of learning rates and discounts. The car has 3 actions, and the decision space has 2 features, each divided into 20 discrete steps. Therefore the dataset is 3x20x20 or 1200 dimensions. Code based on this tutorial: https://pythonprogramming.net/q-learning-reinforcement-learning-python-tutorial/.
{{< youtube id="soTidu-0xd4" >}}
![](https://github.com/EduardoVernier/dynamic-projections/blob/master/Plots/Figs/trails-qtables.png?raw=true)
{{< /expand >}}

{{< expand "8. quickdraw - 600 observations - 89 timesteps - 784 dimensions (28x28 pixels) - 6 classes" "..." >}}
Google has a little fun project called Quick Draw (https://quickdraw.withgoogle.com/data). It’s a website where they give you a few seconds to draw some object while a neural network is trying to guess what is it that you are trying to draw. What I did was extract drawing sequences for 600 objects of 6 different classes drawn by random people. In my sample, each final drawing is composed of an average of 36.1 partial drawings. Each image is a 28x28 pixel binary map.
{{< youtube id="MIj8yY6iPtI" >}}
![](https://github.com/EduardoVernier/dynamic-projections/blob/master/Plots/Figs/trails-quickdraw.png?raw=true)
{{< /expand >}}

{{< expand "9. sorts - 80 observations - 100 timesteps - 100 dimensions - 8 classes" "..." >}}
Intermediate states of 8 sorting algorithms. Arrays initially have 100 random elements. Based on franciscouzo.github.io/sort/
{{< youtube id="X86myugVDVY" >}}
![](https://github.com/EduardoVernier/dynamic-projections/blob/master/Plots/Figs/trails-sorts.png?raw=true)
{{< /expand >}}

{{< expand "10. walk - 300 observations - 50 timesteps - 100 dimensions - 3 classes" "..." >}}
There are three classes, in one the values of the dimensions start low and go high, one the values start high and decrease over time, and in the last, they stay roughly the same. For all of them, there is noise added (see example). This is supposed to be a "ground-truth" dataset with simple dynamics.
{{< youtube id="VJWRNnnKyp4" >}}
![](https://github.com/EduardoVernier/dynamic-projections/blob/master/Plots/Figs/trails-walk.png?raw=true)
{{< /expand >}}


Youtube playlist: https://www.youtube.com/playlist?list=PLy5Y4CMtJ7mIWjq8Sx1-mij5LxSv589wo

Trails: https://github.com/EduardoVernier/dynamic-projections/blob/master/Plots/Figs
