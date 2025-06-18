
#  Predicting Ad Conversion Using Neural Networks and Classical Machine Learning Models

## Problem Statement & Dataset

In today’s e-commerce landscape, understanding which ads convert is critical to optimizing digital strategy.  
This project explores how Machine Learning can predict **whether an ad will lead to conversion**, based on various features of Adidas product listings.  
We use a real-world dataset (`adidas_usa.csv`) with fields like price, availability, and product metadata to build our classification models.  
The goal: compare different ML strategies—Neural Networks with optimization techniques vs. classical ML models like Logistic Regression.

---

## 📊 Discussion of Findings

| Instance | Optimizer Used | Regularizer Used | Epochs | Early Stopping | # Layers | Learning Rate | Accuracy | F1 Score | Recall | Precision |
|----------|----------------|------------------|--------|----------------|----------|----------------|----------|----------|--------|-----------|
| 1        | Default (Adam) | None             | 20     | No             | 3        | Default         | 0.9921   | 0.9933   | 0.9867 | 1.0000    |
| 2        | Adam           | L2               | 20     | Yes            | 3        | 0.001           | 0.9921   | 0.9953   | 0.9907 | 1.0000    |
| 3        | RMSprop        | L1               | 20     | No             | 3        | 0.0005          | 0.9843   | 0.9876   | 0.9780 | 0.9974    |
| 4        | Adam           | None             | 20     | Yes            | 3        | 0.005           | 0.9921   | 0.9953   | 0.9907 | 1.0000    |
| 5 (LogReg)| liblinear     | L2               | —      | No             | —        | —               | 0.9921   | 0.9953   | 0.9907 | 1.0000    |

---

## Which Combination Worked Better?

The best F1 score was achieved by:
- **Model 2**: Adam Optimizer, L2 regularization, Learning Rate = 0.001, with Early Stopping
- **Model 4** (identical performance, different learning rate)
- **Logistic Regression** surprisingly performed **equally well** with only L2 regularization and no tuning beyond solver choice.

---

##  Neural Network vs Classical ML?

While both approaches performed similarly in this dataset, **Logistic Regression matched the neural networks** in all major metrics—F1, Accuracy, Precision, and Recall.

However, the **neural network models offered more flexibility** for applying optimization techniques like:
- Dropout
- Learning Rate tuning
- Early Stopping

This flexibility becomes critical with more complex, high-dimensional data.

---

## 🎥 Video Presentation

