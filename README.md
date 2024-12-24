# SMS Spam Detection with Predictive Coding Network

This project implements an SMS Spam Detection system using a **Predictive Coding Network (PCN)**. It preprocesses the popular SMS Spam dataset from Kaggle, trains a model, and evaluates its performance. Batch size and epoch experiments were conducted to optimize the model's accuracy and efficiency.

---

## Dataset
The project uses the **SMS Spam Collection Dataset** from Kaggle. The dataset contains labeled SMS messages (spam or ham) that were preprocessed and vectorized to serve as input for training.

Dataset link: [SMS Spam Dataset](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)

---

## Preprocessing Steps
1. **Load Dataset**: 
   - Extracts the `Label` and `Message` columns from the CSV file.
2. **Label Encoding**:
   - Labels (`spam` and `ham`) are converted into binary numeric format.
3. **Text Vectorization**:
   - Messages are vectorized using **TF-IDF Vectorizer** with 1,000 features.
4. **One-Hot Encoding**:
   - Labels are further transformed into one-hot vectors for model compatibility.
5. **Train-Validation Split**:
   - Data is split into 80% training and 20% validation sets.
6. **Save Preprocessed Data**:
   - Processed data is saved as `.npy` files for reuse.

---

## Model Training
- The **Predictive Coding Network (PCN)** is used for training.
- Multiple experiments were conducted with varying batch sizes and epochs to analyze their impact on model performance.

---

## Results
The table below summarizes key results:

| **Epochs** | **Batch Size** | **Simulation Time (h)** | **Accuracy** |
|------------|----------------|-------------------------|--------------|
| 5          | 50             | 0.0088                 | 0.8834       |
| 15         | 100            | 0.0164                 | 0.8834       |
| 30         | 150            | 0.0263                 | 0.8843       |
| 30         | 50             | 0.0592                 | 0.8852       |

For detailed results, see the `Results` section in the code.

---

## Repository Structure
