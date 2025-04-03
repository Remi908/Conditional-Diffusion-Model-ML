# Conditional-Diffusion-Model-ML
https://colab.research.google.com/gist/Remi908/40b05da5b992671591368dd550225529/untitled16.ipynb
🧠 Contextual Diffusion Model for MNIST
This project implements a conditional diffusion model using a Contextual U-Net architecture to generate handwritten digits from the MNIST dataset.

🔍 Key Features:
Dataset: 28x28 grayscale MNIST images (digits 0–9)

Architecture: U-Net enhanced with residual convolution blocks
![image](https://github.com/user-attachments/assets/aa8c62b7-27dc-4a59-b42f-5ff1540b6142)


Conditional Generation: Class-conditioned via Classifier-Free Guidance and context masking

Diffusion Process:

Forward Diffusion: Adds Gaussian noise using a linear beta schedule

Reverse Process: Learned by the model using MSE loss

Sampling Control: guide_w allows adjustment of how strongly the output aligns with the target class

Optimizer: Adam with linearly decaying learning rate
![image](https://github.com/user-attachments/assets/2439f0c9-c568-4443-bd02-dfe544f27f34)


Data Pipeline:

Normalize and convert images to tensors

Batch and shuffle (batch size = 256)

One-hot encode class labels
![image](https://github.com/user-attachments/assets/d1108778-76b5-4492-a211-ef9115a9045d)


📦 Output:
Generates MNIST-like digit images conditioned on target classes with adjustable guidance strength.
![image](https://github.com/user-attachments/assets/c67d5d2b-fcaf-4772-8632-a7347a13ab00)


