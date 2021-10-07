import speech_recognition as sr
import smtplib
import pyaudio
import platform
import sys
from bs4 import BeautifulSoup
import email
import imaplib
from gtts import gTTS
import piglet
import os, time
tts = gTTS(text="Project: Voice based Email for blind", lang='en’)
ttsname=("name.mp3")
tts.save(ttsname)
music = pyglet.media.load(ttsname, streaming = False)
music.play()
time.sleep(music.duration)
os.remove(ttsname)
tts = gTTS(text="option 1. composed a mail.", lang='en’)
ttsname=("hello.mp3").
tts.save(ttsname)
music = pyglet.media.load(ttsname, streaming = False)
music.play()
time.sleep(music.duration)
os.remove(ttsname)
print ("2. Check your inbox")
tts = gTTS(text="option 2. Check your inbox", lang='en’)
ttsname=("second.mp3")

tts.save(ttsname)music = pyglet.media.load(ttsname, streaming = False)
music.play()
time.sleep(music.duration)
os.remove(ttsname)
tts = gTTS(text="Your choice ", lang='en')ttsname=("hello.mp3”)
tts.save(ttsname)
time.sleep(music.duration)
os.remove(ttsname)
tts = gTTS(text="option 1. composed a mail.", lang='en’)
ttsname=("hello.mp3").
tts.save(ttsname)
music = pyglet.media.load(ttsname, streaming = False)
music.play()
time.sleep(music.duration)
os.remove(ttsname)
print ("2. Check your inbox")
tts = gTTS(text="option 2. Check your inbox", lang='en’)
ttsname=("second.mp3")
tts.save(ttsname)music = pyglet.media.load(ttsname, streaming = False)
music.play()
time.sleep(music.duration)
os.remove(ttsname)
tts = gTTS(text="Your choice ", lang='en')ttsname=("hello.mp3”)
tts.save(ttsname)
unseen = mail.search(None, 'UnSeen’)
print ("Number of UnSeen mails :"+str(unseen))
tts = gTTS(text="Your Unseen mail :"+str(unseen), lang='en’)
ttsname=("unseen.mp3")
tts.save(ttsname) 

music = pyglet.media.load(ttsname, streaming = False)
music.play()
time.sleep(music.duration)
os.remove(ttsname)
result, data = mail.uid('search',None, "ALL")
inbox_item_list = data[0].split()
new = inbox_item_list[-1]
old = inbox_item_list[0]
result2, email_data = mail.uid('fetch', new, '(RFC822)’)
raw_email = email_data[0][1].decode("utf-8")
email_message = email.message_from_string(raw_email)
print ("From: "+email_message['From'])
print ("Subject: "+str(email_message['Subject']))
tts = gTTS(text="From: "+email_message['From']+" And Your subject:
"+str(email_message['Subject']), lang='en')
stat, total1 = mail.select('Inbox')
stat, data1 = mail.fetch(total1[0], "(UID BODY[TEXT])")
msg = data1[0][1]
soup = BeautifulSoup(msg, "html.parser")
txt = soup.get_text()
print ("Body :"+txt)
tts = gTTS(text="Body: "+txt, lang='en’)
ttsname=("body.mp3")
tts.save(ttsname)
music = pyglet.media.load(ttsname, streaming = False)
music.play()
time.sleep(music.duration)
os.remove(ttsname)
mail.close() mail.logout()
