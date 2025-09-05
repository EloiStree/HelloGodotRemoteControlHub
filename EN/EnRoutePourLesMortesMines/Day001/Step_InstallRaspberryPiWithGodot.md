

The Raspberry Pi is a small computer created in the UK to teach kids about computers and how they work.

> 🐛 If you are too young to do the following steps, you can ask someone else to do them for you.

It costs under 150 euros, depending on the equipment you choose to use.

[<img width="1143" height="442" alt="image" src="https://github.com/user-attachments/assets/56c01852-a0b9-4289-b4f1-85be480759fb" />](https://www.amazon.com.be/Raspberry-Pi-SC1112-5-8Gb/dp/B0CK2FCG1K/)  
https://www.amazon.com.be/Raspberry-Pi-SC1112-5-8Gb/dp/B0CK2FCG1K/

It will cost you around 200 euros if, like me, you want to use a small touchscreen dedicated to the Pi 5.  
[<img width="1155" height="478" alt="image" src="https://github.com/user-attachments/assets/4b4dae6d-ee85-40b6-862e-cab979c0563c" />](https://www.amazon.com.be/GeeekPi-Capacitive-Touchscreen-Raspberry-Dual-Speaker/dp/B0DHV6DZC1/)  
https://www.amazon.com.be/GeeekPi-Capacitive-Touchscreen-Raspberry-Dual-Speaker/dp/B0DHV6DZC1/

You are going to need a memory card called an SD card, with a capacity of 32–128 GB, and an SD card reader.

I’m not sure of the maximum size, but 32 GB fills up quickly.  
[<img width="1158" height="550" alt="image" src="https://github.com/user-attachments/assets/5f30cb2d-985d-40e8-850e-c405c48646fc" />](https://www.amazon.com.be/-/en/SanDisk-256GB-microSDXC-Adapter-Approved/dp/B0B7NV73PJ/)  
https://www.amazon.com.be/-/en/SanDisk-256GB-microSDXC-Adapter-Approved/dp/B0B7NV73PJ/

[<img width="1141" height="496" alt="image" src="https://github.com/user-attachments/assets/b3d00cb8-f799-4275-a2cf-4c2075d668a5" />](https://www.amazon.com.be/Lecteur-Adaptateur-Mémoire-Compatible-MacBook/dp/B0DQ71G4G4)  
https://www.amazon.com.be/Lecteur-Adaptateur-Mémoire-Compatible-MacBook/dp/B0DQ71G4G4

---

Download the Raspberry Pi Imager application.  
[<img width="1181" height="482" alt="image" src="https://github.com/user-attachments/assets/7d48ca65-7974-4427-ae1e-3520a7d2188e" />](https://www.raspberrypi.com/software)  
https://www.raspberrypi.com/software

Plug the USB SD card reader with the SD card inserted.  
<img width="717" height="281" alt="image" src="https://github.com/user-attachments/assets/f46cf74c-4c8e-47aa-adf7-a11cd9b2a74f" />

Launch the Raspberry Pi Imager application.  
<img width="1101" height="573" alt="image" src="https://github.com/user-attachments/assets/5e5226d7-96d7-4617-ab6a-780b4d9ef3be" />

Choose the device: Raspberry Pi 5.  
<img width="1107" height="644" alt="image" src="https://github.com/user-attachments/assets/b405a953-c6aa-4842-839a-0d5d45a04b79" />

Choose the OS: Bookworm 64-bit.  
<img width="1100" height="647" alt="image" src="https://github.com/user-attachments/assets/97e8dfb1-da0b-4585-8a62-5b923d5e42bd" />

Choose the disk.  
<img width="1100" height="645" alt="image" src="https://github.com/user-attachments/assets/df088dbe-58bf-4adc-9232-0e5259705c2b" />

Edit the settings.  
<img width="1104" height="641" alt="image" src="https://github.com/user-attachments/assets/eb936aca-26a0-459f-97f4-3b42875fd79f" />

Configure a student account with a password you won’t forget.  
<img width="1101" height="646" alt="image" src="https://github.com/user-attachments/assets/713f3df6-6f20-4a9f-b285-34b8706c7566" />

Set up the Wi-Fi you want to use in advance.

Then validate and overwrite the disk.  
<img width="1104" height="650" alt="image" src="https://github.com/user-attachments/assets/b4a3781d-40b0-4fa7-9c74-d3625bf8cba8" />

Wait for the imager to install and verify that it was written correctly.  
<img width="1100" height="641" alt="image" src="https://github.com/user-attachments/assets/671155ad-0746-4dc4-b3a1-b6d619c2d21c" />

Your Pi is ready 😁  
<img width="1102" height="643" alt="image" src="https://github.com/user-attachments/assets/6c29f14f-6d3d-4b2d-85d2-a750513baf15" />

I made a video on assembling all of this:  
[To add later here]

Insert the SD card into the Pi.  
<img width="1059" height="533" alt="image" src="https://github.com/user-attachments/assets/03e51808-4d5d-4753-b57f-5436ca02f9d9" />

Let the Pi install what it needs.  
<img width="1015" height="562" alt="image" src="https://github.com/user-attachments/assets/aceb318b-f67b-4979-8fa5-69c96be145b2" />  
<img width="1207" height="675" alt="image" src="https://github.com/user-attachments/assets/fd7521a3-81cb-477e-9dd7-8ac76bdf5780" />

And voilà, you are ready!  
<img width="1233" height="687" alt="image" src="https://github.com/user-attachments/assets/5dd22cfa-684c-4c93-bc1f-5ce23bc914ee" />

For the next part, you will need to know what a terminal (also called a console) is:  
<img width="234" height="183" alt="image" src="https://github.com/user-attachments/assets/3d6d52a7-6c1d-4e9c-9f45-475ef2c1b5ec" />

Install Pi-Apps.  
[<img width="1151" height="683" alt="image" src="https://github.com/user-attachments/assets/96ed0991-8aee-4711-98e6-1fd4d7b692ee" />](https://github.com/EloiStree/HelloGodotRemoteControlHub/issues/4)  
https://github.com/EloiStree/HelloGodotRemoteControlHub/issues/4  
```
wget -qO- https://raw.githubusercontent.com/Botspot/pi-apps/master/install | bash
```  
<img width="611" height="123" alt="image" src="https://github.com/user-attachments/assets/3da330f5-b158-4d83-93c2-87785ad8de88" />

Now, let’s install what you’ll need. You can choose from this list:  
https://github.com/EloiStree/HelloGodotRemoteControlHub/issues/5

If you want to work in the video game industry with Godot, you can study these tools with confidence:

**Blender** to create 3D models:  
```
sudo apt update
sudo apt full-upgrade
sudo apt install blender -y
```  
<img width="912" height="574" alt="image" src="https://github.com/user-attachments/assets/ad2f26a3-fdfb-4e29-a68f-b4a0a2bcb0d1" />

**Git** is already installed, but it’s better to be sure because it’s an essential tool:  
```
# Update your system
sudo apt update
sudo apt upgrade -y
# Install Git
sudo apt install git -y
# Verify installation
git --version
# Configure Git (replace with your info)
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
# Check configuration
git config --list
```

**Python**, a language you’ll need to learn one day:  
```
# Update your system
sudo apt update
sudo apt upgrade -y
# Install Python 3 and pip
sudo apt install python3 python3-pip -y
# Verify Python installation
python3 --version
# Verify pip installation
pip3 --version
```

Since you installed Pi-Apps, you can now install what you need:

**Godot**… obviously:  
```
~/pi-apps/manage install "Godot"
```

**Krita** to edit 2D images:  
``` 
~/pi-apps/manage install "Krita"
```  
<img width="908" height="559" alt="image" src="https://github.com/user-attachments/assets/9aae7983-9eb3-403d-a59e-54ae4ba0a758" />

**Audacity** to edit sound and music:  
``` 
~/pi-apps/manage install "Audacity"
```  
<img width="910" height="561" alt="image" src="https://github.com/user-attachments/assets/05cd7e11-f443-40c8-9f8a-9a274d6d7591" />

**Visual Studio Code**, a user-friendly text editor for coding (can be used with Copilot to assist with coding):  
``` 
~/pi-apps/manage install "Visual Studio Code"
```  
<img width="912" height="573" alt="image" src="https://github.com/user-attachments/assets/cf5eb1f9-8932-44e8-95b6-abf3791eb19b" />

There are other great apps you can install on the Pi, but these are the essentials.

If you want to remotely control your Raspberry Pi to work from a distance, you can use Raspberry Pi Connect.  
<img width="980" height="131" alt="image" src="https://github.com/user-attachments/assets/fde89865-04de-4642-999e-7fc6918bbb5c" />

Try to sign in.  
<img width="1105" height="474" alt="image" src="https://github.com/user-attachments/assets/7a50d3c7-93f0-4e55-b2f6-f7d92b5dee0e" />

Create an account with an email address.  
<img width="981" height="522" alt="image" src="https://github.com/user-attachments/assets/fb8c52d0-33e6-46f2-869a-e715330af980" />

Add two-factor authentication if possible.  
<img width="596" height="542" alt="image" src="https://github.com/user-attachments/assets/d7ad7d86-e7ab-4a1b-9d0c-5417ddc8c2cf" />

Log in to your account with your email.  
<img width="901" height="490" alt="image" src="https://github.com/user-attachments/assets/e2cce56c-d3d1-4d2c-8289-f99ad2ae04b2" />

If you added two-factor authentication, enter the 6-digit code generated by Google Authenticator.  
<img width="888" height="411" alt="image" src="https://github.com/user-attachments/assets/9f52d606-06d8-40fc-8ff2-4e2f73a337ce" />

By default, the keyboard layout is not set to US International.  
<img width="800" height="373" alt="image" src="https://github.com/user-attachments/assets/18f504c9-10db-4797-883c-49fdc9802602" />

