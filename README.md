# 3-tier-architecture-temperature-and-humidity-IoT-based-system.



 
 
I have decided to implement a 3-tier architecture temperature and humidity IoT based system. The have used IoT hardware in this project which includes raspberry Pi 3 model b+, sensor temperature and humidity sensor, Arduino uno R3.


 
 ![image](https://user-images.githubusercontent.com/32312941/114443312-66578e80-9b82-11eb-8f5e-70792ae86fd4.png)

 
Fig 3: Arduino, sensor, and raspberry pi 3 set up
 
It is a three-tire, the first layer is the user interface. When the user turns on the system and run the program. It requires Wi-Fi connection. It has to be set by the client in the Arduino application by modifying the Wi-Fi name and password. The second layer is the functional logic in python. Where it connects to mqtt client, mqtt login and password is required. The third layer is the storage layer, where I used to get data through the api key I created on Thinkspeak.
I use the Arduino micro-controllers as satellites in my home where in the center is the Raspberry Pi in a server rack.
The first step is to set up the publisher so I could test that the temperature and humidity is read correctly and published to the network via MQTT.

![image](https://user-images.githubusercontent.com/32312941/114443411-80916c80-9b82-11eb-950d-54366394f088.png)


Fig 4: used Arduino temhum file to get this output
 
The publisher part 1 finished that the temperature and humidity are stored in a variable and printed to the serial. In this part 2 we establish the WiFi connection to the home network and send the data as payload via the MQTT protocol to the broker.
![image](https://user-images.githubusercontent.com/32312941/114443472-92730f80-9b82-11eb-9fe7-7591f01a478f.png)


Fig 5: Wi-Fi connected and showing temp and humidity frequently, run Arduino Wi-Fi file to get this output.


![image](https://user-images.githubusercontent.com/32312941/114443506-a0289500-9b82-11eb-899e-43b4b032f49d.png)

Fig 6: the system showing the temp and humidity of living room.
 
I have used Thinkspeak to collect data from Arduino. It saves data, where you can see the average to temperature, average of humidity.
 ![image](https://user-images.githubusercontent.com/32312941/114443574-b33b6500-9b82-11eb-8b9a-070e92462ba4.png)

