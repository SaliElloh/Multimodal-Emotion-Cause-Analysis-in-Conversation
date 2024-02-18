# Multimodal-Emotion-Cause-Analysis-in-Conversation
SemEval 2024 Task 3 Subtask 2 project focusing on emotion recognition in conversations using text and audio data

A real-time diagnostic and predictive application that collects and evaluates data from your Fitbit watch.

For more information about me, please visit my LinkedIn:

[![LinkedIn][LinkedIn.js]][LinkedIn-url]

<!-- ABOUT THE PROJECT -->

## About The Project:

### Introduction:

12 million Americans are affected by misdiagnosis errors, often caused by factors such as human error and knowledge gaps. To address this issue, we recognized the potential of smartphones and smartwatches, which are widely used and can collect valuable health data such as heart rate, breathing rate, sleep patterns, and blood pressure. This led us to create Predi, a live diagnostics mobile application that aims to improve communication between doctors and patients. Predi provides:

1. Real-time reporting of health data,
2. Allows users to search for symptoms, 
3. and tracks Fitbit data to identify trends and potential issues that may be missed by doctors.

### How is it different?

Predi is different from other technology in several ways: 

1. it uses user search queries and Fitbit data for more personalized symptom identification.
2. It is accessible and affordable with only a smartphone and smartwatch needed.
3. It continuously monitors and analyzes health data for a more comprehensive understanding of a user's health status over time, and provides a reliable reporting system for doctors to verify patient data.

### Who Does it Serve: 

Predi serves doctors who want a faster and more accurate diagnosis, regular users who want continuous health monitoring and assistance, and those who want to connect with their doctor outside of the hospital.

## Getting Started:

To get the project running, there's a few programs and steps needed.

### Built With:

![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
* <img src="https://img.shields.io/badge/-TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white">


### Prerequisites:

* A computer with a supported operating system (Windows, macOS, or Linux)
* Flutter SDK
* Integrated development environment (IDE) 
* Android SDK or Xcode (Android or iOS)
* A device or emulator to test the app on
* Basic knowledge of programming concepts and the Dart programming language.

### System Design

To simplify and allocate dedicated resources to the system, it was divied into four distinct components: 

1. Front-end (mobile app)
2. Back-end (controller)
3. AI model
4. Database

The controller and AI model were further separated into two distinct components to minimize complexity. They can communicate with each other only through a message broker.

### Steps to run the code:

Download the "predi-health-app" zip file found in the uploaded files.
 
To do that, simply press on the zip file, then press "view raw" as shown below to download it:

![image](https://github.com/SaliElloh/predi-health-app/assets/112829375/d2292731-c6a6-4f65-ae87-51a248e1124f)

## Demo:

### User Stories: 

The table below outlines the app's objectives and the corresponding achievements:

<table>
  <tr>
    <th>As an...</th>
    <th>I want to...</th>
    <th>So that...</th>
  </tr>
  <tr>
    <td>Doctor</td>
    <td>keep track of my patients drug intake</td>
    <td>they are not prescribed drugs that could have negative interactions</td>
  </tr>
  <tr>
    <td>Doctor</td>
    <td>monitor my patients possible negative interactions</td>
    <td>so that I can warn them correctly</td>
  </tr>
  <tr>
    <td>New user</td>
    <td>create an account on the app and link with my Fitbit watch</td>
    <td>I can track my health through the app</td>
  </tr>
  <tr>
    <td>Regular user</td>
    <td>link my account with my Google account</td>
    <td>The app can access my search history</td>
  </tr>
  <tr>
    <td>Regular user</td>
    <td>get suggestions based on my search history and Fitbit data</td>
    <td>I can get suggestions on what's the best course of action</td>
  </tr>
  <tr>
    <td>Doctor</td>
    <td>view my patient's search history and Fitbit data</td>
    <td>I can correlate it with their health record</td>
  </tr>
  <tr>
    <td>Doctor</td>
    <td>get notified if one of my patients has a serious accident</td>
    <td>I can assist them at the earliest</td>
  </tr>
  <tr>
    <td>Regular user</td>
    <td>use the app to Google my symptoms</td>
    <td>The app sends warnings of serious health issues to my assigned doctor</td>
  </tr>
  <tr>
    <td>Doctor</td>
    <td>be able to validate or deny the serious warnings</td>
    <td>My assigned patient can receive only the valid warnings</td>
  </tr>
  <tr>
    <td>Regular user</td>
    <td>have access to a set of articles</td>
    <td>Can have an idea about the app's diagnosis</td>
  </tr>
  <tr>
    <td>Regular user</td>
    <td>get suggestions based on my search history and Fitbit data</td>
    <td>I can get suggestions on what's the best course of action</td>
  </tr>
</table>


### Screen shots from Demo:

To gain a clearer picture of the app's functionality, take a look at these screenshots showcasing it in different scenarios:

<b> a. Scenario 1: Signing into your account </b>

To get started, you need to sign up/log into the app with your email address. If you want to sync your fitbit watch, you need to log in with the email address associated with your fitbit watch. 

![image](https://github.com/SaliElloh/predi-health-app/assets/112829375/f261c4f1-770c-483f-bdc7-db98f4ac7273)

<b> b. Scenario 2: Doctor Monitering Patient's Drug Intake </b>

Say your doctor, Steve Jobs, has prescribed you certain medications that you have to take on a a time schedule. With the app, you can easily keep track of your medication schedule. The app logs the time you take your medication and automatically reports it to your doctor. 

![image](https://github.com/SaliElloh/predi-health-app/assets/112829375/7de18583-d068-4021-8da1-9140a19f3c14)

<b> c. Scenario 3: Beverly Hills Plastic Surgeon </b>

Dr Todd a famous plastic surgeon in LA wants to check his patient Kim Kardashian's health search history to monitor her condition: 

![image](https://github.com/SaliElloh/predi-health-app/assets/112829375/5a783f30-6038-4ff9-bb4b-3a0706db0d7b)

<b> c. Scenario 4: App Informed Decision Making: </b>

The app uses your search history to make informed decisions on your symptoms, which are reported to your doctor for validation.

![image](https://github.com/SaliElloh/predi-health-app/assets/112829375/b9128a69-4adb-46c1-8bec-999816c689c9)

<!-- LICENSE -->
## License:

No License used.

<!-- CONTACT -->
## Contact:

Sali E-loh - [@Sali El-loh](https://www.linkedin.com/in/salielloh12/) - ellohsali@gmail.com

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments:

* I would like to extend my gratitude to my fellow classmates who worked diligently alongside me on this project during our CIS 553 Software Engineering course: Amine Dakhli (Aminedak@umich.edu), Alaa Houerbi (houerbi@umich.edu), and Matthew Bryce (mdbryce@umich.edu)."

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[LinkedIn.js]: https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white
[LinkedIn-url]: https://www.linkedin.com/in/salielloh12/

