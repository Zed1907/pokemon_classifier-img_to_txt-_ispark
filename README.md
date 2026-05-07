# Pokemon Image Classification Benchmark

A comparative benchmarking project that evaluates three different AI approaches for identifying Pokémon characters from images using Hugging Face Transformers.

This project compares:

- **Specialist Image Classification Model** — trained specifically for Pokémon recognition.
- **Generalist Zero-Shot CLIP Model** — predicts Pokémon names using candidate labels.
- **BLIP Vision Question Answering (VQA) Model** — answers a natural language question about the image.

The goal is to compare:
- Accuracy
- Confidence scores
- Inference speed
- Model behavior across different architectures

---

# Features

- Upload one or multiple Pokémon images
- Compare predictions from 3 AI models
- Measure inference time for each model
- Evaluate confidence levels
- Works directly in Google Colab
- Uses state-of-the-art Hugging Face models

---

# Models Used

## 1. Specialist Pokémon Classifier
Model:
`imjeffhi/pokemon_classifier`

Purpose:
- Fine-tuned specifically for Pokémon image classification
- Expected to achieve the highest accuracy

Pipeline:
```python
pipeline("image-classification")
```

---

## 2. Generalist Zero-Shot CLIP Model
Model:
`openai/clip-vit-base-patch32`

Purpose:
- Performs zero-shot classification
- Predicts among provided Pokémon labels without task-specific training

Pipeline:
```python
pipeline("zero-shot-image-classification")
```

---

## 3. BLIP Vision Question Answering Model
Model:
`Salesforce/blip-vqa-base`

Purpose:
- Answers natural language questions about images
- Used here to identify Pokémon names through VQA

Pipeline:
```python
pipeline("visual-question-answering")
```

---

# Technologies Used

- Python
- Hugging Face Transformers
- PyTorch
- PIL (Python Imaging Library)
- Google Colab

---

# Installation

## Clone Repository

```bash
git clone https://github.com/your-username/pokemon-image-classification-benchmark.git
cd pokemon-image-classification-benchmark
```

## Install Dependencies

```bash
pip install transformers torch pillow
```

---

# How to Run

1. Open the notebook or Python script
2. Run all cells
3. Upload Pokémon images when prompted
4. Compare outputs from all three models

---

# Example Output

```text
Testing Image: pikachu.png

Model 1 (Specialist): Pikachu
Confidence: 99.4%
Time: 0.42s

Model 2 (Generalist): Pikachu
Confidence: 87.2%
Time: 1.10s

Model 3 (BLIP VQA): Pikachu
Time: 1.48s
```

---

# Future Improvements

- Add support for all Pokémon classes
- Build a Streamlit or Flask web app
- Add performance graphs
- Save predictions to CSV
- Compare additional multimodal models

---

# License

MIT License
