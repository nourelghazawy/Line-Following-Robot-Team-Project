# Line-Following-Robot-Team-Project
Working in a team of 5 to build and program a line following robot. 

As part of the project I collaborated with another memeber to desing the robot using SolidWorks. The design was as shown below: 

Robot Isometric View

![](Robot%20Isometric%20View.PNG)

Robot Front View

![](Robot%20Front%20View.PNG)

Robot Side View

![](Robot%20Side%20View.PNG)

In addition to this I tested a the ultransonic circuit which is used to track the white line. The circuit uses 6 ultransonic sensors, each two are connected to one comparater which will out 1 or 0 to one pin on the PIC. The wiring diagram is as shown below. 

Sensor Board Wiring Diagram
![](Sensor%20Array%20Wiring%20Diagram.png)


1 means there's white line below the sensor, 0 means there's no white line below the sensor. After successfully testing the circuit on a breadboard I designed the circuit on a stripboard so that it can be tested on the robot. The circuit was as shown below.  

Stripboard Circuit
![](Ultrasonic%20Sensor%20Stripboard%20Circuit%20Picture.jpg)

The main microcontroller used on the robot was PIC which had the advantage of having many pins allowing it to be used for the sensor array circuit and the motor drive. However there was challenges on the track that needed to be tackled. Such as an end of track wall which the robot needs to sense to know that the track finished then rotate 180 degrees. Also a slope that the robot needs to speed on so that it can pass it. 

To sense the end of wall an additional Utralsonic needs to be used which is used for obstacle detection. Also, to detect the slope a gyrosope sensor needs to be used in order to sense the inclination of the robot. 

The PIC is quite an old microcontroller also its slow and has limited support online. Therefore an additional microconontroller was needed. an arduino for instance. Buying an Arduino wasn't possible due to budget limitations. Therefore I Designed and built an interface circuitry board for an ATmega chip. This reduced the cost of the additional microcontroller with atleast 75%. 

I also programmed the ATmega chip using Arduino IDE to read the ultrasonic and gyroscope sensors and output processed data to PIC18F8722. The code is avaible as ATmega Code.txt.







