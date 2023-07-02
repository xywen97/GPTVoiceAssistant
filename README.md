[中文版说明（README）](README_CN.md)

# Voice Assistant with Speech Recognition and AI Chatbot

This project demonstrates a voice assistant that uses speech recognition to convert audio input into text and then utilizes an AI chatbot for generating responses. The assistant records audio input, recognizes speech using the Xunfei (iFlytek) cloud speech recognition API, and generates responses using the OpenAI GPT-3.5 language model.

## Requirements

- Python 3.x
- PyAudio
- Wave
- Time
- Os
- Sys
- Threading
- Queue
- Datetime
- Ipywidgets
- Websocket
- Hashlib
- Base64
- Hmac
- Json
- Urllib
- Ssl
- Wsgiref.handlers
- Numpy
- OpenAI
- Pyttsx3
- Ctypes
- Inspect
- Pygame

## Installation

1. Clone this repository to your local machine.

2. Install the required Python packages using pip:

   ```shell
   pip install pyaudio wave ipywidgets websocket-client numpy openai pyttsx3 pygame
   ```

3. Obtain API credentials from Xunfei (iFlytek) and OpenAI:

   - For Xunfei (iFlytek) API credentials, sign up for an account and create an application to get the required `APPID`, `APIKey`, and `APISecret`.

   - For OpenAI API credentials, sign up for an account and generate an API key. Copy the generated API key.

4. Update the following variables in the code with your API credentials:

   - `APPID`: Xunfei (iFlytek) application ID
   - `APIKey`: Xunfei (iFlytek) API key
   - `APISecret`: Xunfei (iFlytek) API secret
   - `openai.api_key`: OpenAI API key

5. Run the code:

   ```shell
   python voice_assistant.py
   ```

   You can also use in the Jupyter Notebook. But note that:
   1. There is some bugs when you use `engine.save_to_file(reply, outfile)` in the Notebook;
   2. When you interupt the notebook, the file it used in the last round is still in use/busy;
   3. So, you cannot successfully write new voice in it, and cannot delete it before using (alert permission denied)
   ```
   demo.ipynb
   ```

## Usage

1. The voice assistant will start listening for audio input.

2. Speak into the microphone to provide voice input.

3. Once you finish speaking, the assistant will recognize the speech, process it using the AI chatbot, and generate a response.

4. The assistant will then convert the response into speech and play it back using the speakers.

5. The conversation will be displayed in the terminal.

6. To exit the voice assistant, press `Ctrl + C` in the terminal.

## Notes

- The code uses the PyAudio library for audio recording and playback. Make sure your microphone and speakers are properly configured.

- The code uses the Xunfei (iFlytek) cloud speech recognition API for converting speech to text. You need to provide valid API credentials for the code to work.

- The code uses the OpenAI GPT-3.5 language model for generating responses. You need to provide a valid OpenAI API key for the code to work.

- The code saves temporary audio files (in PCM format) during the recording and speech recognition process. These files are deleted after processing.

- The code uses the Pygame library for playing back the generated speech. Make sure your speakers are properly configured.

## License

This project is licensed under the [MIT License](LICENSE).

```

Please note that the above markdown file assumes the presence of a `LICENSE` file in the repository, which is a common practice for open-source projects. If you don't have a license file, you can omit the "License" section in the README.md file.