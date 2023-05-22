# Breast Cancer Detection using CNNs in TensorFlow

This project uses Convolutional Neural Network (CNN) for Breast Cancer detection (a classification problem). 

## Stats about breast cancer

According to the World Health Organization (WHO), in 2020 alone, there were [2.3 million](https://www.who.int/news-room/fact-sheets/detail/breast-cancer) reported cases of breast cancer among women, resulting in **685,000** deaths worldwide. By the end of the same year, there were approximately **7.8 million** women who had been diagnosed with breast cancer within the past five years, establishing it as the most prevalent form of cancer globally.

Worldwide, female breast cancer is the [fifth](https://www.cancer.net/cancer-types/breast-cancer/statistics#:~:text=It%20is%20estimated%20that%2043%2C700,world%20died%20from%20breast%20cancer.) leading cause of death. 

## Introduction


As stated by [Pamela Wright](https://www.hopkinsmedicine.org/health/conditions-and-diseases/breast-cancer/invasive-ductal-carcinoma-idc), the medical director of the Breast Center at Johns Hopkins, **Invasive Ductal Carcinoma** (**IDC**), also referred to as **infiltrating ductal carcinoma**, is the predominant type of breast cancer. It represents 80% of all breast cancer diagnoses. For further information about IDC, please refer to this [article](https://www.breastcancer.org/types/invasive-ductal-carcinoma). In the context of this project, we have developed a classification model based on Convolutional Neural Networks (CNNs) using TensorFlow. The model utilizes **Histopathology Images** of patients to classify whether they have breast cancer or not!

## Dataset
We are using the dataset from Kaggle. It can be accessed [here](https://www.kaggle.com/datasets/paultimothymooney/breast-histopathology-images/code?datasetId=7415&sortBy=voteCount). Following are some of the properties of this dataset:

The initial dataset comprised 162 slide images of breast cancer specimens scanned at a magnification of 40x. Due to their large dimensions, 277,524 patches measuring 50×50 pixels were extracted from these images to improve their manageability. These patches encompass the regions that contain Invasive Ductal Carcinoma (IDC), thereby enabling more efficient processing and analysis.

* 198,738 negative examples (i.e., no breast cancer)
* 78,786 positive examples (i.e., indicating breast cancer)

The dataset assigns a unique filename structure to each image, like:
```
u_xX_yY_classC.png 

```
For example:
```
10253_idx5_x1351_y1101_class0.png
```

- "u" is patient id
- "u" is the patient ID (10253_idx5), 
- "X" is the x-coordinate of where this patch was cropped from, 
- "Y" is the y-coordinate of where this patch was cropped from, and 
- "C" indicates the class where 0 is non-IDC and 1 is IDC. 
