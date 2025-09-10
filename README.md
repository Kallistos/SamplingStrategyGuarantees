# Performance Modeling of Software Configurations Through the Lens of Scenario Theory

This directory contains the supplementary material for the paper "Performance Modeling of Software Configurations Through the Lens of Scenario Theory" submitted to the ACM SIGSOFT International Symposium on Foundations of Software Engineering (FSE) 2026.

## Abstract

This work introduces a novel probabilistic framework to evaluate the guarantees that different sampling strategies offer for estimating performance bounds of configurable software systems. We leverage scenario theory to establish a foundation for analyzing sampling strategies beyond uniform random sampling, introducing measures such as posterior risk, posterior confidence, confidence discrepancy, and integrated confidence discrepancy.

## Structure

The directory is structured as follows:

- `Readme.md`: This file.
- `data/sampling/`: The raw sampling and measurement data used in the paper, organized by case study and sampling strategy.
- `main.ipynb`: The main Jupyter notebook containing the code used to analyze the data and produce the results in the paper.
- `SRS-sampling.ipynb`: The Jupyter notebook containing the code used to sample the data with the Statistical Recursive Search (SRS) algorithm.
- `results/`: Directory where generated plots and figures are saved (created automatically when running the notebooks).

## Key Components

### Data Analysis (`main.ipynb`)
The main notebook contains the complete analysis pipeline:
- **Data processing**: Loading and merging measurement data with sampling configurations
- **Posterior risk calculation**: Computing empirical probabilities for performance bounds
- **Confidence analysis**: Calculating posterior and prior confidence levels
- **Visualization**: Generating plots for confidence discrepancies and integrated confidence measures
- **Results for RQ1**: Confidence discrepancy analysis across different sampling strategies
- **Results for RQ2**: Sample size impact analysis on integrated confidence discrepancy
- **Discussion plots**: Detailed analysis for specific case studies (e.g., Polly)

### Sampling Strategy Implementation (`SRS-sampling.ipynb`)
Contains the implementation and execution of the Statistical Recursive Search (SRS) algorithm used as one of the evaluated sampling strategies.

## Requirements

To run the analysis, you need:
- Python 3.x
- Jupyter Notebook
- Required packages: `matplotlib`, `numpy`, `pandas`, `scipy`, `seaborn`, `collections`, `bisect`, `os`

## Usage

1. Ensure all required Python packages are installed
2. Run `main.ipynb` to reproduce the analysis and generate figures
3. Generated plots will be saved in the `results/` directory
4. Data files for TikZ/PGFPlots are saved in `data/sampling/` for paper figure generation

## Case Studies

The evaluation includes seven configurable software systems:
- 7z (Compression performance)
- Berkeley DB (Database performance)
- Dune (Scientific computing performance)
- Hipacc (Image processing performance)
- Java GC (Garbage collection performance)
- LLVM (Compiler performance)
- Polly (Loop optimization performance)

## Sampling Strategies Evaluated

- Uniform Random
- Distance-based
- Solver-based
- Statistical Recursive Search (SRS)
- BAITAL (s=1 through s=5)
- Henard
- Grammar-based

## Output

The code produces:
- Confidence discrepancy plots for all case studies and sampling strategies
- Sample size analysis showing integrated confidence discrepancy trends
- Raw data files in CSV format for external plotting tools
- Statistical analysis results supporting the paper's research questions
