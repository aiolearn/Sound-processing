# Sound processing

In this project, we have written a voice processing program that processes the voice with artificial intelligence and displays the read text

## Modules

```python
!pip install SpeechRecognition
# !pip install PyAudio
import speech_recognition as sr
```

## Usage

This code first creates a sound detection object, then selects the microphone as the sound source and displays the message "Listening...". After that, by setting the stop threshold, it waits for the input sound to be recorded from the microphone and stores it in a variable called audio.

```python
r = sr.Recognizer()
with sr.Microphone() as source:
     print("Listening...")
     r.pause_threshold = 1
     audio = r.listen(source)
```

This part of the code displays the message "Recognizing..." after recording the sound, then converts the recorded sound to Farsi text and prints it on the console.

```python
print("Recognizing...")
query = r.recognize_google(audio, language ='fa-IR')
print("User said: ",query)
```

## Result

This project was written by Majid Tajanjari and the Aiolearn team, and we need your support!❤️

# پردازش صدا

در این پروژه یک برنامه پردازش صدا نوشته ایم که صدا را با هوش مصنوعی پردازش کرده و متن خوانده شده را نمایش می دهد

## ماژول ها

```python
!pip install SpeechRecognition
# !pip install PyAudio
import speech_recognition as sr
```

## نحوه استقاده

این کد ابتدا یک شی تشخیص صدا ایجاد می کند، سپس میکروفون را به عنوان منبع صدا انتخاب می کند و پیام "Listening..." را نمایش می دهد. پس از آن با تنظیم آستانه توقف، منتظر می ماند تا صدای ورودی از میکروفون ضبط شود و آن را در متغیری به نام صدا ذخیره می کند.

```python
r = sr.Recognizer()
with sr.Microphone() as source:
     print("Listening...")
     r.pause_threshold = 1
     audio = r.listen(source)
```

این قسمت از کد پس از ضبط صدا پیغام Recognizing... را نمایش می دهد و سپس صدای ضبط شده را به متن فارسی تبدیل کرده و روی کنسول چاپ می کند.

```python
print("Recognizing...")
query = r.recognize_google(audio, language ='fa-IR')
print("User said: ",query)
```

## نتیجه

این پروژه توسط مجید تجن جاری و تیم Aiolearn نوشته شده است و ما به حمایت شما نیازمندیم!❤️