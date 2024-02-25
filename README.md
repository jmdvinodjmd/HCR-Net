
## Implementation for HCR-Net:
[1] Chauhan, V.K., Singh, S. & Sharma, A. HCR-Net: a deep learning based script independent handwritten character recognition network. Multimed Tools Appl (2024). [paper](https://doi.org/10.1007/s11042-024-18655-5), [preprint](https://arxiv.org/abs/2108.06663)



## ARCHITECTURE

<p align="center">
<img align="middle" src="./figures/architecture.png" width="800" />
</p>


## Folder and File Structure
----------------------------
<pre>
./                                  - This is top directory.
./README.md                         - This is readme file.
./HCR-Net.ipynb                     - This Jupyter Notebook contains implementation of HCR-Net [1]. By default, it runs with UCI Devanagari Numeral dataset, but you need to change this to run with your script.
./HCR-Net-Augmentation.ipynb        - This Jupyter Notebook runs HCR-Net with image-augmentation.
./Study-miss-classification.ipynb   - This Jupyter Notebook is used study mis-classification of HCR-Net.
./learning_rate.py                  - This python file implements custom learning rates used by HCR-Net.
|data/                              - Contains the datasets used in the expriments
|exps/                              - Contains raw files used for running experiments with different scripts as reported in paper.
|results/                           - This folder contains trained models (on UCI Devanagari Numeral dataset).
|figures/                           - This folder contains images of architecture and convergence results.
</pre>    



This documentation provides information to the users and developers for using HCR-Net.


Table of Contents
=================
- Installation
- Quick Start Example
- Run your script
- More Information


## Installation
- Download the latest version of the library from the following URL: https://github.com/jmdvinodjmd/HCR-Net
- Prerequisite:
    + Tensorflow, seaborn and sklearn.
I think, as long as these libraries are compatible with each other, the code should run with any version and should produce results similar to reported in the paper.

## Quick Start Example
It's very easy to run the library - simply run the 'HCR-Net.ipynb' jupyter notebook. This will run the HCR-Net model with default dataset, i.e., UCI Devanagari Numeral dataset, present in the data folder. Please cite the data source from [here](https://archive.ics.uci.edu/ml/datasets/Devanagari+Handwritten+Character+Dataset).

The experimental results for running HCR-Net with UCI Devanagari Numeral dataset are given below.

<p align="center">
<img width="350" src="./figures/loss.png">&nbsp; &nbsp; &nbsp; &nbsp;<img width="350" src="./figures/acc.png" width="400">
</p>
<br /><br />

## Run your script
- To run your script without image-augmentation, please open 'HCR-Net.ipynb' jupyter notebook and change the following:
    + path of data folders
    + number of samples
    + number of classes

You may like to set number of epochs and learning rate for phase one and two or batch-size.
- Similarly, to run your script with image-augmentation, you need to use 'HCR-Net-Augmentation.ipynb', and to study mis-classification, you have to use 'Study-miss-classification.ipynb'.

It is recommended to run this code for at least 5 times due to randomness associated with different machines/architectures. For this you can set seed from 1-5.


## More Information
If you find this code useful, then please consider citing our work.

## Contact us
[Vinod Kumar Chauhan](https://sites.google.com/site/jmdvinodjmd/)
