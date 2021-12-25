# __**Kerala IoT Challenge: Level-1**__

# Experiment 1 - Hello World LED Blinking

> A basic Program similar to printing "*Hello World* " in any programming language. The Aim is to blink an LED using **Arduino Uno Board**.

> Arduino Uno is an open-source microcontroller board developed by Arduino.cc. It has several advantages over the conventional microcontrollers. It comes with a pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also it is less expensive & beginner friendly.

## Components Required  
* Arduino Uno Board 
* USB Cable 
* LED (Any Color) x 1 Nos
* 220 OHM Resistor X 1 Nos
* Breadboard 
* Jumper Wires (Male to Male ) X 2 Nos

## Circuit Diagram

<iframe src="https://drive.google.com/file/d/1a7StPJyJS_xLxvAypo7lb9wxHR5HKGno/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int ledPin=10;   // define digital pin 10.

void setup() {
  pinMode(ledPin,OUTPUT); // define pin with LED connected as output.
}

void loop() {
  digitalWrite(ledPin,HIGH);  // set the LED on.
  delay(1000);                // wait for a second.
  digitalWrite(ledPin,LOW);   // set the LED off.
  delay(1000);                // wait for a second.
}

```

## Output

> The LED is blinked with a time interval of 1 second

<iframe src="https://drive.google.com/file/d/1_vFBUMslCSqiNlfPoc9ICI4rU2lpY0wn/preview" width="640" height="480" allow="autoplay"></iframe>

# Experiment 2 : Traffic Light

> In the previous program, we have done the LED blinking experiment with one LED. Now, it’s time to up the stakes and do a bit more complicated experiment-traffic lights. Actually, these two experiments are similar. While in this traffic lights experiment, we use 3 LEDs with different colors rather than 1 LED.

## Components Required 

* Arduino board *1
* USB cable *1
* Red M5 LED*1
* Yellow M5 LED*1
* Green M5 LED*1
* 220Ω resistor *3

## Circuit Diagram

<iframe src="https://drive.google.com/file/d/1aOzUVYDMJTpzoL7NUcoNC5oCRviyUSPb/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int redLED = 10;
int yellowLED = 7;
int greenLED = 4;

void setup() {
  pinMode(redLED, OUTPUT);
  pinMode(yellowLED, OUTPUT);
  pinMode(greenLED, OUTPUT);
}

void loop() {
  digitalWrite(greenLED, HIGH);
  delay(5000);
  digitalWrite(greenLED, LOW);

  for (int i = 0; i < 3; i++) {
    delay(500);   // wait 5 seconds
    digitalWrite(yellowLED, HIGH);
    delay(500);
    digitalWrite(yellowLED, LOW);
  }
  
  delay(500);
  digitalWrite(redLED, HIGH);
  delay(5000);
  digitalWrite(redLED, LOW);
}
```

## Output

> In Traffic light the green LED blink about 5 second, then it is turnoff. Then the yellow LED blinks 3 times with a time interval of 0.5 second.Then the red LED blink about 5 seconds. This process continues.

<iframe src="https://drive.google.com/file/d/1aNLQ9esjV7VXee6iXbvcMZN3RidI1_2V/preview" width="640" height="480" allow="autoplay"></iframe>

# Experiment 3 : LED Chasing Effect

> We often see billboards composed of colorful LEDs. They are constantly changing to form various light effects. In this experiment, we compile a program to simulate LED chasing effect. The long lead of LED is the positive side; short lead is negative.

## Components Required

* Led *6
* Arduino board *1
* 220Ω resistor *6
* Breadboard *1
* USB cable*1
* Breadboard wire *13

## Circuit Diagram

