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
  
### singlemotiondetector.py:
#### Theory:
  A class SingleMotionDetector has been defined with the functions update and detect
  class has the objects accumWeight and bg.
  ##### detect(self,image,tVal=25):
  This function is used to detect motion.The paremeters  image and tVal are passed.  
  
  # What is tVal
  First the absolute difference between the background image and current image is obtained and stored, then threshold the image , perform erosion and dilation . Then the countours in the image are detected and we find the biggest countour and send return it.  
  
   
