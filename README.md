# :heartbeat:ECG Heartbeat Classification  

This project develops a sophisticated model for ECG heartbeat classification to identify various arrhythmias, leveraging the **ResNet** and **transfer learning** techniques. Utilizing the MIT-BIH Arrhythmia Dataset and the PTB Diagnostic ECG Database, the model overcomes **data imbalance** with SMOTE and ENN, achieving an optimized accuracy of 99.743%. This approach significantly enhances the detection and classification of **cardiovascular diseases**, offering a pivotal tool for medical diagnostics and patient care.  

## Dataset    
The dataset for this project comprises heartbeat signals from two renowned sources: the [Massachusetts Institute of Technology-Beth Israel Hospital (MIT-BIH) Arrhythmia Dataset](https://www.physionet.org/content/mitdb/1.0.0/ "悬停显示") and the [Physikalisch-Technische Bundesanstalt (PTB) Diagnostic ECG Database](https://www.physionet.org/content/ptbdb/1.0.0/ "悬停显示"). The MIT-BIH dataset includes 48 half-hour excerpts of two-channel ECG recordings from 47 individuals, designed primarily for arrhythmia detection research. It features 109,446 samples divided into training and testing sets, with five possible arrhythmia category labels.  

## Methodology
### Imbalanced Data
The project addresses imbalanced data prevalent in binary classification by employing the Synthetic Minority Oversampling Technique (**SMOTE**) and Edited Nearest Neighbours (**ENN**). SMOTE generates synthetic data points to achieve a balanced dataset, while ENN removes misclassified instances, enhancing the model's generalization and performance​​.

### Residual Networks (ResNet)  
ResNet, utilized in this project, incorporates **residual blocks** with skip connections that facilitate the training of deep networks by **alleviating vanishing gradient** issues. This architecture improves learning by directly propagating feature maps from earlier to later layers, optimizing the network's performance without complicating the model unnecessarily​​.  

### Transfer Learning  
The project leverages transfer learning to apply knowledge from pre-trained models on the MIT-BIH dataset to classify arrhythmias in the PTB Diagnostic ECG Database. This approach enables the reuse of learned features, reducing the need for extensive dataset-specific training and enhancing model adaptability across different tasks​​.  

### Model Tuning  
Model tuning is achieved through **cyclical learning rates** and **grid search** methods, focusing on optimizing hyperparameters for improved accuracy. **Cyclical learning rates** adjust the learning rate between set boundaries in a predefined manner, while **grid search** systematically explores various hyperparameter combinations to identify the most effective model configuration​  

## Result
ECG classification results presented with the method using a **ResNet** model architecture combined with **transfer learning**. Specifically, a **deep convolutional neural network** has been trained with a **residual block** for arrhythmia classification. The model classifies five different arrhythmias as well as a numerical control classification by diagnostic category. The best resulted accuracy on validation data is 99.743%. This accuracy is significantly higher than the related ResNet model with a 93.4% accuracy.  

Our project's model achieved remarkably high accuracy, a result that, while promising, warrants careful scrutiny. This unprecedented performance raises questions about potential overfitting, data leakage, or biases within our training dataset. Such issues could artificially inflate the model's apparent effectiveness, especially when dealing with real-world, noisy data.  

## Future direction  
To ensure the robustness and applicability of our findings, several steps to undertake:  

* ***Cross-Validation***: Implement more rigorous cross-validation techniques to assess model generalizability across different data subsets.  
* ***External Dataset Evaluation***: Test the model on additional, external ECG datasets to validate its performance in a broader context.  
* ***Complexity Reduction***: Explore simplifying the model to reduce the risk of overfitting while maintaining high accuracy.  
* ***Bias Mitigation***: Investigate and correct for any potential biases in the dataset that may contribute to overly optimistic results.  
