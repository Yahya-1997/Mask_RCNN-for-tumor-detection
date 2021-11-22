# Mask_RCNN-for-tumor-detection
Uses Mask_RCNN for brain tumor detection in MRI images

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

![image](https://user-images.githubusercontent.com/70836660/142829967-3858364b-0d6e-438f-be88-5f64532ddf2a.png)

![image](https://user-images.githubusercontent.com/70836660/142829996-fb6b83e3-f6c2-47a1-b669-940276cb93b1.png)
