---

title: "Arduino Code"

---


    #include <AccelStepper.h> //adds the AccelStepper Library


    //define motor pins

    const int stepPin = 2;

    const int dirPin = 3;


    //sets the pins for the stepper motor

    AccelStepper stepper(AccelStepper::DRIVER, stepPin, dirPin);


    //define led pins

    const int greenLED = 8;

    const int redLED = 9;


    //define button/switch pins

    const int latchingButton = 7;

    const int limitSwitch = 4;
    

    //define movement pins

    const int backwardPin = 11;

    const int forwardPin = 12;



    //declare variables for input values

    int buttonValue;

    int switchValue;

    int backValue;

    int forwardValue;


    //define changeable variables

    float diameter = 18.89;        //diameter of syringe (mm)

    float volFlowRate = 5;         //Flow rate of pump (ml/min)



    //constant variables for calculations

    const float pi = 3.14;      

    //defining pi
  
    const int rotationSteps = 3200;   

    //(steps/revolution) for motor (sixteenth step resolution microstepping)
  
    const int distancePerRotation = 8;   

    //(mm/rotation) for lead screw


    //calculating values for other variables

    float radius = diameter / 2;   

    //convert diameter to radius
  
    float area = pi * radius * radius;       

    //calculates cross-secitonal area of syringe
  
    float velocity = (volFlowRate * 1000 / 60) / area; 

    //calculates linear velocity of the syringe (mm/s) from the flow rate
  
    float speed = (velocity / distancePerRotation) * rotationSteps;  

    //converts velocity from mm/s to steps/s


    void setup() {

      //set green and red LED pins to output
  
      pinMode(greenLED, OUTPUT);
  
      pinMode(redLED, OUTPUT);
  
      //set the input components to input pullups
  
      pinMode(latchingButton, INPUT_PULLUP);
  
      pinMode(limitSwitch, INPUT_PULLUP);
  
      pinMode(forwardPin, INPUT_PULLUP);
  
      pinMode(backwardPin, INPUT_PULLUP);
  


      stepper.setAcceleration(100);         
  
      //sets the acceleration of motor to 100 steps/s^2
        
      stepper.setMaxSpeed(1000);            
  
      //sets stepper motor max speed
    
      /* max speed = 1000 steps/s but motor goes 3200 steps/rotation*/
  
    }


    void loop() {

      //defining previously declared variables by reading the input values
  
      buttonValue = digitalRead(latchingButton);
  
      switchValue = digitalRead(limitSwitch);
  
      backValue = digitalRead(backwardPin);
  
      forwardValue = digitalRead(forwardPin);
  


    if (buttonValue == 0 && switchValue == 0) {         
  
      //if latching button is pressed and the switch is not pressed
    
      stepper.setSpeed(speed);                          
    
      //sets the speed of the stepper motor based on calculation
      
      stepper.runSpeed();                               
    
      //runs the speed set for motor
      
      digitalWrite(greenLED, 1); //turns green LED on
    
      digitalWrite(redLED, 0);   //turns red LED off
    
      stepper.runSpeed();                  
    
      //runs the speed again to ensure motor is working at correct speed
      
    } else if (buttonValue == 0 && switchValue == 1) {  
  
      //if latching button on and switch is pressed stop motor
      
      digitalWrite(greenLED, 0);  //turn green LED off
    
      digitalWrite(redLED, 1);    //turn red LED on
    
      } else {                                            
  
        //if previous conditions are not met pause motor
      
        digitalWrite(greenLED, 1);  //turn on green LED
    
        digitalWrite(redLED, 1);    //turn on red LED
    
        if (forwardValue == 0 && buttonValue == 1) {      
    
        //while paused, if forward button is pressed move carriage forwards
      
        stepper.setSpeed(1000);                         
      
        //sets the speed of the stepper motor to max speed (steps/s)
          
        stepper.runSpeed();  //runs the speed
      
    } else if (backValue == 0 && buttonValue == 1) {  
    
        //while paused if back buttton is pressed move carriage backwards
        
        stepper.setSpeed(-1000);                        
      
        //set speed of motor to max speed in opposite direction (step/s)
  
        stepper.runSpeed();  //runs the speed
      
     } else {                                         
    
        //while paused, if neither button is pressed do nothing
  
      }
    
     }
  
    }
