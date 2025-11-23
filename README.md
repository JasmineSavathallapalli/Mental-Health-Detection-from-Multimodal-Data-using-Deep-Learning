#  Mental Health Detection from Multimodal Data Using Deep Learning

This project presents a multimodal deep learning system designed to detect depression severity using **audio**, **video**, and **text** information from the **DAIC-WOZ dataset**.  
Since mental‐health symptoms cannot be captured reliably through a single modality, this approach combines multiple behavioral cues using a **Modality Attention Gated Fusion (MAGF)** model for more accurate and robust predictions.

---

## 📌 Project Overview

The complete research pipeline is implemented in **`final.ipynb`**, covering:

### **1. Preprocessing**
- Extracts features from audio, video frames, and text transcripts  
- Builds tensors and mask files for handling missing or noisy segments  
- Normalizes and prepares data for model training  

### **2. Unimodal Models**
- **Audio Model:** BiLSTM  
- **Video Model:** BiLSTM  
- **Text Model:** Embedding + Sequential Model  
- Each modality is trained independently to assess individual performance

### **3. Fusion Model (MAGF)**
- Combines outputs from all modalities  
- Learns dynamic weights for each modality  
- Handles missing data via mask integration  
- Produces the final depression probability

---

## 🧱 Architecture Summary

| Modality | Model Used | Learns |
|----------|-------------|--------|
| **Audio** | BiLSTM | Patterns in tone, prosody, emotional cues |
| **Video** | BiLSTM | Facial expressions, movements, affect |
| **Text** | Embedding + Sequence Encoder | Linguistic behavior & content |
| **Fusion** | MAGF | Cross-modal weighting & final prediction |

---


## ⚠️ Dataset License Notice (IMPORTANT)

This project uses the **DAIC-WOZ dataset**, which is protected under a strict End-User License Agreement.

Therefore, this repository **does NOT include**:
- Raw audio/video files  
- Transcripts  
- Labels  
- Extracted `.pt` tensors or mask files  

Users must request dataset access from the official source.

[1] Gratch J, Artstein R, Lucas GM, Stratou G, Scherer S, Nazarian A, Wood R, Boberg J, DeVault D, Marsella S, Traum DR.
The Distress Analysis Interview Corpus of human and computer interviews.
In LREC 2014, pp. 3123–3128.

[2] DeVault D., Artstein R., Benn G., Dey T., Fast E., Gainer A., Georgila K., Gratch J., Hartholt A., Lhommet M., Lucas G., Marsella S., Morbini F., Nazarian A., Scherer S., Stratou G., Suri A., Traum D., Wood R., Xu Y., Rizzo A., Morency L.-P.
SimSensei Kiosk: A virtual human interviewer for healthcare decision support.
In AAMAS 2014, Paris.

---
Author

Jasmine Savathallapalli
