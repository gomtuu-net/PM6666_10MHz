# 10MHz OCXO for Philips/Fluke PM6666 counter
Alternative 10MHz oscillator for Philips/Fluke PM6665 and PM6666 frequency counters.

[Created with KiCAD ver. 7.0.11](https://kicad.org)

## Design ideas
* fuse/PTCC
* Vref with trim-pot for fine tune (Vc xtal: 0-4V)
* DC-DC conv (12V-to-5V)
* LCD-backlight power & trim-pot
* jumper to choose always-on or power-switch 
* SMA and Vref test-point
* 4 mount holes for alternative use
* status LED after fuse/DC-DC conv.
- temp.sensor under/near OCXO (LM35/DS18b20)
- Window-comparator with warm/cold LED indicator
- filter/circuit to convert square to sine-wave
- freq. divider
* currently usable OCXO: CTI OSC5A2B02 / NDK ENE3311B
- allow multiple footprints to fit other OCXO (ISOtemp/Vectron)

## Issues/todo
- Pk-Pk voltage from OCXO to high, need 470 load resistor
- change diameter hole for OCXO (0.8mm is to narrow)
- update/correct footprint thp Elco's (47uF & 100uF)
- improv. Vref tuning (20-turn trim-pot?)
- add solder-jumper to seperate 10MHz signal (antenne!)
- power-on LED at better location
- update part marking (pin.1, +, etc)


MHz.kHz.Hz
010.000.000
123.456.789

## Possible voltage references
- ADR4540| 4.096V| 2ppm| Vin: 4.2 - 15V
* LM4140| 4.096V| 3ppm| Vin: 5V
- LT1019-5| 5.000V| 5ppm
- LT1021| 5.000V| 5ppm| Vin: >10V
- MAX874| 4.096V| 20ppm| Vin: 4.3 - 20V
- MAX6070AAUT| 4.096V| 6ppm| Vin: 4.3 - 5.5V
- MAX6194A| 4.500V| 5ppm| Vin: 5 - 12.6V
* MAX6198A| 4.096V| 2ppm| Vin: 5 - 12.6V
- MAX6241| 4.096V| 5ppm| Vin: 8 - 36V
- MAX6341| 4.096V| 2.5ppm| Vin: 8 - 36V
- MAX6250BESA| 5.000V| 7ppm|	
- REF5040| 4.096V| 3ppm| Vin: 4.3 - 18V

