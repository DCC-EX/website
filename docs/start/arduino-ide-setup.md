# Basic Setup using the Arduino IDE

The Arduino IDE is an "Integrated Development Environment". Don't let the name scare you away from giving it a try, it is really just a program that lets you open a project, like our DCC++ EX Software files, compile them into instructions the Arduino understands, and uploads them from your computer into the Arduino using a serial cable. It is extremely easy to use. If you are a Tinkerer or an Engineer (See [levels/path choice](levels.md)), You may want to make changes to the code or just learn more about how the Command Station software works. At a minimum, you may need to change options in the config.h file or use the IDE's "Serial Monitor" to monitor your CS, get logs if something is not working, or enter commands to test out features.

## Download and install the Arduino IDE

Rather than go into details that are already covered in great detail on the Arduino web page, just follow the instructions in the following link and then return here.

[Arduino IDE Guide](https://www.arduino.cc/en/Guide)

## Download the DCC++ EX zip file

Use the link to either the zip or tar file at the botom of our Github page here:

[DCC++ EX Download Page](https://github.com/DCC-EX/CommandStation-EX/releases/tag/v3.0.0)

## Unzip the file into the Arduino IDE project folder

Find the location to where you downloaded the zip file (usually the "downloads" folder) on your computer and unzip it to the Arduino projects folder, called the "sketchbook folder". Arduino likes to call "programs" "sketches". The default name of the Sketchbook folder is “Arduino” and the default location of the Sketchbook folder is in the “My Documents” folder (or just “Documents” for Mac users).

Make sure the path is correct. You should now have a ``<documents/arduino/CommandStation-EX>`` folder with the entire DCC-EX project inside it.

## Copy the config.example.h file or rename it

DCC-EX provides you with an example configuration file. This file holds settings that you can change for things like your choice of motor controller, Wifi login credentials, etc. Rather than a future update potentially have you lose any changes you make to your configuration, we give this file a different name and leave it up to you to edit if you need to. Therefore, copy this file and name it's clone "config.h" or simply rename this file to "config.h".

## Run the Arduino IDE Program

Find the Arduino IDE program on your Start Menu/Mac Finder, etc. and open the application. You will see this screen:

![Arduino IDE](../images/arduino-ide/arduino_ide.jpg)
<br>
Figure 1 - Arduino IDE

## Open the CommandStation-EX Project

Choose "File -> Open" from the menu to open the file manager.<br>


![File Open Menu](../images/arduino-ide/file_open.jpg)
<br>
Figure 2 - File Open Menu

<br>
Then click on the "CommandStation-EX" sketch folder to open it. Scroll down to the "CommandStation-EX.ino" file (It should have the round, blue Arduino logo on it) and open that file. We also provide example .ino files for those Tinkerers or Engineers who want to use optional features like the "User Command Override" feature, high current motor boards, etc. But for now, and for most users, this will be all you need
<br>

![Find the CommandStation-EX.ino File](../images/arduino-ide/commandstation-ex.jpg)
<br>
Figure 3 - Find the CommandStation-EX.ino file

## Install the DIO2.h Library

From the "Tools" menu, select "Manage Libraries". It may take a few seconds for it to load the list of all the libraries. Libraries are shared pieces of code that can be used by sketches to add functionality without someone having to write them from scratch. Type "DIO2" into the search box. You should then see a box below with "DIO2" by Thierry Paris of Locduino. Click "Install" to install this library. After it installs, close the libary manger window and go back to the main window.

![Find the DIO2.h Library](../images/arduino-ide/library_manager.jpg)
<br>
Figure 3 - Find and install the DIO2.h Library

## Edit the config.h file (optional)

If you are using the standard Arduino Motor Shield and if optionally using one of the supported Wifi boards and want to connect directly to the Command Station in Access Point Mode (AP) from your WiFi controller <link here to wifi controllers page>, there is nothing to do! Just upload the software to the Command Station in the next step.

If you are using a different motor shield or motor controller board or if you wish to connect your CS to your home network instead of having a separate access point, click here for more detailed instructions on how to edit your config.h file <add a link here>.

If you want to take a look at this file or make a simple change, just open the file and take a look. You should see many files open in tabs at the top of the IDE Window. Find the down facinng triangle near the upper right of the window and click on it to open the entire list of files. Scroll down to near the bottom and click on the "config.h" file you renamed in the previous step to open it in the editing window. If you are sure of your changes, make sure to click on "file -> save" from the top menu to save them.

## Select the board type and com port

Before you attempt this step, make sure that you have everything connected properly from the [assembly page](assembly.md). And a final reminder to make sure you cut the Vin trace on the bottom of the Arduino Motor Shield. Ready? Then proceed.

Connect the computer to the Arduino with the USB cable. Note the 5V coming from your computer/raspberry Pi is enough to power the Mega temporarily since it bypasses the regulator that converts your 7-9V power supply down to 5V and goes right to the 5V bus on the board. So don't be alarmed by lights on your Arduino.

From the "tools" menu select the "board" menu, then "Arduino AVR boards", and then "Arduino Mega or Mega 2560". 

![Select Arduino Mega](../images/arduino-ide/board_type_mega.jpg)
<br>
Figure 4 - Select your board type

Then select "Processor" and make sure it says "ATMega2560"

Last, select "Port" and find the port on your computer that recognizes the Arduino. If you don't see a port listed there and are using a clone board, you may have to install a driver for a CH340 USB chip that is on these boards. See here [Drivers for the CH340](https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all)

![Select the COM Port](../images/arduino-ide/board_port_mega.jpg)
<br>
Figure 4 - Select the correct COM Port

## Upload the software

We are finally ready for the last step that will complete your Command Station. Click on the upload button near the top left. If is a circle with a right arrow next to the compile button that looks like a check mark.

![Upload the CS Software to the Arduino](../images/arduino-ide/upload_arrow.jpg)
<br>
Figure 3 - Upload the CS Software to the Arduino

The IDE will go through a compile process which will build all the files into an application the Arduino can run and upload it. You may see many lines of logging as it finishes its task. When done, it will upload the file to the Arduino which you may see as some lights blinking on the Arduino. Make sure there are no errors in the log window and that it shows "done uploading" in the status bar and  "SUCCESS" and a listing of how much memory is used on the Arduino in the log window. If you see errors, try our troubleshooting steps here <link> or contact us on Discord <link>.

Don't unplug the serial cable yet!

## Plug in your power adapters

You should already have the 7-9V adapter plugged into the Arduino and the 13-14V adapter plugged into the motor shield. Now you can plug both of them into the power socket. Nothing should happen. Be sure that nothing bad happens like smoke escaping from your CS. If anything seems wrong, unplug the power adapters immediately.

## Use the Serial Monitor to do a quick test

The Arduino IDE has a built in serial monitor. That means that in addition to uploading updates to your Command Station, we can interact with the Command Station. Select "Tools -> Serial Monitor". Or click on the "serial monitor" icon near the upper right of the window.

![Open the Serial Monitor](../images/installer/arduino_ide2.jpg)
<br>
Figure 8 - Open the Serial Monitor

Make sure the baud rate at the lower right of the window is set to "115200". Make sure the dropdown next to that says "Both NL & CR". That makes sure you send a new line command and carriage return which the Arduino expects.

![Serial Monitor](../images/installer/serial_monitor.jpg)
<br>
Figure 9 - Serial Monitor

You should see log information immediately display in the window. If you have a Network shield or WiFi shield connected, you will see the CS setup its AP or connect to your network if you gave it your credentials. If you don't have a network, that's fine, the CS will sense that, the network test will fail, but everything else will be working as it should.

# Type in a command or two

There is an entire language that DCC-EX understands. We call this the DCC-EX API for "Application Programming Language". If you are interested, the list of all the commands is here in the [DCC++ EX Wiki](https://github.com/DCC-EX/CommandStation-EX/wiki). Let's just try two commands to make sure everything is working.

All DCC-EX commands begin with a less than sign and end with a greater than sign. In the command window, type ```<1>``` and press the ```send``` button. Power should come on to the main track. You should see 2 red leds light on the "A" power output. If not, try the troubleshooting steps here <insert link here>

Now enter ```<s>```. That is a lowercase "s". You should see status information for your command station appear in the log.

Turn off the power to the track by sending ```<0>``` to the CS. That is a "zero".

__Exit the Arduino IDE software__.

# Run you trains!

Making sure power is off to your track, place your DCC enabled loco (not DCC ready! Ready just means it has the plumbing inside the loco to install an optional DCC decoder, but it is NOT yet DCC compatible). Now either download our WebThrottle-EX found here [WebThrottle-EX](../throttles/webthrottle=ex.md) and run it in your browser, or run it directly from our web page. Follow the instructions on that page to enable chromium "experimental features".

The rest of the instructions show you how to use WebThrottle-EX. You should be able to find the CS by its serial port and enable it, then turn on the track power, then acquire your loco by its ID. After that, you should be able to use the throttle slider and function buttons to operate you locomotive!

You can also watch the [WebThrottle-EX Video](https://www.youtube.com/watch?v=BkgsEOjxWaU) by clicking the hyperlink in this sentence.

NEXT: Test with WebThrottle-EX [WebThrottle-EX Page](../throttles/webthrottle-ex.md)

link to using WiFi and Engine driver - coming soon

link to using JMRI - coming soon