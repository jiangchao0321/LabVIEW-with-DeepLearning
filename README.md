# LabVIEW DeepLTK Bearing Fault Diagnosis Demo
A LabVIEW DeepLTK demo for CNN-based bearing fault diagnosis using the CWRU dataset.

This repository provides a LabVIEW DeepLTK-based demo for intelligent bearing fault diagnosis using the CWRU bearing dataset. The demo demonstrates how to integrate a deep learning model into the LabVIEW environment through DeepLTK, including signal loading, CNN-based fault classification, prediction output, and diagnostic result visualization. The current version focuses on validating the feasibility of implementing deep learning-based bearing fault diagnosis within LabVIEW using DeepLTK.

## Environment Requirements
- **Operating System:** Windows 10 / Windows 11, 64-bit recommended  
- **LabVIEW:** LabVIEW 2020 or later recommended  
- **Deep Learning Toolkit:** DeepLTK / Deep Learning Toolkit for LabVIEW  
- **Package Manager:** NI Package Manager or JKI VI Package Manager (VIPM)  
- **Dataset:** CWRU Bearing Fault Dataset  
- **Hardware:** No real-time DAQ hardware is required for the current offline demo


## “Model Train” Interface Usage

The model training interface is shown below. The main operation steps are as follows:

<p align="center">
  <img src="model_train_interface.png" alt="Model Training Interface" width="900">
</p>


1. **Load dataset paths**  
   Set the paths of the training dataset and test dataset in Area ①, and then click the **DataIn** button to load the data.

2. **Configure training parameters**  
   Configure the optimizer, learning rate update policy, data sampling strategy, warm-up settings, and accelerator device in Area ②.

3. **Start model training**  
   Click the **Start** button to begin training. During training, the training loss, test loss, and test error curves are displayed in real time in Area ③.

4. **Validate the model**  
   Click the **Eval** button during or after training to evaluate the model performance. The confusion matrix, recall, and precision values are displayed in Area ④.

5. **Monitor training status**  
   The current epoch, total iterations, learning rate, training loss, test loss, test error, and elapsed training time are displayed on the right side of the interface.

6. **Stop and save the model**  
   After the loss has converged, click the **STOP** button. The trained network configuration and weights will be automatically saved as `.cfg` and `.bin` files in the following folder: working/Fault_Classifier.

