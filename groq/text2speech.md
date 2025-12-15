---
description: Instantly generate lifelike audio from text using Groq&#x27;s fast text-to-speech API with support for multiple voices and languages.
title: Text to Speech - GroqDocs
image: https://console.groq.com/og_cloudv5.jpg
---

# Text to Speech

Learn how to instantly generate lifelike audio from text.

## [Overview](#overview)

The Groq API speech endpoint provides fast text-to-speech (TTS), enabling you to convert text to spoken audio in seconds with our available TTS models.

With support for 23 voices, 19 in English and 4 in Arabic, you can instantly create life-like audio content for customer support agents, characters for game development, and more.

## [API Endpoint](#api-endpoint)

| Endpoint | Usage                 | API Endpoint                                |
| -------- | --------------------- | ------------------------------------------- |
| Speech   | Convert text to audio | https://api.groq.com/openai/v1/audio/speech |

## [Supported Models](#supported-models)

| Model ID          | Model Card                             | Supported Language(s) | Description                                           |
| ----------------- | -------------------------------------- | --------------------- | ----------------------------------------------------- |
| playai-tts        | [Card ](https://console.groq.com/docs/model/playai-tts)        | English               | High-quality TTS model for English speech generation. |
| playai-tts-arabic | [Card ](https://console.groq.com/docs/model/playai-tts-arabic) | Arabic                | High-quality TTS model for Arabic speech generation.  |

## [Working with Speech](#working-with-speech)

### [Quick Start](#quick-start)

The speech endpoint takes four key inputs:

* **model:** `playai-tts` or `playai-tts-arabic`
* **input:** the text to generate audio from
* **voice:** the desired voice for output
* **response format:** defaults to `"wav"`

PythonJavaScriptcurl

The Groq SDK package can be installed using the following command:

shell

```
pip install groq
```

The following is an example of a request using `playai-tts`. To use the Arabic model, use the `playai-tts-arabic` model ID and an Arabic prompt:

Python

```
import os
from groq import Groq

client = Groq(api_key=os.environ.get("GROQ_API_KEY"))

speech_file_path = "speech.wav" 
model = "playai-tts"
voice = "Fritz-PlayAI"
text = "I love building and shipping new features for our users!"
response_format = "wav"

response = client.audio.speech.create(
    model=model,
    voice=voice,
    input=text,
    response_format=response_format
)

response.write_to_file(speech_file_path)
```

### [Parameters](#parameters)

| Parameter        | Type   | Required | Value                                                                                                                                       | Description                                                                                                                              |
| ---------------- | ------ | -------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| model            | string | Yes      | playai-ttsplayai-tts-arabic                                                                                                                 | Model ID to use for TTS.                                                                                                                 |
| input            | string | Yes      | \-                                                                                                                                          | User input text to be converted to speech. Maximum length is 10K characters.                                                             |
| voice            | string | Yes      | See available [English](https://console.groq.com/docs/text-to-speech/#available-english-voices) and [Arabic](https://console.groq.com/docs/text-to-speech/#available-arabic-voices) voices. | The voice to use for audio generation. There are currently 26 English options for playai-tts and 4 Arabic options for playai-tts-arabic. |
| response\_format | string | Optional | "wav"                                                                                                                                       | Format of the response audio file. Defaults to currently supported "wav".                                                                |

### [Available English Voices](#available-english-voices)

The `playai-tts` model currently supports 19 English voices that you can pass into the `voice` parameter (`Arista-PlayAI`, `Atlas-PlayAI`, `Basil-PlayAI`, `Briggs-PlayAI`, `Calum-PlayAI`,`Celeste-PlayAI`, `Cheyenne-PlayAI`, `Chip-PlayAI`, `Cillian-PlayAI`, `Deedee-PlayAI`, `Fritz-PlayAI`, `Gail-PlayAI`,`Indigo-PlayAI`, `Mamaw-PlayAI`, `Mason-PlayAI`, `Mikail-PlayAI`, `Mitch-PlayAI`, `Quinn-PlayAI`, `Thunder-PlayAI`).

Experiment to find the voice you need for your application:

Arista-PlayAI

0:000:00

Atlas-PlayAI

0:000:00

Basil-PlayAI

0:000:00

Briggs-PlayAI

0:000:00

Calum-PlayAI

0:000:00

Celeste-PlayAI

0:000:00

Cheyenne-PlayAI

0:000:00

Chip-PlayAI

0:000:00

Cillian-PlayAI

0:000:00

Deedee-PlayAI

0:000:00

Fritz-PlayAI

0:000:00

Gail-PlayAI

0:000:00

Indigo-PlayAI

0:000:00

Mamaw-PlayAI

0:000:00

Mason-PlayAI

0:000:00

Mikail-PlayAI

0:000:00

Mitch-PlayAI

0:000:00

Quinn-PlayAI

0:000:00

Thunder-PlayAI

0:000:00

### [Available Arabic Voices](#available-arabic-voices)

The `playai-tts-arabic` model currently supports 4 Arabic voices that you can pass into the `voice` parameter (`Ahmad-PlayAI`, `Amira-PlayAI`, `Khalid-PlayAI`, `Nasser-PlayAI`).

Experiment to find the voice you need for your application:

Ahmad-PlayAI

0:000:00

Amira-PlayAI

0:000:00

Khalid-PlayAI

0:000:00

Nasser-PlayAI

0:000:00