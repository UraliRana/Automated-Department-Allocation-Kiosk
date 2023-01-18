# Automated-Department-Allocation-Kiosk

Information regarding the Dataset:

Dataset: https://www.kaggle.com/datasets/neelima98/disease-prediction-using-machine-learning

Data is taken for a hospital located in the USA from Kaggle data. Dataset contains ~130 different features that result in the occurrence of a prognosis/disease. The dataset contains a total of 40 diseases with each having a good number of samples (100-120 each). Total row count is around 5K, and the data is spread across a period of 15 months to be exact. The data is for the year 2021 and is spread evenly for each disease.

Steps excution in Phase 1:

Steps for Execution:

Data preparation:

Creating new columns and combining some of the classifications for making things easy to predict was the focus in this part of work
  - Dates were fixed for a certain period – Year 2021 (Jan 1st to Dec 31st)
  
  - 4 Seasons were added next to the dates. 
  
  - Department was added against each prognosis/disease. Research was done for each prognosis and a department was assigned. This helped to combine 40 different prognoses into 13 departments.

Extracted the Data inta a DataFrame.

Perfromed EDA for the different features to check how they ar correlated.

Label the categorical features 'Department', 'Season'.

Dropped the irrelevent features which won't be used anymore.

As the data give was separate for the train set an test set, assigned the proper features for X and y.

Created a Machine Learning Model using LogisticRegression, Decision Tree, Random Forest, XG Gradient Boosting and Fully connected network by tuning the models.

Plot a confusion matrix for each method and select the optimal algorithm with the highest accuracy and the most 20 essential attribute. 

Now the set of chosen 20 features are fed into fully connected deep learning network, with a ‘relu’ function to predict the accuracy of the outcome on the validation data. Tests were run on test set as well as live inputs.

    -two hidden layers with 128 and 64 neurons respectively.
    
    -Dense layer with sofmax function.

To compile the model we used 'Adam' as an optimizer, 'categorical_crossentropy' as Loss Function and metric used was 'Accuracy'.
 
The Model created was trained for 10 epochs which gave an Accuracy of around 81%.
 

Epoch 1/10

96/96 [==============================] - 1s 7ms/step - loss: 2.4836 - accuracy: 0.2228 - val_loss: 2.3853 - val_accuracy: 0.5156

Epoch 2/10

96/96 [==============================] - 0s 4ms/step - loss: 2.2801 - accuracy: 0.5670 - val_loss: 2.1772 - val_accuracy: 0.5698

Epoch 3/10

96/96 [==============================] - 0s 4ms/step - loss: 2.0480 - accuracy: 0.5785 - val_loss: 1.9247 - val_accuracy: 0.5698

Epoch 4/10

96/96 [==============================] - 0s 3ms/step - loss: 1.7832 - accuracy: 0.5856 - val_loss: 1.6603 - val_accuracy: 0.6375

Epoch 5/10

96/96 [==============================] - 0s 4ms/step - loss: 1.5291 - accuracy: 0.6555 - val_loss: 1.4282 - val_accuracy: 0.6375

Epoch 6/10

96/96 [==============================] - 0s 4ms/step - loss: 1.3143 - accuracy: 0.6562 - val_loss: 1.2346 - val_accuracy: 0.6375

Epoch 7/10

96/96 [==============================] - 0s 4ms/step - loss: 1.1354 - accuracy: 0.6797 - val_loss: 1.0721 - val_accuracy: 0.6833

Epoch 8/10

96/96 [==============================] - 0s 4ms/step - loss: 0.9862 - accuracy: 0.7303 - val_loss: 0.9365 - val_accuracy: 0.7437

Epoch 9/10

96/96 [==============================] - 0s 4ms/step - loss: 0.8621 - accuracy: 0.7705 - val_loss: 0.8230 - val_accuracy: 0.7927

Epoch 10/10

96/96 [==============================] - 0s 4ms/step - loss: 0.7590 - accuracy: 0.8106 - val_loss: 0.7284 - val_accuracy: 0.8188

Phase 2:

In this phase the above data is put into a visualization model to describe and predict the various stats out of the data, major objectives are 
  -Compare the hospital data against national/state averages on diseases 
  -Predict next major diseases for what the hospital needs to be ready for
  -other useful stats that the hospital can get benefited from

Phase 3:

The final phase involves development of a crisp, precise form (just 20 features) which can predict with same accuracy as that of 130 odd features. In this the plan is to use the best algorithm and best features (both outcome of phase 1) and try to make the user experience less time consuming and more accurate.  This can help the staff to route the patient to right doctors and prescribe better medicine (if it’s a on call consultation)
