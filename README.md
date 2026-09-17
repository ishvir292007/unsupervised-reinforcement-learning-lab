# Unsupervised & Reinforcement Learning Lab

> **Applied Machine Learning Practicals for Business Intelligence & Decision-Making**

A practical machine learning repository demonstrating **Unsupervised Learning** and **Reinforcement Learning** concepts through simple, business-oriented Python implementations. The project focuses on customer segmentation using **K-Means Clustering** and reward-based decision-making through a **Reinforcement Learning route optimization example**.

---

## Overview

This repository explores two important machine learning paradigms:

* **Unsupervised Learning** — discovering hidden patterns and groups within data without predefined labels.
* **Reinforcement Learning** — learning decision-making strategies through actions, feedback, and rewards.

The practical is designed to connect machine learning concepts with real-world business applications such as **customer segmentation, personalized marketing, delivery optimization, and decision systems**.

---

## Key Objectives

By completing this practical, you will understand:

* Customer segmentation using **K-Means Clustering**
* How clustering identifies groups of similar customers
* Business interpretation of machine-generated clusters
* The fundamental workflow of **Reinforcement Learning**
* The roles of **Agent, Environment, Action, and Reward**
* The difference between **Exploration and Exploitation**
* How machine learning can support business decision-making

---

## Project Structure

```text
unsupervised-reinforcement-learning-lab/
│
├── part-a/
│   └── unsupervised-learning/
│       └── Unsupervised_and_Reinforcement_Learning_Practical_Name.ipynb
│
├── screenshots/
│   └── customer-segmentation.png
│
└── README.md
```

The practical notebook is intended to be placed under:

```text
part-a/unsupervised-learning/
```

as specified in the project submission requirements.

---

# Part A — Unsupervised Learning

## Customer Segmentation with K-Means

The first part addresses a business problem faced by an online retailer: identifying different types of customers based on their **monthly spending** and **app visit frequency**.

The dataset contains:

| Feature          | Description                 |
| ---------------- | --------------------------- |
| Customer         | Customer identifier         |
| Monthly Spending | Customer's monthly spending |
| App Visits       | Number of app visits        |

The K-Means algorithm is configured to create **three customer groups**.

### Example Dataset

```text
Customer A → ₹9,000 spending → 20 app visits
Customer B → ₹8,500 spending → 18 app visits
Customer C → ₹1,200 spending → 3 app visits
Customer D → ₹1,500 spending → 4 app visits
Customer E → ₹5,000 spending → 10 app visits
Customer F → ₹5,500 spending → 12 app visits
Customer G → ₹8,800 spending → 19 app visits
Customer H → ₹1,800 spending → 5 app visits
```

### Technologies Used

```python
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
```

The implementation uses **Pandas** for data handling, **Scikit-learn's KMeans** for clustering, and **Matplotlib** for visualization.

---

## K-Means Implementation

The clustering model is configured with three clusters:

```python
model = KMeans(
    n_clusters=3,
    random_state=42,
    n_init=10
)

df["Cluster"] = model.fit_predict(X)
```

The resulting cluster labels represent machine-generated groups. The numerical labels themselves do not indicate whether a customer is "good" or "bad"; they are simply identifiers assigned to the discovered groups.

---

## Business Application

Customer segmentation can help organizations design differentiated strategies for different behavioral groups.

Potential applications include:

* **Loyalty rewards**
* **Personalized recommendations**
* **Customer re-engagement campaigns**
* Targeted marketing
* Behavioral analysis

The practical specifically encourages interpreting clusters based on **spending, app visits, and customer behavior** rather than relying only on cluster numbers.

---

# Part B — Reinforcement Learning

## Route Optimization Concept

The second part introduces the fundamentals of Reinforcement Learning using a simplified delivery-route scenario.

A delivery company has two possible routes:

```text
Route A
Route B
```

The system receives a reward based on delivery performance, with faster delivery receiving a higher reward.

---

## Reinforcement Learning Framework

