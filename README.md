# Advanced driver assistance system (ADAS)

## Lane Detection:

• The road conditions may not be the same in every part of the region. Sometimes the road 
may be freeway, town road, etc. Every road has different lane markings. 

• For every condition there will be different types of road markings. These road markings 
variation is calculated and then the road lane is detected.

• Major functions used in the lane detection are Canny, Masking, Hough lines.

• This code will detect the road lane lines perfectly if both sides of the lane’s markings are 
visible. The accuracy is 100% for it.

• The road having the road markings as dotted markings or the broken line markings may 
need the use of math to calculate the lane in continuous form.

• Code will show the broken lines as straight line using the slope and average calculations 
of lines.

• Whenever there is a turn in the video, road lines will be detected if the car stays in the lane 
and not on the road line as this will change the region of interest. 

• The roads with no markings will cause a problem for detection as the functionality will 
predict the wrong points dependent on the previous lane lines detected.

• If any other vehicle comes right in front of our vehicle, the lane detection makes some 
random predictions of the hidden lane line.

• A single ongoing lane will be detected on the multilane road. Crossings and intersections 
of road has some false detections of the road lane.



## Pedestrian Detection:

• Pedestrian detection detects the pedestrians which are captured in the specific region of 
interest.

• Main functions used in pedestrian detection are HOG Descriptor, SVM detector.

• Pedestrians which are directly in front of the vehicle will be detected. 

• This work does not focus on occlusion handling; hence the occluded pedestrian regions are 
not considered.

• Pedestrians are detected in the video by red rectangles.

• the pedestrians are not usually seen on the freeway, but as the vehicle enters the downtown 
area, the pedestrians are detected in it.



## Stop Sign detection:

• Stop signs are detected and shown for every frame if there are any.

• Main functions used to detect stop signs are HSV image conversion, Hough Circles, ROI.

• Areas having unclear stop signs are difficult to detect.

• The accuracy of stop sign detection depends on the clarity of video.



## Stop Light Detection:

• Stop light is detected whenever there is red traffic light on the road. 

• This function is detected using Hough Circles.

• The main functions of Stop light detection are conversion to HSV, taking only the upper 
half of the frame (ROI).

• Stop light is detected for every frame.

• A red circular marker is drawn around the red traffic light to warn the driver about the stop 
light and, text is also shown on the screen as “STOP LIGHT” in red color as a warning 
message. 

• By using command line arguments, the lane detection, pedestrian detection, stop sign 
detection and stop light detection can be toggled to turn it ON/OFF
