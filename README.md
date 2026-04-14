# 🌊 Intelligent Flood Forecasting using Delay-Aware Terrain-Informed Graph Network (DT-FPN)

## 📌 Overview
This project presents an intelligent flood forecasting system using a Delay-Aware Terrain-Informed Flood Propagation Network (DT-FPN). The model represents river systems as directed graphs and incorporates terrain-based delays to simulate realistic downstream flood propagation.

The goal is to improve prediction accuracy and capture flood peak timing more effectively compared to traditional models.

---

## 🎯 Objectives
- Model river networks as directed graphs  
- Incorporate terrain features (slope, elevation, length)  
- Simulate delay-aware flood propagation  
- Compare performance with baseline models (LSTM, Synchronous GNN)  
- Evaluate forecasting accuracy using standard metrics  

---

## 🧠 Methodology

### 1. Data Generation
- Synthetic river network (Directed Acyclic Graph)
- Terrain attributes:
  - Slope
  - Elevation drop
  - Reach length
- Flood events generated with time delays across nodes

### 2. Models Implemented
- **LSTM**: Captures temporal dependencies only  
- **Synchronous GNN**: Captures spatial dependencies  
- **DT-FPN (Proposed)**:
  - Uses terrain-informed delay modeling  
  - Applies asynchronous message passing  
  - Simulates realistic flood propagation  

### 3. Evaluation Metrics
- RMSE (Root Mean Square Error)  
- MAE (Mean Absolute Error)  
- NSE (Nash–Sutcliffe Efficiency)  
- Peak Timing Error (PTE)  

---

## 📊 Results

| Model | RMSE | MAE |
|------|------|------|
| LSTM | 0.0101 | 0.0089 |
| Synchronous GNN | **0.0034** | **0.0026** |
| DT-FPN (Proposed) | 0.0056 | 0.0043 |

### 🔍 Observations
- Graph-based models outperform traditional LSTM  
- DT-FPN improves over LSTM by capturing spatial-temporal dependencies  
- Delay-aware modeling enhances realism of flood propagation  
- Synchronous GNN performs best in current setup, but DT-FPN provides more physically meaningful modeling  

---

## 📈 Sample Output
- Model comparison bar graphs (RMSE, MAE)  
- Flood prediction curves  
- Peak timing analysis  

*(Add your output images here)*

---

## 🛠️ Tech Stack
- Python  
- PyTorch  
- NumPy  
- Matplotlib  

---

## ▶️ How to Run

```bash
pip install torch numpy matplotlib
python main.py
