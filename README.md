# ChatGPT voice assistant
Using this program, you can ask chatgpt your questions in the form of voice and receive answers in the form of voice.
# How to install and operate 
To run this program, you must have whisper, openai, gTTS installed
### If you don't have it installed, you can install it with the following commands in the terminal :
``` 
 pip install openai
```
```
 pip install whisper
```
```
 pip install gTTS
```

# Using the microphone in google colab
I used js, html to get the sound in google colab, which can be seen in the source code.

# Convert audio to text
To convert voice to text, I took help from one of Openai's products called Whisper, which had several models. I used the large model because I wanted my program to support the Persian language.

# Connect to chatgpt
```
import openai

API_KEY = "your api key"
openai.api_key = API_KEY
response = openai.chat.completions.create(model="gpt-3.5-turbo",messages=[{"role":"user",f"content":x}])
print(response.choices[0].message.content)
 ```

# Convert audio to text using Google
```
from gtts import gTTS
from IPython.display import Audio

file = "./audio1.mp3" // Audio file storage location

gTTS (text = response_text,lang = "en").save(file)


wn = Audio("./audio1.mp3", autoplay=True)
display(wn)

```

