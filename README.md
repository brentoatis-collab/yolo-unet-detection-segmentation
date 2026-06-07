# CST 544 Week 4 Assignment  
## Object Detection and Segmentation Model Using YOLO and U-Net

### Project Overview

This project integrates YOLO for object detection and U-Net for semantic segmentation using the Pascal VOC 2012 dataset. The goal is to simulate an AI-powered smart surveillance system that can detect objects in images and segment their boundaries.

### Dataset

The Pascal VOC 2012 dataset contains labeled images for object recognition, detection, and segmentation. This project uses the segmentation dataset to train U-Net and sample images for YOLO object detection.

### Models Used

#### YOLO

YOLO was used for object detection because it detects objects quickly in a single forward pass. This makes it useful for real-time applications such as smart surveillance systems.

#### U-Net

U-Net was used for semantic segmentation because it performs pixel-level classification. The encoder-decoder architecture with skip connections helps preserve spatial details while producing segmentation masks.

### Pipeline

1. Load Pascal VOC 2012 dataset.
2. Resize and normalize images.
3. Train U-Net on segmentation masks.
4. Run YOLO on sample images.
5. Extract YOLO bounding boxes.
6. Pass detected object regions into U-Net.
7. Overlay segmentation masks on detected regions.

### Results

The system successfully demonstrates a combined object detection and segmentation workflow. YOLO identifies objects using bounding boxes, while U-Net generates segmentation masks that outline object regions. This proof-of-concept shows how detection and segmentation can be combined for smart surveillance applications.

### Limitations

The model was trained for a limited number of epochs due to local compute constraints. Additional training, GPU acceleration, and dataset tuning would improve segmentation accuracy.

### Files

- `week4_yolo_unet_pipeline.ipynb`: Main notebook
- `requirements.txt`: Python dependencies
- `screenshots/`: Output images and training screenshots
- `models/`: Saved U-Net model

### References

CV-Tricks.com. (2018, January 2). Zero to hero: Guide to object detection using deep learning: Faster R-CNN, YOLO, SSD. https://cv-tricks.com/object-detection/faster-r-cnn-yolo-ssd/

Everingham, M., Van Gool, L., Williams, C. K. I., Winn, J., & Zisserman, A. (2010). The Pascal Visual Object Classes (VOC) challenge. *International Journal of Computer Vision, 88*(2), 303–338. https://doi.org/10.1007/s11263-009-0275-4

Redmon, J., Divvala, S., Girshick, R., & Farhadi, A. (2016). You only look once: Unified, real-time object detection. *2016 IEEE Conference on Computer Vision and Pattern Recognition*, 779–788. https://doi.org/10.1109/CVPR.2016.91

Ronneberger, O., Fischer, P., & Brox, T. (2015). U-Net: Convolutional networks for biomedical image segmentation. *Lecture Notes in Computer Science, 9351*, 234–241. https://doi.org/10.1007/978-3-319-24574-4_28

Ultralytics. (n.d.). Ultralytics YOLO documentation. https://docs.ultralytics.com/
