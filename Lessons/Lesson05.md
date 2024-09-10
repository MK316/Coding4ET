🔍[BACK to the Main page](https://github.com/MK316/Coding4ET/blob/main/README.md)

# Lesson 05 Multimodality

Multimodality in the context of programming, especially for English language teachers, refers to the use of multiple modes of input and output to interact with a program. This can include text, audio, visuals, and more. In an educational setting, multimodal programs can enhance the teaching and learning experience, catering to different learning styles and needs.

Below are simple Python code examples that demonstrate basic multimodal interactions. These examples assume a teaching environment where text (written words) and audio (spoken words) are key modes of interaction.

![image](https://github.com/user-attachments/assets/1ca656ea-2274-415b-a977-8af8c031dd77)


## 1. Text input and Text output
This example takes text input from the user and responds with text output. It's a simple program that asks the user for their favorite book and responds with a message.

```
favorite_book = input("Enter your favorite book: ")
print("Your favorite book is:", favorite_book)
```



## 2. Text Input and Audio Output
In this example, Python takes a text input and responds with an audio output. This requires the gTTS (Google Text-to-Speech) library, which converts text into spoken words. This example might require installing the gTTS and playsound modules via pip.

```
# Install gTTS (Google Text-To-Speech)
!pip install gTTS
```

Wait for the above code to complete, and then run the code below.

```
# Install the necessary libraries if not already installed

from gtts import gTTS
from IPython.display import Audio
import os

def text_to_audio_and_play(text):
    tts = gTTS(text)
    filename = "temp_audio.mp3"
    tts.save(filename)
    display(Audio(filename, autoplay=True))
    os.remove(filename)

# Usage
text_to_speak = input("Type what you want to hear: ")
text_to_audio_and_play(text_to_speak)

```


## 3. Speech to text

```
# Install the necessary libraries if not already installed
!pip install SpeechRecognition

```

# 🌱 More code to practice

### Multimodality practice coding [Goto Colab](https://github.com/MK316/Coding4ET/blob/main/Multimodality_practice.ipynb)
### Text to text, text to speech, speech to text, image to text, Open online video, etc.


[🔝](#Lesson-05-Multimodality)
🔍[BACK to the Main page](https://github.com/MK316/Coding4ET/blob/main/README.md)
