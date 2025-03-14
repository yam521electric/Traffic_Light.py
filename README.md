# Traffic_Light.py
import gpiozero
from gpiozero import LED
import time
#These libraries are cool and junk and you kind of need them for this code

Stop_light = {'red_LED': LED(26), 'yellow_LED': LED(27), 'green_LED': LED(22)}
#Making a dictionary and pins for each different LED 'cause who wants to right all that crap out?

#The definition to run the traffic light and junk. Also lyrics to a Rammestein song because why not 
#You can change the times with the numbers or if you import a random function it will randomize the pattern theres load of complicated junk that could be executed here

#the def neame is a reference too teehee
def Everybodys_got_a_little_light_under_the_sun():
    print("Hier Kommt Die Sonne")
    FLASH_LIGHT = [('red_LED', 5), ('yellow_LED', 5), ('green_LED', 5)]
    
    for light, duration in FLASH_LIGHT:
        Stop_light[light].on()
        time.sleep(duration)
        Stop_light[light].off()
#since the previous statements only tell the LED what to do they kind of forget the important part of turning it on so you need this

Everybodys_got_a_little_light_under_the_sun()
#This just calls the function in the end to execute it

# ============================================================================
# Source: My Brain (there's a previous light and song code I took reference from)
# Hacker: Noah A. Murillo (he's pretty cool I heard)
# Program/Design Name: Traffic_Light.py
# Description:    This is a program to drive a set of LED's in a traffic light manner (it's pretty simple)
# that can be called with external parameters that are read using a post/get feature.
# program description:
# 1) Reads Dictionary for pin definitions
# 2) Executes def function to read the timing of each pin function
# 3) Finishes up doing the code with final call of def functiom
# Dependencies:   python3, Raspberry Pi (5 preferable), 3 LED's, 3 resistors, 6 wires, 6 shrink tubes
#   Inputs: <list any expected user input here>
#   Outputs: <list any expected program output here>
# Additional Comments: 
# 
# ============================================================================
