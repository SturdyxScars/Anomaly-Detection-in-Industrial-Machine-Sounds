# Audio Anomaly Detection using Autoencoders and 1D CNN

This project demonstrates unsupervised anomaly detection in audio signals using a 1D Convolutional Autoencoder and reconstruction error-based decision thresholds. It focuses on identifying anomalous patterns by training only on normal audio signals and leveraging reconstruction errors during inference to flag deviations.

---

## 📌 Project Highlights

- **Preprocessing**: Converted raw audio samples into normalized mel spectrograms.
- **Autoencoder Model**: A 1D Convolutional Autoencoder was trained using only normal audio signals to learn latent representations that minimize reconstruction loss.
- **Reconstruction Error Analysis**:
  - Mean Squared Logarithmic Error (MSLE) was used to compute reconstruction loss.
  - A histogram of reconstruction errors on normal data was plotted to estimate a statistical threshold.
  - During testing, audio samples (including anomalies) were evaluated — high error indicated abnormality.
- **Anomaly Detection Logic**:
  - If reconstruction error > threshold ⇒ **Abnormal**
  - Else ⇒ **Normal**

---

## 🧠 Techniques Used

- Unsupervised training (normal sounds only)
- 1D Convolutional Autoencoder
- MSLE for reconstruction loss
- Threshold-based binary classification (statistical cutoff)
- Histogram-based threshold calibration

---

## 🧪 Technologies Used

- Python  
- TensorFlow / Keras  
- Librosa  
- NumPy, Matplotlib  

---

## 📊 Results

- Clear separation between normal and abnormal reconstruction error distributions.
- MSLE reconstruction threshold successfully detected outliers in unseen data.
- Mel spectrogram visualizations reinforced spectral differences in abnormal signals.

---

## ⚠️ Dataset

Audio files used for training and testing are not included in this repository. You may use:
- Your own `.wav` samples
- Public datasets like [DCASE Challenge](https://dcase.community/challenge2020/task-unsupervised-detection-of-anomalous-sounds)

---

## 🚀 Future Extensions

- Replace static thresholding with probabilistic or adaptive methods (e.g., z-score, KDE)
- Real-time anomaly flagging from microphone input
- Transfer to edge devices using TensorFlow Lite

---

## 👤 Author

**Chinmay Bhandare**  
📫 [chinmay.bhandare2003@gmail.com](mailto:chinmay.bhandare2003@gmail.com)  
🔗 [GitHub](https://github.com/SturdyxScars)
