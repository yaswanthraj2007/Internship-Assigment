                        Character Recognition Neural Network — From Scratch (NumPy) 

A feedforward neural network implemented entirely from scratch using NumPy (no TensorFlow/PyTorch/Keras) to classify 35 character classes: uppercase letters A–Z and digits 1–9.

==> Overview

- Dataset : 2,100 synthetically generated character images (60 samples/class), created with multiple fonts + random rotation/noise augmentation
- Architecture : 784 → 128 (ReLU) → 64 (ReLU) → 35 (Softmax)
- Training : mini-batch gradient descent, cross-entropy loss, manually derived backpropagation
- Results : 100% test accuracy on in-distribution data; 70% accuracy on a deliberately harder stress-test set (see `report/report.md` for full analysis)

==> Repository Structure

```
character-recognition-nn/
├── Assigment.ipynb          # Full notebook: data generation, network, training, analysis
├── data/
│   └── character_dataset.npz
├── images/
│   ├── training_curves.png
│   ├── confusion_matrix.png
│   └── hard_misclassified_examples.png
├── report/
│   └── report.md             # Full methodology & analysis report
├── .gitignore
└── README.md
```
==> How to Run

1. Clone the repo:
   ```
   git clone https://github.com/<your-username>/character-recognition-nn.git
   cd character-recognition-nn
   ```
   
2. Set up environment:
```
   python -m venv venv
   venv\Scripts\activate      # Windows
   source venv/bin/activate   # Mac/Linux
   pip install jupyter numpy matplotlib seaborn pillow scikit-learn
  ```
3. Launch Jupyter and open `Assigment.ipynb`:
   ```
   jupyter notebook
   ```
4. Run all cells sequentially (Kernel → Restart Kernel and Run All Cells).

==> Key Results

                            +======================================================+
                            |                    Metric                   |  Value |
                            |---------------------------------------------|------- |
                            | Test Accuracy                               | 100.0% |
                            | Test Loss                                   | 0.0027 |
                            | Stress-test Accuracy (heavy rotation/noise) | 70.0%  |
                            +======================================================+

See `report/report.md` for the full methodology, architecture reasoning, and misclassification analysis.

== >Author

Yaswanth Raj R — B.Tech AI & Data Science, 
Chennai Institute of Technology

