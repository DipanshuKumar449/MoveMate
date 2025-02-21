# Move Mate

AI-Based Movement Detection & Advisory System

## Overview

This project implements an AI-based system to detect a person's movement (walking, running, or stepping on stairs) using smartphone sensors such as accelerometer and GPS. Based on the detected movement, the system provides a human-like advisory using a **Generative AI model (Ollama)**. The advice takes into account the user's **age**, **gender**, **weight**, and environmental conditions like **temperature** to provide insights into the safety of the activity, and whether the user should change their activity type or take a break.

## Features

- **Movement Detection**: Classifies the user's movement into **walking**, **running**, or **stepping on stairs** based on accelerometer and GPS data.
- **Human-like Advisory**: Provides advice on the safety of the activity using the **Llama 3.1 model**.
- **Speech Output**: Converts the advisory response into speech, making it easy for the user to receive the feedback.
- **Simulated Data**: For now, random values are used to simulate accelerometer, GPS, and temperature data (since real sensor data from a smartphone is not accessible in this notebook).In a real implementation on a smartphone, we could replace the random data generation with actual sensor inputs using the following APIs that I have found from the internet: SensorManager API,CoreMotion API,LocationManager API,CoreLocation APIs etc.

## Installation

### Prerequisites
To run this system, you need:
- **Google Colab** (recommended for GPU support).
- **Packages**:
  - `gTTS`: For converting text to speech.
  - `ipython.display`: To play the audio in Google Colab.
  - `langchain-ollama`: For interacting with the Ollama API and generating human-like responses.
  - `random`, `time`, `os`: For simulating data and managing file operations.

### Setup

1. **Clone the repository**:
    ```bash
    git clone https://github.com/DipanshuKumar449/MoveMate.git
    cd movement-detection-advisory
    ```

2. **Install dependencies**:
    If you're using **Google Colab**, run the following cells to install necessary packages:
    ```python
    !pip install gTTS
    !pip install langchain-ollama
    ```

## How to Run

1. **Open the notebook in Google Colab**:
   - Navigate to the `movement-detection-advisory.ipynb` file in the repository.
   - Open it in **Google Colab** by selecting **Open in Colab**.

2. **Run the cells**:
   - Ensure your runtime is set to **GPU** for better performance.
   - Run each cell sequentially starting from the imports and setup.
   - Execute the `main()` function to begin detecting movements and generating advisory feedback.

3. **Interaction**:
   - The system will run indefinitely, simulating sensor data, detecting movement, generating advice, and converting it to speech at regular intervals.

## Future Enhancements

- **Real Data Integration**: Replace simulated random values with actual sensor data from a smartphone using **Android** or **iOS** APIs (Accelerometer, GPS, Temperature).
- **User Interface**: Create a mobile app interface for real-time usage.

## Acknowledgements

- **Ollama**: Used for generating human-like advisory responses.
- **Google Colab**: Used for development and testing the system with GPU support.
- **gTTS**: Used for converting text to speech in the notebook.
- **Langchain**: Facilitates communication with Llama model.

---
