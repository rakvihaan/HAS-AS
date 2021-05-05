# HAS-AS
---
- For sure many of you were always fascinated about the idea of controlling electric appliances over internet using your phones or other electronic gadgets rather than using the old traditional wall switches.
- **HAS-AS** is just the thing for you to get started with IoT and learn to control electronic appliances using your phones or other electronic gadgets.
- **HAS-AS** is a simple **Home Automation** solution to turn on or off simple appliances, with an integrated **Laser Tripwire Alarm System** which sends e-mail alerts when an intruder breaks in(Lets hope that never happens...XD).



## Working
---
- Let's start with the working of the **Laser Tripwire Alarm System**
  - The Alarm system uses a traditional laser module, an LDR, a buzzer, a 16x2 LCD Display and to carry out the function an Arduino (Any Arduino will work fine).
    - An **LDR or Light Dependent Resistor** changes it's resistance value depending on the level of light, which can be used as an input device to the arduino to read, and detect the light levels. In simple words it is used to detect light levels.
    - The laser acts as an invisible tripwire which when blocked alters the light level falling on the **LDR** which causes the **Alarm System** to activate.
    - The **Arduino** is the main part of this system, it reads the light level from the **LDR** and turns on the alarm if the laser light is blocked, which could mean that an intuder has broken in.
    - The **LCD Diaplay** is used to display the state of the **Alarm System**.  


    
- Let's check the working of the **Home Automation System**
  - This system uses a Raspberry Pi and few Relays that's it, that's the beauty of using a Raspberry Pi, minimal components when compared to an Arduino version and limitless possiblities.
  - We will be looking at two ways to control the GPIO pins on the Rapberry Pi, one using Flash and the other using Blynk.
    - We will be hosting a webpage on the Pi using a software called Flask. Flask is simple python micro web framework which we will be using to host our control page, and allow us to control some protocols. To learn more on Flask click [here](https://flask.palletsprojects.com/en/1.1.x/).
    - We will also be using a python module called RPi.GPIO to controll the GPIO pins of the Raspberry Pi. To learn more about the module click [here](https://pythonhosted.org/RPIO/).
    - We will also be using Blynk to control the GPIO pins on the Pi. Blynk is a platform used to control IoT hardware remotely over the internet. To learn more about Blynk click [here](https://docs.blynk.cc/).  
    - Since the power supply on single board computers like Raspberry Pi or on microcontrollers like Arduino cannot be enough to power high current devices or AC appliances we use **Relays** to help us with that. **Relays** are basically electrically operated switches with their own isolated power supply. They can be controlled just like an LED.



## Parts Required
---
- For Laser Alarm System : 
  - An Arduino (any one is fine)
  - An LDR
  - A buzzer
  - 16x2 LCD Display
  - Laser module
  - Jumper wires
  - Breadboard

- For Home Automation System : 
  - A Raspberry Pi
  - Relays
  - Jumper wires
  - Wires used in household wirings
  

## g 
---
Clone this repo to a proper location on your pc. 
Navigate to the folder a run the following line of code to download necessary modules required.
```
pip install -r requirements.txt
```

---

First lets start with building the alarm system.

- 
- Download Arduino IDE from [here](https://www.arduino.cc/en/software) if already haven't.
- 
