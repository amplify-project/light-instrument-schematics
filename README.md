# Light Instrument Schematics

This repository contains the schematics for the eletronics that are used to
power the AMPLIFY Light Instruments.

The repository is organised as follows:

- `debouncer/`: A hardware switch debouncer based around a 555 timer IC. Used
  in the key instrument.
- `imu-shaker/`: A revised version of the schematic found in `tiltswitch/`,
  based around a Seeed XIAO ESP32-S3 and a MPU-6050 or MMA8451 IMU instead of a
  tiltswitch for activity detection on any axis.
- `input/`: A simpler version of the schematic found in `multiplexer/` with a
  fixed number of three ports, obviating the need for the multiplexer IC.
  Used in the touch instrument.
- `multiplexer/`: A board for connecting up to 8 sensors to a Seeed XIAO
  ESP32-S3 through a CD4051BE analog multiplexer. The number of channels can be
  selected with a dip-switch.
- `rainstick/`: A board fitted with a Seeed XIAO ESP32-S3, a photodiode and two
  infrared LEDs. The LEDs and the photodiode form an IR-barrier, which when
  broken is measured as an analog signal, thereby detecting the moving of
  percussive media inside the rainstick instrument.
- `receiver/`: A board fitted with a Seeed XIAO ESP32-S3 and Molex 436500300
  connectors for connecting up to four WS2812B LED strips, acting as a receiver
  for LED commands.
- `tiltswitch/`: Schematic for a board to be integrated into a maraca, based
  around a Seeed XIAO ESP32-S3 connected to a tilt switch to detect the shaking
  of the maraca.
- `vibration_detector/`: A circuit for detecting vibrations by means of a
  piezoelectric element. Filters and thresholds the signal from the
  piezoelectric element through an operational amplifier so it can be safely
  measured by a microcontroller.
