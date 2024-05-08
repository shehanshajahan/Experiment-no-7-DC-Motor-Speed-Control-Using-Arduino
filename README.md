# Experiment-no-6-DC-Motor-Speed-Control-Using-Arduino
###  DATE: 08/04/2024
###  NAME: Shehan Shajahan
###  ROLL NO : 212223240154
###  DEPARTMENT: Btech AIML
### AIM : To control the speed and the direction of a DC motor using L293D driver ic( H- bridge)

### Components Required:
•	Arduino UNO board
•	L293D driver
•	12V DC motor
•	10K ohm potentiometer
•	Pushbutton
•	12V source
•	Breadboard
•	Jumper wires
### THEORY 
The L293D quadruple half-H drivers chip allows us to drive 2 motors in both directions, with two PWM outputs from the Arduino we can easily control the speed as well as the direction of rotation of one DC motor. (PWM: Pulse Width Modulation).
Arduino DC motor control circuit:
Project circuit schematic diagram is the one below.

![image](https://user-images.githubusercontent.com/36288975/167763051-b230c183-afc5-46f2-ba95-0f95e10dd6c9.png)
FIGURE-01 H BRIDGE CIRUCIT INTERFACE 
 
The speed of the DC motor (both directions) is controlled with the 10k potentiometer which is connected to analog channel 0 (A0) and the direction of rotation is controlled with the push button which is connected to pin 8 of the Arduino UNO board. If the button is pressed the motor will change its direction directly.
The L293D driver has 2 VCCs: VCC1 is +5V and VCC2 is +12V (same as motor nominal voltage). Pins IN1 and IN2 are the control pins where:
![image](https://user-images.githubusercontent.com/36288975/167763120-1421c2c5-8381-49eb-b376-03f6e1113b7a.png)
TABLE-01 EXITATION TABLE FOR H BRIDGE 

As shown in the circuit diagram we need only 3 Arduino terminal pins, pin 8 is for the push button which toggles the motor direction of rotation. Pins 9 and 10 are PWM signal outputs, at any time there is only 1 active PWM, this allows us to control the direction as well as the speed by varying the duty cycle of the PWM signal. The active PWM pin decides the motor direction of rotation (one at a time, the other output is logic 0).

### PROGRAM 
```
int in1=5;
int in2=6;
int en=3;
void setup()
{
  pinMode(in1, OUTPUT);
   pinMode(in2, OUTPUT);
    pinMode(en, OUTPUT);
}

void loop()
{
   analogWrite (en,225);
  digitalWrite(in1,LOW);
   digitalWrite(in2,HIGH);
  delay(500);
 
}
```

### Schematic Simulation
![image](https://github.com/shehanshajahan/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/139317389/1c710d41-f0c5-4ccd-bb66-ee20b242b33d)
### FIGURE 02 OFF CONDITION
![image](https://github.com/shehanshajahan/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/139317389/698153ba-c7df-4bc9-b2ef-c894f52d4f3e)
### OUTPUT
![Screenshot 2024-05-08 111512](https://github.com/shehanshajahan/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/139317389/a3716bcc-7841-41ce-98ee-434b59474120)




### GRAPH AND TABULATION 
![image](https://github.com/shehanshajahan/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/139317389/049da840-f03e-4020-bb80-cb9756e5ffb8)
![image](https://github.com/shehanshajahan/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/139317389/58ade8ad-c8a5-4507-938e-47e79d678896)




### RESULTS AND DISCUSSION 
The program to control the speed and the direction of a DC motor using L293D driver ic( H- bridge) is completed and executed successfully.
