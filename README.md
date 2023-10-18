# Lip-Syncing with Wav2Lip

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1HrJeM-M9kDTCqh45IkU2KioJjYS4kvD6?usp=sharing)

## Introduction

This project is an implementation of lip-syncing using the Wav2Lip model. The primary goal of this project is to demonstrate the synchronization of an audio file with a video file, ensuring that the lip movements of the characters in the video are accurately matched with the corresponding audio file.

## Project Overview

In this project, we aim to achieve the following objectives:

1. Ensure that the lip movements of the characters in the video are synchronized with the corresponding audio, creating a seamless and natural visual and auditory experience for the viewer.

2. Evaluate the lip sync quality, response times, code quality, and submission time for the project.

## Implementation

The primary code for this project can be found in two scripts:

### Original Script

- `inference.py`: [Link to Original Script](https://github.com/Rudrabha/Wav2Lip/blob/master/inference.py)

### Modified Script

- `new_inference.py`: This script implements improvements in face detection and frame processing, particularly in cases where faces are not detected in frames.


### Folder Structure

Lip-Sync/

> ├── inference.py (Original Script)

> ├── new_inference.py (Modified Script)

>├── (Other Various Files)


## Key Modifications

In the `new_inference.py` script, several key modifications have been made to enhance the lip-syncing process:

### Smoothening of Face Detection Boxes

The `get_smoothened_boxes` function has been updated to improve face detection box accuracy and smoothening.

### Handling of Faulty Frames

The script now logs frames where a face is not detected and uses `[0, 0, 92, 92]` as a placeholder for face coordinates.

### Skip Processing for Faulty Frames

Frames with face coordinates `[0, 0, 92, 92]` are skipped during processing.

## Usage

To run the lip-syncing process, you can use the modified `new_inference.py` script. Ensure you have the required dependencies and models in place.

```bash 
python new_inference.py --checkpoint_path <path_to_checkpoint> --face <path_to_video_or_image_with_faces> --audio <path_to_audio_file> --outfile <output_video_path>
```

## Demo Video 

Watch the lip-syncing in action with the following [demo video](https://drive.google.com/file/d/1ibHpTrjYdtHr7nbowkAGHXbLEt7rqHxk/preview).



## Scope of the Project
As an individual creator, my goal is to develop a user-friendly GUI to enhance lip-syncing. This GUI will allow users to monitor lipsync on relevant frames and skip irrelevant ones for more efficient video inference. However, implementing this feature poses challenges, including GUI design, real-time processing, frame relevance determination, user feedback integration, and model-GUI integration. I also plan to ensure scalability and adapt the model for frame skipping, all with the goal of providing a top-quality lip-sync experience.

## Acknowledgments

I would like to express my gratitude to [Listed](https://listed.fans/) for providing the lip-syncing assignment that inspired this project. Additionally, I want to thank Rudra for their original [GitHub repository](https://github.com/Rudrabha/Wav2Lip), which served as a valuable reference for my modifications.
