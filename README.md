````markdown
# 🐒 Monkeypox Skin Image Detection (MSID) using ResNet50 + Multi-Head Attention

This project implements an **Enhanced Monkeypox Detection Model** using the **Monkeypox Skin Image Dataset (MSID)**.  
It combines **ResNet50** feature extraction with a **Multi-Head Attention mechanism**, enabling robust classification of **Monkeypox vs. Non-Monkeypox** skin lesion images.  

---

## 📂 Dataset Preparation

- **Dataset**: [Monkeypox Skin Image Dataset (MSID)](https://www.kaggle.com/datasets/arafathussain/monkeypox-skin-disease-dataset)  
- **Splitting**:
  - Train (80%)  
  - Test (20%)
- **Augmentation**: Applied on training images (rotation, flips, zoom, contrast) for generalization.  
- **Further Split**: Augmented dataset divided into **Train** and **Validation**.  
- **Normalization**: Pixel values of train, validation, and test datasets normalized.

---

## 🏗 Model Architecture

- **Base Model**: Pre-trained **ResNet50** (ImageNet weights, top layers removed, frozen).  
- **Custom Layers**:
  - Multi-Head Attention Layer (captures global feature relationships).  
  - Global Average Pooling.  
  - Dropout (0.5).  
  - Dense (750 units, ReLU).  
  - Dense (Softmax, 2 classes: Monkeypox / Non-Monkeypox).  

---

## ⚙️ Training Strategy

- **Optimizer**: SGD (learning rate = 0.001)  
- **Loss**: Sparse Categorical Crossentropy  
- **Metrics**: Accuracy  
- **Epochs**: 50  
- **Datasets**:  
  - Training: Augmented + normalized data  
  - Validation: Separate validation split  

---

## 📊 Evaluation

- **Validation Dataset**: Validation accuracy/loss tracked per epoch.  
- **Test Dataset**: Final evaluation.  
- **Performance Metrics**:
  - Accuracy (Train, Validation, Test)  
  - Precision, Recall, F1-Score (weighted)  
  - Confusion Matrix  

**✅ Achieved Test Accuracy: 97.35%**

---

## 📈 Visualization

- **Accuracy Curve**: Training vs Validation accuracy across epochs.  
- **Loss Curve**: Training vs Validation loss across epochs.  
- **Confusion Matrix Heatmap**: Monkeypox vs Non-Monkeypox classification performance.  

---

## 🚀 Results

- Robust Monkeypox vs. Non-Monkeypox classifier.  
- High accuracy with strong generalization capability.  
- Potential application as a **clinical decision support system** for early Monkeypox detection.  

---

## 🔮 Future Work

- Extend dataset with more skin disease classes for multi-class classification.  
- Fine-tune ResNet50 layers for improved accuracy.  
- Experiment with advanced attention mechanisms (e.g., Vision Transformer).  

---

````

---

## 📜 Citation

If you use this work, please cite:

```
@inproceedings{sah2025monkeypox,
  title={An Enhanced Monkeypox Detection Model with Deep Residual Networks based Multi-Head Attention Approach},
  author={Gupta, Shashi Kumar and Sah, Krishna Kumar and Raut, Ankush and Muduli, Debendra and Sharma, Santosh Kumar and Jaysawal, Bishal},
  booktitle={Proceedings of the 16th International Conference on Computing Communication and Networking Technologies (ICCCNT)},
  year={2025}
}
```

---

## 🏆 Conference Submission Info

* **Conference**: 16th International Conference on Computing, Communication and Networking Technologies (**ICCCNT 2025**)
* **Paper ID**: 2505
* **Title**: *An Enhanced Monkeypox Detection Model with Deep Residual Networks based Multi Head Attention Approach*
* **Authors**: Shashi Kumar Gupta, Krishna Kumar Sah, Ankush Raut, Debendra Muduli, Santosh Kumar Sharma, Bishal Jaysawal

---

## 👨‍💻 Author

* **Krishna Kumar Sah**
  [GitHub](https://github.com/Krishnasah206) | [LinkedIn](https://linkedin.com/in/krishna-sah)

```
