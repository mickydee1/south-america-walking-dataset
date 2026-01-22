Long-Horizon Human Locomotion and Egocentric Navigation Dataset

(South America, longitudinal, real-world)

Overview

This repository documents a long-duration, real-world dataset of human locomotion and egocentric navigation collected during a continuous on-foot journey across South America.
The dataset emphasizes temporal consistency, spatial grounding, and verification robustness under unconstrained environmental conditions, including rural roads, deserts, semi-urban areas, and variable weather.

The collection protocol is designed to balance scientific rigor with the practical constraints of a multi-month solo expedition.

Dataset Scope

The dataset captures:

Natural human walking behavior over long temporal horizons

Egocentric navigation without predefined routes

Environmental variation (terrain, surface, lighting, weather)

Physiological context (fatigue, water usage, decision notes)

Data is collected in situ, without reenactment, scripting, or artificial stabilization.

Data Components

Each day of collection consists of:

Segmented egocentric video clips (multiple per day)


Daily GPS start and end screenshots

Manual daily metadata logs

Redundant cloud and local storage copies

No post-processing is applied to raw footage beyond standard file handling.

GPS and Temporal Anchoring Protocol
Daily GPS anchors

At the start and end of each collection day, a GPS screenshot is captured.
These daily anchors establish a temporal envelope within which all dataset activity for that day occurs.

The anchors serve as:

Independent time references

Location-verified markers

Boundary conditions for all segments recorded that day

Segment-level GPS anchoring

For each dataset segment:

A GPS screenshot is taken immediately before recording begins

A GPS screenshot is taken immediately after recording ends

Each video segment is therefore bounded by two explicit spatiotemporal reference points.
Segment anchors are nested within the corresponding daily anchors, creating a hierarchical verification structure:

Daily GPS anchors → Segment GPS anchors → Video file metadata

This structure enables cross-validation between independent sources.

Time Handling Policy

UTC is treated as the authoritative temporal reference for the dataset. Local time and UTC offset are recorded as contextual metadata only.

Device time and timezone are set automatically by geographic location

The applicable UTC offset is recorded once per day in the manual metadata log

This approach eliminates ambiguity arising from daylight-saving changes or government-mandated time adjustments

Manual Metadata Logging

At the end of each day, a manual metadata log is generated and stored in cloud storage.

Typical fields include:

Date

Country and region

Timezone (UTC offset)

Terrain classification

Surface type

Weather conditions

Water carried (start / end)

Subjective fatigue rating

Notes on decisions or anomalies

These logs provide contextual ground truth while remaining independent of the video data.

Data Integrity and Verification
Upload and verification workflow

Dataset videos are recorded offline

Files are uploaded to cloud storage when connectivity is available

A second person independently verifies each file by:

Opening the file

Confirming playability and completeness

Verified files are:

Downloaded to a separate local machine

Retained in cloud storage for redundancy

Local capture copies are removed only after verification is complete

This workflow minimizes risks of silent corruption and establishes clear custody from capture to storage.

Intended Research Use

The dataset is intended for applications such as:

Long-horizon egocentric navigation

Human locomotion modeling

Robustness evaluation under real-world conditions

Temporal and environmental generalization studies

Dataset-level benchmarking across heterogeneous environments

The dataset prioritizes authenticity and continuity over controlled laboratory conditions.

Notes and Limitations

Environmental conditions vary naturally and are not controlled

Collection is subject to real-world constraints (weather, terrain, physical fatigue)

GPS accuracy reflects consumer-grade devices

The dataset represents a single subject and perspective

These characteristics are inherent to the dataset’s real-world scope and should be considered in downstream use.

Contact:fieldwalk.data@gmail.com
