<h1 align="center"> Textile Defect Detection</h1> <br>
 
## Introduction:
Fabric defect detection is a necessary and essential step of quality control in the textile manufacturing industry. It is the determination process of the location, type and size of the defects found on the fabric surface. Traditional fabric inspections are usually performed by manual visual methods, which are low in efficiency and poor in precision for long-term industrial. Lack of concentration, human fatigue, and time consumption are the main drawbacks associated with the manual fabric defect detection process. Applications based on computer vision and digital image processing can address the abovementioned limitations and drawbacks. Here we have used machine learning and deep learning approach to identify/categorize defects.

<h4>Youtube Link : https://youtu.be/Vw78gLfCQ44
 
 <br/>
 <br/>


## Instructions For Running WebApp on local server:
1. Go to terminal. 
2. Create a directory tex-detection using ```mkdir tex-detection```
3. cd tex-detection
4. clone the repository using the command ``` https://github.com/Rajvardhan7/Textile-Detection.git```
5. Install all the requirements using command ``` pip install -r requirements.txt```
6. Run the commmand ```streamlit run app.py```
YOUR APP IS READY!!

## 1) Defect Detection

Technology/Framework Used : Numpy, Pandas, Matplotlib, CV2, Skimage, Scipy
<br/>
<br/>

<h4>Hole Detection - circular boundary using Hough Transformation:</h4>
The Hough transform is a feature extraction technique used in image analysis, computer vision, and digital image processing. The purpose of the technique is to find imperfect instances of objects within a certain class of shapes by a voting procedure. The algorithm converts RGB image to Grayscale for improved detection. By optimizing its parameters, we were able to get clear accurate bounding circle around the holes.
<br/>
<p align="left">
<img src = "https://github.com/navyasancheti/Textile-Defect-Detection/blob/53b735bc5e0486897e64cd49b4a82ef74a9d84a7/download%20(1).jpeg" height="210px"/>
<img src = "https://github.com/navyasancheti/Textile-Defect-Detection/blob/53b735bc5e0486897e64cd49b4a82ef74a9d84a7/Hough.png" height="210px"/>
</p>

---

<h4>Gabor & GrayScale Filter Masks </h4>
 In image processing, a Gabor filter, named after Dennis Gabor, is a linear filter used for texture analysis, which essentially means that it analyzes whether there is any specific frequency content in the image in specific directions in a localized region around the point or region of analysis. 
 In the third image, reduced frequency/light/brightness of overall image shows a distinctive dark patch indicating a defect.
 <br/>
<p align="left">
<img src = "https://github.com/navyasancheti/Textile-Defect-Detection/blob/53b735bc5e0486897e64cd49b4a82ef74a9d84a7/download%20(1).jpeg" height="150px"/>
<img src = "https://github.com/navyasancheti/Textile-Defect-Detection/blob/53b735bc5e0486897e64cd49b4a82ef74a9d84a7/GrayScale%20Transform.png" height="150px"/>
<img src = "https://github.com/navyasancheti/Textile-Defect-Detection/blob/53b735bc5e0486897e64cd49b4a82ef74a9d84a7/Gabor_filter.png" height="150px"/>
</p>

---

<h4>Masking or Image Segmentation</h4>
The defect is clearly visible after masking the image.
 <br/>
<p align="left">
 Normal Fabric Image
<img src = "https://github.com/Rajvardhan7/Textile-Detection/blob/05a14835ede3dfe1076ec69b992f88df957629f2/Defect_013.png" height="150px"/>
 <br/>
 Masked Image
<img src = "https://github.com/Rajvardhan7/Textile-Detection/blob/05a14835ede3dfe1076ec69b992f88df957629f2/013.png" height="150px"/>
</p>

---


## 2) Defect Classification

Technology/Framework Used : Numpy, Pandas, Matplotlib, Sklearn, Keras
<br/>
<br/>


<h4>Using CNN Layers : Predicting Color Blending Image Correctly</h4>
The images in the data set were categorised into 'Color','Cut','No Defect','Hole','Metal_Contamination'&'Thread'. Developed a Convolutional Neural Network Model(below figure for reference) to train the large image dataset(about 90,000 samples) in order to get high validation accuracy. 
Able to get good accuracy(about 90%) in few 50 epochs only.
<br/>
<br/>
<p align="center">
<img src = "https://github.com/navyasancheti/Textile-Defect-Detection/blob/5894d40475097a650a885e8e1612a532c2781954/Model.png" height="400px"/>
</p>
<br/>
<p align="left">
<img src = "https://github.com/Rajvardhan7/Textile-Detection/blob/8e9d1a10667f02e4c8f3086524715406572326a8/Thread.png" height="350px"/>
<img src = "https://github.com/navyasancheti/Textile-Defect-Detection/blob/53b735bc5e0486897e64cd49b4a82ef74a9d84a7/Color_blending.png" height="350px"/>
</p>
