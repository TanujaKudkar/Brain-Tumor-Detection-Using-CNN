# 🧠 Brain-Tumor-Detection-Using-CNN 🧠

# Aim:
The main goal of this project is to design CNN model to accurately identify the abnormal tumor region in MRI.

# Dataset Description:
The dataset contains 2 folders: yes and no which contains total 3000 Brain MRI Images. The folder yes contains 1500 Brain MRI Images that are tumorous and the folder no contains 1500 Brain MRI Images that are non-tumorous.

Dataset is here : https://rb.gy/m5y2er

# Part 1: Data Split ✂️
The data was split in the following way:
70% of the data for training, i.e. 1050 positive and 1050 negative examples, resulting in 2100 images.
15% of the data for validation, i.e. 225 positive and 225 negative examples, resulting in 450 example images.
15% of the data for testing, i.e. 225 positive and 225 negative examples, resulting in 450 example images.

# Part 2: Data Preprocessing
Keras's  'ImageDataGenerator' class ensures that model receives new variation of training images at each epoch by applying random transformation.
I've use different transformation techniques like rescaling, zooming, horizontal_flip, nearest filling for training dataset.
I've set batch size = 16 . This will reduce overall memory usage.
'flow_from_directory' method allows to read the images directly from directory and augment them while network model is learning on training images.
For testing dataset, I've set batch size = 1, because in real life scenario, we process 1 image at a time.

# Part 3: CNN architecture that I've built:
Convolutional Neural Network (CNN) is the deep learning technique to perform image classification. The Keras library in Python makes it pretty simple to build a CNN. 

The model type that I have used is Sequential. ‘add()’ function is used to add multiple deep layers to CNN architecture. 24 in the first layer and 64 in the second layer, 128 in the third layer are the number of nodes in each layer. I have set Kernel size = 3 (i.e. 3x3 filter matrix) 

Feature Extaction:
1) Convolution Layer:
Computers see images using pixels. Pixels in images are usually related. Pixels in the form of arrays are fedinto the input layer. Convolution layer perform dot product between matrix with learnable parameter and filter matrix or ‘kernel’, and then sums up the multiplication values. Then the convolution slides over to the next set of pixels and repeats the same process. During forward pass, the kernal slides across the height and width of image until all the image pixels have been covered. This produce 2D representation of image called 'Activation/ Feature map'. Activation map is then fed to other layers to learn several other features of the input image.

2)Pooling Layer:
Primary aim of this layer is to decrease size of activation map. I've used Maxpooling for my model, because it reports the maximum output from the neighborhood.













# Results:
The model was trained for total 51 epochs. The best validation accuracy was achieved on the 44th iteration.

✓ Training Accuracy  : 96.52%     ❌ Training loss  : 0.105923
✓ Validation Accuracy: 97.11%     ❌ Validation loss: 0.125594



Hope this helps🙂. Don't forget to add star 🌟.
Thank you!
