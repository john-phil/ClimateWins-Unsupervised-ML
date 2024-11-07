# ClimateWins: Unsupervised Machine Learning Project
## Project Description: Using various unsupervised machine learning models to assess ability to predict "pleasant weather days" in various cities across Europe using historical weather data from those areas.
### Used Python and various libraries (including sklearn, keras, tensorflow, PIL) to run several iterations on four different algorithms.
- Random Forests
  - Iterated the climate dataset by decade (2010s) and by individual weather station.
  - Used feature importance to discern the top 3 stations driving model performance, and to uncover the top 3 weather variables driving a pleasant or unpleasant day.
  - Futures steps: analyze data through other decades or individual years to confirm feature importance found in previous steps.
- Convolution Neural Networks (CNNs)
  - Adjusted various hyperparameters including the number of epochs, learning rate, number of filters, and batch size.
  - Assessed model performance through examination of mutliabel confusion matrices and various performance metrics, including overall accuracy, recall, precision, and F1-scores.
  - Came to the best test accuracy of 72% after applying class weights and random oversampling to reduce class imbalance.
  - This model still demonstrates significant issues with class imbalance, working better for the well-represented weather stations, and much less so for the underrepresented ones.
- Recurrent Neural Networks (RNNs)
  - Adjusted various hyperparameters including the number of epochs, learning rate, and batch size.
  - Assessed model performance through examination of mutliabel confusion matrices and various performance metrics, including overall accuracy, recall, precision, and F1-scores.
  - Came to the best test accuracy of 73% after adding a third LSTM layer and using random oversampling to reduce class imbalance.
  - This model also demonstrates significant issues with class imbalance, working better for the well-represented weather stations, and much less so for the underrepresented ones.
- Generative Adversarial Networks (GANs)
  - First trained the model on simple handwriting recognition. 
  - Then used the model to train and recognize different pictures of weather conditions (sunrise, shine, rain and cloudy).
  - Improved model performance to a test accuracy of 82%, with it struggling the most to correctly classify cloudy conditions.
  - Assessed model performance through examination of mutliabel confusion matrices.
  - Trained the model on different numbers of epochs and plotted accuracy-loss convergence to determine ideal number of epochs.
### Ran models through grid search, random search and Bayesian optimization to find the optimal hyperparameters.
### Used Principal Components Analysis (PCA) to reduce data components down while keeping sufficient complexity.
### Ran the four different types of hierarchical clustering (single, complete, average, Ward) to discover meaningful groupings within the data.
