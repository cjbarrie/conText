![logo-conText](https://user-images.githubusercontent.com/6556873/138291456-5dd454d2-b37c-478a-8e37-6b2b4c20710e.jpeg)

# About

**conText** provides a fast, flexible and transparent framework to estimate context-specific word and short document embeddings using the 'a la carte' embeddings approach developed by [Khodak et al. (2018)](https://arxiv.org/abs/1805.05388) and evaluate hypotheses about covariate effects on embeddings using the regression framework developed by [Rodriguez et al. (2021)](https://github.com/prodriguezsosa/EmbeddingRegression).

# How to Install

`install.packages("conText")`

# Datasets

To use **conText** you will need three objects: 

1. A (quanteda) **corpus** with the documents and corresponding document variables you want to evaluate.
2. A set of (GloVe) **pre-trained embeddings**.
3. A **transformation matrix** specific to the pre-trained embeddings.

**conText** includes sample objects for all three but keep in mind these are just meant to illustrate function implementations. In [this Dropbox folder](https://www.dropbox.com/sh/jsyrag7opfo7l7i/AAB1z7tumLuKihGu2-FDmhmKa?dl=0) we have included the raw versions of these objects including the full Stanford GloVe 300-dimensional embeddings (labeled _glove.rds_) and its corresponding transformation matrix estimated by Khodak et al. (2018) (labeled _khodakA.rds_).

# Quick Start Guides

Check out this [Quick Start Guide](https://github.com/prodriguezsosa/conText/blob/master/vignettes/quickstart.md) to get going with `conText` (last updated: 08/04/2023).

# Latest Updates

We are hugely thankful to Will Hobbs and Breanna Green for bringing to our attention clear examples where finite sample bias was larger than we had anticipated when implementing our main estimation routine, `conText`. We are actively collaborating with them to evaluate alternative fixes. In the meantime we've implemented and recommend using Jackknife debiasing. Please refer to the [Finite Sample Bias](https://github.com/prodriguezsosa/conText/blob/master/vignettes/finite_sample_bias.md) vignette for additional information on the issue and simulation results using various debiasing methods.
