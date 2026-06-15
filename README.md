# 🚀 NLP Classification: 2023 vs 2026

> *"This is not just another machine learning notebook. It is a time capsule."*

## 👋 Introduction

Back in 2023, I built a multiclass text classification model using traditional NLP techniques and neural networks.

At that time, Large Language Models were not yet everywhere. Most NLP projects relied on:

* Tokenization
* Padding
* Embedding Layers
* LSTM / RNN
* Dense Neural Networks

And honestly?

It worked surprisingly well.

Fast forward to 2026.

The NLP landscape has changed dramatically.

Instead of manually building language understanding from scratch, we now have powerful multilingual embedding models that already understand semantic meaning.

This notebook is an experiment to revisit the exact same problem using modern NLP techniques and compare how far the field has evolved.

---

## 🎯 Objective

Classify Indonesian news headlines into four categories:

* EKONOMI
* KESEHATAN
* OLAH RAGA
* POLITIK

Dataset:

| Category  | Count |
| --------- | ----: |
| EKONOMI   |   751 |
| KESEHATAN |   751 |
| OLAH RAGA |   751 |
| POLITIK   |   751 |

Total: **3004 news headlines**

---

## 🕰️ The 2023 Approach

Typical NLP pipeline in 2023:

```text
Text
↓
Tokenization
↓
Vocabulary
↓
Embedding Layer
↓
LSTM / RNN
↓
Dense Layer
↓
Prediction
```

The model had to learn both:

1. Language representation
2. Classification task

at the same time.

---

## 🤖 The 2026 Approach

Modern pipeline:

```text
News Headline
↓
Sentence Transformer
↓
Semantic Embedding
↓
LightGBM
↓
Prediction
```

Instead of learning language from scratch, we leverage a pretrained multilingual embedding model that already understands semantic relationships between words and sentences.

Examples:

```text
"Harga beras naik"

and

"Biaya beras mengalami kenaikan"
```

are now naturally represented close together in vector space.

---

## 🔬 Why Rebuild This Project in 2026?

Because technology changes.

But more importantly:

**our way of thinking changes.**

In 2023, the question was:

> Which neural network architecture should I use?

In 2026, the question becomes:

> Can this problem be solved using semantic embeddings?

The focus shifts from model architecture to information representation.

---

## 📈 What's New?

### Semantic Embeddings

Using:

```python
intfloat/multilingual-e5-small
```

to transform text into meaningful vectors.

---

### PCA Visualization

For the first time, we can actually visualize how headlines are grouped in semantic space.

```text
POLITIK
      ●●●●●

EKONOMI ●●●●●

      OLAH RAGA

KESEHATAN
```

Not perfectly, but enough to understand how the machine "sees" language.

---

### Modern Evaluation

Instead of only looking at:

```text
Accuracy
```

we also examine:

* Precision
* Recall
* F1 Score
* Confusion Matrix

Because a model can be accurate while still making important mistakes.

---

### Production Mindset

The notebook also demonstrates:

* Saving models with Joblib
* Reloading trained artifacts
* Batch prediction
* Confidence scores
* FastAPI deployment concepts

Moving beyond experimentation toward production-ready workflows.

---

## 💡 Key Lesson

The most interesting part of this notebook is not the final accuracy.

It is seeing how NLP evolved from:

```text
Text → Tokens → Neural Network
```

into:

```text
Text → Meaning → Vector Space → Prediction
```

---

## 🧠 Final Thought

This notebook is a comparison between two generations of NLP.

But it is also a comparison between two versions of an engineer.

The 2023 notebook asked:

> How can I make the model work?

The 2026 notebook asks:

> How does the model understand?

And that might be the most important upgrade of all.

---

Built with ☕, curiosity, and countless "Why?" questions.

Bagustyo 🤖💙
