#🎙️ TTS & Voice Cloning with OpenVoice

This project demonstrates two key tasks:

Text-to-Speech (TTS) → Converting text into natural-sounding speech.

Speech-to-Speech Voice Cloning → Converting an input audio (any speaker) into another speaker’s cloned voice.

Both tasks were implemented in Google Colab using open-source libraries and pretrained models.

🚀 Features

Convert plain text into realistic speech (TTS).

Clone voices using OpenVoice by MyShell.

Process 369+ audio files (cloning + merging).

Supports GPU acceleration (Tesla T4).

Outputs a single merged audio file.

📦 Libraries Used

pydub → Audio file merging and processing.

librosa → Audio loading & feature extraction.

soundfile → Reading & writing .wav files.

torch (PyTorch) → Model inference (OpenVoice requires it).

transformers → HuggingFace pretrained models.

IPython.display (Audio) → Inline audio playback in Colab.

⚙️ Setup Instructions
1. Clone this repo
git clone https://github.com/Malaika-tech/TTS_VoiceCloning.git
cd TTS_VoiceCloning

2. Open in Google Colab

Upload the .ipynb notebooks to Google Colab.

Mount Google Drive for saving input/output files.

from google.colab import drive
drive.mount('/content/drive')

3. Install dependencies
!pip install pydub librosa soundfile torch transformers

4. Text-to-Speech Notebook

Open Text_to_Speech.ipynb.

Provide your text in the script.

Run cells → Output will be saved as .wav.

5. Voice Cloning Notebook

Open Voice_Cloning.ipynb.

Provide:

REFERENCE_FILE → Reference speaker’s voice sample.

INPUT_FOLDER → Folder containing .wav files to be cloned.

OUTPUT_FOLDER → Destination folder for cloned voices.

The script will:

Clone each audio file into reference voice.

Save them into OUTPUT_FOLDER.

Merge all cloned audios into one .wav file.

🛠️ Challenges Tackled

✅ Colab GPU setup

Ensured compatibility with Tesla T4 GPU.

Fixed PyTorch & CUDA version mismatches.

✅ Inference issues

OpenVoice originally required inference.py.

We removed that dependency → directly imported functions instead.

✅ File not found errors

Scripts were modified to create output folders automatically.

✅ Merging multiple audio files

Used pydub to merge 369 cloned .wav files into a single audio file.

📊 Workflow:
Text Input  ──► TTS Model ──► Speech Output
Audio Input ──► Voice Cloning Model ──► Cloned Speech ──► Merge ──► Final Audio

🎯 Results

Successfully converted text into speech.

Cloned 369+ audio files into target speaker’s voice.

Final merged audio file created in Google Drive.

📌 Repository Structure
TTS_VoiceCloning/
│── Text_to_Speech.ipynb    # TTS Implementation
│── Voice_Cloning.ipynb     # Speech-to-Speech Voice Cloning
│── README.md               # Documentation

🙌 Acknowledgements

OpenVoice by MyShell

HuggingFace Transformers

PyDub

👉 This repo serves as a complete step-by-step guide to perform both TTS and Voice Cloning using Colab + GPU.
