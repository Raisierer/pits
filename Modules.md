# Modules (Threads) of PITS

## Main Thread

## GPS Thread

### Datatypes

- gps_info: Holds hardware information

### Functions

- OpenGPSPort: Sets GPS-Info
- BitDelay: Sleep for some bits
- CloseGPSPort: Closes connection and releases hardware
- I2CClockHigh: Tries to set clock pin to input, timeout when unable
- I2CClockLow: Sets clock pin to output
- I2CDataLow: Sets data pin to output
- I2CDataHigh: Sets data pin to input
- BusIsFree: Check if bus is free
- I2CStart: Readies for data transmission
- I2CStop: Ends data transmission
- I2CSend: Send one byte of data
- I2CRead: Read one byte of data
- I2Cputs: Send an array of bytes
- I2Cgetc: Read one byte from GPS
- GPSChecksumOK: Returns checksum status
- FixUBXChecksum: Repairs checksum (?)
- SendToGPS: Send data to GPS
- SetFlightMode: Set GPS mode (pedestrian or flight)
- SetPowerMode: Set powermode of GPS module
- setGPS_GNSS: Set GNSS (?)
- setGPS_DynamicModel6: Set dynamic model of GPS module
- FixPosition: (?)
- day_seconds: (?)
- ProcessLine: Calculate flight path

### Thread program

1. Initialize hardware (GPS)

2. Loop:

   1. Open GPS
   2. Create Message
      1. Read character from GPS
      2. Compare if character is:
         - Wait key -> wait
         - \$ -> Set first character of message
         - any other -> write to next free position in message
   3. Close GPS

## APRS Thread

## LoRa Thread

## DS18B20 Thread

## ADC Thread

## Camera Thread

## LED Thread

## Log Thread

## BMP085 Thread

## BME280

## MS5611

## Pipe Thread

## Prediction Thread
