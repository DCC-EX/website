# Command Station API

The DCC++ EX System consists of a DCC++ Library and a Command Station program (or sketch in Arduino terms) that runs your Command Station. The library has its own application programming interface (API) that allows you to write your own version of a Command Station and to easily interface with DCC++ EX. The Command Station software itself uses the API functions to run your trains. Here is an example of how it works.

## Commands List

### General configuration and status functions

getStatus()

getPreamble()

### Waveform Control Functions

setPower()

setSignal()

setBrake()

NOTE: Work in progress. There are many more API functions

