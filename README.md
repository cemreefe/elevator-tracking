# Elevator Tracking

To track an elevator, 
- we extract the seven segment display on its display board.
- we convert it to a B&W binary image
- we can take two approaches to recognize the digits
 * a machine learning approach
 * an algorithmic approach (this works because the digits wont be handwritten, so their positions are fixed)
 
I found [an online IPTV](https://www.insecam.org/en/view/421702/) showing the interior of an elevator in Noord-Holland, Amsterdam.






The source video             |  A seven segment display  |  Our extracted image and prediction
:-------------------------:|:-------------------------:|:-------------------------:
<img src="http://145.53.212.190:8001/mjpg/video.mjpg" width="60%">  |  <img src="https://www.direnc.net/Data/EditorFiles/aciklama-gorselleri-2/7-segment-display-ekran-pinout.jpg" width="60%"> | |  <img src="https://github.com/cemreefe/elevator-tracking/tree/master/snapshots/snap_1584321703x1875768.jpg" width="100%">
