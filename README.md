# SoK : Adversarial-Threats-Against-DL-Approaches-for-AAD-Systems-in-SDN-IoT-Networks

- [Link for the Paper]( soon !!)

## Datasets Used

Please download the original datasets in the following sources:

- [CICIDS2017](https://www.unb.ca/cic/datasets/ids-2017.html)
- [CICIOT2023](https://www.unb.ca/cic/datasets/iotdataset-2023.html)
- [InSDN Dataset](https://aseados.ucd.ie/datasets/SDN/)


## Models Trained

The project trained the following model for each dataset:

- CNN
  
### CNN Model Configuration Summary

| Component     | Configuration |
|---------------|---------------|
| Conv Layers   | 2 × Conv1D (64 → 128 filters, kernel size = 6, ReLU) |
| Pooling       | MaxPooling1D (pool size = 2) after each Conv layer |
| Dense Layers  | 2 × Dense (128 → 64 units, ReLU) + Dropout (rate = 0.1) |
| Output Layer  | Dense (*n_classes* units, Softmax) |
| Training      | Adam (learning rate = 0.0001), Categorical Cross-Entropy, 30 epochs, batch size = 128 |


Models are trained using standard preprocessing (scaling, encoding, binary labelling).

---

## Adversarial Attacks

The project currently uses the following attacks that were generated using [ART](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/):

- Fast Gradient Method (FGM) Attack
- Carlini and Wagner (C&W) Attack
- DeepFool Attack
- Poisoning Attack
- Membership Inference Attack
- Transferable Attack with FGM


## Tools & Technologies used

- Python, TensorFlow
- CICIDS2017, InSDN, CICIOT23 datasets
- NumPy, Pandas, Scikit-learn, ART