The practical demonstrates the following components:

| Component       | Example                       |
| --------------- | ----------------------------- |
| **Agent**       | Delivery decision system      |
| **Environment** | Roads and traffic             |
| **Action**      | Choose Route A or Route B     |
| **Reward**      | Delivery performance feedback |

The core learning cycle is:

```text
Action
   ↓
Reward
   ↓
Learn from Result
   ↓
Improve Future Decisions
```

---

## Reward Analysis

The practical uses the following example rewards:

```python
route_rewards = {
    "Route A": [5, 4, 6, 5, 4],
    "Route B": [8, 9, 7, 10, 8]
}
```

The average reward for each route is then calculated:

```python
for route, rewards in route_rewards.items():
    average_reward = sum(rewards) / len(rewards)
    print(route, "Average Reward =", average_reward)
```

This illustrates how reward feedback can be used to compare available decisions.

---

# Exploration vs Exploitation

A key Reinforcement Learning concept demonstrated in the practical is the balance between **exploration** and **exploitation**.

### Exploration

Trying a new or less-used option to gather additional information.

```text
Example:
Try Route A even when Route B has historically
performed better.
```

### Exploitation

Selecting an option that is already known to perform well.

```text
Example:
Choose Route B because it has previously
generated higher rewards.
```

---

## Technologies

| Technology       | Purpose                           |
| ---------------- | --------------------------------- |
| **Python**       | Core programming language         |
| **Pandas**       | Dataset creation and manipulation |
| **Scikit-learn** | K-Means clustering                |
| **Matplotlib**   | Data visualization                |
| **Google Colab** | Notebook execution environment    |

---

## Machine Learning Concepts Covered

```text
Machine Learning
│
├── Supervised Learning
│   └── Learning from known answers
│
├── Unsupervised Learning
│   └── Customer Segmentation
│       └── K-Means Clustering
│
└── Reinforcement Learning
    └── Learning from Actions & Rewards
        └── Route Optimization
```

The practical contrasts these three learning paradigms through business examples.

---

## Running the Project

### 1. Open Google Colab

Open the notebook in Google Colab.

### 2. Run the Notebook

Execute the cells sequentially from top to bottom.

### 3. Review the Outputs

Analyze:

* Customer dataset
* K-Means cluster assignments
* Customer segmentation visualization
* Route rewards
* Average route rewards
* Exploration example
* Exploitation example

### 4. Complete the Reflection

The practical includes reflection questions covering clustering, K-Means, customer segmentation, Reinforcement Learning, Agent, Action, Reward, and Exploration vs Exploitation.

---

## Learning Outcomes

After completing this practical, you should be able to:

* Explain the purpose of unsupervised learning.
* Describe how K-Means clustering works at a basic level.
* Interpret customer clusters from a business perspective.
* Explain the fundamental components of Reinforcement Learning.
* Distinguish between exploration and exploitation.
* Connect machine learning techniques to practical business problems.

---

## Business Use Cases

The concepts demonstrated here can be extended to real-world applications such as:

### Customer Analytics

```text
Customer Data
     ↓
Behavior Analysis
     ↓
K-Means Clustering
     ↓
Customer Segments
     ↓
Targeted Business Strategies
```

### Delivery Optimization

```text
Routes
  ↓
Actions
  ↓
Delivery Outcomes
  ↓
Rewards
  ↓
Decision Learning
  ↓
Improved Route Selection
```

---

## Repository Status

**Status:** Academic / Practical Implementation

**Domain:** Machine Learning · Artificial Intelligence · Business Analytics

**Environment:** Google Colab

**Language:** Python

---

## Author

**Ishvir Singh Matharoo**

BBA FinTech & AI
Chitkara University

---

## License

This repository is intended for **educational and academic purposes**.

---

## Acknowledgements

Developed as part of practical coursework covering **Unsupervised Learning and Reinforcement Learning**, with an emphasis on understanding machine learning concepts through business-oriented examples.
