# Face-recognition-in-segmented-live-video-feed
In the age of big data ,the world produce an enormous amount of data, which creates a challenge for big data and artificial intelligence. A lot of video surveillance streams require focus on only one part of the video and this model helps in setting the focus area of the live video feed where face recognition is required and ignores the extra data.
This model can be applied to various systems such as surveillance system, entertainment systems, searching systems etc. to enhance the focus on the required part of the live video stream.

## Methodology:
There are mainly three parts involved in development of my project:
a) Data Preparation
b) Model Training
c) Model Testing

### a) Data Preparation
I am preparing data for 3 individuals, i.e., Aditya, Anjali, and Divyansh. For eachclass, I am collecting approx. 1000 images for training and 250 for validation
and saving them into unique directories.
In order to collect the face images, I am using Haar cascade frontal face default object detection algorithm through haarcascade_frontalface_defaul.xml for
detecting just the face out of the whole image and I am also using OpenCV library to process the result image.

➔ Data Splitting:
I made two folders: Training and Validation. Each having 3 subfolders of the
3 classes. I categorized the data into training and validation directories in ratio
of 4:1 before feeding it into the model for training.

## b) Model Training
• Transfer learning approach has been used to train the model to achieve high
accuracy.
• Pre-trained weights of ImageNet have been used and the Neural Network
layers have been added to it.
• The NN consists of 3 hidden layers and a single output layer which will
classify the images into categories.
• Model has been saved with the name F1.h5 after performing 20 epochs on it.

## c) Model Testing:
• We are capturing live video feed and giving the frame as input to our model
after cropping and adjusting the frame accordingly.
• The model will detect the face in a segment of the live video and will show
the person’s name as the output. 
