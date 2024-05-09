# Fake-News-Classifier-using-CNNs-and-LSTMs
by
Tayyib Ismail 20k-0461
Farhan Siddiki 20k-0439
Muaaz Alam 20k-0212

This project aims to develop and evaluate a neural network model capable of accurately distinguishing between fake and real news articles. By leveraging natural language processing (NLP) techniques and deep learning architectures, the goal is to create a robust classifier that can assist in mitigating the spread of misinformation.



![image](https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/675dbf0e-c899-483d-acad-78db681bfe2d)




Model 1(Training Data: https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset):
https://www.kaggle.com/code/i200439/notebook9fe2e56786?scriptVersionId=176525229

Model 2(Training Data: https://www.kaggle.com/datasets/saurabhshahane/fake-news-classification):
https://www.kaggle.com/code/tayyibi/2nd-fake-news-classifier

## Methodology
Data Collection: The datasets used include WELFake_Dataset.csv, Fake.csv, and True.csv. These contain labeled news articles where labels indicate the authenticity of the article.

Preprocessing:
Textual data is cleaned by removing punctuation, numbers, and stopwords.
Texts are converted to lowercase to maintain consistency.
Lemmatization is applied to reduce words to their base or root form.

Feature Engineering:
Texts are converted into sequences using the Tokenizer class in Keras, which also restricts the vocabulary to the top 10,000 words to avoid overfitting.
Sequences are padded to ensure that they all share the same length, a requirement for training deep learning models.

Model Building:
An embedding layer is used to transform text into meaningful and trainable vectors. It utilizes pre-trained GloVe embeddings.
The model includes convolutional and LSTM layers to capture both local features of the text and long-range dependencies.
Dropout layers are included to prevent overfitting.
The output layer uses a sigmoid activation function to classify the input as fake or real.

Training:
The model is trained on a subset of the data, with a validation split to monitor performance and combat overfitting.
The optimizer used is RMSprop with a learning rate of 0.001.

## Architecture
### Model 1: 

<img width="418" alt="image" src="https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/b69a1091-9785-4223-820f-74f37cdfbacc">

![image](https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/7c274007-e752-415a-b53a-4c41e7334465)

### Model 2:

<img width="418" alt="image" src="https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/7d66841c-e46c-4b86-8349-db59ab7c4313">


![diagram](https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/ed40775f-ffb0-4505-8a06-d28b0e220d2a)


## Training
### Model 1: 

<img width="698" alt="image" src="https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/c8a9d776-95c0-455c-b68e-0b8b85aa4622">

### Model 2: 
<img width="836" alt="image" src="https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/e9aebdad-cee2-4808-b2f1-b0ade00a7e2c">

## Results
### Model 1:
![image](https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/a9c6129f-2ad9-46cb-8442-5d4ec7750fb9)

### Model 2:
![image](https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/d15c9bc4-ec64-46b9-abf9-a113a40ba5d3)

## Model Accuracy
### Model 2: 
<img width="418" alt="image" src="https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/1f1b4218-e58e-4ad2-a0e3-de9becb7e691">

## Model Loss
### Model 2:
<img width="418" alt="image" src="https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/1dd96398-7d10-4ef1-a2f7-12c55b3c8b19">


