Dataset : https://www.kaggle.com/datasets/hasaniqbal777/pakistan-sign-language/data


# PSL-Detection-
Developed a Pakistan Sign Language detection system for Urdu alphabet recognition using Google's Teachable Machine to help deaf community communicate effectively. Implemented real-time computer vision to capture and classify Urdu alphabet hand gestures with high accuracy through webcam input. Created an educational AI tool that     bridges the communication gap by translating Urdu sign language gestures into digital text format. 
<h2>Pakistan Sign Language Detection using Google Teachable Machine</h2>
<h3>Abstract</h3>
This project aims to build a Pakistan Sign Language (PSL) detection model using Google Teachable Machine, a no-code machine learning platform. The model is trained on a custom dataset of PSL hand signs to recognize and classify different gestures. Unlike traditional deep learning methods where CNN architectures or pretrained models are coded manually, this project leverages transfer learning with MobileNet via TensorFlow.js inside Teachable Machine. The model achieves high accuracy and can be deployed in web or mobile applications, making it accessible and easy to use.

<h3>Result</h3>
- Achieved high training and validation accuracy on PSL dataset.<br>
- Model successfully recognizes PSL signs in real-time using a webcam.<br>
- Lightweight model (few MB) → suitable for mobile/web apps.<br>

<h3>Technologies Used</h3>
- Google Teachable Machine<br>
- TensorFlow.js<br>
- MobileNet (Transfer Learning)<br>
- Web Browser (for training)<br>
- OpenCV, Mediapipe (Computer Vision Libraries) <br>
- gTTS/pyttsx3 (Text-to-Speech Voice Tools) <br>

## Pakistan Sign Language (PSL) Detection — Workflow

Below is the high-level workflow for the PSL detection system built using Google Teachable Machine and a simple web/desktop integration:

```mermaid
flowchart TD
  A[1. Data Collection] --> B[2. Data Labeling]
  B --> C[3. Preprocessing]
  C --> D[4. Train Model (Teachable Machine)]
  D --> E[5. Export Model (TensorFlow / TF.js)]
  E --> F[6. Integration & Inference]
  F --> G[7. Post-processing & Smoothing]
  G --> H[8. Application / UI]
  subgraph PreprocessingDetails
    C1[Resize & Crop Hands] --> C2[Normalize / Augment]
  end
  subgraph IntegrationDetails
    F1[Load TF.js model in browser] --> F2[Use webcam or uploaded image]
    F2 --> F3[Run inference per frame]
  end

  C --> PreprocessingDetails
  F --> IntegrationDetails

  %% Notes nodes
  Note1([Note: Use diverse subjects, lighting variations, plain background]) --> A
  Note2([Tip: Keep labels consistent and >=100 images per class]) --> B







