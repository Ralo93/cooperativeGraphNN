
# Cooperative Graph Neural Network (CoGNN)

## Overview

This repository implements a **Cooperative Graph Neural Network (CoGNN)** designed to tackle benchmark graph learning tasks. 
The model combines principles of cooperation and competition among neural units to improve performance on challenging 
datasets while maintaining computational efficiency.

By leveraging cooperative learning paradigms, CoGNN optimizes information flow across graph structures, making it particularly 
suited for applications requiring fine-grained node and edge predictions.

## Features

- **Cooperative Neural Network Architecture**: A novel framework combining cooperation and traditional GNN mechanisms.
- **Benchmark Dataset Evaluation**: Supports evaluation on widely-used datasets such as:
  - Cora
  - Citeseer
  - PubMed
  - ogbn-arxiv
- **Highly Modular Implementation**: Easily extendable to custom datasets and use cases.
- **Performance Metrics**: Integrated tools to measure and compare accuracy, F1-score, precision, and recall.

## Key Features and Capabilities

### Attention Visualization
- Implements functions to **extract and visualize attention weights** in Graph Attention Networks (GATs).
- Provides node-level and edge-level attention insights through **visualizations** and **detailed logging**.

### Top Contributors Analysis
- Identifies and visualizes the **top contributors** (1-hop and 2-hop neighbors) to a node's prediction in GAT layers.
- Highlights key nodes contributing to model decisions.

### Flexible Graph Neural Network Architectures
- Includes implementations for multiple GNN models:
  - **GAT (Graph Attention Network)**: Employs multi-head attention to aggregate node information.
  - **GCN (Graph Convolutional Network)**: Focuses on convolutional operations for graph-structured data.
  - **Enhanced GCN**: Adds regularization (dropout, batch normalization) and depth for improved learning.
  - **TransformerAttentionModule**: Explores transformer-style attention for graph nodes.

### Modular Design for Custom Applications
- Supports custom datasets using the `torch_geometric.data.Data` class.
- Handles common tasks like adding self-loops, data preprocessing, and train-test splitting.

### Training and Evaluation Workflow
- **Training Loop**: Logs performance metrics and supports early stopping based on validation accuracy.
- **Evaluation Metrics**: Computes accuracy and generates classification reports for insights into model performance.
- **Visualization Tools**: Visualizes graph embeddings and key contributors to node predictions.

### Additional Features
- **Custom Dataset Handling**: Configured for benchmarking on datasets like Cora, Citeseer, and PubMed.
- **Minesweeper Visualization**: Converts graphs into a Minesweeper-like field for experimental visualization of nodes and edges.
- **Scalable Attention Mechanisms**: Integrates efficient multi-head attention for large graphs.


## Installation

### Prerequisites

- Python >= 3.8
- PyTorch >= 1.10
- PyTorch Geometric
- NetworkX

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/username/CoGNN.git
   cd CoGNN
   ```
2. Create a virtual environment and activate it:
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Train the Model

Run the following command to train CoGNN on a benchmark dataset:
```bash
python train.py --dataset cora --epochs 100 --learning_rate 0.01
```

### Evaluate the Model

To evaluate the model on a specific dataset:
```bash
python evaluate.py --dataset citeseer
```

### Visualize Results

Generate visualizations for graph embeddings:
```bash
python visualize.py --dataset pubmed
```

## Project Structure

```
CoGNN/
│
├── data/               # Benchmark datasets (Cora, Citeseer, PubMed, etc.)
├── models/             # Model architectures
├── utils/              # Utility scripts for data processing and metrics
├── train.py            # Training script
├── evaluate.py         # Evaluation script
├── visualize.py        # Visualization script
├── requirements.txt    # Required dependencies
└── README.md           # Project documentation
```

## Contributing

We welcome contributions! Please fork the repository, create a new branch for your feature, and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions, suggestions, or issues, please contact:
- **Name**: Raphael von Lottner
- **Email**: your.email@example.com
- **GitHub**: [Your GitHub Profile](https://github.com/username)

---

Happy Graph Learning! 🎉
