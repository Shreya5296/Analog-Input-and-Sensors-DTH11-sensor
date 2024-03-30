# Analog-Input-and-Sensors-DTH11-sensor

Sensors: A sensor is a device that measures a physical quantity like pressure temperature and converts it into a 'signal' which can be read by an observer or by an instrument.
To measure Temperature and humidity sensors we have a DTH11 sensor
Our main task is to read the temperature and humidity value from DHT11 and print it to Serial Monitor and check the same in the form of analog input too.

DHT11 include 4 pins:
1. GND pin: connect this pin to GND (0V)
2. VCC pin: connect this pin to VCC (3.3V)
3. DATA pin: the pin is used to communicate between the sensor and ESP32, outputs the voltage to ESP32's input pin.

Step -1:Gather the material from the IoT kit:
● 1 x ESP32
● 1 x USB Cable
● 1 x Breadboard
● 4 x Jumper wires
● 1 x Potentiometer
● 1 x Rotary Potentiometer

Step -2 : Let’s do connections:
● Supply positive(VCC (+ve)) from the ESP 32 to breadboard terminal
● Supply negative(GND (-ve)) from the ESP 32 to breadboard negative terminal
● Now our breadboard have (VCC (+ve)) and (GND (-ve)) supply
● Take the DHT11 sensor, female jumper wires are already connected with DHT11
● Take three male jumper wires to insert into DHT11 sensor
● Now connect VCC (+ve) of DHT11 with VCC (+ve) of the breadboard
● connect GND(-ve) of DHT11 with GND(-ve) of the breadboard
● Connect data/output pin of DHT11 with D15 of the ESP32

Step-3 Let’s write a code:

Define Pins
● define DHTPIN 15
● define DHTPIN DHT11

Initialize the setup()
● Serial. begin(9600) is used for data exchange speed This tells the Arduino to get ready to exchange messages with the Serial Monitor at a data rate of 9600 bits per second. That's 9600 binary ones or zeros per second and is commonly called a baud rate.
● Serial.printIn is used to print data. Print (“DHT11 sensor!”)
● dht. begin() is used to begin the process

To execute the main process write the void loop()
● Create float h and float t variable to store decimal value
● readHumidity() will read the sensor’s humidity value.
● readTemperature() will read the sensor’s temperature value.
● Check if any reads failed and exit early using isnan()
● Serial.print used to print data. Print (“Failed to read from DHT sensor!”)
● Return the process using return()
● Serial.print() is used to print the value, print Humidity, (h), Temperature, (t)
● Set delay of 2000ms

Output:
Compile and upload the program to ESP32 board using Arduino IDE
● Verify the program on clicking Tick option
● Upload the program on clicking arrow option

Note: If port is not selected, insert the USB cable in Computer’s port and select the port

● Go to Tools and select Serial Monitor
● Rotate the potentiometer and see the output

Error Message: If an error message comes like no such file or directory then use the below method to resolve this error
Go to Tools
● Click on Manage Libraries
● Write the component name which needs to install
● Click on Install

Go to Tools and select Serial Monitor
● See the Humidity and Temperature value

As we are learning analog input let’s see analog waveform
● Go to Tools and select Serial Plotter
● See the Humidity and Temperature value
