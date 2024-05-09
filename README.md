# About Center for Epidemiological Modelling & Analysis (CEMA)
CEMA brings together a multidisciplinary consortium of epidemiologists, infectious disease specialists, clinicians, mathematicians, statisticians, computer scientists and data scientists using data-driven approaches to control infectious diseases and improve health in Kenya and the African Continent. It bridges disciplines across different schools within the University of Nairobi (UoN) and the private sector to deliver timely analysis to inform policy to tackle infectious diseases and improve health outcomes. Read more about CEMA from their [official website](https://cema-africa.uonbi.ac.ke/).
 
 # CEMA Internship - Computer Science Track
 In this repo, you will find a machine learning model that I was assigned to come up with using TensorFlow.<br><br>
 ## OBJECTIVE<br>
 Create a machine learning model that is able to classify whether a blood smear is either uninfected or parasitized with the Plasmodium parasite.<br><br> 
 ## METHODOLOGY<br>
 ### 1). Data Collection
For this task, I used a sample* of thin blood smear slide images of segmented cells data from the simplified [Kaggle Malaria Dataset](https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria) that was obtained under licenses by [The National Institutes of Health](https://lhncbc.nlm.nih.gov/LHC-downloads/downloads.html#malaria-datasets).<br>
### 2). Data Pre-Processing
After checking & organizing the cell images based on whether they were uninfected or parasitized, the following step was to pre-process the images (both uninfected & parasitized cell images) using TensorFlow's `ImageDataGenerator` in rescaling, augmentation, & resizing.<br>
### 3). Model Building
I proceeded with designing a Convolutional Neural Network (CNN) that utilized convolutional layers for feature extraction, pooling layers for dimensionality reduction, & connected layers for classification. The number of layers, filters, & activation functions were hyperparameters that can be tuned for optimal performance.<br>
### 4). Model Training
The training data was used to train the built model using the `model.fit` which iterated through the training data while adjusting the model's internal parameters to minimize the loss function which indicates how well the model classifies. A validation set was used to monitor the model's performance during training thus reducing overfitting (in case there was).<br>
### 5). Model Evaluation<br>
The trained model was then subjected to evaluation using the metrics: accuracy, precision, and recall - These metrics provided a comprehensive understanding to me on the model's effectiveness in classifying the blood smear as either uninfected or parasitized.<br>
### 6). Model Reflection<br>
This' a basic framework for building a machine learning model for malaria parasite classification, its effectiveness depends heavily on the quality & size of the training data - Utilizing more complex architectures can potentially enhance performance.

## IDE GUIDE DOCUMENTATION
For this task, I utilized Google's online platform - Google Colab, because of the free GPU access which significantly sped up my model training & testing which are computationally intensive. If you prefer to perform this offline, then there are few modifications that should be made to few sections in the  general structure for the model to be successful. Here are the steps:<br><br>
i). Download the ["datasets" folder](https://drive.google.com/drive/folders/1z_0JfgpLw0IgjNx68NjElKwohd_0LzbP?usp=drive_link) & save it in your local computing device. If you prefer to use the entire non-sampled dataset, you can download the ["Kaggle Simplified Dataset"](https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria) or the ["NIH Original Dataset"](https://data.lhncbc.nlm.nih.gov/public/Malaria/NIH-NLM-ThinBloodSmearsPf/index.html).<br>
ii). Download the `CEMA ML.ipynb` file from this repository & save it locally.<br>
iii). Using your IDE, open the `CEMA ML.ipynb` & make the following changes:<br>
- delete the `GOOGLE DRIVE MOUNTING` cell block because you already have the data saved locally.<br>
- delete the `EXECUTING SHELL COMMANDS` cell block in the `ENVIRONMENT SET-UP` section if you already have the listed libraries installed, but if you lack then remove the `!` mark from the codes in the cell block & execute the cell.<br>
- in the `IMAGE PATH DEFINITIONS` section, rename the data paths to that of your device where your respective folders & subfolders are located.<br>
iv). Execute the other model sections without making any changes (unless you are making modifications).<br><br>

For any questions or clarifications regarding this repo/task, write to me via philipmudambo1999@icloud.com<br><br>

#### STARRED NOTE!<br>
sample* - In an ordered manner, I sampled the first few images for this task based on the availability of my computing resources (laptop's CPU & clock speeds). Training the model with the whole set of data would require a computer with very high processing speed and power. In case you need the whole data for that, you can obtain it from [NIH Official Website](https://lhncbc.nlm.nih.gov/LHC-research/LHC-projects/image-processing/malaria-datasheet.html)
