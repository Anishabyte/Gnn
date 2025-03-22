# 🚀 Graph Neural Network for Node Ranking

This repository contains the implementation for approximating betweenness and closeness centrality, two key measures used to identify influential nodes in a graph based on information spread and connectivity.

## 📌 Betweenness and Closeness Centrality
🔹 Betweenness Centrality – Measures how often a node appears on the shortest paths between other nodes.
🔹 Closeness Centrality – Evaluates how close a node is to all other nodes in the network.
🔹 A higher centrality value 📈 indicates that a node plays a crucial role in information flow and connectivity.

## 🏗️ Model Framework
⚡ The model uses shortest paths for message aggregation.


⚡ It is inductive, meaning it can be trained on one graph set and evaluated on another.


⚡ We employ two models for approximation:

🔸 GNN-Bet  for betweenness centrality

🔸 GNN-Close  for closeness centrality

⚡ Embeddings are computed by multiplying the lookup table with the adjacency matrix derived from shortest paths.


⚡ The loss function used is margin loss 🎯.


⚡ Predictions are generated using multiple MLP layers 🧠.


⚡ Kendall Tau (KT) Score 📊 is used to evaluate the ranking performance.

## ⚡ Performance and Scalability
✅ Tested on graphs with 5,000 to 10,000 nodes but can scale to larger graphs based on system capabilities.

📖 This implementation is based on the research paper by Sunil Kumar Marya (Tokyo Institute of Technology).

