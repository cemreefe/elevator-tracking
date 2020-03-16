# Elevator Tracking

To track an elevator, 
1. we extract the seven segment display on its display board.
2. we convert it to a B&W binary image
3. we can take two approaches to recognize the digits
  * a machine learning approach
  * an algorithmic approach (this works because the digits wont be handwritten, so their positions are fixed)
 
I found [an online IPTV](https://www.insecam.org/en/view/421702/) showing the interior of an elevator in Noord-Holland, Amsterdam. After extracting the 7 segment board form the image, I straightened it to easily detect the 7 display leds.
There is no Computer Vision ML involved here. By just taking the average values of where the leds are ought to be, we can see if the led is on or not. 

After determining if each led is on or off, we convert this reading into a binary string of length seven. Which can be used as a key to our digit dictionary.

key | value
:--------:|:--:
 1111110 | 0 
 0110000 | 1 
 1101101 | 2 
 1111001 | 3 
 0110011 | 4 
 1011011 | 5 
 1011111 | 6 
 1110000 | 7 
 1111111 | 8 
 1111011 | 9 

Now that we can read what digit is written in the seven segment display, log the first floor we read after connecting to the IPTV.
Every time te digit changes, we add a new log in the format "&lt;local system time&gt; : &lt;digit&gt;".

## EDA

<i>incoming</i>




The source video           |  Extracted image          |  B&W image and prediction |  A seven segment display
:-------------------------:|:-------------------------:|:-------------------------:|:-------------------------:
<img src="https://github.com/cemreefe/elevator-tracking/blob/master/media/elevator1.png" width="60%"> | <img src="https://github.com/cemreefe/elevator-tracking/blob/master/media/elevator2.png" width="60%">  |  <img src="https://github.com/cemreefe/elevator-tracking/blob/master/snapshots/snap_1584321703x1875768.jpg" width="100%"> | <img src="https://www.direnc.net/Data/EditorFiles/aciklama-gorselleri-2/7-segment-display-ekran-pinout.jpg" width="70%"> |
