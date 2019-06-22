# Pytorch implementation: Long- and Short-term Dependencies for Sequential Recommendation
## Abstract
In this thesis, we study the influence of long- and short-term dependencies for sequential recommendation. The problem of recommendation stems from the enormous amount of content that is provided by companies such as Spotify and Netflix. 
By treating consumption behaviour of a user as a sequence, the task of recommendation turns into a problem of predicting the next movie and or song in a sequence. Previous work has focused on the usage of various recurrent models and personalized recommendations by integrating user information in a Gated Recurrent Unit (GRU). Our first contribution consists of the extension of this previous work by performing a thorough analysis of the hyperparameters and methods of preprocessing that were used. We find that the integration of user information is not as significant as was portrayed in previous work. For our second contribution we studied the influence of long- and short-term dependencies on our models. As some recurrent models are said to have difficulties with handling longer sequences, we employ a Differentiable Neural Computer, which uses an external memory component. We find that long-term dependencies have less influence on recommendation effectiveness than anticipated. As we decrease the size of our training set, while keeping it temporally close to the evaluation set, we find that the decrease in Recall@k scores is not linear, meaning that most of the important information is temporally closest to our evaluation set. When evaluating various sequence lengths, and even when distinguishing between popular, semi-popular and unpopular items, there does not seem to be a clear relation between the resulting scores and the corresponding sequence lengths. We conclude that if runtime is key, one might consider using a smaller dataset and shortening sequence lengths. This could be of importance to companies, such as Netflix, which deal with a tremendous amount of data.

## Usage
The notebook that can be found in this repository contains the code for the work performed by J.M. van Hulst for his thesis. Using this Notebook is fairly easy, one only has to alter the variable names in the notebook to the name of the **Google Drive** folder where the experiments should be stored (**NOTE**: make sure that the variable name does not end with a backslash) and the **folder** where the LastFM dataset is stored. The LastFM dataset is freely available [here](https://www.dtic.upf.edu/~ocelma/MusicRecommendationDataset/lastfm-1K.html). We encourage users to run this notebook on Google Colab as the models are computationally expensive.

To obtain results for this work, one only has to run all the cells, which can be done by pressing CTRL+F9 (or click on Runtime above). 

The code for the DNC was largely based on the work performed by Csordas et al., their code can be found [here](https://github.com/xdever/dnc).
