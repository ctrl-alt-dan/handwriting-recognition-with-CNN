# Doctor's handwriting recognition with a CNN Classifier
#### Summary
This capstone project trained a 78-class CNN in PyTorch on 3,120 handwritten medication samples to learn visual handwriting features and predict drug names. In two weeks, the model achieved 82.9% Top-1 accuracy and 0.826 Macro F1 using adaptive pooling, regularisation, label smoothing, and confusion-aware optimisation.

#### Problem Statement
Australia’s online pharmacy market remains constrained because many doctors still issue handwritten prescriptions, requiring patients to mail physical scripts or submit an eScript when they purchase medications digitally. This project develops a prototype CNN-based handwriting recognition system that classifies handwritten prescription images, enabling patients to upload prescriptions online and complete medication purchases without postal delays or the need for eScripts.

## Original Project Requirements
The capstone project will allow you to showcase skills learned throughout the course by defining, designing and
delivering an end-to-end data science solution.
You will need to prepare an 8-12 minute PowerPoint presentation.

The presentation should cover the following:
- Business Problem
- Data Science Problem
- Stakeholders
- Dataset
- EDA
- Models
- Evaluation and comparison
- Result
- Conclusion / Future Work
  
The Jupyter notebooks should be readable and well-commented.

## Data Set: Doctor’s Handwritten Prescription BD dataset
[Doctor’s Handwritten Prescription BD dataset](https://www.kaggle.com/datasets/mamun1113/doctors-handwritten-prescription-bd-dataset)

## Exploratory Data Analysis
-  **Shape, Info, Describe**: Basic evaulation was performed to understand the number of classes and available data in each column. Also identifying any null, NA or missing values.
-  **Visual Inspection**: As Data set contain images, a visual inspection was preformed through Python using Image from the PIL. 
-  **Distribution Visualisation & Analysis**: Distribution Analysis on the character length of text labels, height x width of image samples, image mode, and sample of image intensity and contrast.

View the full analysis in the [Jupyter Notebook here. (1-doctors-handwritting-EDA.ipynb)](./1-doctors-handwritting-EDA.ipynb)
## Preprocessing
Preprocesing was performed to normalise the data. Steps taken.

- Convert to Greyscale (Mode: “L”)
- Noise reduction with Gaussian Blur
- Contrast Enhancement
- Mild sharpening
- Resize image to height 
- Width normalising via Padding or Cropping
- Pixel Normalisation
- Export as .npy file + generation new manifest


View the preprocessing steps in the [Jupyter Notebook here. (2-doctors-handwritting-Preprocessing.ipynb)](./2-doctors-handwritting-Preprocessing.ipynb)

## Modelling
A custom CNN Classifier was built and optimised to identify and discremenate the 78 classes.

Below processes were added and adjusted to improve Top-1 and Macro F-1 accuracy.
- Adaptive pooling,
- Regularisation
- Image skewing
- Label smoothing
- A change from 2x2 to 2x1 on last max pool to retain more of the spatial width
- Confusion-aware optimisation at epoch 20


View the model, train, val and text in the [Jupyter Notebook here. (3-doctors-handwritting-Modelling.ipynb)](./3-doctors-handwritting-Modelling.ipynb)

#### Diagram of Model Architecture
<img width="1131" height="513" alt="image" src="https://github.com/user-attachments/assets/6d5518ae-802a-4de1-9732-63293c5f43ac" />

## Presentation
**Presentation Video** - [Capstone-Video-Presentation](https://youtu.be/4GUOo_ePfms) \
**Powerpoint Presentation Slides** - [Capstone-Powerpoint-Presentation.pdf](./Capstone-Powerpoint-Presentation.pdf)
## Written Report
**Written Report** - [Capstone-Written-Report.pdf](./Capstone-Written-Report.pdf)
