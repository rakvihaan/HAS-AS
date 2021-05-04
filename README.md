# HAS-AS
---
- For sure many of you were always fascinated about the idea of controlling electric appliances over internet using your phones or other electronic gadgets rather than using the old traditional wall switches.
- **HAS-AS** is just the thing for you to get started with IoT and learn to control electronic appliances using your phones or other electronic gadgets.
- **HAS-AS** is a simple **Home Automation** solution to turn on or off simple appliances, with an integrated **Laser Tripwire Alarm System** which sends e-mail alerts when an intruder breaks in(Lets hope that never happens...XD).

## Working
---
- Let's start with the working of the **Laser Tripwire Alarm System**
  - The Alarm system uses a traditional laser module, an LDR, a buzzer, an LED, a 16x2 LCD Display and to carry out the function an Arduino (Any Arduino will work fine).
    - An **LDR or Light Dependent Resistor** changes it's resistance value depending on the level of light, which can be used as an input device to the arduino to read, and detect the light levels. In simple words it is used to detect light levels.
    - The laser acts as an invisible tripwire which when blocked alters the light level falling on the **LDR** which causes the **Alarm System** to activate.
    - The **Arduino** is the main part of this system, it reads the light level from the **LDR** and turns on the alarm if the laser light is blocked, which could mean that an intuder has broken in.
    - The **LCD Diaplay** is used to display the state of the **Alarm System**.  
    
    
- Let's check the working of the **Home Automation System**
  - This system uses a Raspberry Pi and few Relays that's it, that's the beauty of using a Raspberry Pi, minimal components when compared to an Arduino version and limitless possiblities.
    - We will be hosting a webpage on the Pi using a software called Flask. Flask is simple python micro web framework which we will be using to host our control page, and allow us to control some protocols. To learn more on Flask click [here](https://flask.palletsprojects.com/en/1.1.x/)
    - 
