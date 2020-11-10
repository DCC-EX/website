# Motor boards

There are many motor boards available to use with DCC++ EX. Also called "Dual-H Bridges" and "Motor Shields". Some require a little work, but others are mostly plug and play.

!!! Note
    We recommend the Arduino Motor Shield R3 or a supported clone board like the Deek-Robot ($15 US).


![Deek Robot Motor Shield](../images/deek_robot1_sm.jpg)


## Boards currently supported

* Arduino Motor Shield R3
* Deek-Robot Motor Shield
* DIY More L298HN Motor Shield
* LMD18200 Motor Driver Module
* Pololu MC33926 Motor Shield
* LMD18200 Based Motor Boards
* BTS7960 Based Motor Boards

There are other boards, some requiring modification, which are covered in the advanced section.

## But I saw this board, will it work?

This is a checklist for what your motor controller needs to work with DCC++ EX:

* A dual H-Bridge (one for MAIN and one for PROG)
* Handle enough current for the layout (most boards support 2 Amps, enough for 3-5 locos)
* Have working current sense (many do not)
* Be able to allow our fast switching speeds (some do not)
* Plug on shield to eliminate wiring (optional feature)

## Work with little or no modification (Conductor friendly)

* Arduino Motor Shield R3
* Deek-Robot Motor Shield

## Need a little tinkering (Tinkerer path)

The following are not shields, they are discrete boards. You will need to connect them with wires.

* LMD18200
* BTS70960 - The "IBT_2" board. This board also has separate direction pins, so after selecting the correct motor board type in the config.h, it will use one more of the Arduino's pins.
* L6201P/6203

## Need more modification (Engineer path)

* "Beeper Board" - You have to lift two traces and solder 2 resistors and use 2 jumpers.
* Velleman KA03 (kit) VMA03 (soldered) - Must cut traces and solder resistors to get current sensing. Pin assignments must be added to a new motorboard entry in the config.h file.
* Pololu MC33926 - While we have a motor board type for this board, the current sense is not acceptable. We recommend using an external current sense board like the MAX471

## Boards that are NOT compatible for use with DCC

* VNH2SP30 - Sparkfun Monster Moto and other boards from China based on this chip. It can't switch fast enough to generate a reliable DCC signal
* IFX9202ED - Infineon Dual H-Bridge. Can't switch fast enough.
