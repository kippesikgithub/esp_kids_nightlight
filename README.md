# ESP WLED Nightlight / Sleeptrainer
ESP WLED driven, integrated in Home Assistant, Nightlight / Sleeptrainer, to help the toddlers when they have to be 'In bed' or when they are allowed to come 'Out of bed'.  
Giving you or the toddler the ability to choose every light color available (even different ones for open and closed eyes), controll the light manual, and automate the light based on datetime helpers in Home Assistant.  
![image](https://github.com/kippesikgithub/esp_kids_nightlight/assets/100353268/b9dae179-6cb1-4d85-9185-682a2aa91dea)
![image](https://github.com/kippesikgithub/esp_kids_nightlight/assets/100353268/044eaf4b-2680-4f82-8fa0-32f2fb62c527)
![image](https://github.com/kippesikgithub/esp_kids_nightlight/assets/100353268/16167580-d81c-400a-beb6-447158b5ab55)


#### Requirements
ESP board (esp8266 or esp32 based)  
2x 3 WS2812 Leds  
USB (micro or usb-c) for connecting to power source  
3d Print the housing https://www.printables.com/model/625681-nightlighttoddler-clockok-to-wake-lightsleep-train (created by rparish_1262093, thanks!)  
note: I dont use the setup (internals) that the original creater has on the printables article, since I want the ability to choose every possible color, and had some strips of ws2812b leds laying around, waiting for a purpose.    
## How To create
- Print the housing from the link provided on Printables  
- Flash WLED firmware on the ESP chip of your choise, and connect it to your WIFI  
- Connect/Solder 2 strips (or 1 strip, and create segments in WLED) to your ESP chip on your favorite GPIO port  
- Place the ESP and ledstrips into the housing like on the picture below (I used ledstrip diffuser strips to create a nice surface to put double sided tape behind)  
![image](https://github.com/kippesikgithub/esp_kids_nightlight/assets/100353268/7f787ed2-508f-4db0-bd42-5ef298da0aab)  
1: ESP Board (used an Wemos D1 mini esp8266 based)  
2: 2 x 3 WS2812B Leds (or create one string and create segments in WLED)  
3: Usb powerconnector of the ESP, used to power the project (on the back of the light)  
- Create Segments out of the upper and lower led strips, so you can controll them separately  
- Connect the usb (usb-c or micro-usb) Power on the back of the Light (into the esp)  
![image](https://github.com/kippesikgithub/esp_kids_nightlight/assets/100353268/05f606d3-38ad-4dd0-889f-0aa93d2951a3)  
- Integrate the WLED light into your Home Assistant environment  
- Create to DateTime helpers for 'In Bedtime' and 'Out of Bedtime'  
- Create some flows in Node Red or Home Assistant Automations to turn on or off the upper of lower part of the light  
- Create a Home Assistant Card for controlling the light manually and setting the helpers for 'In Bedtime' and 'Out of Bedtime'  
![image](https://github.com/kippesikgithub/esp_kids_nightlight/assets/100353268/3b8c5334-b40a-4f48-a857-741b47420682)  
Create Segments in WLED firmware
![image](https://github.com/kippesikgithub/esp_kids_nightlight/assets/100353268/0d30ec03-53e9-48bc-a2e7-03021004e06c)
