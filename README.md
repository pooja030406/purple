# Retail Store Intelligence Pipeline

## Overview

A computer vision pipeline that processes retail store surveillance videos to generate customer activity events and analytics.

The system combines person detection, tracking, zone analysis, queue monitoring, and event generation to convert raw video footage into structured business insights.

---

## Features

- YOLOv8-based person detection
- Multi-object tracking
- Entry and exit detection
- Zone occupancy analytics
- Queue monitoring
- Staff filtering
- JSONL event export

---

## Project Structure

```text
configs/      -> Store, camera, and zone configurations
detection/    -> Detection and tracking modules
events/       -> Event generation logic
pipeline/     -> Pipeline execution scripts
output/       -> Generated outputs
logs/         -> Execution logs
```

---

## Installation

```bash
pip install -r requirements.txt
```

---

## Run

Process all videos:

```bash
python pipeline/run_pipeline.py
```

Process a specific store:

```bash
python pipeline/run_pipeline.py --store store1
```

---

## Output

The pipeline generates structured events such as:

- Customer Entry
- Customer Exit
- Zone Entry/Exit
- Queue Join/Leave
- Dwell Time Events

Outputs are stored in the `output/` directory.

---

## Technologies Used

- Python
- OpenCV
- YOLOv8
- NumPy
- JSONL Processing

---
