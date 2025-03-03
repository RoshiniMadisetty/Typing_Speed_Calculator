# Typing_Speed_Calculator
from time import *
import random as r
def mistake(testdata,usertest):
    error = 0
    for i in range(len(testdata)):
        try:
            if testdata[i] != usertest[i]:
                error = error + 1
        except:
            error = error + 1
    return error

def speed_time(time_s,time_e,userinput):
    time_delay = time_e - time_s
    time_R = round(time_delay,2)
    speed = len(userinput)/time_R
    return round(speed)


test = ['The cat jumped onto the windowsill and stared at the birds outside',
'A sudden gust of wind knocked over the stack of papers on the desk',
'She found an old photograph tucked inside the pages of her favorite book',
'The sound of rain tapping against the roof was oddly comforting',
'He took a deep breath before stepping onto the stage']


test1 = r.choice(test)
print('***Typing Speed Calculator***')
print(test1)
print()
print()

time_1 = time()
testinput = input("Enter the given sentence:")
time_2 = time()

print('Speed :',speed_time(time_1,time_2,testinput) , 'word/second')
print('Error :',mistake(test1,testinput))
