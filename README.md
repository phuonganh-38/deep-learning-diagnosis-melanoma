# **Deep Learning System for Differential Diagnosis of Melanoma**
This project is a deep learning system designed to assist in the differential diagnosis of melanoma using medical imaging. The project includes data preprocessing, model training, evaluation, and deployment recommendations for real-world applications in healthcare.

---

## **Introduction**

Melanoma is one of the most aggressive types of skin cancer. Early and accurate diagnosis is essential for effective treatment and improved patient outcomes. This project leverages deep learning to classify images as melanoma or non-melanoma, aiming to support dermatologists in making more accurate diagnostic decisions.



## **Key objectives**

1.	Develop an Effective Model: Using deep learning, primarily convolutional neural networks (CNNs), trained on the selected dataset, to obtain high accuracy in diagnosing melanoma in skin lesion images. This model seeks to meet clinical requirements and deliver trustworthy findings by attaining an accuracy rate of at least eighty percent.
2.	Improve Diagnostic Efficiency: Automating the image analysis procedure will reduce on the amount of time doctors need to identify melanoma. Dermatologists may be able to concentrate more on treating patients as a result, improving health outcomes.
3.	Establish an Accessible Interface: Make the model available through an accessible Streamlit app so that dermatologists and other medical professionals can readily use it. By offering real-time melanoma detection, this application improves accessibility in distant and clinical settings.
4.	Enhance dermatological Research with AI: We also intend for further study on dermatological uses of AI by investigating how deep learning may help identify melanoma early and could be modified for other skin conditions.



## **Usage**

1. Upload the datasets to Google Drive (if you use Google Colab) or Jupyter Notebook (if you use Jupyter Notebook)

  - HAM10000_metadata.csv: contains 10,015 rows of metadata for the HAM10000 dataset
  - HAM10000_images_part_1: contains 5000 skin lesion images
  - HAM10000_images_part_1: contains 5015 skin lesion images
3. Run the notebook `model.jpynb`



## **Dataset**

The [HAM10000 dataset](#https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000) comprises a total of 10,015 dermatoscopic images for detecting pigmented skin lesions, including a representative collection of 7 diagnostic categories. We divided into 2 classes: melanoma (11.2%) and non-melanoma (88.8%).



## **Features**

- [Data Preprocessing](data-preprocessing-and-EDA.jpynb)
- [Exploratory Data Analysis (EDA)](data-preprocessing-and-EDA.jpynb)
- [Hair Removal](hair-removal.jpynb)
- [Streamlit App](https://dlsd-melanoma-detection.streamlit.app/)
- Data Augmentation

| Techniques         | Range             | Description                                                                 |
|--------------------|-------------------|-----------------------------------------------------------------------------|
| Resize             | 224x224           | Resizes all images to 224x224 pixels to standardize input dimensions for the model |
| Rotation           | 20 degrees        | Randomly rotates images by up to 20 degrees to add variability in orientation. |
| Width shift range  | 0.2               | Shifts images horizontally by 20% of the image width to simulate movement or misalignment. |
| Height shift range | 0.2               | Shifts images vertically by 20% of the image height to simulate movement or misalignment. |
| Shear range        | 0.2               | Applies shearing transformations with a range of 0.2 to slightly tilt the image. |
| Zoom               | 0.2               | Zooms images by up to 20% in or out                                        |
| Horizontal flip    | True              | Randomly flips images horizontally to enhance the model’s robustness        |
| Brightness range   | [0.8, 1.2]        | Adjusts brightness within the range of 0.8 to 1.2                           |
| Fill mode          | nearest           | Fills any empty areas created by transformations with the nearest pixel value to avoid artifacts |



## **Models Used** 

Convolutional Neural Network (CNNs) with these architecture:
1. Inception-V3
2. ResNet-50
3. EfficienNet-B4


