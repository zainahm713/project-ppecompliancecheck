# PPE Compliance Detection Using YOLO11

**Tier 3 – Safety-Critical Computer Vision**

**Team Members:**
- Eva Abou Harb
- Mary Ann Mastri
- Zain Ahmed

---

## Tier Selection

**Tier 3 – Safety-Critical Computer Vision (PPE Detection)**

This is classified as Tier 3 because it detects personal protective equipment (PPE) in the workplace 
environment. Missed detections can impact worker safety, with death as the ultimate consequence, 
and consequently create financial risk to the company.

The system is designed to identify required PPE such as helmets, safety vests, gloves, boots, and 
goggles to help with safety compliance monitoring.

## Problem Statement

Safety requirements in construction and industrial workplaces reduce the risk of injury when wearing 
personal protective equipment (PPE). Manual monitoring is time-consuming and risks human error. This 
project will automate PPE detection using computer vision to increase workplace safety and compliance.

## Solution Overview

This project uses the YOLO11 object detection model to identify workers and detect whether required 
PPE is being worn. The trained model performs object detection on images and can be exported to 
ONNX for deployment in lightweight inference applications. The goal is to achieve real-time detection 
running on a live video feed.

## Technical Approach

- **Technique:** Deep Learning Object Detection
- **Model:** YOLO11 (Ultralytics)
- **Framework:** Python, Ultralytics YOLO
- **Computer Vision:** OpenCV
- **Visualization:** Matplotlib
- **Deployment:** ONNX Runtime and Flask API
- **Development Environment:** Google Colab with GPU acceleration

---

## Dataset Plan

### Dataset Source
- Public PPE Detection Dataset (Roboflow/Kaggle)
- https://www.kaggle.com/
- https://roboflow.com/

### Classes
- Helmet
- No Helmet
- Vest
- Goggles
- No Goggles
- Person
- Boots
- No Boots
- Gloves
- No Gloves

### Annotations
YOLO bounding-box format

### Dataset Size
Training, validation, and test image splits with corresponding label files.

### Public Datasets
- https://www.kaggle.com/datasets/mustafatayyipbayram/ppe-detection
- https://universe.roboflow.com/training-rs3kg/ppe-detection-rrq9i

---

## Evaluation Metrics

**Primary Metric**
- Mean Average Precision (mAP@50-95)

**Secondary Metrics**
- Precision
- Recall
- mAP@50
- Inference Speed
- Number of detections per image

## Week-by-Week Plan

| Week | Task |
|------|------|
| Week 1 | Project planning, literature review, dataset selection |
| Week 1 | Configure Google Colab environment and load dataset |
| Week 2 | Verify dataset, visualize images, prepare YOLO configuration |
| Week 2 | Train baseline YOLO model and tune hyperparameters |
| Week 3 | Evaluate model performance using validation metrics |
| Week 3 | Perform inference on test images and analyze results |
| Week 4 | Export trained model to ONNX and benchmark inference |
| Week 4 | Develop Flask API for deployment and prepare final documentation |

## Resources Needed

| Resource | Purpose |
|----------|---------|
| Google Colab GPU | Model training |
| Google Drive | Dataset and model storage |
| Python 3.x | Development |
| Ultralytics YOLO | Object detection framework |
| OpenCV | Image processing |
| Matplotlib | Visualization |
| ONNX Runtime | Model deployment |
| Flask | REST API deployment |

### Estimated Cost
- Google Colab — Free
- Public datasets — Free
- Open-source software libraries — Free
- HCC GPU use — Free

---

## Risks & Mitigation

| Risk | Probability | Mitigation |
|------|-------------|------------|
| Low detection accuracy | Medium | Increase training epochs, tune hyperparameters, apply data augmentation |
| Missing or incorrect labels | Medium | Verify dataset annotations and visually inspect training/validation images |
| Limited GPU availability | Medium | Reduce batch size or use CPU for testing before GPU training |
| Overfitting | Medium | Monitor validation metrics and use early stopping |
| Model deployment issues | Low | Export to ONNX and validate inference before deployment |

## Expected Outcomes

The completed model will automatically detect workers and identify if they are wearing the required 
PPE in the image. The trained YOLO11 model will be evaluated using standard object detection metrics 
and exported to ONNX for deployment into real-world PPE monitoring software.