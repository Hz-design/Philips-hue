# Getting started - making a phillips hue lamp with ESP8266 and RGB led strip
Philips hue documentation 

By Hong Zhou
Last updated 5 october 2022

#Introduction
Using this manual you'll be able to build a basic "Phillips hue" prototype.

#Required hardware components
- 1x ARduino Board (We'll be using the ESP8266 Development board)
- 1x RBG Led strip

Step 1: Installing the Arduino IO Libraries 

Installing the required libraries in Arduino IDE
Installing Arduino IO Libraries
1. click on the 3e tab of Arduino IE programm
2. Search for Adafruit IO Arduino (by Adafruit) in the searchfield
3. Install, choose install all
<img width="250" alt="Schermafbeelding 2022-10-05 om 23 56 51" src="https://user-images.githubusercontent.com/70894669/194171453-8cd7b0e7-2ede-4bc5-a1f3-b4d8332745f8.png">

Step 2: Adafruit IO Setup
Before we make use of Adafruit IO, we have to create an account and make a dashboard.
Follow these steps: 
1. Go to https://io.adafruit.com/, click on "Get started for Free" and make an account.
2. Go back to the website https://io.adafruit.com/ and look for the yellow key and click on it. (tips:widen your webbrowser to see it)
3. Copy your key and username.

Step 3: Create Adafruit IO Feed and colorpicker 
1. Go to Dashboards > New dashboard (make a dashboard)give it a fitting name.
2. Go to Dashboard click on your new dashboard
3. Create a new block via:
<img width="1005" alt="Schermafbeelding 2022-10-05 om 23 57 38" src="https://user-images.githubusercontent.com/70894669/194171566-6e6f4175-1640-483e-addd-71bddda31bea.png">
The cogwheel icon with a dropdown V.

4. Choose a color picker
5. Create the feed name: color
6. Create the block
7. Choose a color with color picker.
8. If the desired color isn't visible in the Dashboard select it again.

Step 4: Changing code
1. in Arduino IE: File > Examples > Adafruit IO Arduino > Adafruitio_14_neopixel
(if adafruit IO Arduino is not available check if you installed the right library)
2. Fill in your username and key. example: #define IO_USERNAME "fill in your username" etc.
3. Fill in your wifi netwerk and password.
a. NodeMCU doesn't work on 5Ghz WiFi
b. Please use your own hotspot of your phone, don't worry it uses less than <0.1 Mb data a hour.
4. Switch to the different tab: adafruit_14_Neopixel.ino
a. change: #define PIXEL_PIN 5 to #define PIXEL_PIN D5

Step 5: Uploading the required code

1. Upload the code (I got the error: Compilation error: Missing FQBN (Fully Qualified Board Name)
a. How to fix this: tools > Board > esp8266 > NodeMCU 1.0 and your port: Tools > Port > SLAB_USBtoUART.
2. activate the serial monitor
3. Open the serial Monitor the icon right above
4. set the serial monitor on 115200 buad.
image<img width="1142" alt="Schermafbeelding 2022-10-05 om 23 47 19" src="https://user-images.githubusercontent.com/70894669/194170763-c021ce71-fd3d-4179-80d0-01ec9cab92fd.png">

5. If this succeed your serial monitor should be connected.
a. Occuring problem The Arduino doesn't connect to the wi-fi hotspot because hotspot is probably a 5Ghz hotspot.
b. Problem solved: Miss typed my username, what I did was I changed my bandwidth on my phone from 5Ghz to 2.4 Ghz with the option Maximaise compability. After the transformation I still struggled with the Arduino not connecting to my computer. Because the Arduino wouldn't connect. So I changed my hotspot network name and restarted my iPhone 14 pro. I could see that a device has connected on my phone so one step to victory. So I was thinking, it's connected to wifi yes, the code has been uploaded yes, could it connect to the adafruit.io website? No. So I went on checking my username and keypass and I saw that my username missed a capitol. 

6. You should be able to change to color settings, and see it in Serial Monitor.
7. If your Ledstrip is connected you'll be able too see the difference in color.

Congrats you just made your own Philips (Signify) HUE, for a couple euro. Adafruit also works on your phone, so you can almost do anything from the video from lesson 1.

Final result

https://user-images.githubusercontent.com/70894669/194171930-548110f9-0d18-4221-bf09-6cb9e80a84e7.MOV

