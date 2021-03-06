# DCC++ EX Starter Kit

This guide is designed for do-it-yourselfers to build their own system. Anyone can do it, however if you don't feel technically inclined or just want to save the time, you can purchase a starter kit that contains:

* __Controller:__ A Raspberry Pi with SD Card already configured with everything you need including the JMRI software. 
* __Command Station:__ An Arduino with DCC++ software already uploaded and a Motor Controller Shield prepped and installed. This is often abbreviated to just "CS"

!!! NOTE 
    Keep in mind that if you just want to run trains and start without the separate Raspberry Pi and JMRI, you can purchase just the Arduino Mega and Motorshield combination and use our WebThrottle-EX.

# What You Will Need

- A "main" track aka "operations" track - most people already have this, it's your layout
- A "programming" track aka "service" track - a short section of track that you will use to program locomotives and other pieces of equipment that use "accessory decoders". This can be an electrically isolated siding if you like and DCC++ EX will allow that to be part of your main track when not programming locos
- A locomotive equipped with a DCC decoder (either a standard or sound decoder)

![DCC++ Overview](../images/dccpp_starter.png)

### Equipment List:

#### Hardware

* A compatible Arduino Board
    * Arduino Mega (clones work too)
    * Arduino UNO R3 (clones work too)
    * Arduino Nano (Tinkerers and Engineers)
