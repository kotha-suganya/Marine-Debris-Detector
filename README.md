# Marine-Debris-Detector

## 📌 Project Overview
Marine debris is a critical threat to global oceanic ecosystems. This repository contains a pipeline that handles:
1. **Data Ingestion:** Automatically fetching raw data from the NASA/Source Cooperative S3 repository.
2. **Data Parsing:** Converting NASA's bounding box coordinates (`.npy`) into standard normalized YOLO format.
3. **Model Training:** Training an ultralightweight `YOLOv8n` model optimized for rapid detection.
4. **Inference & Evaluation:** Testing the trained weights on web or local test images to visually verify detections.




The model successfully initiates training on 739 images containing 1640 distinct debris instances. And predicts the presence of debris based on the confidence score.

Initial metrics indicate steady optimization within the first few epochs:

Image Size: 256x256

Hardware: Tesla T4 GPU (~0.48G memory utilization per batch)

Optimization Progression:

Epoch 1: mAP50 = 0.105

Epoch 7: mAP50 = 0.284 (Showing rapid localization gains)
