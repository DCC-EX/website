# Motor boards

There are many motor boards available to use with DCC++ EX. Also called "Dual-H Bridges" and "Motor Shields". Some require a little work, but others are mostly plug and play.

!!! Note
    We recommend the Arduino Motor Shield R3 or a supported clone board like the Deek-Robot ($15 US).


![Deek Robot Motor Shield](../images/deek_robot1_sm.jpg)


## Boards currently supported

* Arduino Motor Shield R3
* Deek-Robot Motor Shield
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

## Work with little or now modification (Conductor friendly)

* Arduino Motor Shield R3
* Deek-Robot Motor Shield

## Need a little tinkering (Tinkerer path)

The following are not shields, they are discrete boards. You will need to connect them with wires.

* LMD18200
* BTS70960

## Need more modification (Engineer path)

* "Beeper Board" - You have to lift two traces and solder 2 resistors and use 2 jumpers.

## Connecting your motor shield

 **** coming soon ****