# ViorikaLM-models
**An open-source family of Transformer-based language models, trained from scratch on consumer hardware.**

[![Hugging Face Hub](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Models-yellow.svg)](https://huggingface.co/ViorikaAI)
![Status](https://img.shields.io/badge/Status-Under--Training-orange.svg)

## 🧠 About the Project

ViorikaLM is a personal research project focused on demonstrating that meaningful language model development is possible without access to industrial-scale compute resources. All models are implemented and pre-trained from the ground up on a **single NVIDIA GTX 1070** GPU.

**Key Goals:**
- 🧪 **Experiment** with Transformer architectures and training methodologies.
- 🤖 **Democratize AI** by proving that model training is accessible on consumer-grade hardware.
- 📚 **Educate** by sharing pre-trained checkpoints and documenting the process.

## 🗂️ Model Zoo

All models are available on the Hugging Face Hub:

| Model Name | Parameters | Architecture | Status | HF Link |
| :--- | :--- | :--- | :--- | :--- |
| **ViorikaLM-CHAT** | ~200M | GPT-style (12L, 12H) | 🚧 Early Pre-Training | [Link](https://huggingface.co/ViorikaAI/ViorikaLM-CHAT) |
| *More coming soon...* | | | | |

## ⚙️ Technical Details

- **Framework:** PyTorch
- **Training Hardware:** 1x NVIDIA GTX 1070 (8GB VRAM)
- **Base Architecture:** Decoder-only Transformer (GPT)
- **Pre-training Data:** WikiText-103
- **License:** Not specified (All rights reserved)

## 📊 Training Progress

Current training status across all models:

| Model | Epoch | Train Loss | Val Loss | Notes |
| :--- | :--- | :--- | :--- | :--- |
| ViorikaLM-CHAT | 2 | ~6.0 | No | Initial pre-training phase |

## 🤝 Contributing & Feedback

This is primarily a research and educational project. We welcome:

- 💡 Suggestions and ideas
- 🐛 Bug reports
- 📊 Performance feedback
- ⭐ Starring the repository if you find this project interesting

## 📜 License

All rights reserved. No license specified.

## 🚀 Usage

All models are available via the `transformers` library:

```python
from transformers import AutoModelForCausalLM, AutoTokenizer

model_name = "ViorikaAI/ViorikaLM-CHAT"
tokenizer = AutoTokenizer.from_pretrained(model_name)
model = AutoModelForCausalLM.from_pretrained(model_name)
