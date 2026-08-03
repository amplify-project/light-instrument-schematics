# Light Instrument Schematics

This repository contains the schematics for the eletronics that are used to
power the AMPLIFY Light Instruments.

The repository is organised as follows:

- `debouncer/`: A hardware switch debouncer based around a 555 timer IC. Used
  in the key instrument
- `vibration_detector/`: A circuit for detecting vibrations by means of a
  piezoelectric element. Filters and thresholds the signal from the
  piezoelectric element through an operational amplifier so it can be safely
  measured by a microcontroller.
- `multiplexer/`: A board for connecting up to 8 sensors to a Seeed XIAO
  ESP32-S3 through a CD4051BE analog multiplexer. The number of channels can be
  selected with a dip-switch.
