# Multilingual and Cross-Lingual Speech Emotion Recognition with Wav2Vec2: An English–Hindi Study

[![Conference](https://img.shields.io/badge/Proceedings-ICICV%202026%20Vol.%203-blue.svg)](https://github.com/farhanwajid/multilingual-ser-wav2vec2-hindi-english)
[![Framework](https://img.shields.io/badge/PyTorch-Hugging%20Face-yellow.svg)](https://pytorch.org/)
[![Status](https://img.shields.io/badge/Status-In%20Proceedings-brightgreen.svg)](#)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Official PyTorch implementation of the paper **"Multilingual and Cross Lingual Speech Emotion Recognition with Wav2Vec2: An English Hindi Study"**, accepted and appearing in the *Proceedings of the International Conference on Inventive Computation Technologies (ICICV 2026), Volume 3*.

---

## 📌 Abstract

Speech Emotion Recognition (SER) is a crucial component of Human-Computer Interaction (HCI). While monolingual SER systems perform reasonably well, their accuracy degrades significantly across languages—particularly for unseen, low-resource languages such as Hindi. 

This repository evaluates zero-shot cross-lingual transfer, target-language fine-tuning, and joint multilingual training using the **Wav2Vec 2.0** self-supervised transformer across English (**RAVDESS**) and Hindi (**IESC**) datasets over four shared affective categories: *Angry, Happy, Neutral, and Sad*.

### Key Findings:
- **Zero-Shot Limitation:** Direct zero-shot cross-lingual transfer yields low accuracy (42% on English, 44% on Hindi) due to acoustic and phonetic distribution shifts.
- **Target-Language Adaptation:** Fine-tuning on target language data substantially recovers performance, reaching **90.62%** on Hindi.
- **Joint Multilingual Superiority:** Jointly training on combined English + Hindi data achieves peak performance, outperforming cross-lingual baselines with **99.55% accuracy on English** and **90.62% accuracy on Hindi**.

---

## 📊 Summary of Results

| Configuration | Training Set | Evaluation Set | Accuracy | Macro F1 |
| :--- | :--- | :--- | :---: | :---: |
| **Direct Cross-Lingual (Zero-Shot)** | Pretrained Weights | RAVDESS (English) | 42.00% | 0.34 |
| **Direct Cross-Lingual (Zero-Shot)** | RAVDESS (English) | IESC (Hindi) | 44.00% | 0.41 |
| **Cross-Lingual + Fine-Tuning** | IESC (Hindi) | RAVDESS (English) | 85.71% | 0.85 |
| **Cross-Lingual + Fine-Tuning** | RAVDESS (English) | IESC (Hindi) | 90.62% | 0.9064 |
| **Multilingual Joint Training** | English + Hindi Pool | IESC (Hindi) | **90.62%** | **0.9065** |
| **Multilingual Joint Training** | English + Hindi Pool | RAVDESS (English) | **99.55%** | **0.9961** |
