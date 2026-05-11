# Case Study - Fine-Grained Retail Product Recognition

## Context

Retail shelf analysis requires detecting products and identifying their exact SKU. This is a fine-grained recognition problem: many products look extremely similar, packaging changes over time, and shelf images differ strongly from clean studio reference images.

This project was completed in a client-confidential context. Product images, exact product names, client identity, and code are not public.

## Problem

The system had to recognize approximately 500 product categories/SKUs from real supermarket shelf images.

Main difficulties:

- strong similarity between products;
- different lighting and camera angles;
- studio-reference vs real-shelf domain shift;
- small visual differences between packages;
- noisy crops from detection models;
- need for scalable product reference galleries.

## Data Work

- Worked with more than 20,000 annotated product instances.
- Built and cleaned product crops from shelf images.
- Compared studio references with real-world shelf crops.
- Explored reference gallery enrichment with multiple images per product.
- Used annotation and clustering workflows to reduce manual work.

## Methods

Detection:

- YOLO-based object detection for product localization.

Recognition:

- ResNet / EfficientNet-style classification experiments.
- DINOv2 and DINOv3 visual embeddings.
- FAISS similarity search.
- kNN retrieval.
- Linear adapters trained on frozen features.
- Score fusion and top-k evaluation.

## Results

Depending on dataset split and experimental conditions, controlled evaluations reached approximately:

- top-1 accuracy around 94-98%;
- top-5 accuracy near 99% in strong runs.

These numbers should be interpreted as internal experimental results, not public benchmark claims.

## Deployment Work

The recognition system was transformed into a backend service with:

- FastAPI endpoints;
- `/predict`, `/predict-batch`, and `/health`;
- batch ZIP outputs;
- annotated images;
- JSON predictions;
- AWS/EC2 GPU inference;
- frontend integration testing.

## Key Lessons

1. Fine-grained recognition often needs retrieval and reference management, not only classification.
2. Foundation model embeddings can be very strong when adapted carefully.
3. The gallery quality can become as important as the model.
4. A practical product-recognition system must include detection, cropping, recognition, evaluation, deployment, and error analysis.

## Research Directions

- Domain adaptation between studio and shelf images.
- Open-set product recognition.
- Continual learning when products or packaging change.
- Better active learning for selecting references.
- Hybrid classification-retrieval systems.

