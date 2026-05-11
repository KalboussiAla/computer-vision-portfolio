# Case Study - PCB Anomaly Detection / AOI

## Context

Automated Optical Inspection (AOI) aims to detect defects or differences between a reference object and a tested object. In this project, the target setting was PCB inspection with a fixed camera and controlled lighting assumptions.

## Problem

The objective was to compare a reference PCB image and a test PCB image in order to highlight abnormal regions.

Challenges:

- precise image alignment;
- tolerance to small lighting changes;
- separating meaningful differences from noise;
- generating useful crops for review;
- defining thresholds that can be defended technically.

## Approach

- OpenCV-based preprocessing.
- Reference/test alignment.
- SSIM comparison.
- Difference masks.
- Morphological processing.
- Abnormal region extraction.
- Crop generation for human review.
- Manual bounding-box comparison tool for corresponding zones.

## Key Lessons

1. Controlled acquisition conditions can simplify anomaly detection significantly.
2. Classical vision methods remain useful when the environment is constrained.
3. Anomaly detection must be evaluated with tolerance rules, not only visual intuition.
4. Hybrid systems can combine reference comparison with learned classifiers later.

## Research Directions

- Learning-based anomaly detection with few defective examples.
- Robust image registration for small variations.
- Patch-level embedding comparison.
- Human-in-the-loop defect validation.

