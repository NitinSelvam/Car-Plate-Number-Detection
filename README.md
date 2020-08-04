# Car-Plate-Number-Detection

Car Number Plate recognition has a wide range of applications, from using it to solve crimes to finding lost cars which get washed away during high-intensity floods.
This is a simple number plate recognition system, which gives the result on input of a car image.

Inspired from quangnhat185's work. Below are the Medium links to his project series:
1. [Detection License Plate with Wpod-Net](https://medium.com/@quangnhatnguyenle/detect-and-recognize-vehicles-license-plate-with-machine-learning-and-python-part-1-detection-795fda47e922)
2. [Plate character segmentation with OpenCV](https://medium.com/@quangnhatnguyenle/detect-and-recognize-vehicles-license-plate-with-machine-learning-and-python-part-2-plate-de644de9849f)
3. [Recognize plate license characters with OpenCV and Deep Learning](https://medium.com/@quangnhatnguyenle/detect-and-recognize-vehicles-license-plate-with-machine-learning-and-python-part-3-recognize-be2eca1a9f12)

Steps involved:
1. Implementing a pre-trained model named Wpod-Net to detect and extract License Plates of vehicle images from 10 different countries (Germany, Vietnam, Japan, Thailand, Saudi, Russia, Korea, USA, India, China). (Explained in part 1 of the Medium link above).
2. Read the text in number plate as a string.

I have implemented Step 2 in 2 ways.

Method 1: Perform Plate character segmentation and predict these segmented characters using a pretrained MobileNets_character_recognition model. (Explained in Part 2 and Part 3 of the Medium links above).

Method 2: Directly get the text present in image using Python's [PyTesseract](https://github.com/madmaze/pytesseract) module.

I have observed that method 1 performs better than method 2 in some images, and the reverse is true in some images. Hence, I have kept both the methods for now.

## Sample input:

![Input Image](https://github.com/NitinSelvam/Car-Plate-Number-Detection/blob/master/sample/car_back_5.jpg)

## Sample output:

<p float="left">
  <img src="https://github.com/NitinSelvam/Car-Plate-Number-Detection/blob/master/sample/Car%20image.png" width="400" />
  <img src="https://github.com/NitinSelvam/Car-Plate-Number-Detection/blob/master/sample/Number_plate.png" width="400" /> 
</p>

### Console Output:
Character Segmentation prediction:  MCV1154 --> (From Method 1) \
Tesseract Predict:  BMS CV 1154! --> (From Method 2)
