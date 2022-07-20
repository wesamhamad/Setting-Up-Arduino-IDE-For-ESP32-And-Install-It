# Setting Fp Arduino IDE For ESP32 And Install It
<p align="center">
  <img width="460" height="300" src="https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2018/08/ESP32-DOIT-DEVKIT-V1-Board-Pinout-30-GPIOs-Copy.png?resize=828%2C492&quality=100&strip=all&ssl=1">
</p>

## What is ESP32 And The Advantages of using It Compared To Arduino Modules?
ESP32 is a series of low-cost power systems on a chip microcontroller. The ESP32 is an advanced version of the ESP8266 series. The ESP32 series is created and developed by Espressif Systems. The ESP32 have dual-core and Ultra low power co-processor. It was developed for the lack of security, which was in ESP8266

#### Advantages:  

- ESP32 offers you dual-core 160MHZ to 240MHZ.
- You can control and monitor your device with the help of Wi-fi or Bluetooth at a very low price.
- ESP32 offers you more GPIOs.
- ESP32 gives you a high speed of 150Mbps.

## How Setting up Arduino IDE for ESP32 and Run The LED On It? (Step By Step)

#### 1- Downlaod and install [Arduino IDE](https://www.arduino.cc/en/software).
#### 2- Install SP32 board in Arduino IDE.
- ####  Go to File -> Prefrences then past the [link].(https://dl.espressif.com/dl/package_esp32_index.json) in the Additional Boards Manager URLs.

  <img width="500" height="390" src="https://user-images.githubusercontent.com/74800962/180086991-dc983bd6-db18-4d98-ac2f-975fcfbc6fcc.png">
- #### Now go to the board manager and type ESP32 and install the latest version.
  <img width="500" height="390" src="https://user-images.githubusercontent.com/74800962/180087844-f0eca6ae-82dd-4439-82c9-bd51c1a8a461.png">

  <img width="500" height="390"  alt="Screen Shot 1443-12-21 at 8 23 49 PM" src="https://user-images.githubusercontent.com/74800962/180088537-207ae77f-00c6-4903-ab63-93071ee7c693.png">

#### 3- write the code that flash the LED and save the sketch.
```c
#define LED_BUILTIN 22
void setup() {
 pinMode(LED_BUILTIN, OUTPUT)

}

void loop() {
  digitalWrite(LED_BUILTIN, HIGH);
  delay(500);
  digitalWrite(LED_BUILTIN, LOW);
  delay(500);
}
```

#### 4- Select which board that you want to flash this program onto.
- ####  Go to Tools -> Board -> WEMOS LOLIN32.
        ``
        NOTE:You must select your ESP32 board in my case I have LOLIN32
        ``
<img width="500" height="390" alt="Screen Shot 1443-12-22 at 1 08 22 AM" src="https://user-images.githubusercontent.com/74800962/180091039-b3d02ae7-1616-4712-b658-71b65b8f47ad.png">
        
#### 5- Select correct port.       
- ####  Go to Tools -> Port -> /dev/cu.wchusbserial1420.
 
<img width="500" height="390" alt="Screen Shot 1443-12-22 at 1 17 08 AM" src="https://user-images.githubusercontent.com/74800962/180092213-238dfbe8-c340-47ea-8caf-a25108f7bd20.png">

#### 6- Upload Code to the ESP32 board.
<img width="500" height="390" alt="Screen Shot 1443-12-22 at 1 21 33 AM" src="https://user-images.githubusercontent.com/74800962/180092640-85e53eff-a0fe-457b-b95a-8971be5daabd.png">


- ####  This will compile your code and the transfer it to the ESP32.
- ####  After uploading the sketch you should see the blue LED blinking every 500ms.
     ![output](https://user-images.githubusercontent.com/74800962/180094250-151bd872-2c18-42b4-9069-f326107a4c10.gif)


##  Refrences:
- ####  Botletics's ESP32-Arduino-Setup [repository](https://github.com/botletics/Reflowduino/wiki/ESP32-Arduino-Setup).
- ###  Youtube [video](https://youtu.be/tkDJQkB9eEY).
