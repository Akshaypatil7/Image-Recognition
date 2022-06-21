# Image-Recognition
Creating image recognition pipeline with low amount of data


### PROBLEM STATEMENT
#### BACKGROUND:
Muzzle is the area between a cow or a buffalo’s nostrils. This region contains a pattern of beads and ridges which is unique to each and every cattle, similar to fingerprints in humans. We are in the process of developing a novel solution to create a unique identity for cattle, similar to Aadhar.

#### PROBLEM: 
1.	In the Images.zip attachment, there are 2 folders named Database and Test. 
2.	Under Database folder, there are 20 images belonging to 20 different cattle.
3.	Under Test folder there are 5 test images, belonging to 5 different cattle.
4.	Define an algorithm that would identify a Test Cattle image in a database of many cattle images. 
5.	Given a random Test Image, the algo should return the corresponding database image. Else return “Not Found”.  


### Solution
General Idea is to find out features on individual images from both Database and Test folder and then get the name of image pairs where number of matched features is maximum. I have tried 2 techniques: using basic image processing and using latest deep learning method.
1.	Feature Detection: 
Here I have used 2 methods:
      1. Using traditional feature detection technique: 
ORB detector from OpenCV Python Library.
      2.	Using Deep learning technique:
LoFTR for feature detection 
2.	Feature Matching: 
      1.	For ORB I have tried FLANN and BFmatcher, BFmatcher worked well
      2.	For LoFTR I used the LoFTR’s own matching technique
3.	Finally, I converted the result into Dataframe and then saved it into .csv file.
#### Instructions to run the jupyter notebook:
1.	You can run ‘Using ORB.ipynb’ on your CPU.
2.	Run ‘Using LoFTR.ipynb’ on google colab.
#### Note: Link for LoFTR repository: https://github.com/zju3dv/LoFTR
#### Result/Conclusion:
1.	Using traditional method 2 out of 5 images were identified correctly.
2.	Using Deep learning method, all images were correctly identified.
