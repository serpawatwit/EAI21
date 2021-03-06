# Lab3_CNN

## Assessment 1:

  The MSE (Mean Squared Error) for the linear regression model was 14.25 while the MAE (Mean Absolute Error) for the linear regression model was 2.57. In comparison, my tuned nural network with a longer train time, additional hidden layers, a larger batch_size, and a greater number of neurons had a MSE of 11.60 and an MAE of 2.34.
  
  Below are the Models obtained through both approaches. The Linear Regression Model is on the left and the Tuned Neural Network Model is on the right. The code for this assessment can be found [here](https://github.com/serpawatwit/Lab3_CNN/blob/main/Boston_housing_dense_NN_using_Keras_pipeline.ipynb).

<p align="center">
  <img src="Linear_Regression_Model.PNG">
  <img src="My_Tuned_Neural_Network.PNG">
</p>

  The train and test results of the tuned Neural Network after adding 5 hidden layers with 128 neurons each became slightly closer. The trained results became closer to the test results, however they were not exact. The changes betweem the two are clearly noticable when looking at the graphs. It had a MSE of 12.46 and an MAE of 2.12.
  
<p align="center">
  <img src="Tuned_Neural_Network.PNG">
</p>
  
## Assessment 2:

Notes taken for lecture 2 can be found below:

<p align="center">
  <img src="Lecture_2_Notes.jpg">
</p> 
  
## Assessment 3:

  **Question:** If I apply pooling of 2 (2,2 window with a stride of 2) to a (6,6) array, what is the resulting size?
  
  **Answer:** The resulting size would be (3, 3).
  
<p align="center">
  <img src="A3.JPG">
</p> 
  
## Assessment 4:

  **Question:** What is my output size if: Input = (100,100), kernel size=(2,2), stride of 1 and no pooling? 
  
  **Answer:**  The output size would be (99, 99).
  
  **Question:** How many weights do I have if I have 24 such filters stacked (conv2_24)?
  
  **Answer:**  You would have 96 weights if there were 24 stacked (2,2) filters (2,2,24).
  
  **Question:** What is a better idea: To use one larger kernel (7,7) or multiple stacked smaller ones, 3x(3,3)? 
  
  **Answer:**  The better idea is to use multiple stacked smaller kernels. This is because using multiple smaller kernels will lead to greater efficiency when computing since there will be only 27 weights (3,3,3) compared to the 49 weights used for the one larger kernel (7,7,1). Using three smaller kernels will also lead to greater complexity than a single large kernel.
  
  **Question:** Solve for the padding (P), in terms of I, F and S, if we want the input and output size to remain the same. 
  
  **Answer:** The number of padding layers needed in both the x and y direction can be found with the following equation:
  
<p align="center">
  <img src="Padding_Layers_Equation.PNG">
</p>

When Using this equation always round up to the nearest whole number. The following equation can be used to find the size of the output after substituting in the value found for P:

<p align="center">
  <img src="Size_Of_Output.PNG">
</p>

## Assessment 5:

  When creating and fitting the model to identify cats and dogs I decided to go with 16 layers, segmented with three Conv2D layers followed by a MaxPooling2D() layer three seperate times. The MaxPooling2D() layers are used to minimize overfitting the model. After this series of layers, a Flatten layer is created to prepare the data for the dense layers. Then two dense layers are made, one to take the neurons from the previous layers and deeply connect them. The other is used for the y_train data.

The notebook can be found [here](https://github.com/serpawatwit/EAI21/blob/main/PA5_CNN.ipynb).
