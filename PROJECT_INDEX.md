# Project Index

This index presents the full scope of my applied AI and computer vision work. Some projects are client-confidential, so they are described at system and methodology level.

## 1. Industrial Pipe Counting

**Domain:** Industrial automation  
**Core problem:** Detect and count packed industrial tubes/pipes.  
**Methods:** YOLO, dataset correction, difficult-sample selection, NMS analysis, image-size experiments, precision/recall/MAE evaluation.  
**Why it matters:** It replaces or assists manual counting, where errors and delays can affect production workflows.  
**Case study:** [industrial-pipe-counting.md](case-studies/industrial-pipe-counting.md)

## 2. Hydra Annotation Platform

**Domain:** Dataset engineering  
**Core problem:** Accelerate image annotation and correction for computer vision datasets.  
**Methods:** React frontend, Go backend, gRPC, Redis, S3-compatible storage, YOLO/COCO-style flows, semi-annotation.  
**Personal contribution:** Full frontend and part of backend.  
**Case study:** [annotation-platform-hydra.md](case-studies/annotation-platform-hydra.md)

## 3. Video Counting with a Virtual Line

**Domain:** Video analytics  
**Core problem:** Count objects crossing horizontal or vertical virtual lines without double counting.  
**Methods:** YOLO, frame-to-frame association, direction logic, event counting, Excel reports.  
**Case study:** [video-analytics-line-crossing.md](case-studies/video-analytics-line-crossing.md)

## 4. Long Video Processing and FFmpeg Robustness

**Domain:** Production video processing  
**Core problem:** Process long videos without losing duration, breaking on corrupted frames, or producing unusable outputs.  
**Methods:** FPS control, FFmpeg compression, duration validation, corrupted-frame handling, batch progress, ETA.  
**Related to:** Video analytics and industrial reporting.

## 5. Open/Closed Carton Detection

**Domain:** Industrial video inspection  
**Core problem:** Detect state transitions from open carton to closed carton and count valid closing events.  
**Methods:** YOLO classes, ROI logic, cooldown strategies, region occupancy, timestamps, cadence calculation, CSV/Excel logs.

## 6. Face Detection and Blurring

**Domain:** Privacy-aware video processing  
**Core problem:** Blur faces automatically in industrial or retail videos.  
**Methods:** YOLO face model, ROI processing, video compression, robust handling of AVI/corrupted files.

## 7. Fine-Grained Retail Product Recognition

**Domain:** Retail analytics  
**Core problem:** Recognize approximately 500 visually similar products/SKUs from supermarket shelf images.  
**Methods:** YOLO detection, crops, DINOv2/DINOv3 embeddings, ResNet, FAISS, kNN, adapters, top-k evaluation.  
**Scale:** 20,000+ annotated product instances.  
**Case study:** [fine-grained-retail-recognition.md](case-studies/fine-grained-retail-recognition.md)

## 8. DINOv2 / DINOv3 Adapter Experiments

**Domain:** Visual representation learning  
**Core problem:** Improve fine-grained recognition with frozen foundation model features and lightweight adapters.  
**Methods:** DINOv2 ViT-S/14, DINOv3, 384-d embeddings, 80/10/10 splits, linear adapters, Optuna, top-1/top-5 evaluation, Excel logs.  
**Reported internal range:** Approximately 94-98% top-1 depending on split and run conditions.

## 9. FastAPI Retail Prediction Backend

**Domain:** AI deployment  
**Core problem:** Serve product recognition through API endpoints for frontend and batch usage.  
**Methods:** FastAPI, Uvicorn, `/predict`, `/predict-batch`, `/health`, YOLO + DINO/FAISS pipeline, JSON outputs, annotated images, ZIP batch, GPU deployment.

## 10. Automatic Product Clustering

**Domain:** Dataset organization and retrieval  
**Core problem:** Group visually similar products automatically to clean and build reference galleries.  
**Methods:** YOLO crops, embeddings, FAISS, clustering thresholds, GPU acceleration.

## 11. Enriched Reference Gallery

**Domain:** Fine-grained recognition improvement  
**Core problem:** Reduce studio-vs-shelf domain shift.  
**Methods:** Multi-image references, angle/light variation, real-shelf crops, DINO/ResNet/CLIP comparisons, top-k benchmark.

## 12. PCB Anomaly Detection / AOI

**Domain:** Industrial visual inspection  
**Core problem:** Compare reference and test PCB images to detect anomalies.  
**Methods:** OpenCV, alignment, SSIM, masks, crop extraction, tolerance parameters.  
**Case study:** [industrial-anomaly-detection-pcb.md](case-studies/industrial-anomaly-detection-pcb.md)

## 13. Manual PCB Region Comparison

**Domain:** Human-in-the-loop inspection  
**Core problem:** Compare manually selected corresponding areas between reference and test images.  
**Methods:** Bounding-box selection, ordered region comparison, output visualizations, measurement tool.

## 14. Black/Brown Spot Counting

**Domain:** Classical image processing  
**Core problem:** Count black or brown spots with tunable thresholds and expected-count optimization.  
**Methods:** OpenCV color thresholds, parameter search, folder processing, best-parameter saving, prediction script.

## 15. YOLO Defect Detection for Black/Brown Marks

**Domain:** Defect detection  
**Classes:** `Piquages_Brun`, `Piquages_Noirs`  
**Core problem:** Detect and count small visual defects while avoiding duplicate boxes.  
**Methods:** YOLO prediction, thin boxes, class-specific colors, overlap handling, priority rules.

## 16. YOLO Auto-Annotation

**Domain:** Dataset acceleration  
**Core problem:** Generate first-pass labels and previews from model predictions.  
**Methods:** YOLO inference, `.txt` label export, preview generation, bbox/arrow overlays, folder batch processing.

## 17. Generic Segmentation and Few-Shot Counting Research

**Domain:** Advanced vision research exploration  
**Core problem:** Move beyond training a YOLO model for every new object type.  
**Methods explored:** SAM/SAM2, DINO embeddings, FAISS, FSC-147, few-shot object counting, generic segmentation and retrieval.

## 18. Cable / Line / Connection Analysis

**Domain:** Structural image understanding  
**Core problem:** Detect or reconstruct cable/line connections in images.  
**Methods:** Distance/path logic, Dijkstra-like reasoning, colored overlays, crossing-line handling, transparency.

## 19. SSRI - Systeme de Surveillance Routiere Intelligent

**Domain:** Smart city / road safety concept  
**Core problem:** Use road camera intelligence for safety and mobility analysis.  
**Methods concept:** License plate recognition, route-level average speed estimation, rule-based violation detection, map integration, privacy-aware design.

## 20. Planum.AI

**Domain:** AI agents and product planning  
**Core problem:** Automate project research, cost estimation, roadmap generation, supplier discovery, and execution planning.  
**Methods concept:** Multi-AI workflow, web research, planning automation, AI-assisted decision support.

