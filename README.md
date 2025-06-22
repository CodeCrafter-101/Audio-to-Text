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



