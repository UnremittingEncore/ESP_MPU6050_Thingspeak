# ESP32_MPU_6050 Data Uploaded on ThingSpeak cloud

## ThingSpeak
- ThingSpeak is an open data platform for the Internet of Things with MATLAB analytics and visualization
- ThingSpeak offers free data storage and analysis of time-stamped numeric or alphanumeric data. Users can access ThingSpeak by visiting http://thingspeak.com and creating a ThingSpeak user account.
- ThingSpeak stores data in channels. Channels support an unlimited number of timestamped observations (think of these as rows in a spreadsheet). Each channel has up to 8 fields (think of these as columns in a speadsheet). Check out this [video](http://www.mathworks.com/videos/introduction-to-thingspeak-107749.html) for an overview.
- You can visualize and do online analytics of your data on ThingSpeak using the built in version of MATLAB, or use the desktop version of MATLAB to get deeper historical insight. Visit https://www.mathworks.com/hardware-support/thingspeak.html to learn more.
- Libraries and examples for Particle devices can be found here: https://github.com/mathworks/thingspeak-particle

## Project Overview
- Uploading data from the MOCAP sensor onto the cloud (ThingSpeak or AWS). In addition, add a GATE authentication system to the sensor for better digital security
- We use Server-Sent Events to update all the readings
- The 3D object is created using a JavaScript library called [three.js](https://threejs.org)

## Update Network Credentials & Connection Details (in secrets.h file)
```
#define SECRET_SSID "MySSID"    // replace MySSID with your WiFi network name
#define SECRET_PASS "MyPassword"  // replace MyPassword with your WiFi password

#define SECRET_CH_ID 000000     // replace 0000000 with your channel number
#define SECRET_WRITE_APIKEY "XYZ"   // replace XYZ with your channel write API Key
```
## Accesible Operations

* **ReadField:** Reading from a public channel and a private channel on ThingSpeak.
* **WriteSingleField:** Writing a value to a single field on ThingSpeak.
* **WriteMultipleFields:** Writing values to multiple fields and status in one transaction with ThingSpeak.
* **ReadMultipleFields:** Reading values from multiple fields, status, location, created-at timestamp from a public channel on ThingSpeak
* **SecureConnect:** Using the above features and connecting securely to ThingSpeak.


## Useful Links
- https://randomnerdtutorials.com/esp32-mpu-6050-accelerometer-gyroscope-arduino/
- https://github.com/mathworks/thingspeak-arduino

 
