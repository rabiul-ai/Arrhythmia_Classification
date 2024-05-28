# Arrhythmia Classification
## CAT-Net: Convolution, attention, and transformer based network for single-lead ECG arrhythmia classification
by-**Md Rabiul Islam**, PhD Student, Electrical and Computer Engineering, Texas A&M Univeristy; (BSc, MSc: EEE, KUET, Bangladesh).

## **Task - At A Glance:**
Assalamu Alaikum. A CNN, attention and transformer based efficient hybrid model is developed to classify 5 classes of arrhythmias using single-lead ECG signals.
1. **Task:** Arrhythmia Classification - 5 Classes (N, S, V, F, Q)
2. **Input:** ECG Signal (Actually ECG Heartbeats)
3. **Output:** Arrhythmia Class
4. **Class Balancing Approach:** 3 techniques (SMOTE, SMOTE-Tomek, ADASYN) implemented - Finally SMOTE-Tomek is applied
5. **Datasets:** 2, (1) MIT-BIH, (2) INCART
6. **Results:** State-of-the-art, MIT-BIH - **99.14%** (5 Class), INCART - **99.58%** (3 Class)


## **Coding Details- Main Parts of the Study:** 
The complete code is given in the 'Arrhythmia Classification Full and Final Code.ipynb' file.
1.   **Part A: Installing Packages and Basic Visualization of ECG**
2.   **Part B: Denoising, R-Peak Detection, Segmentation**
3.   **Part C: Dataset Loading**
4.   **Part D: Train-Test Splitting and Class Balancing**
5.   **Part E: Model Building and Training**
6.   **Part F: Results**

## **Publication**
The paper is published in **Biomedical Signal Processing and Control** Journal, Elsevier. You are rcommended to check the [PAPER](https://www.sciencedirect.com/science/article/pii/S1746809424002696).
### **Abstract**
Machine learning technologies have been applied extensively in the last decade to automatically detect and analyze various forms of arrhythmia from electrocardiogram (ECG) signals. Existing deep learning-based models focus on enhancing classification performance by exploring spatial–temporal ECG features or by implementing multi-modal and ensemble classifiers. Such approaches perform well but do not provide comprehensive accessibility for real-life applications due to the multi-lead ECG requirement. To address the issue, a single-lead ECG based network is considered. The proposed convolution, attention, and transformer-based network (CAT-Net) exhibits promising performance on arrhythmia classification by adeptly capturing local and global heartbeats’ morphological characteristics. Along with the local information captured by the convolution layer, the contextual ECG information is extracted by the multi-head attention layer present in the transformer encoder. In addition, most of the existing models suffer from lower predictive performance in minority-class arrhythmias due to the highly imbalanced ECG data. To enhance the predictive performance in minority classes, three balancing techniques – SMOTE-ENN, SMOTE-Tomek, and ADASYN – are systematically evaluated, and SMOTE-Tomek is ultimately integrated. To mitigate potential dataset bias, CAT-Net was assessed across two distinct datasets: MIT-BIH and INCART, respectively, and was shown to achieve state-of-the-art performance. CAT-Net establishes new benchmarks, achieving 99.14% overall accuracy and 94.69% macro F1 score on 5-class arrhythmia classification in the MIT-BIH dataset and 99.58% accuracy with 96.15% macro F1 score for 3-class classification in the INCART dataset.

## **My Personal Website**
> [!NOTE]
> To know more about me, you are requested to visit my [Personal Website](https://sites.google.com/view/rabiuleeekuet/home)

## **Research Collaboration - Open**
> [!IMPORTANT]
> To extend my research work, I have some exciting ideas. To make reseach collaboration with me, feel free to contact by email-rabiul_islam@tamu.edu or contacts available in my [Personal Website](https://sites.google.com/view/rabiuleeekuet/home). Thank you. Bye.

## **CAT-Net Overview**
### **Highlights** ###
* Integrates convolution, attention, and transformer for local–global ECG insights.
* Employs SMOTE-Tomek for improved minority class predictions.
* Achieves top results on two different datasets validate the model’s generalization capacity.
* Suited for 1-lead ECG data in real-world IoT and wearable applications.
![CAT-Net overview](https://github.com/rabiul-ai/Arrhythmia_Classification/assets/106368359/b1441371-5487-4c56-bab1-739412e79c88)

## **Dataset- 1: MIT-BIH**
This study employed two datasets, (i) MIT-BIH Arrhythmia Database and (ii) St. Petersburg INCART 12-lead Arrhythmia Database.
![fig all heartbeats](https://github.com/rabiul-ai/Arrhythmia_Classification/assets/106368359/f82942a5-4c89-43ee-9089-3050c6a4dac4)

## **Dataset- 2: INCART**
![all_heartbeats_INCART](https://github.com/rabiul-ai/Arrhythmia_Classification/assets/106368359/486b9626-340a-425f-a519-0c5c03efed30)

## **Preprocessing**
Data preprocessing assumes two consecutive steps: (i) signal denoising and (ii) heartbeat segmentation. The raw ECG signals downloaded from the MIT-BIH and INCART website are perturbed by noise induced by the power line interface, myoelectric interface, etc. The popular discrete wavelet transform (DWT)-based method is used to denoise the 1D ECG signal. The wavelet denoising procedure undertakes three distinct operations to remove noise from the ECG signal: (i) wavelet decomposition, (ii) coefficient processing, and (iii) wavelet reconstruction, respectively.
![fig preporcessing](https://github.com/rabiul-ai/Arrhythmia_Classification/assets/106368359/44d87854-bf77-485e-9dc4-e3969ef7f6f4)

## **CAT-Net Architecture**
The classification model architecture consists of three main components: (i) CNN, (ii) attention mechanism, and (iii) transformer encoder. The transformer encoder is described in a separate sub-section with its components. At the end of the complete framework, the feature map is sent to a flattened layer and to the dense layers for prediction.
![CAT Net Model](https://github.com/rabiul-ai/Arrhythmia_Classification/assets/106368359/45c89631-2c69-40a2-b6df-3a886a69c7e8)


## **Conclusion **
The study proposed a novel CAT-Net model to predict five distinct arrhythmia classes using single-lead ECG signals. By leveraging the capabilities of CNN, channel attention, and transformer encoder architectures, both local and global ECG features were incorporated into the model. It was found that SMOTE-Tomek represents the optimal class balancing approach for ECG data. The model’s robustness is validated across two distinct datasets, and it exhibits consistent performance. Using only 1-lead ECG data, the proposed model achieved 99.14% accuracy and 94.69% F1 score, which represent a remarkable performance. This study corroborates that only 1-lead ECG data is adequate to predict arrhythmias provided that the model is properly designed. The proposed model can be used in IoT-based and mobile arrhythmia diagnosis systems due to the low requirement of working in real-time with patients’ ECG data captured by only one sensing device.

