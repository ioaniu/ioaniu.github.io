---
title: Automatic Door Control System
---

---
### INTRODUCTION

<center>![](/automaticdoor/lafaya.png)</center>

&emsp;&emsp;A door is a moving mechanism used to block off, and allow access to, an entrance to or within an enclosed space, such as a building, room or vehicle. Then, the automatic door is the progress and perception of the door.  
&emsp;&emsp;The automatic door control system is similar to the brain of the door, it generally connects with some auxiliary equipment. When receiving and recognizing the action directive, the system may open or close the door and motion the process of opening and closing.

---
### HARDWARE

<center>![](/automaticdoor/circuit.png)
<font size = "2px">Fig.1. Automatic Door Control System Hardware Diagram. </font></center>

&emsp;&emsp;The design principle of the automatic door control system circuit is illustrated in Fig.1. The circuit contains power circuit, MCU circuit, motor driver circuit, sensors circuit, bus circuit and ports circuit. The final design is a **4-layer PCBA** that combines analog signals and digital signals. They are described below:  
* Power Circuit: it provides a stable supply environment for the system, and offers 24VDC/10A, 12VDC/3A and 5VDC/1A, respectively.
* MCU Circuit: **Microchip's 16-bit DsPIC** digital signal controller is selected as main control chip in this system, which includes a rich set of high performance peripherals ans satisfies the requirements of motor control well. 
* Motors Driver Circuit: Driver is composed by **Infineon's** three phase driver IC and **MOSFET**, which can support more than 240 watts of power.
* Sensors Circuit: Sensing the current, the speed, and the position of the motor.
* Bus Circuit: CAN-bus and RS485-bus are offered network communication. Here, we choose Microchip's MCP2551 to CAN-bus and MAXIM's MAX13085 to RS-485.
* Ports Circuit: The ports are used to connect the ancillary equipment, succ as access, motion sensor, switch, etc.  


---
### SOFTWARE

&emsp;&emsp;Software function of the automatic door control system includes door logical processing, motor control, network interface processing, parameter sensing. Fig.2 shows the software flowchart. Firstly, the software initiates the system to configure the general parameters, then learns or recovers the motor parameters, then executes the main loop of the system (such as communication, sensing, motor running, etc.).
<center>![](/automaticdoor/flow.png)
<font size = "2px">Fig.2. Software flowchart of Automatic Door Control System. </font></center>

&emsp;&emsp;The key of the system is how to control the motor to adapt the various loads and run smoothly. The method of motor control is based on fuzzy adaptive algorithm，which implements three-loop controller of position, velocity and current feedback(show in Fig.3).

<center>![](/automaticdoor/fuzzy.png)
<font size = "2px">Fig.3. Based on Fuzzy Control for Motor Control. </font></center>

---
### CONCLUSION

&emsp;&emsp;The automatic door control system has the advantages of stabilised performance, high speed, vigoroso flexibility, etc.  The system not only supports  abundant external equipment interfaces and motor interfaces (compatible DC brush motor and DC brushless motor), and implements various control function of the automatic door (such as sliding door, swing door, folding door, revolving door, etc.). The system has already been certified by CE, and has gotten the copyright of China.  
&emsp;&emsp;The system has powerful function, however,  there are many areas in need of improvement, such as high-cost, complex operation and limited load adaptability. In the further, the system still need to be refined.

---
