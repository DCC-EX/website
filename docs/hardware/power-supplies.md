# Power Supplies

The power supply is one of the most important parts of your setup. You need to select a clean, filtered power supply that can supply at least the amount of current required by your motor controllers. 

## Do I need two power supplies?

Both your microcontroler (the Arduino) and the motor controller need power. While we recommend a 9 Volt, 1 Amp, DC power supply for the microcontroler, there are other ways to power it. The voltage to the motor controller does not change, you need the correct voltage and amperage for your guage and layout.

#### Three ways to power the Arduino

Barrel Connector - This is where we can connect our 9V supply. This requires two power supplies, one for the Arduino and a separate one for the motor controller. The power goes through a voltage regulator on the Arduino and converts the 9V to the 5V the board can use.

Vcc pin - 

USB Connector - If you always will have a computer connected to your Command Station (for example when using JMRI), the 5V from your computer can power it. You won't need another power supply. Most USB ports can only supply 500 milliamps, so be careful about adding anything that will draw current from the CS. A motor shield, a wifi shield and a fan that draws 50mA should be fine. Even if you don't have a laptop, you can use a 5V, 1A USB power supply like a phone charger and connect it to the USB port.

5V pin - You can connect a good quality 5V power supply directly to the 5V pin and ground. This bypasses the voltage regulator on the board which means you can use more current. We recommend a 5V, 1A power supply. Since there are many dual-voltage power supplies on the market, you can use one power supply with two outputs.

## Voltage

N and Z scale layouts should run at at about 12V-14V to avoid damage to the motors. See this thread to learn more about the pros and cons of running at higher voltages at this [Trainboard Thread](https://www.trainboard.com/highball/index.php?threads/dcc-voltage-and-n-scale-locomotives.56342/) Another good link (along with just about anything written by Mark Gurries, is here: [Mark Gurries - Choosing the Right Booster](https://sites.google.com/site/markgurries/home/technical-discussions/boosters/choosing-the-right-booster)

Most larger scales will run higher voltages. For reference, the Digitrax systems put the rails at around 14V. Do some homework to determine what voltage is best for your system.

## Amperage

You'll need to be able to supply 3A per channel to the tracks on which you intend to run trains, assuming you're using the Arduino motor shield or Pololu motor shield. For larger motor driver shields, you'll want a larger power supply.

## Recommended Power Supplies

- Wall warts are a good choice for beginners and those not comfortable with mains wiring. You can get a 12V, 3A, relatively small one for around $8 US. 

![12V Wall Wart](../images/12v-3A-wall-wart-sm.jpg)

- You can also find plenty of laptop type "brick" power supplies. They come in ranges from 12V to 18V and 3-5 Amps.

![12V 3A Brick Power Supply](../images/12v-3A-brick.jpg)

- The Meanwell LRS-100-15 power supply is a good choice for larger scales. It supplies 15V and 105W (that's 7 amps), so it is plenty for running two channels simutaneously. At only $18, it is an inexpensive and solid option.

![Meanwell](../images/meanwell-lrs100.jpg)

https://www.digikey.com/product-detail/en/mean-well-usa-inc/LRS-100-15/1866-3313-ND/7705005

  - You'll need to do your own mains wiring, if you don't have experience with this get a friend who does or hire an electrician to do it for you. MAINS POWER IS DANGEROUS.