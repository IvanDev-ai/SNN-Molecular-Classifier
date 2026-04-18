# 🧠 Spikes Before Attention
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Deep Learning](https://img.shields.io/badge/Framework-PyTorch%20%2F%20snntorch-orange.svg)]()
[![License](https://img.shields.io/badge/License-MIT-green.svg)]()
[![Academic](https://img.shields.io/badge/Research-HND%20Computing%20%26%20AI-red.svg)]()
### Evaluating Spiking Neural Networks for Drug–Target Interaction Prediction

**Bachelor Thesis Project** — PHE Applied Computing & Artificial Intelligence  
**Author:** Iván Lumbreras Martín  
**Academic Year:** 2024-2025

---

## 📌 Overview

This research project investigates whether **Spiking Neural Networks (SNNs)** can offer a more computationally efficient and biologically plausible alternative to **Transformer architectures** in the critical task of **drug–target interaction prediction** using **SMILES molecular representations**.

In an era where AI is revolutionizing drug discovery, the computational cost of state-of-the-art models has become a major bottleneck. This work directly addresses that challenge by comparing two fundamentally different neural paradigms: the powerful but resource-heavy Transformer and the event-driven, brain-inspired Spiking Neural Network.

**Key takeaway:** SNNs delivered **comparable predictive performance** while training **~50% faster** and consuming dramatically less memory — demonstrating their potential as a sustainable and scalable solution for real-world biomedical AI.

---

## ❓ Research Question

> **How can the architecture of a Spiking Neural Network optimize computational efficiency in the prediction of drug–target interactions compared to the Transformer architecture?**

This question guided the entire project and remains at the core of the investigation.

---

## 📖 Background

### SMILES Representation
SMILES (Simplified Molecular Input Line Entry System) is the standard textual notation for encoding molecular structures as ASCII strings. It allows complex chemical compounds to be processed by machine learning models similarly to natural language.

**Examples included in the study:**
- Nicotine: `CN1CCC[C@H]1C2=CN=CC=C2`
- Caffeine: `CN1C=NC2=C1C(=O)N(C(=O)N2C)C`

These strings were converted into numerical features using RDKit for model input.

### Transformer Architecture
Transformers dominate modern AI thanks to their **self-attention mechanism**, which excels at capturing long-range dependencies. They have been highly successful in molecular modeling, but come with significant drawbacks:
- Extremely high computational and memory requirements
- Large carbon footprint during training
- Difficulty deploying in resource-constrained environments

### Spiking Neural Networks (SNNs)
SNNs are the third generation of neural networks. Inspired by biological neurons, they communicate through **discrete spike events** rather than continuous activations.

**Core advantages:**
- Event-driven computation (only active when needed)
- Significantly lower energy consumption
- Greater biological realism
- Natural suitability for neuromorphic hardware

---

## ⚔️ SNN vs Transformer – Direct Comparison

| Feature                      | Spiking Neural Network (SNN)          | Transformer                          |
|-----------------------------|---------------------------------------|--------------------------------------|
| Computation Style           | Event-driven, spike-based            | Continuous, attention-based         |
| Energy Efficiency           | Very high (brain-like)               | High computational demand           |
| Biological Plausibility     | High                                 | Low                                 |
| Training Speed (this study) | ~29 seconds                          | ~61 seconds                         |
| Memory Usage (this study)   | ~4.6 MB                              | ~464 MB                             |
| Maturity                    | Emerging                             | Mature                              |
| Suitability for Drug Discovery | Promising for efficiency-critical tasks | Excellent performance, costly      |

**Resultados reales del experimento:** La SNN mantuvo un rendimiento predictivo similar al Transformer pero con una reducción drástica en tiempo y memoria.

---

## 🚀 Opportunities & Impact

This research opens doors to:
- Accelerating drug discovery pipelines
- Enabling rapid response to emerging health threats
- Reducing the environmental impact of AI in pharma
- Deploying advanced models in low-resource settings (hospitals, startups, edge devices)
- Exploring hybrid SNN–Transformer architectures

---

## 👥 Stakeholders

- **Pharmaceutical companies** – faster and cheaper drug screening
- **Academic & research institutions** – methodological advancement in neuromorphic AI
- **Healthcare systems** – more sustainable AI tools
- **Patients & society** – long-term benefits from faster drug development

---

## 🔬 Methodology

1. **Data Preparation**  
   - Downloaded Big Molecules SMILES Dataset (Kaggle)  
   - Converted SMILES to molecular descriptors using RDKit  
   - Normalized features with Scikit-learn

2. **Model Implementation**  
   - Baseline: Transformer model (multi-head attention)  
   - Proposed: Custom Spiking Neural Network  
   - Both models trained for 20 epochs with identical data split

3. **Resource Monitoring**  
   - Real-time tracking of training time and memory usage (psutil)  
   - Fair comparison under the same hardware (Google Colab)

4. **Evaluation**  
   - Predictive performance (validation loss)  
   - Computational efficiency (time + memory)  
   - Qualitative prediction on unseen SMILES molecules

---

## 📊 Key Results

- Both models achieved competitive validation loss.
- **SNN trained in half the time** of the Transformer.
- **SNN used dramatically less memory** during training.
- Successful predictions on new molecules (e.g. acetic acid, cyclohexane, and a complex drug-like compound).

**Conclusión clara:** Las SNNs demuestran ser una alternativa altamente eficiente sin sacrificar precisión.

---

## ⚖️ Ethical Considerations & Limitations

- Responsible AI in biomedicine
- Transparency in methodology and results
- Awareness of limitations (data quality, model generalizability, hardware constraints)
- Commitment to open science (code and data openly available)

---

## 🔮 Future Work

- Integration with neuromorphic hardware
- Testing on larger and more diverse datasets
- Development of hybrid SNN-Transformer models
- Real-world validation with pharmaceutical partners
- Exploration of energy consumption metrics on physical hardware

---

## 🛠️ Tech Stack

- **Python** • **TensorFlow / Keras** • **RDKit** • **NumPy / Pandas** • **Scikit-learn** • **psutil** (resource monitoring)

---

## 📂 Repository Contents

- `notebooks/` – Complete reproducible pipeline (4 notebooks)
- `results/` – All graphs, tables and prediction examples
- `docs/` – Full thesis PDF (51 pages) and presentation (20 pages)

---

## 📄 Academic Output

- Full thesis submitted and defended
- LaTeX version (Overleaf) prepared for arXiv submission
- Code and data openly available to promote reproducibility

---

## 👤 Author

**Iván Lumbreras Martín**  
Computer Science Graduate | Aspiring Junior Data Scientist / ML Engineer  
C1 English • International experience (Belgium)  
**Actively seeking** Junior Data Scientist, ML Engineer or Quantitative roles in Fintech / HealthTech.

---

**This project represents my strongest demonstration of applied AI in a high-impact domain.**  
It combines deep technical implementation, rigorous experimental design, and a clear focus on efficiency — skills directly transferable to real-world Data Science and Fintech challenges.

Feel free to explore the code, run the notebooks, or reach out if this work resonates with your team.

---

**Made with passion for more efficient, sustainable and biologically inspired AI.**

*Last updated: April 2026*
