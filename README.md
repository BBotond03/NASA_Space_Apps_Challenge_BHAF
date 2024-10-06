# NASA-Space-Apps-Challenge-B.H.A.F.

In this project, we aim to reduce power consumption in space by reducing the size of seismic event data. We achieve this by using algorithms and filtering the data. In this GitHub repository, we provide example databases, along with relevant algorithms that detect seismic events and filters that help clean the data for better detection.

## Documentation
For detailed documentation, you can access our project [here](https://drive.google.com/file/d/1356yBqcECAjn_dYa0D1YLX2tcMhEJhN8/view?usp=sharing).

## main_algo
Our best working and most versatile algorithm. It detects the start and end of a seismic event, as well as the entire seismic event itself based on the dampening of the data. It achieved nearly 99% precision on the test data, with a certain confidence interval.

## STA/LTA
In this file, we used the STA/LTA algorithm to detect the start of a seismic event. It also employs a k-means filtering algorithm to detect quick, irrelevant peaks in the data.

## RNN
This approach uses a recurrent neural network to analyze data. The main problem is the same as with a CNN (Convolutional Neural Network): it overfits the data on the training set.

## Test
This file primarily works with the `main_algo`, but it can be modified for other algorithms as well. It returns the ratio of correct detections to the total number of detections.

## demo_notebook
This notebook was provided to us by NASA to help us get started with the problem. It includes basic file handling, data plotting, and other useful features.

## filter
This filter uses a Segmented Adaptive Filter and a Wavelet Transform. These were combined to produce clear data with significantly reduced noise.

## integral_method
This method integrates the data across batches, then calculates the average of these integrals. If the average exceeds a certain threshold, it detects a seismic wave.

## Filter
Various filtering approaches were applied to the data. Upon evaluation, these filters were found to be not entirely useful.

## RAW_ID
This method uses the peaks in the seismic data to determine the locations of events in the given file. A red vertical line is plotted as an approximation of the earthquake's beginning.
