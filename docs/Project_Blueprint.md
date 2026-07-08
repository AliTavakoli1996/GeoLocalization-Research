# GeoLocalization Research Project

## Main Goal

Build a cross-view geo-localization system that matches a ground-level image with its corresponding satellite/aerial image.

## Research Direction

How can we combine strong semantic visual features with geometric layout-aware representations?

## Planned Datasets

- CVUSA
- VIGOR
- CVACT
- Custom Dataset

## Planned Models

- GeoDTR+
- TransGeo
- Our Proposed Model

## Modular Pipeline

Ground Image / Satellite Image

Image Encoder

Geometry Encoder

Cross-view Fusion

Shared Embedding

FAISS Retrieval

VLM Re-ranking

## Research Ideas

- Replace ResNet/ConvNeXt with DINOv2 or CLIP.
- Keep GeoDTR+ geometric layout extractor.
- Add FAISS for scalable retrieval.
- Use VLM for top-k re-ranking.
- Compare polar vs non-polar satellite input.
