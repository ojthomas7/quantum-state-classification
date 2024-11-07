# Machine Learning: Electron Orbital Classification using TensorFlow

- Modelling the wavefunctions and electron orbitals of the hydrogen atom
- Building, training and testing a ML model for electron orbital classification

## Motivation

Having studied machine learning in various ways and completed a few guided projects on codecademy.com, I wanted to develop and present my skills by creating an independently led project. Inspired by my degree, I wanted to explore machine learning in the context of quantum mechanics.

Here I explore how machine learning can be used to classify quantum states/ electron orbitals about the hydrogen atom. First of all, within the file electron-orbitals.ipynb I construct a couple of functions which come together to plot a 2-D cross section of the probability density of an electrons orbit about the hydrogen nucleus (explained below). The code saves this as an image (.png) for use later. The file electron-orbital-classification.ipynb is where i construct my ML model.

The images are loaded into the file and the quantum data (n, l and m) is extracted from the filename of each image. This training data is then labelled before we use TensorFlow to build the model. After the models construction it is trained over 200 epochs before it takes the input of an image, created using electron-orbitals.ipynb. The model then makes a prediction of the principle quantum number of the input.

## Notes

The model in this form did not end up being very accurate, not even being able to classify orbital states within its own training set, let alone states outside. This could be for a variety of reasons:

- Training data quality: the training data set is very small, filled with very similar images at varying levels of zoom, confusing the model.
- Model architecture: the model used an overly complex architecture for the task, with no physics-informed input.

Model accuracy could  be impeded by the quality of the training data set. The images may not be dinstinctly different enough between states, and often look similar e.g. [n, 0, 0] states and [3, 2, 2], [4, 2, 2], [5, 2, 2] etc:

<p align="center">
  <img src="training-data/1_0_0.png" alt="Image 1" width="200"/>
  <img src="training-data/3_0_0.png" alt="Image 2" width="200"/>
  <img src="training-data/5_0_0.png" alt="Image 3" width="200"/>
</p>
<p align = "center">
<i>Electron density plot for [n, 0, 0] quantum states</i>
</p> 
<p align="center">
  <img src="training-data/3_2_2.png" alt="Image 1" width="200"/>
  <img src="training-data/4_2_2.png" alt="Image 2" width="200"/>
  <img src="training-data/5_2_2.png" alt="Image 3" width="200"/>
</p>

<p align = "center">
<i>Electron density plot for [(3,4,5), 2, 2] quantum states</i>
</p> 
