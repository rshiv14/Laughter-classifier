# Automatic Emotional Content Interpretation in Laughter for Robot Assistants

## Overview
This repository contains code for a project aimed at developing a system to automatically interpret the emotional content of laughter, enhancing robot assistants' understanding of human communication. Laughter serves as a vital social signal, conveying various emotions and intentions, thereby facilitating effective human-robot interaction. By analyzing both audio and visual cues of laughter, this system can differentiate between different emotional contexts, enabling robots to respond appropriately in diverse situations.

## Dataset
### MAHNOB Laughter Database
- The MAHNOB database comprises audiovisual recordings of laughter, speech, posed smiles, and acted laughter.
- It includes data from 22 subjects recorded across four sessions, covering scenarios such as watching funny video clips, posing smiles, producing acted laughter, and speaking in different languages.
- Annotations were used to segment the dataset into clips, with labels for emotional content, dominance, and arousal.

## Feature Extraction
### Audio Feature Extraction
- Mel Frequency Cepstral Coefficients (MFCCs) were extracted from the audio signal to represent frequency components over time.
- Gender and length of the laughter episode were used as static features to enhance the detection of affective states.

### Video Feature Extraction
- From each laughter clip, 25 frames were sampled evenly across its length.
- Facial landmarks were extracted using dlib and OpenCV, focusing on regions around the mouth, eyes, and eyebrows.
- These facial features were directly fed into the model to capture expressions without explicit calculations of distances.

## Model Architecture
### Long Short-term Memory (LSTM)
- LSTM models play a central role in the multimodal emotion recognition approach.
- By integrating audio and video data, these models analyze cues such as pitch, intensity, facial expressions, and body language.
- The multimodal approach enriches the understanding of human emotions by capturing their evolution over time and in response to different stimuli.
