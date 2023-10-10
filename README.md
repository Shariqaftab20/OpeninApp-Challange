# OpeninApp-Challange
# Wav2Lip Inference Colab Notebook

## Overview
This Colab notebook provides a step-by-step guide for running the Wav2Lip inference on Google Colab. Wav2Lip is a lip-syncing tool that generates realistic lip movements based on audio input.

### 3. Setup Google Drive
- In your Google Drive:
  1. Create a folder called `Wav2Lip` in `MyDrive`.
  2. Upload your input video (`input_vid.mp4`) and input audio (`input_aud.wav`) to this folder.
  3. Download the pretrained model weights from [https://github.com/Rudrabha/Wav2Lip#getting-the-weights](https://github.com/Rudrabha/Wav2Lip#getting-the-weights).
  4. Create a folder called `Wav2lip` in `MyDrive` and upload the pretrained model weights in there.


## How to Run

### 1. Setup Environment
- The notebook starts by checking the CUDA version and mounting Google Drive.

### 2. Clone Wav2Lip Repository
- The Wav2Lip repository is cloned from [https://github.com/Rudrabha/Wav2Lip.git](https://github.com/Rudrabha/Wav2Lip.git).

### 3. Check Google Drive Contents
- List the contents of the specified Google Drive folder to ensure the required input files (`input_aud.wav` and `input_vid.mp4`) are present.

### 4. Copy Pre-trained Model
- Copy the pre-trained Wav2Lip-GAN (or any other pretrained model) model (`wav2lip_gan.pth`) from Google Drive to the Wav2Lip checkpoints folder.

### 5. Install Dependencies
- Install the necessary dependencies listed in `requirements.txt`. Note: There might be an issue with OpenCV version compatibility, and an attempt to install a specific version of OpenCV might fail.

### 6. Resolve OpenCV Version Issue
- Since there's an issue with the OpenCV version, an attempt to install a different version (`opencv-python==4.1.0.25`) fails. The notebook then resolves this issue by installing an alternative version (`librosa==0.8.0`).

### 7. Download Face Detection Model
- Download the face detection model (`s3fd.pth`) from [https://www.adrianbulat.com/downloads/python-fan/s3fd-619a316812.pth](https://www.adrianbulat.com/downloads/python-fan/s3fd-619a316812.pth) and save it in the appropriate directory.

### 8. Copy Input Files to Sample Data
- Copy input video and audio files from Google Drive to the Colab sample data folder.

### 9. Run Wav2Lip Inference
- Run the Wav2Lip inference script (`inference.py`) with the specified checkpoint path, input video, and audio files. The inference is initially attempted without resizing, and later, a resized version is attempted with a specified resize factor.

### 10. View Results
- The final step involves viewing the generated lip-synced video results.

## Notes
- The notebook uses the CPU for inference due to potential limitations in Colab's GPU support.
- Ensure that the input files are correctly placed in the Google Drive folder.
- If any issues arise during installation or execution, refer to the respective sections for troubleshooting.

Feel free to adapt this Colab notebook for your specific use case and experiment with different input files and parameters. Happy lip-syncing!
