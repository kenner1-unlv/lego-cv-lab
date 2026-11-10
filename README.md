# LEGO CV Lab

A public computer vision and machine learning lab for detecting and measuring
individual LEGO pieces. The first image source is an OAK 4 camera. The detector
will be trained from human-reviewed piece annotations, then evaluated on held-out
board scenes.

## First experiment

Start with roughly 20 pieces of varied colors and footprints on a board. Shake
them flat, verify that they do not touch or overlap, and record the actual count.
Piece orientation may vary. Later stages will change spacing, count, contact,
overlap, occlusion, and lighting one condition at a time.

The first model baseline will fine-tune a suitable pretrained detector or
instance segmenter. A model initialized from scratch can be compared with the
same held-out scenes when enough labeled images and compute are available.
Reports will separate count error, instance detection, color, footprint, and
orientation results.

## Status

This repository is at setup stage. It contains the project structure and
experiment plan. No LEGO detector has been trained or physically verified on
the OAK 4 yet. Existing House V inference, Orin identity fusion, and Unitree L2
are separate work and are not required for this lab.

## Repository layout

- lego_cv_lab/: capture, dataset, training, and evaluation code as it is built.
- protocols/: board setup and label rules.
- findings/: shareable reports with methods, denominators, and limitations.
- specs/: specification, design, and ordered tasks.
- tests/: synthetic fixtures and behavior checks.

Raw images, private scenes, model weights, and generated runs belong in an
external data directory and are excluded from Git. The public history will
contain code, protocols, synthetic fixtures, and reviewed findings.
