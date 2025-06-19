
#  AdIQ: Predicting Ad Conversion Using Neural Networks and Classical Machine Learning Models

## Problem Statement & Dataset

In today’s e-commerce landscape, understanding which ads convert is critical to optimizing digital strategy.  
This project explores how Machine Learning can predict **whether an ad will lead to conversion**, based on various features of Adidas product listings.  
We use a real-world dataset (`adidas_usa.csv`) with fields like price, availability, and product metadata to build our classification models.  
The goal: compare different ML strategies, Neural Networks with optimization techniques vs. classical ML models like Logistic Regression.

---

## 📊 Discussion of Findings

| Instance | Optimizer Used | Regularizer Used | Epochs | Early Stopping | # Layers | Learning Rate | Accuracy | F1 Score | Recall | Precision |
|----------|----------------|------------------|--------|----------------|----------|----------------|----------|----------|--------|-----------|
| 1        | Default        | None             | 20     | No             | 3        | Default         | 0.8976   | 0.9095  | 0.9528 | 0.9266    |
| 2        | Adam           | L2               | 20     | Yes            | 3        | 0.001           | 0.8661   | 0.9257  | 1.0    | 0.8617    |
| 3        | RMSprop        | L1               | 20     | No             | 3        | 0.0005          | 0.8267   | 0.8971  | 0.9056 | 0.8888    |
| 4        | Adam           | None             | 20     | Yes            | 3        | 0.005           | 0.8346   | 0.9198  | 1.0    | 0.8346    |
| 5	       |Liblinear       |	L2               | 200    | No             | 3        |  Default        | 0.9370   | 0.9565  | 0.9500 | 0.9633    |


---

## Which Combination Worked Better?

The best F1 score was achieved by:
- **Model 2**: Adam Optimizer, L2 regularization, Learning Rate = 0.001, with Early Stopping
- **Model 4** (identical performance, different learning rate)
  
---

##  Neural Network vs Classical ML?

While both approaches performed similarly in this dataset, **Logistic Regression matched the neural networks** in all major metrics—F1, Accuracy, Precision, and Recall.

However, the **neural network models offered more flexibility** for applying optimization techniques like:
- Dropout
- Learning Rate tuning
- Early Stopping

This flexibility becomes critical with more complex, high-dimensional data.

---

These can be loaded for further prediction or evaluation.

---

## 🚀 How to Run This Project

To run the project on your local machine:

1. **Clone the Repository**
```bash
git clone https://github.com/your-username/ad-conversion-prediction.git
cd ad-conversion-prediction
```

2. **(Optional) Create a Virtual Environment**
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

3. **Install Dependencies**
```bash
pip install -r requirements.txt
```

4. **Launch the Notebook**
```bash
jupyter notebook
```
Open the notebook: `Summative_Intro_to_ml_[Lievin_Murayire_number]_assignment.ipynb`

---

## 🎥 Video Presentation
The accompanying 5-minute video explains:

- My implementation logic
- Parameter tuning
- Libraries used
- Results of each model (as seen in the table above)

https://youtu.be/eDdwCyXkXvE
