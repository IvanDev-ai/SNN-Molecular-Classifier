# Spikes Before Attention

[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Deep Learning](https://img.shields.io/badge/Framework-TensorFlow%20%2F%20Keras-orange.svg)]()
[![License](https://img.shields.io/badge/License-MIT-green.svg)]()
[![Thesis](https://img.shields.io/badge/Bachelor%20Thesis-PHE%20Applied%20Computing%20%26%20AI-red.svg)]()

**Evaluating Spiking Neural Networks for Drug–Target Interaction Prediction**

**Bachelor Thesis Project**  
**Programme:** PHE Applied Computing & Artificial Intelligence  
**Author:** Iván Lumbreras Martín  
**Academic Year:** 2024–2025

---

## Abstract

This thesis investigates whether Spiking Neural Networks (SNNs) can provide a computationally more efficient and biologically plausible alternative to Transformer architectures in the prediction of drug–target interactions from SMILES molecular representations. The research directly addresses the escalating computational costs of state-of-the-art models in drug discovery and evaluates the practical advantages of event-driven neural architectures.

---

## Introduction

The rapid advancement of artificial intelligence in recent months has exposed a fundamental limitation of current dominant architectures. The emergence of high-performing Asian models such as DeepSeek and Qwen demonstrated that it is possible to achieve competitive results at a fraction of the cost of Western counterparts. Their significantly lower API pricing triggered immediate declines in the stock values of major technology companies. The underlying reason is architectural: these models employ a sparse, “divide-and-conquer” activation strategy in which only the necessary components of the network are engaged for each inference. This approach mirrors the operational principle of Spiking Neural Networks.

Traditional Transformer models, by contrast, activate the entire network at every step, resulting in computational and energy costs that increasingly exceed the marginal performance gains they deliver. This thesis examines whether SNNs can mitigate these limitations while maintaining predictive accuracy in a real-world biomedical task.

The central research question guiding the work is:

> How can the architecture of a Spiking Neural Network optimise computational efficiency in the prediction of drug–target interactions compared to the Transformer architecture?

---

## Background

### SMILES Representation

SMILES (Simplified Molecular Input Line Entry System) is the de facto textual standard for encoding molecular structures as ASCII strings. These strings enable machine learning models to process chemical compounds in a manner analogous to natural language processing.

Examples used in the study include:
- Nicotine: `CN1CCC[C@H]1C2=CN=CC=C2`
- Caffeine: `CN1C=NC2=C1C(=O)N(C(=O)N2C)C`

The model predicts the pIC50 value (a logarithmic measure of inhibitory potency) from derived molecular descriptors. Accurate pIC50 prediction is particularly valuable because it directly indicates the viability of a candidate molecule early in the drug development pipeline, thereby reducing the need for costly and time-intensive laboratory assays.

### Transformer Architecture

Transformers rely on the self-attention mechanism introduced in the seminal paper “Attention Is All You Need” (Vaswani et al., 2017). This mechanism excels at capturing long-range dependencies in sequential data and has been successfully adapted to molecular modelling, most notably in DNABERT (Ji et al., 2021), a pre-trained bidirectional Transformer for DNA-language tasks. Despite their effectiveness, Transformers incur substantial computational and memory overhead, making deployment in resource-constrained environments challenging.

### Spiking Neural Networks (SNNs)

Spiking Neural Networks represent the third generation of neural networks. They emulate biological neurons by transmitting information through discrete electrical impulses (“spikes”) rather than continuous activations. A neuron fires only when its membrane potential exceeds a defined threshold, resulting in a binary (0/1) communication pattern.

This event-driven paradigm offers significant advantages in training speed and energy efficiency because only the relevant neurons activate at each step. The approach is supported by key literature, including “Spiking Convolutional Neural Networks for Text Classification” (Lv et al., 2024) and the comprehensive review “Direct training high-performance deep spiking neural networks: a review of theories and methods” (Zhou et al., 2024).

---

## Experimental Comparison

Both architectures were implemented and evaluated under identical conditions (Google Colab environment, same dataset, 20 training epochs, validation split of 0.2).

| Feature                        | Transformer          | Spiking Neural Network (SNN) | 
|--------------------------------|----------------------|------------------------------|
| Training time                  | 60.62 seconds       | 29.14 seconds               | 
| Memory consumption             | 464.55 MB           | 4.60 MB                     | 
| Validation loss                | 5.2545              | 1.8311                      | 

The SNN achieved comparable (and in this case superior) predictive performance while requiring dramatically fewer resources.

---

## Opportunities and Impact

The results open several practical avenues:
- Deployment in resource-limited environments such as portable diagnostic stations or small laboratories.
- Acceleration of drug development cycles, particularly in response to emerging health threats.
- Reduction of the environmental footprint of AI-driven pharmaceutical research.
- Exploration of hybrid SNN–Transformer architectures for optimal performance-efficiency trade-offs.

---

## Stakeholders

- **Academic institutions**: provision of resources, infrastructure and scientific prestige.
- **Pharmaceutical companies**: translation of research into commercial applications and competitive advantage in R&D.
- **Academic community**: validation, enrichment and constructive critique through seminars and publications.
- **General public and patients**: increased legitimacy and long-term societal benefit through faster, more sustainable drug development.

---

## Qualitative Component

The study incorporated a mixed-methods approach. A questionnaire was administered to 76 respondents, and three semi-structured interviews were conducted with healthcare professionals from Hospital Rey Juan Carlos (Móstoles, Madrid): one named interviewee (Daniel Labella Dios, laboratory technician and medical student with over two years of experience) and two anonymous participants (a nuclear medicine technician and a medical student).

All interviewees and the majority of questionnaire respondents agreed that artificial intelligence will be highly valuable in reducing both time and financial investment in drug discovery, especially in the event of future viral outbreaks. However, they expressed caution regarding fully autonomous AI-generated drugs. Respondents supported the use of AI as a decision-support tool while maintaining that medical professionals must retain final responsibility.

---

## Reflection and Future Work

This project has underscored that computational efficiency is no longer optional but essential for the responsible application of AI in biomedicine. The integration of quantitative experimental results with qualitative stakeholder insights has provided a comprehensive view of both the technical potential and the practical, ethical boundaries of the technology.

**Proposed future directions include:**
- Expansion and diversification of the dataset.
- Validation in real-world environments and pilot studies.
- Integration with specialised neuromorphic hardware.
- Strengthening of collaboration with domain professionals.
- Testing under clinical stress conditions and pandemic-simulation scenarios.

---

## Technology Stack

- Python
- TensorFlow / Keras
- RDKit
- NumPy / Pandas
- Scikit-learn
- psutil (resource monitoring)

---

## Repository Structure

- `notebooks/` — Complete reproducible experimental pipeline
- `results/` — Graphs, tables and prediction outputs
- `docs/` — Full thesis (31 pages) and final presentation (20 pages)

---

## Academic Output

- Thesis submitted and defended
- LaTeX version prepared in Overleaf for potential arXiv submission
- Code and data released openly to ensure reproducibility

---

## Author

**Iván Lumbreras Martín**  
Computer Science Graduate  
Aspiring Junior Data Scientist / ML Engineer  
C1 English • International experience (Belgium)

This thesis constitutes the strongest demonstration in my portfolio of applied artificial intelligence in a high-impact domain. It combines rigorous technical implementation, experimental design and a clear emphasis on efficiency—skills directly transferable to roles in data science, machine learning engineering and quantitative analysis within fintech or healthtech sectors.

The complete code, notebooks and documentation are available in this repository. I welcome any questions or opportunities for collaboration.

*Last updated: April 2026*
