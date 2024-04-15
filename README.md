# Anomaly Detection in Electrocardiograms using Autoencoders
The use of autoencoder architectures in anomaly detection.

## Overview
This project aims to detect anomalies in Electrocardiograms (ECGs) using autoencoders. The autoencoder model has been trained on normal ECG data and leverages reconstruction error to identify anomalies. When the model attempts to reconstruct anomalous data, the reconstruction error tends to be higher compared to normal data. This discrepancy in error serves as a distinguishing factor, allowing the model to identify and flag anomalies in the ECG signals.

## Autoencoder Network Architechture
![RAG](ae.png)
Image credit to 'Lilian Weng'

## How it Works
<i><b>Data Preparation</b></i><br/>
- The ECG data is preprocessed and normalized before being fed into the autoencoder model.<br/>

<i><b>Model Training</i></b><br/>
- The autoencoder model is trained on a dataset consisting of normal ECG samples.
- During training, the model learns to reconstruct normal ECG patterns with minimal error.<br/>

<i><b>Anomaly Detection</i></b><br/>
- Once the model is trained, it is used to reconstruct both normal and anomalous ECG samples.
- The reconstruction error, which measures the difference between the original ECG and its reconstruction by the autoencoder, is calculated for each sample.
- Anomalies are detected based on a threshold set on the reconstruction error.
- ECG samples with reconstruction errors exceeding the threshold are flagged as anomalies.




