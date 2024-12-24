# Plant-Disease-Detection-using-Object-Detection

**A comprehensive AI-powered system for early detection and classification of plant diseases, enabling smarter agricultural practices and improved crop yields.**

## Introduction  

Plant diseases are a major threat to global agriculture, affecting crop quality and yield. Traditional disease detection methods are manual, time-consuming, and prone to error. This project leverages advancements in computer vision and machine learning to develop an automated plant disease detection system using object detection techniques.  

The dataset used comprises over 61,000 images of healthy and diseased plant leaves, with annotations in YOLO format. Various object detection models, including Faster R-CNN, YOLOv5, YOLOv7, YOLOv8, and YOLOv11, were evaluated to identify the most suitable approach for real-world agricultural applications.  

## Problem Statement  

Conventional plant disease detection relies on manual inspection, which is inefficient and prone to human error. The challenge is to develop a scalable, automated solution using object detection models that can accurately classify and localize diseases in plant images, ensuring timely intervention and sustainable farming practices.  


## Objectives  

1. **Early Detection:** Enable rapid and accurate identification of plant diseases.  
2. **Automation:** Automate disease detection using advanced object detection models.  
3. **Scalability:** Ensure the solution is adaptable to diverse agricultural settings.  
4. **Efficiency:** Balance computational efficiency with detection accuracy for real-time applications.  

## Dataset Description  

- **Source:** Mendeley Plant Leaf Dataset  
- **Content:**  
  - 61,486 images across 39 classes (diseased and healthy leaves).  
  - Bounding box annotations for object detection tasks.  
- **Augmentation Techniques:**  
  - Image flipping, Gamma correction, noise injection, PCA color augmentation, rotation, and scaling.  
- **Split:**  
  - Training: 60%  
  - Validation: 20%  
  - Testing: 20%  


## Methodology  

1. **Preprocessing:**  
   - Resize images to 640x640 pixels.  
   - Normalize bounding box coordinates.  
2. **Model Training:**  
   - Leverage pre-trained weights.  
   - Optimize hyperparameters (e.g., learning rate, batch size).  
3. **Evaluation Metrics:**  
   - Precision, Recall, mAP@50, and mAP@50-95.  
4. **Visualization:**  
   - Annotated bounding boxes for detected regions.  


## Performance Metrics  

| Model          | Precision (%) | Recall (%) | mAP@50 (%) | mAP@50-95 (%) | Notes                        |  
|----------------|---------------|------------|------------|---------------|------------------------------|  
| YOLOv5s        | 99.2          | 99.2       | 99.5       | 98.8          | Balanced speed and accuracy. |  
| YOLOv5n        | 99.3          | 98.9       | 99.5       | 96.1          | Good precision.              |  
| YOLOv7         | 80.6          | 12.4       | 10.2       | 74.53         | Optimized for speed.         |  
| YOLOv8s        | 99.5          | 99.5       | 99.5       | 99.5          | Best overall performance.    |  
| YOLOv8n        | 99.4          | 99.1       | 99.5       | 99.4          | Good overall performance.    |  
| YOLOv11n       | 70.18         | 60.74      | 70.6       | 70.55         | Lightweight for edge devices.|  
| YOLOv11s       | 74.11         | 64.39      | 74.6       | 74.53         | Enhanced for complex tasks.  |  
| Faster R-CNN   | 1.00          |            |            |               | Heavy compuatational demands.|  

---

## Results and Discussion  

YOLOv8 emerged as the most effective model, excelling in both precision and recall, making it suitable for real-world agricultural applications. Lightweight versions like YOLOv11n demonstrated efficiency for edge deployment, while Faster R-CNN provided robust detection for complex scenarios.  
