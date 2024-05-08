# Fake-News-Classifier-using-CNNs-and-LSTMs
The objective of this project is to develop and evaluate a neural network model capable of accurately distinguishing between fake and real news articles. By leveraging natural language processing (NLP) techniques and deep learning architectures, the goal is to create a robust classifier that can assist in mitigating the spread of misinformation.


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

## Results
The model achieves a training accuracy of approximately 97.61% and a validation accuracy of about 95.55% after five epochs, indicating strong predictive performance on the training dataset. However, when evaluated on a new set of data, the model shows a significant drop in performance, with an accuracy of only 46.73%. This discrepancy suggests issues such as overfitting to the training data or a difference in the distribution between the training and new datasets.

## Architecture

<img width="221" alt="image" src="https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/7d66841c-e46c-4b86-8349-db59ab7c4313">

<img width="231" alt="image" src="https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/c36b41b7-41e8-4826-9db8-17ce5bd7a518">

## Trainig

<img width="418" alt="image" src="https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/e9aebdad-cee2-4808-b2f1-b0ade00a7e2c">

## Model Accuracy

<img width="231" alt="image" src="https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/1f1b4218-e58e-4ad2-a0e3-de9becb7e691">

## Model Loss

<img width="236" alt="image" src="https://github.com/TayyibI/Fake-News-Classifier-using-CNNs-and-LSTMs/assets/94107654/1dd96398-7d10-4ef1-a2f7-12c55b3c8b19">


