# Pose-Based Shot Intensity Classification & flexiSeq Framework  

## 📌 Overview  
This project focuses on **classifying cricket batsman shots as high or low intensity** from match video using pose landmarks. It also introduces **flexiSeq**, a modular benchmarking framework for sequence models that streamlines experimentation, comparison, and reproducibility.  

The repository is organized into three components:  
1. **`flexiSeq/`** – Framework for benchmarking deep sequence models.  
2. **`commentary_cricket_project/`** – Tools for scraping match commentary and aligning it with video frames.  
3. **`anuj_batsman_detect/`** – Code for batsman detection and pose-based feature extraction from cricket videos.  

---

## 🚀 Features  
- **Batsman Detection & Pose Extraction**  
  - YOLOv8 used for tracking and cropping the batsman.  
  - MediaPipe Pose for per-frame keypoint extraction.  

- **Preprocessing & Filtering**  
  - Sequence normalization, masking/padding for variable-length clips.  
  - Optional smoothing with Kalman, EMA, and SMA filters.  

- **flexiSeq Framework**  
  - Object-oriented, plug-and-play design.  
  - Model registry for easy addition of new architectures.  
  - Unified training/evaluation loops and checkpointing.  

- **Model Benchmarking**  
  - Implemented and compared LSTM, CNN1D, TCN, Transformer, and LSTM Autoencoder.  
  - Weighted F1 score performance across models.  

- **Commentary Integration**  
  - Selenium-based scraping of live/archived match commentary.  
  - Temporal alignment of commentary with video events.  

- **Visualization & Analysis**  
  - Matplotlib-based dashboards for per-shot intensity labeling.  
  - Player-wise statistics and match summaries.  

---

## 📊 Results  
- Achieved best performance with **CNN1D + moving average filter**:  
  - **Weighted F1 = 0.737**  
- Overall model performance: **0.70 – 0.737 (weighted F1)**  
- Delivered robust per-shot intensity labels for cricket analytics dashboards.  
- Reduced benchmarking overhead with flexiSeq, improving reproducibility and modular experimentation.


---

## 📂 Repository Structure
```
├── flexiSeq/                 # Benchmarking framework (OOP design, model registry, training loops)
├── commentary_cricket_project/ # Commentary scraping & temporal alignment tools
├── anuj_batsman_detect/        # YOLOv8 + MediaPipe Pose for player detection & pose sequence extraction
└── README.md                 # Project documentation
```

---

## 🔧 Tech Stack  
- **Computer Vision**: YOLOv8, MediaPipe Pose  
- **ML/DL Frameworks**: PyTorch, scikit-learn, NumPy, SciPy  
- **Visualization**: Matplotlib  
- **Web Scraping**: Selenium  
- **Utilities**: Pandas, OOP-based framework design  

---


