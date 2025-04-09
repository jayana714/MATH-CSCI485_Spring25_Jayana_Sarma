# **Heuristic and Gradient-Based Perceptron Learning on a Binary Classification Task**

## **Introduction to Perceptron Learning**
Perceptron algorithms are foundational tools for binary classification. They work by learning a linear decision boundary between two classes based on input features. This project explores two distinct approaches:

- **Heuristic Perceptron**: A continuous update mechanism using sigmoid activation and gradient descent based on prediction error.
- **Gradient Based Perceptron**: A rule-based update method that adjusts weights only when predictions are misclassified using a thresholded sigmoid output.

The goal is to evaluate how both methods perform under varying learning rates on a linearly separable dataset.
---

## **Overview**
This project implements and compares two types of perceptrons trained on a 2D binary classification dataset (`data.csv`) using three learning rates (0.01, 0.1, 1.0). The experiments analyze:

- Decision boundary evolution over epochs  
- Accuracy of predictions  
- Log loss trends  
- Impact of learning rate on convergence and model behavior  

---

## **Requirements**
To run this project, you need the following Python libraries:

- `numpy`  
- `pandas`  
- `matplotlib`  
- `scikit-learn` (optional for preprocessing or evaluation)
## **Dataset Description**
The dataset (`data.csv`) contains:

- `x1`, `x2`: Numeric input features  
- `y`: Binary labels (0 or 1)

The dataset is linearly separable and ideal for binary classification experiments.

---

## **Project Steps**

### 1. Data Loading
- Load the dataset using pandas  
- Extract features and target  
- Visualize the input space to confirm linear separability

---

### 2. Heuristic Perceptron

#### **Algorithm**
```python
y_hat = sigmoid(np.dot(w, x) + b)
error = y - y_hat
w = w + lr * error * x
b = b + lr * error
```

#### **Results**
| Learning Rate | Accuracy | Observations                                |
|---------------|----------|---------------------------------------------|
| 0.01          | 93%      | Smooth convergence, subtle boundary movement |
| 0.1           | 93%      | Best performance, fast and stable            |
| 1.0           | 91%      | Aggressive updates, risk of overshooting     |

---

### 3. Gradient-Based Perceptron (Thresholded Updates)

#### **Algorithm**
```python
y_hat = sigmoid(np.dot(w, x) + b)
predicted_class = 1 if y_hat >= 0.5 else 0

if predicted_class != y:
    if predicted_class == 0:
        w += lr * x
        b += lr
    else:
        w -= lr * x
        b -= lr
```

#### **Results**
| Learning Rate | Accuracy | Observations                                |
|---------------|----------|---------------------------------------------|
| 0.01          | 91%      | Stable and slow learning                     |
| 0.1           | 93%      | Fast convergence and strong performance      |
| 1.0           | 79%      | Unstable, large jumps and reduced accuracy   |

---

### 4. Log Loss Curve Analysis

| Learning Rate | Log Loss Behavior                                      |
|---------------|--------------------------------------------------------|
| 0.01          | Smooth, steady decline                                 |
| 0.1           | Fastest drop and lowest final loss                     |
| 1.0           | Early instability, eventual convergence with higher loss |

---

### 5. Comparison Summary

| Metric          | Heuristic (Part 1)       | Gradient-Based (Part 2)         |
|-----------------|--------------------------|------------------------------|
| Learning Style  | Gradient-based           | Rule-based (on error class)  |
| Activation      | Sigmoid + error feedback | Sigmoid + hard threshold     |
| Accuracy Range  | 91–93%                   | 79–93%                       |
| Log Loss Trend  | Smooth                   | Depends on learning rate     |
| Best LR         | 0.1                      | 0.1                          |

### Conclusion

Both perceptron models successfully separated the binary classes on the dataset.

- **Heuristic perceptron (Part 1)** was more stable and forgiving with larger learning rates.
- **Gradient-based perceptron (Part 2)** worked well at moderate learning rates but struggled with overshooting at `lr=1.0`.
- Log loss curves and decision boundary visualizations confirmed how learning rate impacts training behavior.
