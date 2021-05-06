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
  - Potentiometer(for controlling the contrast of the display, you can skip this part and just use a resistor if you want)
  - Laser module
  - Jumper wires
  - Breadboard
  - 10K ohms resistor

- For Home Automation System : 
  - A Raspberry Pi
  - Relays
  - Jumper wires
  - Wires used in household wirings
  

## Building

---

### Laser Tripwire Alarm System
---

First lets start with building the alarm system.

- Connect the the components according to the circuit diagram.

    ![Screenshot](alarm_system_circuit.jpeg)


  The pins of the LCD display are connected to the arduino in the following manner: 
    1. VSS/GND ==>  GND
    2. VCC     ==>  5v
    3. VEE     ==>  Potentiometer
    4. RS      ==>  D7
    5. RW      ==>  GND
    6. E       ==>  D8
    7. DB0     ==>  NOTHING  
    8. DB1     ==>  NOTHING
    9. DB2     ==>  NOTHING
    10. DB3    ==>  NOTHING
    11. DB4    ==>  D9
    12. DB5    ==>  D10
    13. DB6    ==>  D11
    14. DB7    ==>  D12
    15. LED+   ==>  5V
    16. LED-   ==>  GND

    After the circuit is complete you can continue with uploading the sketch.

  - Download Arduino IDE from [here](https://www.arduino.cc/en/software) if already haven't.
  - Clone this repo or just download the **Alarm_System.ino** file.
  - Open the sketch **Alarm_System.ino** using the IDE.
  - Select your board and proper port from the **Tools** menu.(To know to which port is the arduino connected to, use Device Manager on Windows or use `dmesg` command on linux)
  - Click on upload.
  - And you are done!!! Your **Laser Tripwire Alarm System** should now be working.


### Home Automation with Raspberry Pi
---

First lets look at the wiring
- Connect the relays according to the circuit diagram. 
