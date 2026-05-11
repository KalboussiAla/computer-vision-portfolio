# Case Study - Confidential Industrial Object Counting

## Context

This PFE project focused on automatic counting of dense repeated industrial objects from real operational images. The business objective was practical: reduce manual counting, improve reliability, and make the counting workflow faster and more consistent.

This public version intentionally removes internal dataset names, diagrams, exact image examples, client identifiers, model weights, and implementation-sensitive details.

## My Role

- Reproduced the initial baseline and validated the evaluation protocol.
- Built and improved dataset versions without exposing internal names publicly.
- Analyzed label quality, difficult images, easy vs difficult cases, and failure modes.
- Ran large-scale experiments on training configuration, image size, data quality, and difficult-case handling.
- Tested edge/contour-oriented preprocessing and alternative annotation strategies.
- Tested advanced prototypes such as segmentation, model-combination ideas, dense-object strategies, and high-level routing experiments.
- Built an online/backend testing environment for model evaluation.
- Selected the final deployment-ready model based on accuracy, stability, speed, memory constraints, and maintainability.

## Results

| Metric / stage | Result |
|---|---|
| Initial reproduced baseline | Around 64% image-level counting accuracy |
| Final image-level accuracy | 91.8% |
| Final precision | 98.9% |
| Final recall | 98.1% |
| Final MAE | 0.6 object per image |
| Training scale | 1310+ training runs |
| Validation scale | 10,000+ prediction and validation runs |

## Technical Approach

### 1. Baseline Reproduction

The first step was to reproduce the existing detector and confirm the evaluation method. This mattered because the project needed a trusted baseline before any improvement could be considered real.

### 2. Data-Centric Improvement

The strongest improvement came from data quality:

- auditing labels;
- correcting inconsistent annotations;
- separating simple and difficult examples;
- selecting representative hard cases;
- comparing dataset quality against dataset size;
- validating with counting metrics, not only detection metrics.

A smaller curated training set performed better than a larger noisy set. This became one of the main engineering lessons of the project.

### 3. Experimentation at Scale

The project included 1310+ training runs and 10,000+ prediction/validation runs. The experiments covered:

- training configuration;
- image resolution;
- annotation correction;
- edge and contour preprocessing;
- alternative annotation strategies;
- difficult-case selection;
- hyperparameter search;
- inference behavior;
- precision, recall, accuracy, and MAE tracking.

### 4. Advanced Prototypes

Several advanced directions were explored, then filtered based on real deployment value:

- segmentation prototypes;
- dense-object counting strategies;
- controlled training on difficult samples;
- model-combination ideas;
- high-level routing/orchestration experiments;
- deployment-focused simplification.

Some prototypes produced interesting results but were not selected because they added complexity, reduced maintainability, or increased the risk of unstable behavior.

## Related Industrial Reuse

The same engineering pattern was reused or adapted across other confidential industrial problems:

- inventory-oriented counting for stacked units;
- model adaptation to related object families;
- conveyor and moving-line counting;
- process-state transition detection for energy/time optimization;
- packaging completion and palletization progress tracking;
- pre-process anomaly detection before costly or irreversible steps;
- calibrated visual quality checks for component placement.

### 5. Online Testing and Deployment Readiness

The final phase was not limited to notebook metrics. I built a backend environment for online model testing so that inference could be evaluated closer to a real usage flow.

The final model was selected based on:

- counting accuracy;
- MAE;
- precision and recall;
- inference stability;
- speed;
- memory constraints;
- maintainability;
- suitability for operational integration.

## Key Lessons

1. In industrial counting, dataset quality can dominate architecture choice.
2. Counting metrics such as MAE are essential; detection metrics alone are not enough.
3. The best experimental prototype is not always the best deployment solution.
4. A smaller, cleaner, well-curated dataset can beat a larger noisy dataset.
5. Annotation tooling and evaluation discipline are part of the AI system, not side work.

## Research Directions

- Active learning for selecting the next most valuable images to annotate.
- Counting-aware post-processing for dense repeated objects.
- Robustness to occlusion, lighting changes, and acquisition variation.
- Foundation-model features for difficult-case retrieval and dataset curation.
- Segmentation-assisted example expansion ideas for objects that are costly to annotate.
