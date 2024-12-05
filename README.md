A Convolutional Neural Network (CNN) written in Python using Tensorflow, which attempts to identify the author of a small excerpt of handwriting.
-

Some key points if you plan on implementing some of this code in your own project:
* Written in Google Colab 
* Created the dataset myself, then uploaded it to files in my Google Drive. All the directories in the code correspond to folders in my own personal Google Drive, so simply running the code on your machine exactly as it is won't work - need to adjust the directories as needed
* In the first part of the code (titled "Ksenia and Yulia: Binary Problem") the images for the datasets used were the same, but stored in a different folder on my Google Drive (hence the different directory in this part of the code)

---

**A very brief summary on the different layers implemented in this code:**
* Input layer: Passes the images of the handwritting into the neural network (however, for this to be possible, the images need to be converted into a tensor format)
* Convolutional layer: The layer that "learns" or "finds" patterns in the handwriting, contains weights which are adjusted based on whether the network is succesful or not at classifying images in the training dataset (hyperparameters include (but are not limited to): number of filters, padding, kernel size, stride)
* Pooling layer: Combines multiple neurons into a single neuron in the following layer (the way this is done is specified, not learned). Helps to highlight the most present feature of the handwriting in the patch - without this, overfitting is very likely to occur
* Flatten layer: Converts all the arrays of numbers (which contain the image pixel values after being manipulated by the weights in the layers of the network) into a single column which can then be passed into the final layer
* Output layer: Outputs the probabilities of the image of handwriting being in each class. Class (author) with the highest probability is defined as the **predicted author**

---
End result (these images were produced using model_35): <br/>

<img width="250" alt="image" src="https://github.com/user-attachments/assets/7520a7b6-c4ee-4750-9e4f-f007be4e5fc3">
<img width="250" alt="image" src="https://github.com/user-attachments/assets/09399135-477a-4d2b-8fee-c715fa19d749">

---
Some useful links:
- https://machinelearningmastery.com/convolutional-layers-for-deep-learning-neural-networks/
- https://poloclub.github.io/cnn-explainer/

