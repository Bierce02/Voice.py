#Voice.py
#A code that used to allow you to scroll down or up with your voice

import speech_recognition as sr
import pyautogui

while 0 < 10:
    speed = 120
    sleepTime = 1

    r = sr.Recognizer()



    with sr.Microphone() as source:
        print("say Down or up")
        audio = r.listen(source)

        try:
            text = r.recognize_google(audio)
            print("you said",format(text))
        except:
            print("sorry I did not understand you")


    if text .__contains__("down"):

        for i in range (10):
            pyautogui.scroll(int(-speed))

            pyautogui.sleep(int(-sleepTime))



    if text .__contains__("up"):
        for i in range (10):
            pyautogui.scroll(int(speed))

            pyautogui.scroll(int(sleepTime))



    if text .__contains__("pause"):
        pyautogui.scroll(int(speed-speed))



input()