<iframe src="https://drive.google.com/file/d/1aRU9ASibO_EVZExIgvXuNEPUkLn4vJNc/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int BASE=2;  // the I/O pin for the first LED
int NUM=6;   // number of LEDs
void setup()
{
   for(int i=BASE;i<BASE+NUM;i++)     //for(i=2;i<8;i++){}
   {
     pinMode(i,OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for(int i=BASE;i<BASE+NUM;i++) 
   {
     digitalWrite(i,LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for(int i=BASE;i<BASE+NUM;i++) 
   {
     digitalWrite(i,HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(200);        // delay
   }  
}

```

## Output

<iframe src="https://drive.google.com/file/d/1aRS9UR71ErY2z8gHnOJLQbja9MWDuJ7g/preview" width="640" height="480" allow="autoplay"></iframe>

# Experiment 4: Button Controlled LED

> An experiment to light an LED using a Push Button.

## Components Required 

* Arduino Uno
* Button switch*1
* Red M5 LED*1
* 220ΩResistor*1
* 10KΩ Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*6
* USB cable*1

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1b9a3Xh35Hpcn2YSD-GWkLJ5_ezjbtI0Q/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int pushButtonPin=7;
int ledPin=10;

void setup() {
  pinMode(pushButtonPin,INPUT);
  pinMode(ledPin,OUTPUT);
}

void loop() {
  int value=digitalRead(pushButtonPin);
  if(value==HIGH){
    digitalWrite(ledPin,HIGH);
    }
  else{
    digitalWrite(ledPin,LOW);
    }  
}

```
## Output

> When the push button is pressed the LED is turned on otherwise it is off.

<iframe src="https://drive.google.com/file/d/1b75s8TpWnPmmIaZ2vRndma61RXcgMiC1/preview" width="640" height="480" allow="autoplay"></iframe>

# Experiment 5 : Buzzer

> An experiment to understand the working of a buzzer.

## Components Required

* Arduino Uno
* Buzzer*1
* Breadboard*1
* Breadboard Jumper Wire*2
* USB cable*1

<iframe src="https://drive.google.com/file/d/1bCYx4HTTnR6r5ofHokuyqMCTUS1FaTIR/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int buzzerPin=8;

void setup() {
  pinMode(buzzerPin,OUTPUT);
}

void loop() {
  digitalWrite(buzzerPin,HIGH);
  delay(5000);
  digitalWrite(buzzerPin,LOW);
  delay(2500);
}

```

## Output

> The Buzzer makes beep sound.

<iframe src="https://drive.google.com/file/d/1b9musasMSkpdPV0hUYHVFDwXQ5Z2pUTT/preview" width="640" height="480" allow="autoplay"></iframe>


# Experiment 6 : RGB LED

> An experiment to understand the working of a RGB LED.

## Components Required

* Arduino Uno
* USB Cable * 1
* RGB LED * 1
* Resistor *3
* Breadboard jumper wire*5

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1bDv9XzsQwxKkAbMQ2d7FdhwT8368cu0T/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int redLED = 11;
int blueLED = 10;
int greenLED = 9;
int val;

void setup() {
  pinMode(redLED, OUTPUT);
  pinMode(blueLED, OUTPUT);
  pinMode(greenLED, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  for (val = 255; val > 0; val--)
  {
    analogWrite(11, val);
    analogWrite(10, 255 - val);
    analogWrite(9, 128 - val);
    delay(1);
  }
  for (val = 0; val < 255; val++)
  {
    analogWrite(11, val);
    analogWrite(10, 255 - val);
    analogWrite(9, 128 - val);
    delay(1);
  }
  Serial.println(val, DEC);
}

```

## Output

> The RGB LED blinks.

<iframe src="https://drive.google.com/file/d/1bDF6kjx_ksgmsZ-uUJKtRNaVgUGCyKvK/preview" width="640" height="480" allow="autoplay"></iframe>

# Experiment 7 - LDR Light Sensor

> An experiment to understand the working of an LDR light Sensor.

## LDR : Light Dependent Sensor

> Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.

## Components Required

* Arduino Uno Board
* Photo Resistor*1
* Red M5 LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*7
* USB cable*1

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1bYp2eFOM836RWwWW7p76h9Ws8N3Npqee/preview" width="640" height="480" allow="autoplay"></iframe>

## Procedure

* Connect the 3.3v output of the Arduino to the positive rail of the breadboard
* Connect the ground to the negative rail of the breadboard
* Place the LDR on the breadboard
* Attach the 10K resistor to one of the legs of the LDR
* Connect the A0 pin of the Arduino to the same column where the LDR and resistor is connected (Since the LDR gives out an analog voltage, it is connected to the analog input pin on the Arduino. The Arduino, with its built-in ADC (Analog to Digital Converter), then converts the analog voltage from 0-5V into a digital value in the range of 0-1023). - Now connect the other end of the 10K resistor to the negative rail
* And the the second (free) leg of the LDR to the positive rail
Pretty much this is what we need for the light sensing. Basic circuits like this can be done without an Arduino aswell. However, if you want to log the values and use it to create charts, run other logics etc. I will recomend an Arduino or ESP8266 or may be a ESP32 for this.
Now, as we want our circuit to do something in the real world other than just displaying the values on the computer screen we will be attaching a LED to the circuit. The LED will turn on when its dark and will go off when its bright. To achieve this we will:
* Place the LED on the breadboard
* Connect the 220ohm resistor to the long leg (+ve) of the LED
* Then we will connect the other leg of the resistor to pin number 13 (digital pin) of the Arduino
* and the shorter leg of the LED to the negative rail of the breadboard

## Code

```

int ledPin=11;
int LDRPin=A0;
int value=0;

void setup() {
  pinMode(ledPin,OUTPUT);
  //pinMode(LDRPin,INPUT);
  Serial.begin(9600);
}

void loop() {
  value=analogRead(A0);
  Serial.println(value);
  if (value<50){
    digitalWrite(ledPin,HIGH);
    }
  else{
    digitalWrite(ledPin,LOW);  
    } 
}

```

## Output

<iframe src="https://drive.google.com/file/d/1bWcJMEvDCdi6tGUzNEvNiH0hdSdv85ZH/preview" width="640" height="480" allow="autoplay"></iframe>


# Experiment 8 : Flame Sensor

> An experiment to understand the working of an Flame sensor.

## Flame Sensor

 **Usage**:These types of sensors are used for short range fire detection and can be used to monitor projects or as a safety precaution to cut devices off / on.

 **Range**:I have found this unit is mostly accurate up to about 3 feet.

 **How it works**:The flame sensor is very sensitive to IR wavelength at 760 nm ~ 1100 nm light.

**Analog output (A0)**: Real-time output voltage signal on the thermal resistance.

**Digital output (D0)**: When the temperature reaches a certain threshold, the output high and low signal threshold adjustable via potentiometer.

**Pins:**

* VCC - Positive voltage input: 5v for analog 3.3v for Digital.

* A0 - Analog output

* D0 - Digital output

* GND -  Ground

## Components Required

* Arduino UNO
* Flame Sensor
* LED
* Buzzer
* BreadBoard
* Jumper

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1cxmamxl2GsNSdq9oZYFPBJLoNjNiGGSX/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int buzzer=9;
int flame=A0;
int value=0;

void setup() {
  pinMode(buzzer,OUTPUT);
  pinMode(flame,INPUT);
  Serial.begin(9600);
}

void loop() {
  value=analogRead(flame);
  Serial.println(value);
  if(value>100){
    digitalWrite(buzzer,HIGH);
    }
  else{
    digitalWrite(buzzer,LOW);
    }  
}

```

## Output

<iframe src="https://drive.google.com/file/d/1crfYcVQjOEZs8XEKlhNs_esmtOyULyZQ/preview" width="640" height="480" allow="autoplay"></iframe>


# Experiment 9 : LM35 Temperature Sensor

> An experiment to understand the working of an LM35 Temperature Sensor.

## LM35 Temperature Sensor

> LM35 is a common and easy-to-use temperature sensor. LM35 is a widely used temperature sensor with many different package types. At room temperature, it can achieve the accuracy of ±1/4°C without additional calibration processing. LM35 temperature sensor can produce different voltage by different temperature When temperature is 0 ℃, it outputs 0V; if increasing 1 ℃, the output voltage will increase 10 mv.

## Components Required

* Arduino Uno  Board*1
* LM35*1
* Breadboard*1
* Breadboard Jumper Wire*5
* USB cable*1

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1bhtQHqxbl2Hrli0SFZcpkpcB68WiRoc-/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int potPin = 0; // initialize analog pin 0 for LM35 temperature sensor

void setup()
{
  Serial.begin(9600);// set baud rate at”9600”
}

void loop()
{
  int val;// define variable
  int dat;// define variable
  val = analogRead(0); // read the analog value of the sensor and assign it to val
  dat = (125 * val) >> 8; // temperature calculation formula
  Serial.print("Temp: ");// output and display characters beginning with Tep
  Serial.print(dat);// output and display value of dat
  Serial.println("°C");// display “C” characters
  delay(500);// wait for 0.5 second
}

```

## Output

<iframe src="https://drive.google.com/file/d/1bcseeXimEUsC-M9T-TZLl_irFxF7SUrn/preview" width="640" height="480" allow="autoplay"></iframe>       


# Experiment 10:IR Remote Control Using TSOP

> An experiment to understand the working of IR Remote Control using TSOP.

## Components Required

* Arduino Uno Board*1
* Infrared Remote Controller(You can use TV Remote or any other remote) *1
* Infrared Receiver *1
* LED *6
* 220ΩResistor *6
* Breadboard Wire 
* USB cable*1

## Circuit Diagrams



## Code

```



```

## Output




# Experiment 11 :Potentiometer analog Value Reading

> An experiment to understand the working of Potentiometer.

## Components Required

* Arduino Uno Board*1
* 10K Potentiometer *1
* Breadboard*1
* Breadboard Jumper Wire*3
* USB cable*1

## Circuit Diagrams


## Code

```

void setup() {
  pinMode(A0,INPUT);
}

void loop() {
  int value=analogRead(A0);
  Serial.println(value);
}

```

## Output




# Experiment 12 : 7 Segment Display
        
> An experiment to understand the working of 7 Segment Display.

## Components Required

* Arduino Uno Board*1
* digit LED Segment Display*1
* 220Ω Resistor*8
* Breadboard*1
* Breadboard Jumper Wires *several
* USB cable*1

## Circuit Diagrams



## Code

```



```

## Output




