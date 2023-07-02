# 带有语音识别和 AI 聊天机器人的语音助手

该项目演示了一个语音助手，它使用语音识别将音频输入转换为文本，并利用 AI 聊天机器人生成回复。该助手记录音频输入，使用讯飞（iFlytek）云语音识别 API 进行语音识别，然后使用 OpenAI GPT-3.5 语言模型生成回复。

## 要求

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

## 安装

1. 将该存储库克隆到本地机器。

2. 使用 pip 安装所需的 Python 包:

   ```shell
   pip install pyaudio wave ipywidgets websocket-client numpy openai pyttsx3 pygame
   ```

3. 从讯飞（iFlytek）和 OpenAI 获取 API 凭据:

   - 对于讯飞（iFlytek）API 凭据，注册一个帐户并创建一个应用程序，以获取所需的 `APPID`、`APIKey` 和 `APISecret`。

   - 对于 OpenAI API 凭据，注册一个帐户并生成一个 API 密钥。复制生成的 API 密钥。

4. 使用你的 API 凭据更新代码中的以下变量:

   - `APPID`: 讯飞（iFlytek）应用程序 ID
   - `APIKey`: 讯飞（iFlytek）API 密钥
   - `APISecret`: 讯飞（iFlytek）API 密钥
   - `openai.api_key`: OpenAI API 密钥

5. 运行代码:

   ```shell
   python voice_assistant.py
   ```

## 用法

1. 语音助手将开始侦听音频输入。

2. 通过麦克风说话以提供语音输入。

3. 一旦你停止说话，助手将识别语音，使用 AI 聊天机器人处理它，并生成一个回复。

4. 然后，助手将把回复转换为语音，并使用扬声器播放。

5. 对话将显示在终端中。

6. 要退出语音助手，请在终端中按 `Ctrl + C`。

## 注意事项

- 代码使用 PyAudio 库进行音频录制和播放。请确保麦克风和扬声器已正确配置。

- 代码使用讯飞（iFlytek）云语音识别 API 将语音转换为文本。你需要提供有效的 API 凭据才能使代码正常工作。

- 代码使用 OpenAI GPT

-3.5 语言模型生成回复。你需要提供有效的 OpenAI API 密钥才能使代码正常工作。

- 代码在录制和语音识别过程中保存临时音频文件（PCM 格式）。这些文件在处理后被删除。

- 代码使用 Pygame 库播放生成的语音。请确保扬声器已正确配置。

## 许可证

该项目使用 [MIT 许可证](LICENSE) 进行许可。