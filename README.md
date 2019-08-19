# Gradient Based Optimization Methods

## Summary
Exploring the performance of 3 gradient based optimization methods:
1. Conventional Gradient Descent 
2. Barzilai and Borwein (or BB) method
3. Nesterov's accelarated gradient descent

One of these methods is later used to denoise an image.

## Denoising an image by reducing Total Variation (TV)
The intuition is based on the  principle that signals with excessive and possibly spurious detail have high total variation, that is, the integral of the absolute gradient of the signal is high. According to this principle, reducing the total variation of the signal subject to it being a close match to the original signal, removes unwanted detail whilst preserving important details such as edges.

This noise removal technique has advantages over simple techniques such as linear smoothing or median filtering which reduce noise but at the same time smooth away edges to a greater or lesser degree. By contrast, total variation denoising is remarkably effective at simultaneously preserving edges whilst smoothing away noise in flat regions. [3]

For a more detailed explanation with equation check the Gradient_Based_Optimization_Methods.ipynb

## Results
**For a general logisitc regression problem**

<p align="center">
  <img width="460" height="350" src="https://github.com/mithun-bharadwaj/Gradient_Based_Optimization_Methods/blob/master/images/Performance.JPG">
</p>

**Image denoising results**

Nosiy Image         |  Denoised Image
:----------------------------------------------------------:|:------------------------------------------------:
<img width="400" height="350" src="https://github.com/mithun-bharadwaj/Gradient_Based_Optimization_Methods/blob/master/images/Noisy.JPG"> |<img width="400" height="350" src="https://github.com/mithun-bharadwaj/Gradient_Based_Optimization_Methods/blob/master/images/Denoised.JPG"> 



## System requirements
1. Jupyter notebook
2. numpy
3. matplotlib

## How to run
Place all 3 files which are in the src folder of this repository in the same root folder and run the cells in Gradient_Based_Optimization_Methods.ipynb

## References
1. https://statweb.stanford.edu/~candes/papers/adap_restart_paper.pdf
2. https://www.cs.umd.edu/~tomg/course/cmsc764/L7_grad_descent.pdf
3. https://en.wikipedia.org/wiki/Total_variation_denoising

This was part of the Advanced Numerical Optimization (CMSC 764) course at the University of Maryland, College Park. The utility.ipynb which contains methods to create classification problems for logistic regression and its unit tests is credited to Prof. Tom Goldstein.

