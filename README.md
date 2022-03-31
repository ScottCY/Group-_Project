# Prediction of Whether a Candidate Star is a Pulsar or not

## Introduction
Background Information About Pulsars
Pulsars are rotating neutron stars that emit beams of electromagnetic radiation that is detectable on Earth (Wikimedia Foundation, 2021). Scientists use pulsars to investigate the state of matter, measure distance of cosmic objects, and even use them to test the universal force of gravity (Cofield, 2016). Machine learning classifiers are used in studying and labelling of pulsar candidates for an efficient analysis. In particular, the binary classification system is commonly used (Lyon et al., 2016).

##### About Our Project
In this project, we wish to answer the question that:
>Is the unknown star a pulsar based on its measurement of variables of interest?

##### About The Dataset
From the dataset provided by Lyon, there is a training dataset and a testing dataset; in this project, we will be using the training dataset only to perform our analysis with reason provided in method part (Lyon et al., 2016). The training dataset contains 12,528 candidates of pulsar stars. Since each pulsar produces slightly different emission patterns as they rotate, each candidate's data is averaged over many rotations of the pulsar (Lyon et al., 2016). Each candidate in the dataset is described with 8 continuous variables, and a single class variable. The first four statistics are obtained from an integrated pulsar profile, which describe a longitude-resolved version of the signal that has been averaged (Lyon et al., 2016). Variables 5 to 8 are obtained from the DM-SNR curve, where DM is a measure of dispersion signal received and SNR is the signal-to-noise ratio (Lyon et al., 2016). The last variable indicates the class of the candidate.

Variables:

1. Mean of the integrated profile - the average
2. Standard deviation of the integrated profile - a summary measure of the differences of observations from the mean
3. Excess kurtosis of the integrated profile - a measure to compare the tail with normal distribution
4. Skewness of the integrated profile - a measure of the degree of symmetry
5. Mean of the DM-SNR curve - the average
6. Standard deviation of the DM-SNR curve - a summary measure of the differences of observations from the mean
7. Excess kurtosis of the DM-SNR curve - a measure to compare the tail with normal distribution
8. Skewness of the DM-SNR curve - a measure of the degree of symmetry
9. Class - class of the candidate



## Discussion
Our model predicts unknown pulsar stars based on 17 nearest neighbors' values, and the accuracy of our model is 92.78%. Before we built the model, we expected that it would correctly predict the class of the testing data majority of the time. The finished model is able to perform what we expected. The impact of our model is significant when identifying pulsar stars since many detections of signals are actually caused by radio frequency interference (RFI) and noise, and real signals from pulsars are sometimes hard to find (Lyon et al., 2016). Our model uses mean, standard deviation, kurtosis, and skewness from integrated profiles to analyse the unknown star and make predictions, which could be used as a guide to more efficiently identify real pulsars rather than RFI. However, as the proportion of real pulsar data is relatively small compared to non-pulsar in our training set, a future question could be: can accuracy be improved by increasing the proportion of real-pulsar, as this helps our model know real-pulsar stars better?

## References
Cofield, C. (2016, April 22). What are pulsars? Space.com. Retrieved November 6, 2021, from https://www.space.com/32661-pulsars.html.

Lyon, R. J., HTRU2, doi: 10.6084/m9.figshare.3080389.v1.

Lyon, R. J., Stappers, B. W., Cooper, S., Brooke, J. M., & Knowles, J. D. (2016). Fifty Years of pulsar candidate selection: From simple filters to a new principled real-time classification approach. Monthly Notices of the Royal Astronomical Society, 459(1), 1104–1123. https://doi.org/10.1093/mnras/stw656.

Wikimedia Foundation. (2021, October 22). Pulsar. Wikipedia. Retrieved November 6, 2021, from https://en.wikipedia.org/wiki/Pulsar.
