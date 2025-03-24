

# README: Museum Guide Robot Project

## Project Overview
The **Museum Guide Robot Project** explores the implementation of a robotic tour guide in museums to enhance visitor engagement and provide automated assistance. The robot, **TIAGo**, utilizes object detection, speech recognition, and natural language processing to recognize artworks, interact with visitors, and answer questions.

## Authors
Nicholas Keatley, Doran Moison, Hussein Naddaf, Dhruv Pandit, Raj Tagore, Vaibhav Tewani

## Motivation
Museum attendance has been declining due to a lack of funding, which leads to fewer human tour guides and reduced visitor engagement. This project proposes an AI-powered robotic guide to address these challenges by providing an interactive and informative experience for visitors.

## Key Technologies
- **Robotics Platform:** TIAGo robot
- **Object Detection:** YOLO V8 for artwork recognition
- **Natural Language Processing (NLP):** ChatGPT API for generating descriptions and answering visitor questions
- **Speech Recognition & Synthesis:** OpenAI Whisper for transcription and VITS for text-to-speech conversion
- **Navigation & Obstacle Avoidance:** ROS-based locomotion and mapping

## Methodology
### Robot Selection & ROS Integration
- TIAGo was chosen due to its **height, RGB-D camera, and mapping capabilities**.
- ROS (Robot Operating System) nodes were developed for seamless communication between different functionalities.

### Object Detection & Localization
- YOLO V8 was trained on **500 images** to detect and recognize **The Mona Lisa, The Starry Night, The Last Supper**, and raised hands for visitor interaction.
- Depth data was used for localization, allowing the robot to calculate the 3D world coordinates of objects.

### Locomotion & Obstacle Avoidance
- The robot navigates using **sensor data (depth camera & laser scanner)**.
- It can distinguish between **static obstacles (find a new path) and human visitors (wait for them to move).**

### LLM Integration & Interaction
- The ChatGPT API generates **descriptions of detected artworks**.
- **Visitor questions are transcribed, classified, and answered** using an optimized NLP pipeline:
  - Whisper ASR for transcription
  - RoBERTa for question filtering
  - Falcon7B-Instruct for answer generation
  - VITS for text-to-speech output
- **Contextual awareness:** The robot references nearby objects when responding to visitor questions.

## Results
- **High accuracy in object detection** with near-perfect validation scores.
- **Effective localization** using depth mapping and camera calibration.
- **Accurate and responsive conversational AI** for answering visitor queries.
- **Smooth and safe navigation** within museum environments.

## Future Work
- Improve **audio preprocessing** to enhance speech recognition in noisy environments.
- Implement **NeMo Guardrails** to filter biased content.
- Add **contextual memory** using vector databases for better dialogue coherence.
- Make the robot more **proactive** by engaging visitors with preemptive questions.

Let me know if you'd like any modifications or if you want to switch back to this version! 🚀
