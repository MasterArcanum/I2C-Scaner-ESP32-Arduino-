# I2C Scaner (ESP32 Arduino)
This repository contains a simple but essential Arduino sketch used for scanning I2C devices connected to an Arduino board. The script systematically checks each address on the I2C bus and reports back the addresses of any devices found. This is particularly useful for troubleshooting or setting up a project where the I2C address of the components is unknown or needs to be confirmed.

<h2>Description</h2>
The sketch initializes the I2C communication and serial connection, then scans through the I2C addresses from 1 to 126. If a device responds at an address, the script prints the address to the Serial Monitor. It's a quick and efficient way to verify the connections and addresses of I2C devices like sensors, displays, and input devices.

<h2>How to Use</h2>
Upload the Sketch: Load this sketch onto your Arduino board using the Arduino IDE or your preferred development environment.

Open Serial Monitor: After uploading, open the Serial Monitor with a baud rate of 115200.

View Results: The scanner will output the results, displaying the addresses of any detected I2C devices.

Troubleshooting: If no devices are found, it will report "No I2C devices found." In this case, check your connections and ensure that your devices are powered.

<h2>Code Explanation</h2>
Wire.begin(): Initializes the I2C communication.
Serial.begin(115200): Begins serial communication at 115200 baud rate.
Wire.beginTransmission(address): Starts transmission to the I2C device at the specified address.
Wire.endTransmission(): Ends the transmission and checks if the device acknowledges.
Serial.print(): Prints the address of any detected device to the Serial Monitor.
<h2>Notes</h2>
Ensure your I2C devices are correctly connected with the right pull-up resistors if needed.
This sketch is compatible with most Arduino boards and I2C devices.
<h2>License</h2>
This project is open source and available under the MIT License.
