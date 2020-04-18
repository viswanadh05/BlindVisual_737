# Project Title
BlindVisual_737 - Android Application to assist blind people in perceiving object

### Getting Started
The Aim of our project is to guide the visually impaired folios to perceive the things in surrounding environment with a sole Android app, concisely which helps them to listen about the things which they can’t see. 

### Prerequisites
  1. Application Platform:     Android
  2. Emulator version:         Android Oreo
  3. Development IDE:          IntelliJ Android Studio
  4. Storage:                  Google Firebase
  5. Visual Recogntn Platform: IBM Blue mix Node red (Watson)
  6. Text to speech service:   Google speech service
  
### Built with

__Android Programming Language__, __Node JS__, __Firebase__, __IBM and Google API's__ 

### Description
The lack of visual capabilities has limited the individuals from completely perceiving their immediate surroundings which has potential safety concerns and lowers their quality of life since they must rely on some sort of aid to get around. We are going to resolve the problem Through a cloud based android application, where the user takes the picture of specific area and then this picture is analyzed by the IBM tool later it is transformed into Audio format and will be send into the user Mobile for which the user can perceive about the picture.

__Project core functions:__
  1. User friendly Android application.
  2. Image analysis with IBM Image recognition in Node red. 
  3. Google's Text to speech analysis. 
  4. Better perspective for blind with Android features.
  5. Better Acoustic with Google's voice.

### Running the Project
  1. Clone the project into a new folder.
  2. Create Google Cloud Services account, get Text to Speech service and firebase API's with access keys.
  3. Update API's and access keys.
  4. Create a new IBM node red account in IBM BlueMix. 
  5. __Node Red:__
    1. Create nodes for getting the images from Android Application. (https get)
    2. Initializing. (Reforming the payload and getting respective image needed for image recognition)
    3. Connecting to IBM visual recognition (Must have IBM Visual Recognition access, select classifyImage)
    4. Reforming the text response. (Loop through the msg.paylod and get the text required)
        __*msg.result.images[0].classifiers[0].classes[i]> and a condition to get classes > 0.60 for accuracy*__
    5. Send the text response output to debug node and http post node.
  6. Build the Android application and set an emulator for test.
  7. Run the application and get the response as an Audio.
  
### Author

__Project Team__
1. __Kishan Patel__ (Responsible for Android Development and Google Services)
2. __Viswanadh Bhaskarla__ (Responsible for Project planning, IBM Cloud services, IBM Node red flows, API Integration and Testing)

### Project Images

![Architecture](https://user-images.githubusercontent.com/6322818/79527378-c704d600-80aa-11ea-92f7-42ef390dcaa2.jpg)

![Nodered_screenshot](https://user-images.githubusercontent.com/6322818/79527511-2531b900-80ab-11ea-95ab-2ef742bdab47.JPG)

![image](https://user-images.githubusercontent.com/6322818/79527629-6fb33580-80ab-11ea-8397-6e35f5cc044a.png)
