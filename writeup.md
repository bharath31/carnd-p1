# Finding Lanes on the Road

The objective of this project is to develop a software pipeline to identify lane lines on the road. The software pipeline is first tested on a series of images and then applied over a video stream. 

# Reflection

### How the pipeline works

The pipeline first detects lanes in a set of images and uses the same techinque to detect lanes in a stream of video. The RGB images are converted to grayscale and gaussian blur is applied over them. Using canny edge detection, we then find the edges and extrapolate lines over the strongest edges. For a video stream, we essentially perform the same operations over every video frame which is inturn an image. The fl_image method comes in handy during lane detection on video streams. 

###  Shortcomings 

The above algorithm works best for smooth and straight lanes. When used on lanes with bumps and curves, this algorithm will fail to detect lanes. This algorithm will also fail in the event of bad weather. 


### Improvements

The current implemntation has some jitters. Pre-processing the images would result in a smoother extrapolation. We can use the intelligent flag on hough lines coupled with other parameters to detect curved lanes. 
