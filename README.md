# Adrenocortical Carcinoma Classifier Deployment on AWS

## Project Summary
Developed and deployed a deep learning classifier for adrenocortical carcinoma (ACC) detection with 96.65% accuracy. Hosted via Flask API on AWS for real-time access by clinicians within the hospital environment.

## Problem Statement
Early-stage diagnosis of adrenocortical carcinoma is difficult due to its rarity and symptom overlap. A fast, accessible ML model was needed to aid clinical decision-making using imaging and structured features.

## Tools & Technologies Used
- **ML Model**: CNN (custom-trained)  
- **Deployment Stack**: Flask, Docker, AWS EC2  
- **Languages**: Python  
- **Data**: Histopathology images, diagnostic reports  
- **Interface**: Internal clinician-facing browser app (form upload, prediction output)

## Model Development
- Preprocessed image data to balance positive/negative samples  
- Trained convolutional neural network using augmented ACC datasets  
- Evaluated with stratified K-Fold CV and confusion matrix analysis  
- Exported model as a serialized `.pkl` object for production use

## System Architecture
```
Upload Image ─▶ Flask API ─▶ CNN Model ─▶ Diagnosis Output ─▶ Clinician Interface
```

## Results & Clinical Value
- Achieved **96.65%** diagnostic accuracy in held-out test evaluations  
- Allowed oncologists to validate ACC suspicions quickly from image scans  
- Reduced diagnostic turnaround time for complex cases

## Maintenance
- AWS EC2 instances monitored via CloudWatch  
- Data logging used for offline retraining on new diagnostic examples

## Challenges & Learnings
- Class imbalance addressed with data augmentation and reweighting  
- Interpretability tools (Grad-CAM) added to support trust in predictions  
- Clinician training ensured effective use of output interface

## Team Collaboration
- Worked alongside oncology departments and histopathology teams  
- Frontend mockups iterated with medical staff to ensure usability

## Code Availability
Due to the medical nature of the data and internal use case, code and interface details are confidential.
