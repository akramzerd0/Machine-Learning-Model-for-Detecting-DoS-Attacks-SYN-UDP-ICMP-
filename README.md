# Machine-Learning-Model-for-Detecting-DoS-Attacks-SYN-UDP-ICMP-

# 🛡️ DoS Attack Detection using Machine Learning

## Project Overview
This project aims to detect **Denial of Service (DoS) attacks** using Machine Learning and Deep Learning techniques.  
The model classifies network traffic into:
- Normal traffic
- SYN Flood
- UDP Flood
- ICMP Flood

---

## Objectives
- Build a dataset from real network traffic
- Apply Machine Learning models to classify attacks
- Compare model performance
- Analyze results using appropriate metrics (F1, Recall, etc.)

---

## Dataset

The dataset was created manually by simulating real attacks:

- SYN Flood  
- UDP Flood  
- ICMP Flood  
- Normal traffic  

### Data Collection Process
- Traffic captured using **Wireshark**
- Converted from `.pcap` to `.csv` using **CICFlowMeter**

### Preprocessing Steps
- Removed irrelevant features (IP, ports, timestamps)
- Handled missing and infinite values
- Encoded labels into numerical format
- Merged and shuffled datasets

---

## Models Used

### Decision Tree
- Simple and interpretable model
- Result: High accuracy (~98%)
- Issue: Overfitting

### MLP (Multilayer Perceptron)
- Neural network model
- Better generalization
- Result: ~70–76% accuracy

---

## Evaluation Metrics

The following metrics were used:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

> Note: Accuracy alone is not reliable due to class imbalance.

---

## Results

| Model          | Accuracy | Comments        |
|----------------|---------|----------------|
| Decision Tree  | ~98%    | Overfitting   |
| MLP            | ~76%    | Best model    |

---

## Limitations

- Dataset size is relatively small
- Real-world traffic is more complex
- Class imbalance affects performance
- Some attacks (e.g., UDP flood) are harder to detect

---

## Future Improvements

- Use larger and more realistic datasets
- Try advanced models (Random Forest, XGBoost)
- Hyperparameter tuning
- Real-time deployment (streaming detection)

---

## Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- TensorFlow / Keras
- Wireshark
- CICFlowMeter

---

## 📁 Project Structure
project-folder/
│
├── data/
├── notebooks/
├── images/
├── README.md
└── requirements.txt

## How to Run

```bash
# Clone the repo
git clone https://github.com/your-username/project-name.git

# Install dependencies
pip install -r requirements.txt

# Run notebook
jupyter notebook
