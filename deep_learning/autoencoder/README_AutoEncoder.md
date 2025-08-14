# 🧠 Simple Autoencoder for MNIST

This project demonstrates a **basic convolutional autoencoder** built using Keras and TensorFlow. It trains on the **MNIST** dataset to learn efficient image representations through unsupervised learning. The goal is to compress and reconstruct handwritten digits.

---

## 📌 Overview

An **autoencoder** is a type of neural network used to learn efficient codings of input data. It consists of two main parts:

- **Encoder**: Compresses the input into a lower-dimensional representation.
- **Decoder**: Reconstructs the original input from this compressed form.

This notebook shows a clean, minimal implementation for beginners to understand how convolutional autoencoders work.

---

## 📂 Project Structure

```
AutoEncoder_Simple_Ver1.ipynb
```

Everything is inside a single, clean notebook for easy understanding and execution.

---

## 🧪 Model Architecture

### 🔷 Encoder:
- Conv2D → 32 filters, ReLU, same padding
- MaxPooling2D
- Conv2D → 16 filters, ReLU, same padding
- MaxPooling2D

### 🔶 Decoder:
(Not shown in code preview, assumed to reverse the encoder)
- Conv2DTranspose or UpSampling2D layers to reconstruct 28x28 image

---

## 🖼️ Dataset

- **MNIST handwritten digits** (28x28 grayscale images)
- Labels are ignored since this is **unsupervised learning**
- Data is normalized to the [0, 1] range

```python
(x_train, _), (x_test, _) = mnist.load_data()
x_train = x_train / 255.0
x_test = x_test / 255.0
```

---

## ▶️ How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Machine-Learning.git
   cd Machine-Learning/autoencoders/
   ```

2. Install dependencies:
   ```bash
   pip install tensorflow keras matplotlib
   ```

3. Open the notebook:
   ```
   jupyter notebook AutoEncoder_Simple_Ver1.ipynb
   ```

4. Run all cells to train the model and view reconstructions.

---

## 📈 Outputs

- Loss curve (optional if implemented)
- Side-by-side comparison of original vs reconstructed MNIST digits

---

## 🛠️ Dependencies

- Python ≥ 3.7
- TensorFlow
- Keras
- Matplotlib (optional for plotting)

---

## 📄 License

MIT License. Feel free to use, modify, and share with attribution.

---

## 🙋‍♂️ Author

Your Name  
📫 [LinkedIn](https://linkedin.com/in/your-profile)  
🌐 [Portfolio](https://your-website.com)

---

## ⭐️ Star This Repo

If you find this useful or educational, please consider giving it a ⭐️ on GitHub!
