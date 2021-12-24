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

> The LED is blinked with a time interval od 1 second

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

<iframe src="https://drive.google.com/file/d/1crfYcVQjOEZs8XEKlhNs_esmtOyULyZQ/preview" width="640" height="480" allow="autoplay"></iframe>

