# MedDefend: A novel lightweight adversarial detection method to detect adversarial attacks in Medical IoT.

Official repo for - MedDefend: Securing Medical IoT with Adaptive Noise Reduction based Adversarial Detection.

If you have any queries, please contact [nirmaljoseph@rit.ac.in](URL)

## 📝 Key Features

* MedDefend is an adversarial detection framework specifically developed for seamless integration with Medical IoT systems.
* MedDefend has been evaluated on five distinct datasets across three image modalities, utilizing five major attack methodologies under multiple classification settings.
* MedDefend can be seamlessly integrated with IoT systems that utilize DNN classifiers, requiring only the classifier specification and no other information.

## 🔧 Instructions to Run the Code

* Download the datasets from [https://ieee-dataport.org/open-access/indian-diabetic-retinopathy-image-dataset-idrid](URL), [https://www.kaggle.com/c/aptos2019-blindness-detection/data](URL), [https://www.kaggle.com/datasets/andrewmvd/isic-2019](URL), https://www.kaggle.com/datasets/bhaveshmittal/melanoma-cancer-dataset or you can use your own dataset and modify the rest of the code accordingly.
* Use PyTorch platform and compatible Python version. (We have used PyTorch version compatible with Python version 3.10.)
* In this work, we have used the base models ResNet-V2,  Inception-v3, ResNet-50, EfficientNet-B0 as backbone architectures for different datasets as explained in the paper. You are free to choose the model as per your convenience. Be sure to fine tune the model to achieve the accuracy we were obtained or even better!!.
* You can train the model as binary or multiclass as you desire. While doing binary classification, please be sure that you are grouping all abnormal classes into one.
* Once the model is ready, generate the Class Activation Map (CAM) for a single image from the final convolutional layer of the model and do a manual verification whether the model actually looks into the area of interest or not.
 ## ⚔️ Attack Generation
* Now since you have a PyTorch model, you can use Torchattacks 3.5.1 package to generate different attacks. pip install the package.
* Implement some attacks and test the attack effectiveness. Tune it by varying the attack parameters to the desired level.
* You can generate the attacks on the go from the input images and directly take corresponding predictions to make everything to be done in a single step and to save memory.
* Now we are good to go, the functions for generating CAM, noise addition, RPCA denoising etc. are provided in the repository. Go to the main function and use them sequentially as explained in the paper (refer the algorithm).

## 🖼️ Sample Images


## 🔬 Experimentation
You can use other publicly available datasets or your own dataset to experiment with MedDefend with new attack methdologies and data modalities. We believe a well trained model with proper parameter tuning will yield good results across all datasets.


## 📃 Citation
If you find this repository useful, please consider citing this paper:   **To be added soon!!!**
