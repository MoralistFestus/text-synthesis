# Text to Speech

<img src="https://raw.githubusercontent.com/MoralistFestus/text-synthesis/master/images (6).jpeg" alt="image">
A Text To Speech program written with Python programming language.
The TTS program uses `pyttsx3` library.

The `gTTS` folder contains python file that uses Google Text to Speech API library. Click the `gTTS` folder
to see installation guide and usage.

## Installation
To install Pyttsx3 library. Type this command in terminal:
 ```python
 pip install pyttsx3
 ```
if you're on Linux, make sure to install `espeak`.

To clone or download from Github <a href="https://github.com/nateshmbhat/pyttsx3" >Pyttsx3 Github</a>

## Documentation
For the  full pyttsx3 documentation, visit <a href="https://pyttsx3.readthedocs.org" >pyttsx3 doc</a>


## Example program

```python
# import module
import pyttsx3
engine = pyttsx3.init()
engine.say('Hello welcome to speech synthesis in Python programming language.')
engine.say('I am Moralist Festus.')
engine.runAndWait()
```
This simple program `simple.py` will convert the text to speech.

```python
import pyttsx3
engine = pyttsx3.init() # object creation

""" RATE"""
rate = engine.getProperty('rate')   # getting details of current speaking rate
print (rate)                        #printing current voice rate
engine.setProperty('rate', 125)     # setting up new voice rate


"""VOLUME"""
volume = engine.getProperty('volume')   #getting to know current volume level (min=0 and max=1)
print (volume)                          #printing current volume level
engine.setProperty('volume',1.0)    # setting up volume level  between 0 and 1

"""VOICE"""
voices = engine.getProperty('voices')       #getting details of current voice
#engine.setProperty('voice', voices[0].id)  #changing index, changes voices. o for male
engine.setProperty('voice', voices[1].id)   #changing index, changes voices. 1 for female

engine.say("Hello World!")
engine.say('My current speaking rate is ' + str(rate))
engine.runAndWait()
engine.stop()

"""Saving Voice to a file"""
# On linux make sure that 'espeak' and 'ffmpeg' are installed
engine.save_to_file('Hello World', 'test.mp3')
engine.runAndWait()
```
This program will set voice index, speech rate and save the program to an mp3 file.


If you love project, Give it a star 🌟 
