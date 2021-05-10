# mcu-pinouts

Collection of human and machine readable text files describing the pin mappings of MCUs (ATTiny, ATTmega, PIC, ESP32, etc.): what pin has which functions

This is work-in-progress...

# Structure

The folder structure should be:

- company 
    - device
      - pins.txt
      - pckg-xxx.txt
      - arduino.txt

### Example:

```
- Atmel
  - ATTiny841
    - pins.txt
    - ...
```

# Files

## pins.txt

A tab-seperated (`\t`) document with the following columns:

  - pin name
  - functions (comma seperated)
  
### Example:

```
PA0\tPCINT0,ADC0,AREF,MISO
PA1\tPCINT1,ADC1,AIN00,TOCC0,TXD0,MOSI
```
  
## pckg-xxx-yy.txt

Text-document that maps pin numbers (aka line numbers) of a package (DIP, SOIC, TQFP, VQFN, …), with `yy` pins, to pin names.

Not connected pins are kept empty or contain `NC`, `N.C.`

### Example:

```
VCC
PB0
```

## arduino.txt

(*Optional*)

A tab-seperated document that maps pin-names to arduino pin numbers.

### Example:

```
PA0\t10
PA1\t9
```

# Guidelines

- Inverted pins are prefixed with a `/` (slash)
- Power lines are `VCC` and `GND`

# TODO

- [ ] how to handle multiple names (ATTiny441/841)?
- [ ] how to describe configurations (pin-mappings, etc.)?
- [ ] describe technical parameters? (info.txt?)
