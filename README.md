# Kalboussi Ala - Computer Vision & Applied AI Portfolio

I build applied AI systems around computer vision, dataset engineering, industrial automation, visual recognition, and deployable inference workflows.

This repository is a public-safe technical portfolio. It does not publish private datasets, internal diagrams, proprietary code, production model weights, client images, internal dataset names, or implementation-sensitive details.

## Quick Links

- Portfolio website: https://kalboussiala.github.io/computer-vision-portfolio/
- Project index: [PROJECT_INDEX.md](PROJECT_INDEX.md)
- Research direction: [RESEARCH_DIRECTION.md](RESEARCH_DIRECTION.md)
- Case studies: [case-studies/](case-studies/)
- Contact: [LinkedIn](https://www.linkedin.com/in/ala-kalboussi-490163320/) | [GitHub](https://github.com/KalboussiAla) | kalboussi9@gmail.com

## Main Proof Point - Confidential Industrial PFE

My PFE focused on automatic counting of dense repeated industrial objects from real operational images.

Key results and work:

- reproduced the initial baseline around **64%** image-level accuracy;
- improved the final system to **91.8%** image-level accuracy;
- reached **98.9% precision**, **98.1% recall**, and **0.6 MAE** per image;
- ran **1310+ training runs** and **10,000+ prediction/validation runs**;
- tested data-centric improvement, difficult-sample selection, label correction, image-size experiments, segmentation prototypes, model-combination ideas, and high-level routing strategies;
- built a backend environment for online model testing;
- selected a deployment-ready model based on accuracy, stability, speed, memory, and maintainability.

Full case study: [case-studies/industrial-pipe-counting.md](case-studies/industrial-pipe-counting.md)

## Main Technical Areas

| Area | What I worked on | Representative projects |
|---|---|---|
| Industrial detection and counting | Detection, counting metrics, difficult-case analysis, video counting | Industrial object counting, line-crossing videos, state-transition detection |
| Fine-grained recognition | Product/SKU classification, retrieval, embeddings, domain shift | Retail product recognition with detection + embeddings + similarity search |
| Dataset engineering | Annotation, auto-annotation, label correction, dataset iteration | Internal annotation platform, YOLO auto-labeling |
| Visual inspection | Reference-vs-test comparison, anomaly masks, defect counting | PCB AOI, black/brown spot counting, defect detection |
| AI systems and deployment | FastAPI, batch inference, GPU deployment, reports | Prediction backends, batch outputs, online model testing |
| Advanced vision research ideas | Foundation models, segmentation, few-shot counting, clustering | Generic segmentation, product clustering, reference gallery enrichment |

## Featured Case Studies

1. [Industrial Object Counting](case-studies/industrial-pipe-counting.md)
   Computer vision system for dense object detection and counting, with data-centric improvement and counting-oriented evaluation.

2. [Fine-Grained Retail Product Recognition](case-studies/fine-grained-retail-recognition.md)
   Recognition workflow for approximately 500 visually similar product/SKU categories using detection, embeddings, similarity search, adapters, and deployment APIs.

3. [Internal Annotation Platform](case-studies/internal-annotation-platform.md)
   Annotation and semi-annotation platform for faster dataset creation and model iteration.

4. [Video Analytics and Line-Crossing Counting](case-studies/video-analytics-line-crossing.md)
   Robust video processing scripts for object passage counting, batch reporting, corrupted frames, and output handling.

5. [PCB Anomaly Detection / AOI](case-studies/industrial-anomaly-detection-pcb.md)
   Reference-vs-test inspection using OpenCV, SSIM, alignment, difference masks, and anomaly crop extraction.

## Extended Project Families

The full project map is in [PROJECT_INDEX.md](PROJECT_INDEX.md). It includes:

- industrial object counting;
- internal annotation and dataset platform;
- video counting with virtual lines;
- long-video processing and output robustness;
- open/closed state detection;
- face detection and blurring;
- retail product recognition;
- adapter and embedding experiments;
- prediction backend services;
- automatic product clustering;
- reference gallery enrichment;
- PCB/AOI anomaly detection;
- manual visual region comparison;
- black/brown spot counting;
- defect detection;
- auto-annotation;
- generic segmentation and few-shot counting research ideas;
- cable/line connection analysis;
- SSRI, an intelligent road surveillance concept.

## Technical Stack

**Computer Vision / AI:** YOLO, DINOv2, DINOv3, ResNet, FAISS, kNN, OpenCV, SSIM, OCR, segmentation concepts, few-shot counting concepts
**ML / Data:** PyTorch, TensorFlow, scikit-learn, NumPy, Pandas, Matplotlib, Seaborn, Optuna, experiment logs
**Backend / Deployment:** FastAPI, Uvicorn, REST APIs, AWS/EC2 GPU deployment, secure tunneling, batch inference, JSON and ZIP outputs
**Software / Platform:** Python, Go, gRPC, Redis, S3-compatible storage, React, TypeScript, JavaScript, HTML/CSS
**Dataset Engineering:** YOLO/COCO formats, semi-annotation, auto-annotation, label correction, dataset versioning, difficult-sample selection

## What This Portfolio Is

This repository is a structured technical portfolio:

- it explains what problems I solved;
- it shows the model families and pipelines I worked with;
- it highlights the engineering decisions behind the systems;
- it separates public information from confidential implementation details;
- it gives supervisors and recruiters a clear starting point for technical discussion.

For deeper technical interviews, I can discuss anonymized architectures, evaluation protocols, failure cases, and non-sensitive results.
