# **Deep Learning System for Differential Diagnosis of Melanoma**
This project is a deep learning system designed to assist in the differential diagnosis of melanoma using medical imaging. The project includes data preprocessing, model training, evaluation, and deployment recommendations for real-world applications in healthcare.

---

## **Introduction**

Melanoma is one of the most aggressive types of skin cancer. Early and accurate diagnosis is essential for effective treatment and improved patient outcomes. This project leverages deep learning to classify images as melanoma or non-melanoma, aiming to support dermatologists in making more accurate diagnostic decisions.

## **Introduction**

Melanoma is a highly aggressive form of skin cancer, where early diagnosis significantly improves patient outcomes. This project develops a deep learning-based system to differentiate between melanoma and non-melanoma skin lesions, using the **HAM10000** dataset—a widely recognized resource in dermatology research.

## **Key objectives**

- Development of a **convolutional neural network (CNN)** to classify skin lesion images.  
- Comprehensive data preprocessing, augmentation, and exploratory data analysis (EDA).  
- Performance evaluation using metrics such as accuracy, precision, recall, and F1-score.

## **Usage**

1. Upload the datasets to Google Drive (if you use Google Colab) or Jupyter Notebook (if you use Jupyter Notebook)
  ○ HAM10000_metadata.csv: contains 10,015 rows of metadata for the HAM10000 dataset
  ○ HAM10000_images_part_1: contains 5000 skin lesion images
  ○ HAM10000_images_part_1: contains 5015 skin lesion images
2. Run the notebook `model.jpynb`

## **Dataset**

The [HAM10000 dataset](#https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000) comprises a total of 10,015 dermatoscopic images for detecting pigmented skin lesions, including a representative collection of 7 diagnostic categories. We divided into 2 classes: melanoma (11.2%) and non-melanoma (88.8%).


## **Features**

- [Data Preprocessing](#data-preprocessing-and-EDA.jpynb)
- [Exploratory Data Analysis (EDA)](#data-preprocessing-and-EDA.jpynb)
- [Hair Removal](#hair-removal.jpynb)
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