* A compatible motor driver shield
    * Arduino Motor Driver Shield Rev 3 (clones work too)
    * Deek-Robot L298 Motor Shield
    * Pololu MC33926 Dual Motor Driver Shield (https://www.pololu.com/product/2503)(Tinkerers/Engineers)
    * Other boards listed in the hardware section (Engineers)
* DC Power Supply for the motor shield 
* DC Power Supply for the Mega
    * You CAN have one power supply, please see more detail at [Power Supplies](../hardware/power-supplies.md)
* USB A to B Cable (aka USB Printer Cable) to connect your Pi or computer to the Arduino
* A MicroSD Card (for the Raspberry Pi if you choose to use one)
* Computer to upload software to the Arduino Command Station and optionally operate as a controller (see note below)

We recommend:

[Elegoo Mega 2560](https://www.amazon.com/ELEGOO-ATmega2560-ATMEGA16U2-Projects-Compliant/dp/B01H4ZLZLQ/ref=asc_df_B01H4ZLZLQ/?tag=hyprod-20&linkCode=df0&hvadid=309743296044&hvpos=&hvnetw=g&hvrand=2075336217815630856&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9009681&hvtargid=pla-490931309987&psc=1)

[Deek-Robot Motor Shield](https://www.aliexpress.com/item/32832049214.html?src=google&src=google&albch=shopping&acnt=494-037-6276&isdl=y&slnk=&plac=&mtctp=&albbt=Google_7_shopping&aff_platform=google&aff_short_key=UneMJZVf&&albagn=888888&albcp=1582410664&albag=59754279756&trgt=743612850874&crea=en32832049214&netw=u&device=c&albpg=743612850874&albpd=en32832049214&gclid=CjwKCAjwrcH3BRApEiwAxjdPTQJGRS7xnxV6FvOM14ZyRdKZHZiOUmS5oI74ytkxk5biSFBRGnazaxoCXaEQAvD_BwE&gclsrc=aw.ds)

[12V 5Amp Power Supply for the Track (connects to the motor shield)](https://www.amazon.com/LEDMO-Power-Supply-Transformers-Adapter/dp/B01461MOGQ/ref=redir_mobile_desktop?ie=UTF8&aaxitk=0jN3RieNiW-Jxn0JuJS6dQ&hsa_cr_id=2529139070101&ref_=sbx_be_s_sparkle_mcd_asin_0)

[9V 1Amp Power Supply for the Arduino](https://www.amazon.com/Arduino-Power-Supply-Adapter-110V/dp/B018OLREG4/ref=asc_df_B018OLREG4/?tag=hyprod-20&linkCode=df0&hvadid=198063088238&hvpos=&hvnetw=g&hvrand=14543638497706269076&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9009681&hvtargid=pla-318768096639&psc=1) There is a way to use your computer connection, a USB charger, or a separate 5V power supply also, please see [Power Supplies](../hardware/power-supplies.md) for options

[Raspberry Pi 4B](https://www.google.com/search?q=raspberry+pi+4&rlz=1C1CHVZ_enUS586US586&sxsrf=ALeKk00RT_osXNqIbJ_Xut4J5jqmo4mWjw:1592847200887&source=lnms&tbm=shop&sa=X&ved=2ahUKEwjNidyc-pXqAhXPct8KHdPXA9kQ_AUoAXoECAwQAw&biw=1230&bih=617#spd=3143731532782929925)

!!! NOTE 
    You may use your own computer instead of the Raspberry Pi. However, the image software below saves you installing software on your computer and does a lot more. See: "My Computer vs. Raspberry Pi" <insert link here> 

You can check Amazon, Ebay, AliExpress, Banggood, Adafruit, Sparkfun and others for all the above

#### Software

* [DCC++ EX Installer](https://github.com/DCC-EX/BaseStation-Installer/releases/tag/v2.1)
* [Steve Todd's Raspberry Pi Image (If you wannt to use a Pi)](https://mstevetodd.com/rpi)
* [JMRI (If you want to use a laptop or desktop)](https://www.jmri.org/)
* [Arduino Software IDE to edit and upload changes (Optional)](https://www.arduino.cc/)
* [WebThrottle-EX Controller](https://dcc-ex.com/throttles/webthrottle-ex/://)

!!! Note
     As mentioned above you can also use your existing computer (PC, Mac, Linux) instead of a Pi. You need a computer or Pi to run our WebThrottle-EX or JMRI and to connect to the Arduino to run your trains (the exception to this is by using the [WiFi Option](wifi-setup.md)). A computer or Pi is needed in any case because you are going to need one to download the installer. You will then use the installer to upload the program into the Arduino and copy the Raspberry Pi image (if you use one) to the MicroSD Card that goes in the Pi. NOTE: Alternately, you could install an ESP8266 WiFi Shield and use your mobile device as a controller using an app like Engine Driver.

#### Using an Uno

While we recommend an Mega, you can use an Uno. However, due to memory and other limitations on an Uno, all the options will not be available. For example, you can't have Ethernet with an Uno. For a more detailed comparison of features and what you can and can't do with an Uno, please see [Microcontroller: Which one do I need?](../hardware/microcontrollers.md)

#### Recap

This can be a little confusing, so let explain it a different way:

  1. You will need to build a command station with An Arduino and a Motor Controller and, optionally, an ESP8266 WiFi shield

  2. You will need a power supply connected to the motor shield to power your track and will need a separate source of power for the Arduino (or perhaps not, keep reading)

  3. You will need a computer and a USB cable to download software and then upload it to the Arduino. You may also want to download an SDCard image to use a Raspberry Pi instead of a computer to upload your Command Station software and run a controller.

  4. You will need a controller that sends commands to the CS and controls your trains. That controller can be any one of the following:

    1. A computer capable of running a Chromium based browser to use our WebThrottle-EX to connect to the CS via a USB cable. This computer does not need to be connected to the internet once you download the WebThrottle-EX files to your computer.

    2. A computer running JMRI. JMRI connects via the USB cable to the CS and you control your trains with the Throttles built into JMRI. You can also use the WiThrottle server built into JMRI to connect any WiThrottle compatible controller (such as the Engine Driver mobile app) via WiFi to JMRI and control your layout that way. 
    
    3. A Raspberry Pi as a computer. You can do any of the things mentioned in 1 and 2 above. With Steve Todd's image burned to an SDCard and installed in the Rasperry Pi, JMRI, the WiThrottle Server with networking, and more is installed and running when you boot. You still need a USB cable to connect the Pi to the CS.

    4. If you install an ESP8266 WiFi Shield, you don't need a computer or a Pi if you don't want it once you upload the software to the Arduino. You can connect directly to the CS via WiFi using any WiThrottle compatible controller such as Engine Driver running on a WiFi device like your mobile phone.

!!! Note
The computer USB port in option 1, 2, or 3 may be able to be the power supply for the Arduino (but you will still need a 12-14V DC power supply for the motor shield) See [Power Supplies](../hardware/power-supplies.md)) for information on how to choose the right power supplies and different ways you can power the Arduino.


<insert graphics showing all the possible connections>

Next Page: [Assembly](assembly.md)
