# VIDEO SURVEILLANCE AND WEB STREAMING
Motion is detected through a camera and it's streamed to a website 

##AIM
To detect motion through a live camera feed and stream the live feed to a website.

## Description:
A project in python using open cv to detect motion in a camera feed and stream it to a website.

## Project Structure:
  templates
    
    --index.html
  
  _init_.py
  
  singlemotiondetector.py
  
  webstreaming.py
  
## singlemotiondetector.py:
 #### Theory:
   A class SingleMotionDetector has been defined with the functions update and detect
   class has the objects accumWeight and bg.
   ####Imports Used :
      -import numpy as np
    
      -import imutils
    
      -import cv2
   #### 
   #### update(self,image):
  
  
  
  
  
   ##### detect(self,image,tVal=25):
   This function is used to detect motion.The paremeters  image and tVal are passed.  
   
   First the absolute difference between the background image and current image is obtained and stored, then threshold the image 
  
   , perform erosion and dilation . Then the countours in the image are detected and we find the biggest countour and send return it.  
  
   #### Activity Diagram:
   ![Detect](https://user-images.githubusercontent.com/82216452/189920778-e5bc99f3-ad9d-40f4-b910-817d1b4d827c.jpeg)


##   webstreaming.py:
  ####Theory:
    We starting processing the live stream or video and detect motion in it.And then mark this motion and stream it to a website.
    The Flask application is used t stream to the website as its light weight, and a common web framework.
    
    
