Download Link: https://assignmentchef.com/product/solved-computer-vision-i-project-1
<br>
<span style="font-size: 2.61792em; letter-spacing: -1px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;">Motion Detection Using Simple Image Filtering</span>

The purpose of this project is to get familiar with manipulating images and image filtering techniques.

<h2>1. Motion Detection</h2>

In this project you will explore a simple technique for motion detection in image sequences captured with a stationary camera where most of the pixels belong to a stationary background and relatively small moving objects pass in front of the camera. In this case, the intensity values observed at a pixel over time is a constant or slowly varying signal, <em>except </em>when a moving object begins to pass through that pixel, in which case the intensity of the background is replaced by the intensity of the foreground object. Thus, we can detect a moving object by looking at <strong>large </strong>gradients in the <em>temporal </em>evolution of the pixel values.

<ol start="2">

 <li>Project Requirements:</li>

</ol>

<ul>

 <li>Write a program to implement the above ideas. Sample videos to test your program are available inblackboard. The basic outline of your program should be as follows:

  <ol>

   <li>Read in a sequence of image frames and make them grayscale.</li>

   <li>As enough frames are available, apply a 1-D differential operator at each pixel to compute a <em>temporal </em> iii. Threshold the absolute values of the derivatives to create a 0 and 1 mask of the moving objects.</li>

   <li>Combine the mask with the original frame to display the results.</li>

  </ol></li>

 <li>You should explore the following variations on the above basic outline:

  <ol>

   <li>For the temporal derivative filter try a simple 0<em>.</em>5[−1<em>,</em>0<em>,</em>1] filter and a 1D derivative of a Gaussian with a user defined standard deviation tsigma. Compare results running these filters; for the Gaussian filter try increasing values of tsigma. Discuss your results.</li>

   <li>Try applying a 2D spatial smoothing filter to the frames before applying the temporal derivativefilter. For the spatial smoothing filter try 3 × 3, 5 × 5 box filters and 2D Gaussian filters with a user defined standard deviation ssigma. Run the program using different amounts of smoothing. Discuss your results. Are there values that make it work better? Explain what you mean by better. iii. Vary the threshold to get the mask and see what works best. Design a strategy to select a good threshold for each image. Hint: Most pixels belonging to the background change little and thus their temporal gradients are close to zero. You can model these values as Gaussian zero mean noise and estimate the standard deviation of this noise.</li>

  </ol></li>

 <li>Write a report. The report should include:

  <ol>

   <li>Abstract, description of algorithms, experiments, values of parameters used, observations and con-clusions.</li>

   <li>Representative images that you tested the algorithms with as well as representative outputs showingboth “good” and “bad” results. iii. An appendix with your code</li>

  </ol></li>

</ul>