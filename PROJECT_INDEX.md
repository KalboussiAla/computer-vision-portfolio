# Project Index

This index presents the full scope of my applied AI and computer vision work. Some projects were built in confidential contexts, so they are described at system and methodology level only.

## 1. Industrial Object Counting

**Domain:** Industrial automation
**Core problem:** Detect and count dense repeated objects in operational images.
**Methods:** YOLO-based detection, dataset correction, difficult-sample selection, image-size experiments, contour/edge preprocessing tests, alternative annotation strategies, segmentation prototypes, model-combination ideas, high-level routing experiments, precision/recall/MAE evaluation.
**Scale and result:** Improved from an initial reproduced baseline around 64% to 91.8% image-level accuracy, with 98.9% precision, 98.1% recall, and 0.6 MAE on evaluated images.
**Engineering:** 1310+ training runs, 10,000+ prediction/validation runs, online backend testing environment, and deployment-ready model selection.
**Why it matters:** It replaces or assists manual counting, where errors and delays can affect operational workflows.
**Case study:** [industrial-pipe-counting.md](case-studies/industrial-pipe-counting.md)

## 2. Internal Annotation Platform

**Domain:** Dataset engineering
**Core problem:** Accelerate image annotation and correction for computer vision datasets.
**Methods:** React frontend, Go backend, gRPC, Redis, S3-compatible storage, YOLO/COCO-style flows, semi-annotation.
**Personal contribution:** Full frontend and part of backend.
**Connection to PFE:** The platform supported the data loop behind model improvement: import, annotation, correction, filtering, export, retraining, and validation.
**Case study:** [internal-annotation-platform.md](case-studies/internal-annotation-platform.md)

## 3. Video Counting with a Virtual Line

**Domain:** Video analytics
**Core problem:** Count objects crossing horizontal or vertical virtual lines without double counting.
**Methods:** YOLO, frame-to-frame association, direction logic, event counting, Excel reports.
**Case study:** [video-analytics-line-crossing.md](case-studies/video-analytics-line-crossing.md)

## 4. Long Video Processing and Output Robustness

**Domain:** Production video processing
**Core problem:** Process long videos without losing duration, breaking on corrupted frames, or producing unusable outputs.
**Methods:** FPS control, compression, duration validation, corrupted-frame handling, batch progress, ETA.
**Related to:** Video analytics and industrial reporting.

## 5. Open/Closed State Detection

**Domain:** Industrial video inspection
**Core problem:** Detect state transitions and count valid events.
**Methods:** YOLO classes, ROI logic, cooldown strategies, region occupancy, timestamps, cadence calculation, CSV/Excel logs.

## 6. Process-State Transition Detection

**Domain:** Process optimization
**Core problem:** Detect a visual transition between two production states to reduce wasted energy, waiting time, and unnecessary machine relaunches.
**Methods:** State classification/detection, temporal transition logic, ROI monitoring, event timestamps, production-cost reasoning.

## 7. Packaging Completion and Palletization Tracking

**Domain:** Industrial packaging analytics
**Core problem:** Detect transitions between not-ready/ready or open/closed states to count completed units, stacking progress, and palletization progress.
**Methods:** State-transition detection, ROI logic, event counting, cadence estimation, reporting.

## 8. Conveyor Material Counting

**Domain:** Production-line counting
**Core problem:** Count moving industrial items or material units on conveyors.
**Methods:** Detection, tracking/event logic, batch reporting, operational robustness.

## 9. Calibrated Installation Quality Checks

**Domain:** Vision-assisted measurement
**Core problem:** Verify placement and quality of components along a linear assembly using images, known distances, and contextual sensor information.
**Methods:** Calibration, distance-aware checks, component localization, quality scoring.

## 10. Industrial Inventory Counting

**Domain:** Stock and inventory automation
**Core problem:** Count stacked industrial units and adapt counting models to related object families for inventory estimation.
**Methods:** Dense-object detection, model adaptation, stock reporting, inventory-oriented evaluation.

## 11. Pre-Process Manufacturing Anomaly Detection

**Domain:** Quality control
**Core problem:** Detect visual anomalies before an irreversible or costly manufacturing step.
**Methods:** Detection/classification, anomaly-oriented datasets, early rejection, reusable inspection pipeline.

## 12. Face Detection and Blurring

**Domain:** Privacy-aware video processing
**Core problem:** Blur faces automatically in industrial or retail videos.
**Methods:** Face detection, ROI processing, video compression, robust handling of damaged files.

## 13. Fine-Grained Retail Product Recognition

**Domain:** Retail analytics
**Core problem:** Recognize approximately 500 visually similar products/SKUs from supermarket shelf images.
**Methods:** Detection, crops, DINOv2/DINOv3 embeddings, ResNet, FAISS, kNN, adapters, top-k evaluation.
**Scale:** 20,000+ annotated product instances.
**Case study:** [fine-grained-retail-recognition.md](case-studies/fine-grained-retail-recognition.md)

