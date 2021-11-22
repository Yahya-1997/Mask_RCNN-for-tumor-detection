# Mask_RCNN-for-tumor-detection
Uses Mask_RCNN for brain tumor detection in MRI images

Architecture

The architecture of the model can be seen below. The first part of the model consists of a Convolutional Neural Network that extracts the dynamic features from the input image and also provides the proposed localization regions of the features. 

Then the features and the proposed regions of features are fed to the next component of the model ROI Align which is a Deep Neural Network model which calculates the similarity between the input features and aligns the RIO which belongs to the same individual object. 

After the RIO alignment, the object features and ROIs are passed to the fully connected layers which classify the detected objects based on features and also calculate the boundary boxes around the objects for output images. The output of RIO Align layer is also fed to another neural network to calculate the masks of the objects which provides the pixels locations that belong to the object.


![image](https://user-images.githubusercontent.com/70836660/142833730-983f6549-8874-42e6-9888-d98415976593.png)


Usage: import the module (see Jupyter notebooks for examples), or run from
       the command line as such:

    # Train a new model starting from pre-trained COCO weights
    python3 tumor.py train --dataset=/path/to/tumor/dataset --weights=coco

    # Resume training a model that you had trained earlier
    python3 tumor.py train --dataset=/path/to/tumor/dataset --weights=last

    # Train a new model starting from ImageNet weights
    python3 tumor.py train --dataset=/path/to/tumor/dataset --weights=imagenet

    # Apply color splash to an image
    python3 tumor.py splash --weights=/path/to/weights/file.h5 --image=<URL or path to file>

    # Apply color splash to video using the last weights you trained
    python3 tumor.py splash --weights=last --video=<URL or path to file>

Resutls:
The final results can be seen below. Provided with an MRI image, the model can accurately detect the cancer and provides a mask accurately enclosing cancerous region.

Input:

![image](https://user-images.githubusercontent.com/70836660/142829967-3858364b-0d6e-438f-be88-5f64532ddf2a.png)

Output:

![image](https://user-images.githubusercontent.com/70836660/142830257-9c44a2e1-f2f7-4f3d-9a7f-cc021e5e73b8.png)

