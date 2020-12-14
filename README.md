# Eye-Blink-Detector

Unlike traditional image processing methods for computing blinks which typically involve some combination of:

Eye localization.

Thresholding to find the whites of the eyes.

Determining if the “white” region of the eyes disappears for a period of time (indicating a blink).


The eye aspect ratio is instead a much more elegant solution that involves a very simple calculation based on the ratio of distances between facial landmarks of the eyes.

Based on the work by Soukupová and Čech in their 2016 paper, Real-Time Eye Blink Detection using Facial Landmarks, we can then derive an equation that reflects this relation called the eye aspect ratio (EAR):

https://www.pyimagesearch.com/wp-content/uploads/2017/04/blink_detection_equation.png

Where p1, …, p6 are 2D facial landmark locations.

The numerator of this equation computes the distance between the vertical eye landmarks while the denominator computes the distance between horizontal eye landmarks, weighting the denominator appropriately since there is only one set of horizontal points but two sets of vertical points.
