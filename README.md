# IOT LED Example

This example is prepared for Introduction to Computers and Informatics course of TTU Cyber Security Engeneering

This example was created and tested on an ESP32, creating a toggle for an LED connected on a pin (pin 5 in this case),
it is controlled via a web browser

Details: https://wiki.itcollege.ee/index.php/Category:I600_Introduction_to_Computers_and_Informatics#Assignment:_Set_up_basic_IoT_scenario

## Requirements
* Python 3.x

## Running

First clone the repository to your computer via Git. Following commands are for Linux and Mac.
```sh
git clone https://github.com/aadityaparashar/led-iot
cd led-iot
```

### On your machine

Run `main.py` like
```sh
python main.py
```
then browse to http://localhost:8080/

### On ESP32

To transfer the boot and main files from your home folder to the ESP32, use:

ampy -p /dev/ttyUSB0 put main.py
ampy -p /dev/ttyUSB0 put boot.py

NB! Upload the main.py before boot.py , as in some cases the boot.py causes issues with the serial connection (after it connects to the wifi)
