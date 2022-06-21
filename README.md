# Image-recognition
Creating image recognition pipeline with low amount of data

General Idea is to find out features on individual images from both Database and Test folder and then get the name of image pairs where number of matched features is maximum. I have tried 2 techniques: using basic image processing and using latest deep learning method.
1.	Feature Detection: 
Here I have used 2 methods:
a.	Using traditional feature detection technique: 
ORB detector from OpenCV Python Library.
b.	Using Deep learning technique:
LoFTR for feature detection 
2.	Feature Matching: 
a.	For ORB I have tried FLANN and BFmatcher, BFmatcher worked well
b.	For LoFTR I used the LoFTR’s own matching technique
3.	Finally, I converted the result into Dataframe and then saved it into .csv file.
Instructions to run the jupyter notebook:
1.	Run ‘Using ORB.ipynb’ on laptop/desktop.
2.	Run ‘Using LoFTR.ipynb’ on google colab.
Note: Link for LoFTR repository: https://github.com/zju3dv/LoFTR
Result/Conclusion:
1.	Using traditional method 2 out of 5 images were identified correctly.
2.	Using Deep learning method, all images were correctly identified.
