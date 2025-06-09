# 🧠 Flickd AI Hackathon 2025 — Fashion Intelligence Pipeline

This repository contains our end-to-end solution for the Flickd AI Hackathon. It processes real-world fashion videos to identify worn items and map them to a product catalog using advanced vision-language models.

---

## 🚀 Pipeline Overview

| Step | Task | Tools Used |
|------|------|------------|
| 1️⃣   | Frame Extraction + Segmentation | OpenCV, DeepLabV3 |
| 2️⃣   | Clothing Detection | YOLOv8 (custom-trained on fashion) |
| 3️⃣   | Product Matching | OpenAI CLIP + FAISS |
| 4️⃣   | Vibe Classification | (Skipped due to missing captions) |
| 5️⃣   | Final JSON Output | Standardized output per competition spec |

---

## 🧾 Sample Output Format

```json
{
  "video_id": "2025-05-28_13-42-32_UTC",
  "vibes": [],
  "items": [
    {
      "type": "handbag",
      "match_type": "similar",
      "matched_product_id": 14983,
      "confidence": 0.872,
      "title": "Mini leather crossbody"
    }
  ]
}
