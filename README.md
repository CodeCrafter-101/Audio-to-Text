# Audio to Text Converter
- Audio to Text is a Python-based application that converts spoken words from audio files into readable, editable text. This tool utilizes automatic speech recognition (ASR) to transcribe audio content—making it useful for tasks like note-taking, transcription, subtitles, accessibility, and voice-driven interfaces.


## Key Features
- Transcribes `.wav`, `.mp3`, and other supported audio formats
- Uses real-time or pre-recorded audio input
- Supports multiple languages (optional)
- Simple CLI-based interface or extendable to GUI/web
- Offline or online options (depending on the library used)

## Libraries Used:
- `speech_recognition` – for recognizing speech from audio
- `pydub` – for audio processing and splitting on silence
- `google.colab` – for uploading and handling files in Colab
- `subprocess`, `os` – for audio format conversion (e.g., using `ffmpeg`)

## Requirements
```` 
pip install SpeechRecognition pydub
````

- Note: On some systems, you may need to install `ffmpeg` to handle `.mp3` or other formats with `pydub`.

## Structure
![image](https://github.com/user-attachments/assets/7f48f8b6-dc81-48ac-8f26-c265d88a901b)

# How It Works
### 1. Upload Audio
- Upload `.wav`, `.mp3`, or `.flac` files via Google Colab’s file upload feature
### 2. Preprocessing
- Convert the audio (if needed) to `.wav` using `ffmpeg` via `subprocess`.
- Load the audio with `pydub.AudioSegment`.
- Split long audio files into smaller chunks based on silence using `split_on_silence`.
### 3. Speech Recognition
- Each chunk is passed to `speech_recognition.Recognizer` to extract text.
- All recognized text segments are combined into a full transcript, `whole_text`.
### 4. Output
- The transcript is printed or saved as a `.txt` file.
