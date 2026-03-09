# ML for the blind (GuideDog)

Description: ML-enabled life assistance app for the visually impaired
Status: Archived
Tags: App
Role: Product manager

[https://youtu.be/JLwBn4g4pC8](https://youtu.be/JLwBn4g4pC8)

# TL;DR

GuideDog is a ML-based life assistance app for the visually impaired. It was built in under 36 hours during a campus-wide hackathon at the Johns Hopkins University. I led a team of ML engineer, backend engineer, and android developer assuming the role of both product manager and frontend developer. I defined the product requirements, roadmap, and UI/UX of the application. 

## 💡Inspiration

![image.png](ML%20for%20the%20blind%20(GuideDog)/image.png)

Technology has made all our lives easier. Wait, has it?

For most, it has, but there are some people whose lives have become more inconvenient than ever because of new technologies. With increasingly more service workers being replaced by automated kiosks, touch screens, and buttons than ever, many visually impaired people find it difficult to navigate even the most basic tasks in everyday life.

## 📱What it does

GuideDog is an AI/ML-based mobile app designed to assist the lives of the visually impaired, 100% voice-controlled. You may as well think of it as "speaking guide dog," as the name suggests. It has three key features based on the scene captured by your mobile phone, GuideDog:

1. Reads text upon command,
2. Describes the scene around you upon command and,
3. Warns you if there is an obstacle in front of you.

## 🛠️ How we built it

### Technologies that we needed

![image.png](ML%20for%20the%20blind%20(GuideDog)/image%201.png)

According to the storyboard for our mobile app, we had to implement 5 main features:

### Speech-to-text in order to recognize user's verbal command

In order to better interact with the visually-impaired, all of our commands are voice-controlled. To do this, we used Google Cloud's Speech-to-Text API to convert the user's voice input into a command that the app can understand an execute.

### Text-to-speech in order to say out loud the output

We use Google Cloud's Text-to-Speech API in our application to guide the user through the app experience, interact with them as personable as it can, and respond back to the user based on the feature it has selected or used.

### Image captioning to describe a scene

The camera feature in the application captures an image and then using Azure Vision API to come up with a sentence description of that scene. The user then is able to understand certain situations based on objects it encounters, but also provided context of what's going on.

### Object detection to detect obstacles

The application is able to detect obstacles and ultimately warn the user of its surroundings in real-time. This is especially useful when the user is not familiar with a certain location and trying to navigate themselves through the street. This was done by incorporating Android's CameraX API, Google ML Kit's Object Detection and Tracking API, and TensorFlow Lite's MobileNet Image Classification Model.

### OCR, text recognition to read text

The text recognition feature is able to detect texts, whether it be typed, printed, or handwritten, and then reads them to the user, when certain situations or locations do not provide adequate accommodations for the visually-impaired.

### Backend API

![](https://raw.githubusercontent.com/kyuheejo/guidedog/main/images/api_diagram.png)

Since we are using a lot of different APIs, we decided to create a Flask API gateway that processes and redirects the request from the mobile app to the different machine learning services we are using. We deployed the Flask application on Google App Engine to create a scalable and fast central API with different endpoints. We also have a self-trained image captioning model that we integrated into the Flask application.

### Client-side Native Android Application

![](https://raw.githubusercontent.com/kyuheejo/guidedog/main/images/app_diagram.png)

The application integrates the Flask API, which processes the image captioning and optical character recognition, with the other features of our product. It uses Speech-to-Text and Text-to-Speech to interact with the user and detects obstacles and points of interests through the camera.

### Training image captioning model

![image.png](ML%20for%20the%20blind%20(GuideDog)/image%202.png)

We used tensorflow to build and train model for image captioning on MS-COCO 2014 based on the paper [Show, Attend and Tell: Neural Image Caption Generation with Visual Attention](https://arxiv.org/pdf/1502.03044.pdf). The model uses standard convolutional network as an encoder to extract features from images (we use Inception V3) and feed the generated features into an attention-based decoder generate sentences. While the paper used LSTM model as a decoder, we use a simpler RNN instead. We used all 80,000 train data to train the model for 10 epochs, which took 5 hours on 3 GPUs.

## 🧗 Challenges we ran into

- We first developed an attention base image captioning model (InceptionV3-RNN) using Tensorflow on 80,000 images with 4 GPUs for 10 hours. In order to deploy it, we connected the model using Flask API. While the performance was good, due to the ML model, we had about ~10 seconds of latency. We thought this would be problematics for end-users. Hence we instead decided to use the image captioning API provided by Azure Vision API.
- The pretrained model that we use for object detection, MobileNet, was not trained specifically for our use case, so the classification and latency proves that we need to train our own model for detecting obstacles and people we meet on the street.

## 🏆Accomplishments that we're proud of

- Deploy machine learning models with API and serve them to the mobile app.
- Create a responsive mobile app that seamlessly incorporates object detection, image captioning, and OCR all in a single weekend

## ✍️What we learned

- API response time is extremely important for app performance.
- Larger machine learning models need more powerful backend servers.
- First time deploying machine learning functionalities on a mobile app

## 🕶️What's next for GuideDog

- Develop "Smart Sunglasses" that could be connected to our mobile app that captures eye-level video, and allow handsfree, seamless voice control using Bluetooth microphone and speaker.
- Develop our own objection detection and image classification models that is catered towards our use cases and train them with objects that may hinder a visually-impared's walk to the grocery store.
- Improve the app's latency and performance, so the user is always alert of their surroundings.