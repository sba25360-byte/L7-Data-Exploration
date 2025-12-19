# L7 Data Exploration & Preparation: Spam Filtering Analysis

## Project Overview
This project explores the "Spambase" dataset to identify key characteristics that distinguish spam emails from non-spam (ham). The analysis includes data cleaning (handling missing values and non-numeric artifacts), Exploratory Data Analysis (EDA), and Dimensionality Reduction using Principal Component Analysis (PCA).

### Dataset Attributes:
- **Word Frequency:** 48 attributes measuring the percentage of specific words.
- **Character Frequency:** 6 attributes measuring the percentage of specific characters (e.g., `!`, `$`).
- **Capital Run Lengths:** 3 attributes measuring sequences of capital letters.
- **Target:** `is_spam` (Boolean).

---

## 1. Exploratory Data Analysis (EDA)
During the exploration phase, we identified that spam emails significantly differ from regular emails in their use of urgency symbols and financial keywords.



### Key Findings:
* **Urgency Indicators:** Spam emails show a much higher frequency of the exclamation mark (`!`) and the dollar sign (`$`).
* **Capitalization:** Total capital run lengths are significantly higher in spam, often used to grab the recipient's attention.


## 2. Principal Component Analysis (PCA)
To address the **Curse of Dimensionality** (57 features), PCA was applied to reduce the feature space while retaining **99.5% of the variance**.



* **Dimensionality Reduction:** We reduced the dataset from 57 features to a smaller set of principal components without significant information loss.
* **Separation:** The PCA scatter plot reveals clear clustering, suggesting that even in a reduced space, spam and non-spam messages remain distinguishable.
