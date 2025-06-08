# smote-ResNet
1. Project Overview
This project focuses on enhancing intrusion detection in Wireless Sensor Networks (WSNs) by combining SMOTE, a powerful class-balancing technique, with a deep learning-based feature extractor, ResNet. The experiments are conducted using the WSN-DS dataset, which includes both normal and attack traffic.

🎯 2. Objectives
To address class imbalance in the WSN-DS dataset using SMOTE.

To fine-tune a ResNet model for effective classification of WSN data.

To compare performance metrics with and without SMOTE.

To evaluate the accuracy, recall, precision, and F1-score of the model in detecting network intrusions.

📊 3. Dataset: WSN-DS
The WSN-DS dataset contains simulated data for WSN traffic including:

Normal traffic

Various attack types: Blackhole, Grayhole, Wormhole, etc.

Features include network and routing-related parameters like:

Transmission time

Packet delay

Energy consumption

Node distance and trust level

Challenge: The dataset is highly imbalanced, with far more normal records than attack records.

🔧 4. Methodology
A. Preprocessing
Normalize numerical features.

Encode categorical features (if any).

Split data into training and test sets.

B. SMOTE (Synthetic Minority Oversampling Technique)
Apply SMOTE only to the training set to synthetically oversample the minority attack classes.

Ensures balanced training for better generalization.

C. ResNet-Based Classifier
Use 1D ResNet or adapt ResNet18 (originally for images) for structured data.

Modify the final fully connected layer to output the number of classes in the WSN dataset.

D. Training
Optimizer: Adam

Loss function: CrossEntropyLoss

Epochs: 20–50

Batch size: 32

Scheduler: StepLR (optional)

🧪 5. Evaluation Metrics
Accuracy – overall correct predictions

Precision – correctness of attack predictions

Recall – ability to detect actual attacks

F1-score – harmonic mean of precision and recall

Confusion Matrix – detailed class-wise performance

📈 6. Expected Outcomes
SMOTE should significantly improve recall on minority (attack) classes.

ResNet will learn deep hierarchical patterns in WSN data, enhancing detection accuracy.

The combination will reduce false negatives, crucial in security applications.

📌 7. Conclusion
This project demonstrates how combining data-level balancing (SMOTE) with deep learning (ResNet) can improve the robustness and effectiveness of intrusion detection systems in WSNs, which are critical for IoT and sensor-based networks.
