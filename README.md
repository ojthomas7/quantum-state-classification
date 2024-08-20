# Machine Learning: Electron Orbital Classification using TensorFlow

- Modelling the wavefunctions and electron orbitals of the hydrogen atom
- Building, training and testing a ML model for electron orbital classification

## Motivation

Having studied machine learning in various ways and completed a few guided projects on codecademy.com, I wanted to develop and present my skills by creating an independently led project. Inspired by my degree, I wanted to explore machine learning in the context of quantum mechanics.

Here I explore how machine learning can be used to classify quantum states/ electron orbitals about the hydrogen atom. First of all, within the file electron-orbitals.ipynb I construct a couple of functions which come together to plot a 2-D cross section of the probability density of an electrons orbit about the hydrogen nucleus (explained below). The code saves this as an image (.png) for use later. The file electron-orbital-classification.ipynb is where i construct my ML model.

The images are loaded into the file and the quantum data (n, l and m) is extracted from the filename of each image. This training data is then labelled before we use TensorFlow to build the model. After the models construction it is trained over 200 epochs before it takes the input of an image, created using electron-orbitals.ipynb. The model then makes a prediction of the principle quantum number of the input.
