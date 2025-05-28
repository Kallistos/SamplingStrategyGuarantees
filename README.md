# Evaluation Scripts for the paper "Evaluating Risk and Confidence in Performance Bounds of Configuration Sampling Strategies"

This repository contains the data and evaluation script to reproduce the results, graphs and tables for the ASE submission "Evaluating Risk and Confidence in Performance Bounds of Configuration Sampling Strategies".

You can find the data in the `sampling` subfolder inside the `data` folder. The files in the `tikz` subfolder of `data` contains the csv files that are used to generate the tikz code for the graphs in the paper.

To reproduce the results, you can use the jupyter notebook `main.ipynb`. There, you can also include your own data and compute the results for your own sampling strategies.
The notebook `SRS-sampling.ipynb` contains the code to compute the results for the SRS sampling strategy based on the paper from Oh et al. (2017).
The notebook `data_conversion.ipynb` contains the code to convert the data from `main.ipynb` to a better suited format for the tikz code generation.
