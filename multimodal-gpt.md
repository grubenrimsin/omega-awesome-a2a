# MultiModal-GPT: A Vision and Language Model for Dialogue with Humans

## Overview
MultiModal-GPT represents a breakthrough in multimodal conversational AI, introducing a unified framework that maintains contextual awareness across multiple conversation turns while processing both images and text. Unlike previous vision-language models limited to single image-text pairs, this architecture enables coherent dialogue incorporating multiple images within a single conversation thread.

## Technical Details
- **Paper:** [MultiModal-GPT: A Vision and Language Model for Dialogue with Humans](https://arxiv.org/abs/2305.04790)
- **GitHub:** [open-mmlab/Multimodal-GPT](https://github.com/open-mmlab/Multimodal-GPT)
- **Released:** May 2023
- **License:** Apache 2.0

### Architecture
- Vision Encoder: CLIP ViT-L/14
- Language Model: ChatGPT
- Training Dataset: MultiModal-GPT-Instruct (147K multi-turn conversations)

### Key Features
- Multi-turn dialogue with persistent image context
- Zero-shot generalization capabilities
- Flexible deployment options
- Comprehensive evaluation framework

## Implementation Example
```python
from mmgpt.model import MultiModalGPT

# Initialize model
model = MultiModalGPT.from_pretrained("openmmlab/MultiModal-GPT")

# Single image dialogue
response = model.chat(
    text="What do you see in this image?",
    image_path="example.jpg"
)

# Multi-image dialogue
response = model.chat(
    text="Compare these two images",
    image_paths=["image1.jpg", "image2.jpg"]
)
