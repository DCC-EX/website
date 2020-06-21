# Power Supplies

The power supply is one of the most important parts of your setup. You need to select a clean, filtered power supply that can supply at least the amount of current required by your motor drivers. 

## Voltage

N and Z scale layouts should run at at about 12V to avoid damage to the motors. See this thread to learn more about the pros and cons of running at higher voltages: https://www.trainboard.com/highball/index.php?threads/dcc-voltage-and-n-scale-locomotives.56342/

Most larger scales will run higher voltages. For reference, the Digitrax systems put the rails at around 14V. Do some homework to determine what voltage is best for your system.

## Amperage

You'll need to be able to supply 3A per channel to the tracks on which you intend to run trains, assuming you're using the Arduino motor shield or Pololu motor shield. For larger motor driver shields, you'll want a larger power supply.

## Recommended Power Supplies

- Wall warts are a good choice for beginners and those not comfortable with mains wiring. *TODO: Add recommended wall warts*
- The Meanwell LRS-100-15 power supply is a good choice for larger scales. It supplies 15V and 105W (that's 7 amps), so it is plenty for running two channels simutaneously. At only $18, it is a cheap option.
  - You'll need to do your own mains wiring, if you don't have experience with this get a friend who does or hire an electrician to do it for you. MAINS POWER IS DANGEROUS.
  - https://www.digikey.com/product-detail/en/mean-well-usa-inc/LRS-100-15/1866-3313-ND/7705005