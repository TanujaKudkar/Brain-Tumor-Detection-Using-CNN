# Brain-Tumor-Detection-Using-CNN
Design a CNN model to detect whether the MRI has a brain tumor or not.

# Aim:
The main goal of this project is to design efficient automatic brain tumor detection technique with high acuracy, performance using CNN.

# About the dataset:
The dataset contains 2 folders: yes and no which contains total 3000 Brain MRI Images. The folder yes contains 1500 Brain MRI Images that are tumorous and the folder no contains 1500 Brain MRI Images that are non-tumorous.

Dataset is here : https://rb.gy/m5y2er

# Part 1: Data Split
The data was split in the following way:
70% of the data for training, i.e. 1050 positive and 1050 negative examples, resulting in 2100 images.
15% of the data for validation, i.e. 225 positive and 225 negative examples, resulting in 450 example images.
15% of the data for testing, i.e. 225 positive and 225 negative examples, resulting in 450 example images.

# Part 2: Data Preprocessing
Keras's  'ImageDataGenerator' class ensures that model receives new variation of training image at each epoch by applying random transformation.
I've use different authentication techniques like 
I've set batch size = .
This will reduce overall memory usage.
flow 
method allows to read the images directory from directory and augment them while network model is learning on training images.
For testing dataset, I've set batch size = 1, because in real life scenario, we process 1 image at a time.

# Part 3: CNN architecture that I've built:

# Results:
The model was trained for 24 epochs. The best validation accuracy was achieved on the 23rd iteration.

# Conclution:

Hope this helps🙂.
Thank you!
