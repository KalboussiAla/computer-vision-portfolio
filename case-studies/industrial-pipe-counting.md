# Case Study - Industrial Pipe Counting with YOLO

## Context

Industrial pipe/tube counting is often performed manually, which creates errors, delays, and inconsistent reporting. The goal was to build a computer vision system capable of detecting and counting visible pipes in industrial images.

This project was completed in a client-confidential context, so the dataset, client name, exact images, and code cannot be made public.

## Problem

The challenge was not only object detection. The real difficulty came from:

- densely packed objects;
- partial occlusion;
- similar visual appearance between neighboring pipes;
- label noise;
- images with different levels of difficulty;
- the need to evaluate counting quality, not only detection quality.

## Approach

- Started from a YOLO-based baseline and reproduced initial performance around 64% in the original evaluation context.
- Compared several YOLO generations and variants, including YOLOv8, YOLOv9, YOLOv10, YOLOv11, YOLOv12, and newer experimental versions.
- Iterated on dataset quality through label correction, difficult-sample selection, and dataset versioning.
- Tested different image sizes, including transitions such as 640 to 1280 where relevant.
- Evaluated NMS behavior, fusion strategies, and simple vs difficult subsets.

## Evaluation

The project used several metrics depending on the experiment:

- accuracy;
- precision;
- recall;
- mean absolute error (MAE);
- subset-level performance;
- manual inspection of difficult cases.

The system was progressively improved toward approximately 90%+ performance in selected evaluation settings.

## Key Lessons

1. In industrial counting, dataset quality can matter as much as model architecture.
2. Detection metrics alone are not enough; counting error must be measured directly.
3. Separating easy and difficult subsets helps identify whether the model is genuinely improving.
4. A strong baseline is only useful when the evaluation protocol is trusted.

## Research Directions

- Active learning for selecting the next most valuable images to label.
- Counting-aware loss functions or post-processing.
- Robustness to occlusion and dense repetitive objects.
- Weakly supervised or few-shot counting methods.

