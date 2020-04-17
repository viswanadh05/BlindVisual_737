# BlindVisual_737

The lack of visual capabilities has limited the individuals from completely perceiving their immediate surroundings which has potential safety concerns and lowers their quality of life since they must rely on some sort of aid to get around. We are going to resolve the problem Through a cloud based android application, where the user takes the picture of specific area and then this picture is analyzed by the IBM tool later it is transformed into Audio format and will be send into the user Mobile for which the user can perceive about the picture.

<!---------------------------------------------------------------------->

The Aim of our project is to guide the visually impaired folios to perceive the things in surrounding environment with a sole Android app, concisely which helps them to listen about the things which they can’t see. 

<!---------------------------------------------------------------------->

Project core functions:

1. User friendly Android application.
2. Image analysis with IBM Image recognition in Node red. 
3. Google's Text to speech analysis. 
4. Better perspective for blind with Android features.
5. Better Acoustic with Google's voice.

Masters Project:
Service Oriented and Architectures Design

Team:
<!----------------->
Kishan Patel
<!----------------->
Viswanadh Bhaskarla

Project specifications:
  1. Application Platform:     Android
  2. Emulator version:         Android Oreo
  3. Development IDE:          IntelliJ Android Studio
  4. Storage:                  Google Firebase
  5. Visual Recogntn Platform: IBM Blue mix Node red (Watson)
  6. Text to speech service:   Google speech service
  
Running the Project:
  1. Clone the project into a new folder
  2. Create Google Cloud Services account, get Text to Speech service and firebase API's with access keys.
  3. Update API's and access keys
  4. Create a new IBM node red account in IBM BlueMix. 
  5. Node Red: 
    1. Create nodes for getting the images from Android Application (https get)
    2. Initializing (Reforming the payload and getting respective image needed for image recognition)
    3. Connecting to IBM visual recognition (Must have IBM Visual Recognition access, select classifyImage)
    4. Reforming the text response (Loop through the msg.paylod and get the text required)
      1. msg.result.images[0].classifiers[0].classes[i]> and a condition to get classes > 0.60 for accuracy
    5. Send the text response output to debug node and (http post node)
  6. Build the Android application and set an emulator for test.
  7. Run the application and get the response as an Audio.
  

