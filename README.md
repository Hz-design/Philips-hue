# Getting started - making a phillips hue lamp with ESP8266 and RGB led strip
Philips hue documentation 

By Hong Zhou
Last updated 5 october 2022

#Introduction
Using this manual you'll be able to build a basic "Phillips hue" prototype.

#Required hardware components
- 1x ARduino Board (We'll be using the ESP8266 Development board)
- 1x RBG Led strip

Step 1: Connecting

Step 2: 

Installing the required libraries in Arduino IDE
Installing Arduino IO Libraries
1. click on the 3e tab of Arduino IE programm
2. Search for Adafruit IO Arduino (by Adafruit) in the searchfield
3. Install, choose install all

image

Adafruit IO Setup
Before we make use of Adafruit IO, we have to create an account and make a dashboard.
Follow these steps: 
1. Go to https://io.adafruit.com/, click on "Get started for Free" and make an account.
2. Go back to the website https://io.adafruit.com/ and look for the yellow key and click on it. (tips:widen your webbrowser to see it)
3. Copy your key and username.

Create Adafruit IO Feed and colorpicker 
1. Go to Dashboards > New dashboard (make a dashboard)give it a fitting name.
2. Go to Dashboard click on your new dashboard
3. Create a new block via:
image
4. Choose a color picker
5. Create the feed name: color
6. Create the block
7. Choose a color with color picker.
8. If the desired color isn't visible in the Dashboard select it again.

1. in Arduino IE: File > Examples > Adafruit IO Arduino > Adafruitio_14_neopixel
(if adafruit IO Arduino is not available check if you installed the right library)
2. Fill in your username and key. example: #define IO_USERNAME "fill in your username" etc.
3. Fill in your wifi netwerk and password.
a. NodeMCU doesn't work on 5Ghz WiFi
b. Please use your own hotspot of your phone, don't worry it uses less than <0.1 Mb data a hour.
4. Switch to the different tab: adafruit_14_Neopixel.ino
a. change: #define PIXEL_PIN 5 to #define PIXEL_PIN D5

Step 3: Uploading the required code

1. Upload the code (I got the error: Compilation error: Missing FQBN (Fully Qualified Board Name)
a. How to fix this: tools > Board > esp8266 > NodeMCU 1.0 and your port: Tools > Port > SLAB_USBtoUART.
2. activate the serial monitor
3. Open the serial Monitor the icon right above
4. set the serial monitor on 115200 buad.
image
5.
a. Occuring problem The Arduino doesn't connect to the wi-fi hotspot because hotspot is probably a 5Ghz hotspot.

4.

Step 4: 
