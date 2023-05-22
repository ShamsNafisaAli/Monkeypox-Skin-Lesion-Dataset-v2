# Monkeypox-Skin-Lesion-Dataset-v2

![License](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset/blob/main/Assests/cc.png)

The recent monkeypox outbreak has become a global healthcare concern owing to its rapid spread in more than 65 countries around the globe. To obstruct its expeditious pace, early diagnosis is a must. But the confirmatory Polymerase Chain Reaction (PCR) tests and other biochemical assays are not readily available in suffiecient quantities. In this scenario, computer-aided monkeypox identification from skin lesion images can be a beneficial measure. Nevertheless, so far, such datasets are not available. Hence, the ["Moneypox Skin Lesion Dataset (MSLD)"](https://www.kaggle.com/datasets/nafin59/monkeypox-skin-lesion-dataset) is created by collecting and processing images from different means of web-scrapping i.e., from news portals, websites and publicly accessible case reports. <br />

Graphical representation of our intended working pipeline:<br />


![Working pipeline](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset/blob/main/Assests/workflow.png)

* * *

# Contents

This repository gives access to the Moneypox Skin Lesion Dataset. The creation of this dataset is primarily focused on distinguishing the monkeypox cases from the similar non-monkeypox cases. Therefore, along with the 'Monkeypox' class, we included skin lesion images of 'Chickenpox' and 'Measles' because of their resemblance to the monkeypox rash and pustules in initial state in another class named 'Others' to perform binary classification.<br />

The dataset itself is available for download at the [Kaggle](https://www.kaggle.com/datasets/nafin59/monkeypox-skin-lesion-dataset) or the [Google Drive](https://drive.google.com/drive/folders/1bIYqAW-vqDBq3Ou_UMXPwgemqfZeqQi5?usp=sharing).<br />


Some sample images from the dataset:<br />


![Sample Images](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset/blob/main/Assests/sample%20images.png)


* * *

# Dataset Description

<!-- ![Data Division](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset/blob/main/Assests/data.JPG) -->

There are 2 folders in the dataset.<br />

1) Original Images: This folder includes a subfolder named "FOLDS" containing five folds (fold1-fold5) for 5-fold cross-validation with the original images. Each fold has separate folders for the test, train, and validation sets.<br />

2) Augmented Images: To aid the classification task, several data augmentation methods such as rotation, translation, reflection, shear, hue, saturation, contrast and brightness jitter, noise, scaling etc. have been applied using MATLAB R2020a. Although this can be readily done using ImageGenerator/other image augmentors, to ensure reproducibility of the results, the augmented images are provided in this folder. ***Post-augmentation, the number of images increased approximately 14-folds; the classes 'Monkeypox' and 'Others' have 1428 and 1764 images, respectively.***<br />


Additionally, a csv file is provided that has 228 rows and two columns. The table contains the list of all the ImageID(s) with their corresponding label.

![Data Preparation](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset/blob/main/Assests/data_split.png)

* * *


# Sample Notebook for Classification

To see, how you can use this dataset for performing binary classification, please refer to the following notebooks:<br />
- [Notebook1](https://www.kaggle.com/code/gpiosenka/monkey-pox-f1-score-90) <br />
- [Notebook2](https://www.kaggle.com/code/nafin59/monkeypox-sample-classification-notebook)<br />

* * *

# Web-Application

Since we intend to build an end to end solution - starting with dataset creation and ending with a live web app, a prototype of the web-app has already been developed using the open-source python streamlit framework with a flask core and has been hosted in the powerful heroku server for better user experience. In the app, [Monkey Pox Detector](https://monkey-pox-detector-mhealthlab.herokuapp.com/), users can get, not only a suggestion but also the accuracy of the suggestion. <br />

The codes required to build and train the model, all the javascript, css and html files as well as the trained model will be made opem-source soon. The app's dynamic and future updates will incorporate the ability to store user data and use them to train the model realtime.<br />

![Sample Images](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset/blob/main/Assests/app_interface.png)

* * *

# Citation

If this dataset helped your research, please cite the following [paper](https://arxiv.org/abs/2207.03342):<br />

Ali, S. N., Ahmed, M. T., Paul, J., Jahan, T., Sani,  S. M. Sakeef, Noor, N., & Hasan, T. (2022). Monkeypox Skin Lesion Detection Using Deep Learning Models: A Preliminary Feasibility Study. arXiv preprint arXiv:2207.03342.

<blockquote>
  
@article{Nafisa2022,<br />
  title={Monkeypox Skin Lesion Detection Using Deep Learning Models: A Preliminary Feasibility Study},<br />
  author={Ali, Shams Nafisa and Ahmed, Md. Tazuddin and Paul, Joydip  and Jahan, Tasnim and Sani,  S. M. Sakeef and Noor, Nawshaba and Hasan, Taufiq},<br />
  journal={arXiv preprint arXiv:2207.03342},<br />
  year={2022}<br />
}
