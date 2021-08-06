
![ESP32-CAM-Station](https://user-images.githubusercontent.com/87124512/128458189-07f76a66-cc20-4097-8450-c3829fe58a46.png)


1- set the ESP32 as an access point

2- Customize the SSID and Password:

const char* ssid = "ESP32-Access-Point";
const char* password = "123456789";

3- Set the ESP32 as an access point from the setup() using the softAP() method:

WiFi.softAP(ssid, password);

4- Get the access point IP address using the softAPIP() method and print it in the Serial Monitor:

IPAddress IP = WiFi.softAPIP();
Serial.print("AP IP address: ");
Serial.println(IP);

5- Connect to the ESP32 Access Point:

To connect to the access point on your computer, go to the Network and Internet Settings and select the “ESP32-Access-Point“.

![esp32-access-point-pc](https://user-images.githubusercontent.com/87124512/128458485-49ddce1d-acb2-4c36-b6bb-f54b66b83777.png)


Insert the password you’ve defined earlier.

![connect-access-point-pc](https://user-images.githubusercontent.com/87124512/128458507-95b4e466-3a2e-4530-8b9d-cab2e4c4e585.png)
