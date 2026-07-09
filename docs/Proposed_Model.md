# Proposed Model: GeoFusion-VL

## Core Idea

GeoFusion-VL combines semantic understanding from transformer-based models with geometry-aware representations from GeoDTR+.

## Motivation

TransGeo is strong at learning global semantic representations using Vision Transformers.

GeoDTR+ is strong at learning geometry-aware layout descriptors.

Our model should combine both strengths in one modular pipeline.

## Proposed Pipeline

Ground Image / Satellite Image

1. Semantic Encoder
   - DeiT, DINOv2, or CLIP-like visual encoder

2. Geometry Encoder
   - Inspired by GeoDTR+ geometry layout extractor

3. Feature Fusion
   - Combine semantic and geometric features

4. Shared Embedding Space
   - Learn comparable ground and satellite embeddings

5. Retrieval
   - Use FAISS for scalable nearest-neighbor search

6. VLM Re-ranking
   - Use a vision-language model only on top-k retrieved candidates

## First Research Hypothesis

Combining semantic transformer features with geometry-aware descriptors can improve cross-view geo-localization, especially in challenging real-world cases where viewpoint, orientation, and spatial alignment differ.

## Initial Implementation Plan

Step 1: Run GeoDTR+ and TransGeo as baselines.

Step 2: Extract embeddings from both models.

Step 3: Test simple feature fusion.

Step 4: Add FAISS retrieval.

Step 5: Add VLM-based re-ranking.

Step 6: Train or fine-tune the proposed architecture.
