# Driver Activity Recognition using Fuzzy Rule-Based Network

## Overview
This project implements **Driver Activity Recognition** using a **Fuzzy Rule-Based Network**. The system employs **fuzzy logic** to classify driver activities based on extracted features from the **StateFarm Distracted Driver Dataset**. The primary goal is to assess driver alertness and identify risky behaviors.

## Algorithm Explanation
A **Fuzzy Rule-Based Network** leverages fuzzy logic principles to map driver activity levels to alertness scores using predefined membership functions and rules.

### **Working Mechanism:**
1. **Fuzzy Variables:**
   - **Activity** (Input): Represents driver actions with values ranging from 0 to 10.
   - **Alertness** (Output): Indicates the driver's level of attention.
   
2. **Membership Functions:**
   - **Activity & Alertness** are categorized into three levels: **Poor, Average, and Good**.

3. **Fuzzy Rules:**
   - If **Activity is Poor**, then **Alertness is Poor**.
   - If **Activity is Average**, then **Alertness is Average**.
   - If **Activity is Good**, then **Alertness is Good**.

4. **Inference and Decision Making:**
   - The fuzzy system processes each driver's activity level and assigns an alertness score.
   - The final alertness score is mapped to a discrete class for classification.

## Dataset
- **Training Set:** Preprocessed driver activity features extracted from the dataset.
- **Test Set:** Unseen driver activity data for performance evaluation.

## Implementation Steps
1. **Load and preprocess the dataset.**
2. **Define fuzzy variables and membership functions.**
3. **Apply fuzzy rules to infer driver alertness.**
4. **Convert fuzzy outputs into discrete classification labels.**
5. **Evaluate the model's performance using accuracy, precision, recall, and F1-score.**

## Performance Metrics
Due to dataset constraints, the model’s performance is currently limited:
- **Train Accuracy:** 21%
- **Test Accuracy:** 20%
- **Overall Accuracy:** 20%
- **Precision:** 49%
- **Recall:** 20%
- **F1-Score:** 11%

### **Why is Accuracy Low?**
1. **Simplified Rules:** A more complex rule set may improve classification.
2. **Limited Feature Representation:** The model relies on a single aggregated activity measure.
3. **Dataset Size:** Increasing the dataset would enhance learning.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/driver-activity-recognition.git
   cd driver-activity-recognition
   ```
2. Install dependencies:
   ```bash
   pip install numpy scikit-learn scikit-fuzzy
   ```
3. Run the script in **Google Colab** or locally:
   ```bash
   python fuzzy_driver_activity.py
   ```

## Future Improvements
- Implement **more granular fuzzy membership functions**.
- Optimize **fuzzy rule definitions** for better classification.
- Explore **hybrid models combining fuzzy logic with machine learning**.
- Expand the dataset for improved accuracy.
