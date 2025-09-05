So ...  
[<img width="716" height="412" alt="image" src="https://github.com/user-attachments/assets/6073d411-01d6-422e-b53d-43b261bc9d60" />](https://www.youtube.com/watch?v=JzY8gB5UcS4&list=RDJzY8gB5UcS4&start_radio=1)  

We are going to need a Raspberry Pi 5 🖥️ and a Window Mini PC 💻 ( or you gaming PC 🎮 ) 
Our aim is to learn coding by becoming a Quality Assurance tester/developer.
We’re gonna hack them all!!!

So 😅, if we want to hack them all,
we’re gonna need some hardware.

Don’t be afraid of that. I am going to restart at a beginner level after this section.
[<img width="600" height="500" alt="image" src="https://github.com/user-attachments/assets/458d9088-f0e3-4479-bede-72e336b8802a" />](https://youtu.be/XNmozHXQ5zk?t=9)

Note that if you don’t like the idea of playing World of Warcraft, you can explore:

* [https://hordes.io](https://hordes.io)
* [10 Second Ninja](https://store.steampowered.com/app/271670/10_Second_Ninja)
* [Stealth Bastard](https://store.steampowered.com/app/209190/Stealth_Bastard_Deluxe)
* [Doom DOS (if you’re old enough)](https://www.gog.com/en/game/doom_doom_ii)

---

> 🧐 "Godot runs on Raspberry Pi 😮 ?!"

Oh yes, it does 😁🐛🌟.
But I wouldn’t try it on Raspberry Pi 2, 3, or 4 😋.

I am going to use two setups.

The Pi 500, because it is very portable:
[<img width="1195" height="356" alt="image" src="https://github.com/user-attachments/assets/24d3a2b8-d993-4e20-a0ff-c77416d8f062" />](https://www.raspberrypi.com/products/raspberry-pi-500/)
[https://www.raspberrypi.com/products/raspberry-pi-500/](https://www.raspberrypi.com/products/raspberry-pi-500/)

And the GeeekPi 10.1" 1280x800 LCD Touchscreen with a Pi 5 for the second setup:
[<img width="1206" height="491" alt="image" src="https://github.com/user-attachments/assets/e66bb407-c32f-4637-a163-22464921405d" />](https://www.amazon.com.be/GeeekPi-Capacitive-Touchscreen-Raspberry-Dual-Speaker/dp/B0DHV6DZC1/)  
[https://www.amazon.com.be/GeeekPi-Capacitive-Touchscreen-Raspberry-Dual-Speaker/dp/B0DHV6DZC1/](https://www.amazon.com.be/GeeekPi-Capacitive-Touchscreen-Raspberry-Dual-Speaker/dp/B0DHV6DZC1/)

The touchscreen is friendlier for building a Godot Hub, but more fragile for traveling.

Since we are going to start with UI buttons in Godot, I’ll begin on the touchscreen.

---

To read input, we can use the keyboard at first, then switch to an Arcade Kit DIY Board:
[<img width="464" height="295" alt="image" src="https://github.com/user-attachments/assets/5620b9c1-0d82-4d57-8f8c-09034fb8c85a" />](https://nl.aliexpress.com/w/wholesale-arcade--board-kit-diy.html?spm=a2g0o.best.search.0)  
[https://nl.aliexpress.com/w/wholesale-arcade--board-kit-diy.html?spm=a2g0o.best.search.0](https://nl.aliexpress.com/w/wholesale-arcade--board-kit-diy.html?spm=a2g0o.best.search.0)

With a bit of 3D printing, we can make some cool footboards with those.
[<img width="1359" height="709" alt="image" src="https://github.com/user-attachments/assets/df2925e2-fc9c-49d3-b138-1c13f31b3e2f" />](https://www.youtube.com/watch?v=N02mYYh78ng&t=27s)  
https://www.youtube.com/watch?v=N02mYYh78ng&t=27s  


---

To play World of Warcraft and other small games, we need a computer to control remotely.  
If you don’t plan to play 3D games outside of WoW, this is the model I used: Mini PC AWow  
[<img width="1159" height="726" alt="image" src="https://github.com/user-attachments/assets/1ee6ec3b-f1f0-4c5a-9eaa-6180ef8c4c41" />](https://www.amazon.com.be/dp/B0DRFDSLK3/)
[https://www.amazon.com.be/dp/B0DRFDSLK3/](https://www.amazon.com.be/dp/B0DRFDSLK3/)    
(The main reason for this one is that when the power goes down, it restarts automatically ⛈️😁)  

---

So:

* We have a computer to run Godot as a controller.
* We have a computer to play some games.

You play remotely on it using Wi-Fi and some Python.
That’s what we are going to do today.

But you also want to test code with any game on any platform.
To do that, you will need two things:

---

An Arduino Leonardo to simulate an XInput Xbox controller:
[<img width="615" height="474" alt="image" src="https://github.com/user-attachments/assets/69dfbcf7-3be2-423b-80fd-fece1b9104a3" />
](https://www.google.com/search?q=Arduino%20Leonardo)   
[https://www.google.com/search?q=Arduino%20Leonardo](https://www.google.com/search?q=Arduino%20Leonardo)

>  🧐 "We can play World of Warcraft with an Xbox?"

Yes—if you are using the Console Port addon:
[<img width="800" height="460" alt="image" src="https://github.com/user-attachments/assets/b65a132b-296d-4620-a7e9-4e3fe3cbbe35" />](https://www.curseforge.com/wow/addons/console-port)
[https://www.curseforge.com/wow/addons/console-port](https://www.curseforge.com/wow/addons/console-port)

---

But you’re right—it would be better with a keyboard.
You can simulate a keyboard with the Arduino Leonardo.
But wouldn’t it be more fun to simulate a keyboard that works everywhere?

In the future, we are going to use the ESP32-S3 to build a Bluetooth keyboard and mouse that work on any device supporting Bluetooth 😮
[<img width="548" height="551" alt="image" src="https://github.com/user-attachments/assets/4721a9dd-59e8-4cb9-a084-84ce8d7883d5" />](https://www.google.com/search?q=esp32+s3)  
[https://www.google.com/search?q=esp32+s3](https://www.google.com/search?q=esp32+s3)

---

Isn’t that too hard? Don’t worry—we are learning Godot, not C++ on Arduino.
I am going to code all of that for you.

All you need to learn is how to send numbers to a script I’ll prepare.
We’ll use UART, Serial, Bluetooth, and a bit of Python.
Don’t think about it too much for now ^^

But you will need this magic device that you’re going to love in your future DIY projects: the HC-05 or a TTL adapter.

HC-05 (Bluetooth, a bit of delay):
[<img width="1500" height="1500" alt="image" src="https://github.com/user-attachments/assets/b35e304a-23f4-4cc1-bd38-ca7afea6fda5" />](https://www.google.com/search?q=hc05)  
[https://www.google.com/search?q=hc05](https://www.google.com/search?q=hc05)

TTL CH340G (USB direct, no delay):
[<img width="277" height="182" alt="image" src="https://github.com/user-attachments/assets/5fb3d833-0231-47cb-8801-21d71be84e95" />](https://www.google.com/search?q=TTL+CH340G)  
[https://www.google.com/search?q=TTL+CH340G](https://www.google.com/search?q=TTL+CH340G)

Both work the same way.

---

> 🧐 "Are we good now?"

We are still missing something.

To read game information safely (and avoid anti-cheat issues), you should use an external capture device.

**Option 1: A capture device like the MiraBox:**
[<img width="1074" height="485" alt="image" src="https://github.com/user-attachments/assets/cd1a679d-5353-4cd7-924f-4760bfde4132" />](https://www.google.com/search?q=mirabox)  
[<img width="800" height="646" alt="image" src="https://github.com/user-attachments/assets/a0adef78-ccd1-40fa-ade5-fe38e991400f" />](https://www.google.com/search?q=mirabox)  
[https://www.google.com/search?q=mirabox](https://www.google.com/search?q=mirabox)
  

**Option 2: A simple webcam:**
[<img width="566" height="552" alt="image" src="https://github.com/user-attachments/assets/dcf4d4d2-f043-40ed-984e-f9796c97042f" />](https://www.amazon.com.be/dp/B0DWFQ4M5C)
[https://www.amazon.com.be/dp/B0DWFQ4M5C](https://www.amazon.com.be/dp/B0DWFQ4M5C)
(I picked the cheap one from Amazon myself 😅)

It is a more direct **approach**, but it is a real **hell** that will teach you all about color, exposure, lighting, and contrast.
That is the worst you can do as a beginner—unless you actually plan to learn color and lighting later in your life.

Here is a taste of the science topic of color spacing that you will need to learn to use webcam;
[<img width="714" height="396" alt="image" src="https://github.com/user-attachments/assets/c2d41985-8898-4816-8509-4d9f2fa19847" />](https://www.google.com/search?q=color+space+3d)  
[<img width="384" height="384" alt="image" src="https://github.com/user-attachments/assets/6e054dab-a970-4ca7-863d-9576a37bdc68" />](https://www.google.com/search?q=color+space+3d)  
[<img width="1200" height="1361" alt="image" src="https://github.com/user-attachments/assets/02e411c4-1161-4b20-9171-4851bbeb0962" />](https://www.google.com/search?q=color+space+3d)  
[https://www.google.com/search?q=color+space+3d](https://www.google.com/search?q=color+space+3d)  

---

> 🧐 "Good?"

Yes. I think we are good now with the equipment.

Let's dive in the unkown together...
[<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/03ec8f07-69e7-42b2-8fe7-f14bb0fcbd6b" />](https://godotengine.org/article/godot-4-2-arrives-in-style)  
[<img width="1272" height="612" alt="image" src="https://github.com/user-attachments/assets/31119cb3-2670-439a-91ec-fd191469442c" />](https://godotengine.org/download)  
[https://godotengine.org/download/](https://godotengine.org/download/)   


