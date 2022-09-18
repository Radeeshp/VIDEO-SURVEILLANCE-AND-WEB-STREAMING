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
 ### Theory:
   A class SingleMotionDetector has been defined with the functions update and detect
  
   class has the objects accumWeight and bg.
 ### Imports Used :
      -import numpy as np
    
      -import imutils
    
      -import cv2
 ### update(self,image):
   Theory:
   
        This function is used to update the background image that is too be compared with the current image to detect 
        
        motion in the detect() function
      
   Built In Functions Used :
         
        -cv2.accumulateWeighted()
        
        
   Activity Diagram:
   
![Screenshot 2022-09-18 110446](https://user-images.githubusercontent.com/82216452/190896846-4df0aab3-131e-45da-839e-84bcd9ea8160.png)  
      
  
 ### detect(self,image,tVal=25):
   Theory:
        
         This function is used to detect motion.The paremeters  image and tVal are passed.  
   
         First the absolute difference between the background image and current image is obtained and stored, then threshold the image 
  
         , perform erosion and dilation . Then the countours in the image are detected and we find the biggest countour and send return it.  
   
   Built In Functions Used :
        
        -cv2.absdiff()
        -cv2.threshold()
        -cv2.erode()
        -cv2.dilate()
        -cv2.findContours()
        -cv2.boundingRect()
        -min()
        -max()
        -imutils.grab_contours()
   
   
   Activity Diagram:
   
![Screenshot 2022-09-18 154446](https://user-images.githubusercontent.com/82216452/190897126-fcb86741-ed29-4d1b-9a80-2d79a31f8c60.png)


##   webstreaming.py:
  ####Theory:
    We starting processing the live stream or video and detect motion in it.And then mark this motion and stream it to a website.
    The Flask application is used t stream to the website as its light weight, and a common web framework.
    
    
