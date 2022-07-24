# 71 Landmark detector 


![samples](https://raw.githubusercontent.com/vanquish630/LandmarkDetector71/master/samples/banner.png)

Landmark detector to detect additional landmarks on top of the head. Uses a 2 stack hourglass architecture for the landmark detector. Used the 300WLP dataset to train the first 68 landmarks. 
Additional landmarks trained on 2000 manually annotated images. This detector was used to train a 3DMM model that accurately models 
head shape. The 3DMM model was used to detect landmarks on 75,000 images and used to train the landmark model further.

## How to use

Download the [trained model](https://drive.google.com/file/d/1UtSW4zx232qtIMwQyli5Uu9jfdsdfJuJ/view?usp=sharing) and place it in the pretrained_models folder. 

    from utils.landmarkDetector import LandmarkDetector71
    landmarkDetector71 = LandmarkDetector71()

    image = Image.open(image_path).convert("RGB")
    lmks71 = landmarkDetector71.detect_landmarks(image)



The landmark numbering is as follows:

![key](https://raw.githubusercontent.com/vanquish630/LandmarkDetector71/master/samples/lmk71.png)


