# Case Study - Video Analytics and Line-Crossing Counting

## Context

Many industrial and retail workflows need counts from video: objects passing through a line, workers visible at once, boxes closing, or items moving through a process.

## Problem

The challenge was to build scripts that remain useful on real videos, not just demo clips.

Constraints included:

- long videos;
- corrupted frames;
- inconsistent codecs;
- changing FPS;
- objects crossing a virtual line;
- objects returning backward;
- avoiding double counts;
- generating simple business-readable reports.

## Approach

- YOLO-based detection on video frames.
- Virtual horizontal or vertical line.
- Direction-aware counting.
- Frame-to-frame association logic.
- Cooldown / region-occupancy strategies depending on the task.
- Minimal overlays for readability.
- Excel/CSV reporting per video.
- Batch processing with progress, ETA, and failure handling.

## Video Robustness

Additional work focused on:

- preserving original video duration;
- forcing output FPS when needed;
- FFmpeg compression;
- recovering from damaged frames;
- avoiding multi-day batch failure due to one bad video.

## Key Lessons

1. Production video analytics depends heavily on failure handling.
2. Counting logic must reflect object behavior, not only detection output.
3. Reporting and batch reliability are part of the value of the model.
4. A visually clean overlay can be more useful than a dense debugging display.

## Research Directions

- More robust tracking under occlusion.
- Event detection from object state transitions.
- Uncertainty-aware counting.
- Lightweight deployment for edge devices.

