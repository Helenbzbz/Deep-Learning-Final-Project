# Deep-Learning-Final-Project

## Overview
This project is a deep learning endeavor focused on developing a graph-based recommendation system using PyTorch and PyTorch Geometric. It consists of several key parts: data exploration, data pre-processing, model design, model training, and model evaluation. This project uses the MovieLens100K and IMDB datasets.

## Installation
To set up your environment to run the `Deep_Learning_Project.ipynb` notebook, you need to install the required dependencies. You can do this by creating a `requirements.txt` file with the following contents:

```
torch
torch-geometric
torch-sparse
torch-scatter
torch-cluster
numpy
pandas
matplotlib
seaborn
```

Then, run the following command to install these packages:

```bash
pip install -r requirements.txt
```

## Project Structure

### Part 1: Data Exploration
- **Datasets Used**: MovieLens100K and IMDB datasets.
- **Tasks Performed**: 
  - Downloading the datasets using PyTorch.
  - Performing exploratory data analysis to understand dataset characteristics.

### Part 2: Pre-Process Data
- **Task Performed**:
  - Pre-processing of MovieLens and IMDB datasets.
  - Creation of new Dataset Classes for each dataset.
  - Initialization of two DataLoader instances for each dataset (with and without sampling).

### Part 3: Model Designing
- **Models Defined**:
  - `NGCF`: A basic model class for Neural Graph Collaborative Filtering.
  - `NGCF_Final`: An advanced version of the NGCF model with additional features and optimizations.
- **References**:
  - [Link Prediction on Heterogeneous Graphs with PyG](https://medium.com/@pytorch_geometric/link-prediction-on-heterogeneous-graphs-with-pyg-6d5c29677c70)
  - [NGCF-PyTorch GitHub Repository](https://github.com/huangtinglin/NGCF-PyTorch/tree/master/NGCF)
  - [Neural Graph Collaborative Filtering Implementation](https://github.com/xiangwang1223/neural_graph_collaborative_filtering/blob/master/NGCF/NGCF.py)
  - [Reproducing Neural Graph Collaborative Filtering](https://medium.com/@meuleman.mathias/reproducing-neural-graph-collaborative-filtering-a8982c7d3df6)
  - [Recommender Systems with GNNs in PyG](https://medium.com/stanford-cs224w/recommender-systems-with-gnns-in-pyg-d8301178e377)

### Part 4: Model Training
- **Task Performed**:
  - Training of 10 different models based on various parameters.
    - Datasets: MovieLens; IMDB
    - Soft Sampling: Yes; No
    - Number of NGCF Layers: 2; 3; 4
    - Risk Function: Total Loss; MSE
  - Visualization of training errors (MSE & Log Error) to monitor model performance.

### Part 5: Model Evaluation
- **Evaluation Technique**:
  - Definition of an `evaluate_model` function.
  - Generation of test loss for each of the 10 models to assess their performance.

## Usage
To use this notebook:
1. Ensure you have Jupyter Notebook or Jupyter Lab installed.
2. Open `Deep_Learning_Project.ipynb` in your Jupyter environment.
3. Run the cells in order to execute different parts of the project.
