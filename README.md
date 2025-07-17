# Link-prediction-across-platforms
# 🔗 Link Prediction in Cross-Domain Social Networks

This project implements a **cross-domain link prediction system** that connects users on **Twitter** to relevant **GitHub repositories** based on a **heterogeneous graph neural network**.

We integrate real-world tweet content, hashtags, semantic topics, and GitHub repository metadata to form a rich heterogeneous graph. The system learns to recommend relevant GitHub repositories to users based on their social media activity.

> 📄 Published Report: [sns.pdf](./sns%20(1).pdf)  
> 🧠 Model Framework: PyTorch Geometric + GraphSAGE + MLP  
> 📊 Visualization: Interactive Graph using PyVis

---

## 📌 Highlights

- 🌐 **Heterogeneous Graph**:
  - Tweets, Hashtags, Topics, Repositories as different node types
  - Typed relations: `Tweet → Hashtag`, `Hashtag → Topic`, `Topic → Repository`

- 🧠 **Heterogeneous Graph Neural Network**:
  - Built using PyTorch Geometric
  - Two-layer **GraphSAGE** with `HeteroConv`
  - Deep **MLP-based link predictor** to learn tweet–repo associations

- 🔍 **Link Prediction**:
  - Predicts potential links between **tweets** and **GitHub repositories**
  - Trained on positive/negative samples using **binary cross-entropy loss**

- 📈 **Visualization**:
  - Subgraph visualization (up to 300 tweets) using **PyVis**
  - Generates interactive HTML graph with color-coded nodes and edges

- 📊 **Recommendations**:
  - After training, recommends **top GitHub repositories** for each user
  - Outputs predictions with confidence scores in CSV format

---

## 🚀 Getting Started

### 🧩 Dependencies

Install the required libraries:

```bash
pip install torch torch-geometric scikit-learn pyvis
