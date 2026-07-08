# Architecture Comparison

## GeoDTR+

- Uses CNN backbones such as ResNet or ConvNeXt.
- Extracts geometry-aware layout descriptors.
- Combines visual feature maps with learned geometric descriptors.
- Uses triplet-style retrieval loss.
- Strong point: explicit geometric layout modeling.

## TransGeo

- Uses DeiT / Vision Transformer as the main encoder.
- Has separate query and reference encoders.
- Uses CLS token and distillation token.
- Uses SoftTripletBiLoss.
- Supports attention-map saving and non-uniform cropping.
- Strong point: strong transformer-based global representation.

## Main Difference

GeoDTR+ focuses on geometry-aware descriptors.

TransGeo focuses on transformer-based semantic representation.

## Initial Research Direction

Our model should combine:

- TransGeo-style transformer semantic encoding
- GeoDTR+-style geometry-aware descriptor extraction
- FAISS retrieval
- VLM-based top-k re-ranking
