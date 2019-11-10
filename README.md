# An api to classify images

One Paragraph of project description goes here

## This a project to build an api to classifiy if an x-ray has Pneumonia or not. An x-ray image will be passed to the api server and the api server will be able to send following JSON response:
1) Prediction of the image i.e if the patient has Pneumonia or not.
2) Confidence of the classification in terms of percentage.

The classification model is build on the kaggle data set to be downloaded from https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia

The classification of the model is using transfer learning. It is using imagenet as the base model. The model is further trained on using tensorflow/keras and the final weights are saved in model folder. The trained weigths are further used by the api.py to classify the image recieved as a request. You can refer to jupyter notebook PneumoniaDetection for details regarding training and building model. You can also refer to https://github.com/mhosankalp/PneumoniaDetection for more details.

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Python 3.6

### Installing

A step by step series of examples that tell you how to get a development env running

1. Git Clone this repository - git clone https://github.com/mhosankalp/automc_api
2. cd automc_api 
3. Create a virual enviornment
4. source activate virtual enviornment
5. pip install -r requirements.txt
6. python api.py
7. Request the api by send a x-ray image and it will send a JSON response

result = {
      "prediction" : class_names[np.argmax(prediction_array)],
      "confidence" : '{:2.0f}%'.format(100*np.max(prediction_array))
  }