## 14. Adapter and Embedding Experiments

**Domain:** Visual representation learning
**Core problem:** Improve fine-grained recognition with frozen foundation model features and lightweight adapters.
**Methods:** DINO features, embedding extraction, train/validation/test splits, linear adapters, Optuna, top-1/top-5 evaluation, Excel logs.
**Reported internal range:** Approximately 94-98% top-1 depending on split and run conditions.

## 15. Prediction Backend Services

**Domain:** AI deployment
**Core problem:** Serve recognition or detection workflows through API endpoints for frontend and batch usage.
**Methods:** FastAPI, Uvicorn, `/predict`, `/predict-batch`, `/health`, detection + embedding pipelines, JSON outputs, annotated outputs, ZIP batch, GPU deployment.

## 16. Automatic Product Clustering

**Domain:** Dataset organization and retrieval
**Core problem:** Group visually similar products automatically to clean and build reference galleries.
**Methods:** Detection crops, embeddings, similarity search, clustering thresholds, GPU acceleration.

## 17. Enriched Reference Gallery

**Domain:** Fine-grained recognition improvement
**Core problem:** Reduce studio-vs-shelf domain shift.
**Methods:** Multi-image references, angle/light variation, real-shelf crops, DINO/ResNet/CLIP comparisons, top-k benchmark.

## 18. PCB Anomaly Detection / AOI

**Domain:** Industrial visual inspection
**Core problem:** Compare reference and test PCB images to detect anomalies.
**Methods:** OpenCV, alignment, SSIM, masks, crop extraction, tolerance parameters.
**Case study:** [industrial-anomaly-detection-pcb.md](case-studies/industrial-anomaly-detection-pcb.md)

## 19. Manual Visual Region Comparison

**Domain:** Human-in-the-loop inspection
**Core problem:** Compare manually selected corresponding areas between reference and test images.
**Methods:** Bounding-box selection, ordered region comparison, output visualizations, measurement tool.

## 20. Black/Brown Spot Counting

**Domain:** Classical image processing
**Core problem:** Count black or brown spots with tunable thresholds and expected-count optimization.
**Methods:** OpenCV color thresholds, parameter search, folder processing, best-parameter saving, prediction script.

## 21. YOLO Defect Detection for Black/Brown Marks

**Domain:** Defect detection
**Core problem:** Detect and count small visual defects while avoiding duplicate boxes.
**Methods:** YOLO prediction, thin boxes, class-specific colors, overlap handling, priority rules.

## 22. YOLO Auto-Annotation

**Domain:** Dataset acceleration
**Core problem:** Generate first-pass labels and previews from model predictions.
**Methods:** YOLO inference, label export, preview generation, bbox/arrow overlays, folder batch processing.

## 23. Segmentation-Assisted Few-Example Concept

**Domain:** Advanced vision research exploration
**Core problem:** Explore how a small number of examples could be expanded without claiming a completed implementation.
**Methods concept:** Segment example objects, look for recurring visual regions or patterns, use a vision-language model or retrieval workflow to search for similar images, then review results before adding them to a dataset.

## 24. Cable / Line / Connection Analysis

**Domain:** Structural image understanding
**Core problem:** Detect or reconstruct cable/line connections in images.
**Methods:** Distance/path logic, Dijkstra-like reasoning, colored overlays, crossing-line handling, transparency.

## 25. SSRI - Systeme de Surveillance Routiere Intelligent

**Domain:** Smart city / road safety concept
**Core problem:** Use road camera intelligence for safety and mobility analysis.
**Methods concept:** License plate recognition, route-level average speed estimation, rule-based violation detection, map integration, privacy-aware design.

## 26. AI Agent Product Ideas

**Domain:** AI agents and product planning
**Core problem:** Automate project research, cost estimation, roadmap generation, supplier discovery, and execution planning.
**Methods concept:** Multi-AI workflow, web research, planning automation, AI-assisted decision support.

## 27. Neuroscience-Inspired Efficient AI

**Domain:** Research direction
**Core problem:** Current AI systems can consume far more energy than biological intelligence for tasks humans solve naturally.
**Methods concept:** Attention, sparse computation, memory, continual learning, biologically inspired perception, efficient inference.

## 28. Context-Aware Vision with Compact Reasoning

**Domain:** Research direction
**Core problem:** Vision models often detect objects without understanding the local situation, which can create false positives.
**Methods concept:** Vision model plus compact contextual reasoning module, local memory, scene understanding, false-positive reduction.

## 29. AI for Climate-Aware Operations

**Domain:** Research direction
**Core problem:** Reduce energy waste, machine restarts, material loss, delays, and preventable operational cost.
**Methods concept:** State-transition detection, process optimization, anomaly detection, energy-aware decision support.
