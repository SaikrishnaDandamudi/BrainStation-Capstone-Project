# **Detection of COVID-19 induced Pneumonia using Chest X-rays (CXR-PA)**  - A Deep Learning Implementation. 

An approach to distinguish between **NORMAL, PNEUMONIA and COVID-19** positive patients using Convolutional Neural Networks for Image classification on Chest X-rays.


### **Disclaimer**: 

* This project is for **educational purposes only**.\
***Please consult a doctor or a professional for expert advice.***

* The methods proposed here are not scientifically proven to help or detect the COVID-19 virus at the moment.

* This is just an apporach at trying to solve this global pandemic as deep learning researchers closely work with medical researchers to improve diagnosis.

* Model Accuracies and claims are based on a small dataset as the chest X-rays are not largely available at the moment for COVID-positive and negative cases. 

* Please do not use these notebook for publishing. Further research and expert opinions are needed to validate the results. 

***Note***:  These notebook were ran on Google's Colab to leverage the GPU processing power. [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/notebooks/intro.ipynb#recent=true)


###### *CXR- Chest X-rays
###### *PA - Posteroanterior View (Frontal View of Chest X-rays)


## Motivation

On March 11, the World Health Organization (W.H.O.) declared Coronavirus disease 2019 **(SARS-CoV-2)** a pandemic characterized by the rapid and global spread of the novel coronavirus around the world. 

As the cases are increasing throughout the world, the major issues is not having access to enough RT-PCR testing kits and the long wait time of the testing results since these are carried out in controlled laboratories. There have been doubts casted about the RT-PCR testing method due to the number of false negatives and false positives reported.

The most vulnerable are people in remote areas within developing countries who generally have inferior healthcare and access to diagnosis. With these in mind, I decided to train and implement a model using CNN detect the COVID-19 positive patients. I decided to train my model on Chest X-rays for the following reasons:

1. Most of the hospitals (including remote areas)  have access to X-ray equipment and they can be produced within a short durations. 
2. These A.I systems can work with the radiologists and help correctly identify. In case a radiologists and medical professionals becomes ill, A.I. systems can still perform the diagnosis. 
3. Once these models become efficient by learning the various patterns, it can minimize the false negatives and false positive diagnosis. 
4. According to a latest statement from W.H.O, there could be more viruses from the coronavirus family with potential of causing another pandemic in future. If successful, we can employ A.I to detect these early and administer proper medical care to the patients. 


## Dataset

#### Preprocessed Dataset

1. The COVID-19 chest X-ray dataset used for the project was derived from the github repository curated by Dr. Joseph Cohen, a postdoctoral fellow at the University of Montreal. This [dataset](https://github.com/ieee8023/covid-chestxray-dataset) is been updated regularly, please support the work and repo.

2. The NORMAL and PNEUMONIA Chest X-ray dataset for the projects were derived from the Kaggle [dataset](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia).


#### Post Processed Dataset

1. COVID-19 vs. NORMAL   
2. COVID-19 vs. NORMAL vs. PNEUMONIA

*Please download the processed X-ray image data [here](https://drive.google.com/drive/folders/1vpX00EI_URZ06-D8Fpqiq6BbPphMy9Jw?usp=sharing)*

##### Description: 
After running through the metadata file available on the COVID-19 [dataset](https://github.com/ieee8023/covid-chestxray-dataset), I was able to download **180 images** of COVID positive patients with the PA view (Frontal view).

In order to avoid class imbalances, only 180 CXR-PA images of NORMAL and PNEUMONIA patients were randomly selected. These were then split into Train and Test sets with 80-20 ratio for both Binary and Multi Class Classification.

*(Please refer to the [EDA_and_Data_Extraction notebook](https://github.com/SaikrishnaDandamudi/BrainStation-Capstone-Project/blob/master/Notebooks/EDA_and_Data_Extraction.ipynb))*

*(The preprocessed data set zip files are provided in this repo)*

## Model Architecture

Binary:

![alt text](https://github.com/SaikrishnaDandamudi/BrainStation-Capstone-Project/blob/master/Images/Model%20Architecture.png?raw=True)

Multi Class:

![alt text](https://github.com/SaikrishnaDandamudi/BrainStation-Capstone-Project/blob/master/Images/Model%20Architecture_Multi.png?raw=True)



### Binary Classification (COVID-19 vs.NORMAL)

Please refer to the [Binary Classification Notebook](https://github.com/SaikrishnaDandamudi/BrainStation-Capstone-Project/blob/master/Binary_Classification_Modeling.ipynb)

##### Statistical Results

Confusion Matrix: 

![alt text](https://github.com/SaikrishnaDandamudi/BrainStation-Capstone-Project/blob/master/Images/Confusion%20Matrix%20Binary%20Class%20Classification.png?raw=True) 

Model Accuracy

![alt text](https://github.com/SaikrishnaDandamudi/BrainStation-Capstone-Project/blob/master/Images/Binary_class_Acc-30Epochs.png?raw=True)

Model Loss

![alt text](https://github.com/SaikrishnaDandamudi/BrainStation-Capstone-Project/blob/master/Images/Binary_class_loss-30Epochs.png?raw=True)



### Multi Class Classification (COVID-19 vs.PNEUMONIA vs.  NORMAL)

Please refer to the [Multi Class Classification Notebook](https://github.com/SaikrishnaDandamudi/BrainStation-Capstone-Project/blob/master/Multi_Class_Classification.ipynb)

##### Statistical Results

Confusion Matrix: 

![alt text](https://github.com/SaikrishnaDandamudi/BrainStation-Capstone-Project/blob/master/Images/Confusion%20Matrix%20Multi%20Class%20Classification.png?raw=True) 


Model Accuracy

![alt text](https://github.com/SaikrishnaDandamudi/BrainStation-Capstone-Project/blob/master/Images/Multi_class_Acc-50Epochs.png?raw=True)

Model Loss

![alt text](https://github.com/SaikrishnaDandamudi/BrainStation-Capstone-Project/blob/master/Images/Multi_class_loss-50Epochs.png?raw=True)

## Run

1. Download the PreProcessed Datasets.
2. Use the EDA_and_Dataextraction.ipynb file to clean, create the train and test sets.
( the processed dataset used along with the zip files and their links are provided in the repo)
3. Open Binary_Classification.ipynb file in Colabs and upload the Binary dataset zip file
4. Run the Binary_Classification.ipynb file for the results
5. Similalry, Open Multi_Class_Classification.ipynb file  and upload the Multi class dataset zip file
6. Run the Multi_Class_Classification.ipynb file for the results

## Contributing
Pull requests are welcome.