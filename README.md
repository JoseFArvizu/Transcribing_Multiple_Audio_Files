# Transcribing Multiple Audio Files 🎙️➡️📝

This Jupyter Notebook allows you to automatically transcribe multiple `.wav` audio files into text using speech recognition. It's perfect for processing batches of voice recordings, audio datasets, or generating subtitles/transcripts.

## 📌 Overview

The notebook performs the following steps:
- Loads all `.wav` files from a user-specified folder
- Transcribes each file using Google Web Speech API
- Saves the transcriptions as `.txt` files using the same base filename
- Handles errors and logs unprocessed files

## 🚀 Features

- Batch audio transcription
- Minimal configuration
- Easy to adapt or expand
- Text output ready for analysis or storage

## 🧰 Requirements

Before running the notebook, make sure the following Python packages are installed:

```bash
pip install speechrecognition
pip install pydub
```

Also, **`ffmpeg` must be installed** on your system and available in your system path for `pydub` to handle audio properly.  
- On Windows: Download from [ffmpeg.org](https://ffmpeg.org/) and add it to your PATH  
- On macOS (with Homebrew): `brew install ffmpeg`  
- On Linux (Debian/Ubuntu): `sudo apt install ffmpeg`

## 🛠️ How to Use

1. Place all your `.wav` audio files in a folder (e.g., `./audios/`).
2. Open the notebook `Transcribing_Multiple_Audio_Files.ipynb`.
3. Set the correct path to your audio folder in the notebook.
4. Run all cells in sequence.
5. The transcribed text for each file will be saved as a `.txt` file in the same directory.

## 📝 Example Output

If your directory contains:

```
/audios/
   ├── interview.wav
   └── lecture.wav
```

You will get:

```
/audios/
   ├── interview.txt
   └── lecture.txt
```

Each `.txt` file contains the transcription of the corresponding audio file.

## ⚠️ Notes

- The notebook uses Google's online speech recognition service, which requires an internet connection and may be rate-limited.
- Accuracy may vary depending on audio quality, background noise, and speech clarity.
- For long or offline transcription, consider switching to models like OpenAI’s Whisper or Vosk.

## 📄 License

This project is released under the MIT License.

## 🙋‍♂️ Contributions

Feel free to fork, suggest improvements, or open a pull request!
