# Case Study - Internal Annotation Platform

## Context

Applied computer vision projects depend heavily on dataset quality. Model performance is often limited less by the neural network itself and more by data collection, annotation, correction, and iteration speed.

This project was an internal annotation and dataset platform built to support computer vision workflows. The public version does not use the internal product name.

## Problem

The goal was to support:

- image import with or without labels;
- manual annotation;
- model-assisted semi-annotation;
- conversion of model predictions into editable annotations;
- filtering and review workflows;
- import/export for computer vision formats.

## Technical Direction

The platform used a multi-component architecture:

- React frontend for annotation and review workflows;
- Go backend;
- typed gRPC communication;
- Redis for metadata, annotations, tags, indexes, bundles, and exports;
- S3-compatible storage for image objects;
- support for YOLO/COCO-style data flows.

## Value

The platform was designed to reduce the delay between:

1. collecting images;
2. labeling or correcting them;
3. training a model;
4. finding mistakes;
5. updating the dataset;
6. retraining.

In the PFE context, this platform supported the data loop behind model improvement: faster correction, cleaner exports, and more reliable dataset iteration.

## Key Lessons

1. Annotation tools are part of the AI system, not separate from it.
2. Semi-annotation only helps if predictions can be corrected easily.
3. Dataset tooling must support iteration, filtering, and export formats.
4. Data engineering can unlock more performance than changing the model.

## Research Directions

- Active learning integrated into annotation interfaces.
- Label quality estimation.
- Human-in-the-loop model improvement.
- Model-assisted annotation for dense or fine-grained tasks.
