Where am I now: https://github.com/EloiStree/HelloGodotRemoteControlHub/issues/40

--------

I was working on *World of Warcraft: Road to the Deadmines* when [Hollow Knight: Silksong](https://store.steampowered.com/app/1030300/Hollow_Knight_Silksong) suddenly appeared on the Steam store!  
[<img width="954" height="498" alt="image" src="https://github.com/user-attachments/assets/17e18bf6-2f1a-4418-bb44-64e3755c3814" />](https://store.steampowered.com/app/1030300/Hollow_Knight_Silksong)

Let’s dive in!

To get started, you’ll need a Raspberry Pi with Godot installed:  
[Step: Install Raspberry Pi with Godot](https://github.com/EloiStree/HelloGodotRemoteControlHub/blob/main/EN/EnRoutePourLesMortesMines/Day001/Step_InstallRaspberryPiWithGodot.md)

This setup is perfect for learning Godot while having fun practicing GDScript through game development.

---

Okay, I’m not entirely sure where this is going, but let’s figure it out!

First, we need to run *Hollow Knight: Silksong* on a mini PC.  
[https://store.steampowered.com/app/1030300/Hollow_Knight_Silksong/](https://store.steampowered.com/app/1030300/Hollow_Knight_Silksong/)

⚠️ **Warning**: Using unauthorized methods to play a game can risk a Steam ban. Consider purchasing the game on a separate account for safety.

We can use an Arduino Leonardo to interface with the mini PC. My code isn’t ready yet, and with *Silksong* out, time’s ticking! ⏰ For now, I’ll use XOMI, a tool I’ve worked with before:  
[https://github.com/EloiStree/2022_01_24_XOMI](https://github.com/EloiStree/2022_01_24_XOMI)

I made a French video explaining how to install and use XOMI:  
[<img width="1902" height="1023" alt="image" src="https://github.com/user-attachments/assets/66c264be-c377-45f3-9efc-7b0aab5f6bff" />](https://youtu.be/_vMG_CROAi4)  
[https://youtu.be/_vMG_CROAi4](https://youtu.be/_vMG_CROAi4)

XOMI lets us send UDP messages over Wi-Fi—small packets of binary data like `10101001110101010101010101111101010101010`. For example, a 32-bit integer like `11111111 11111111 11111111 11111111` represents a number between -2,147,483,648 and 2,147,483,647.

Here’s how binary counting works:  
- `0001` = 1  
- `0010` = 2  
- `0011` = 3  
- `0100` = 4  
- `0101` = 5  

When storing numbers, the order matters:  
- **Big-endian** (e.g., Python): `00 00 09 C5` → `00000000 00000000 00001001 11000101`  
- **Little-endian** (e.g., C#): `C5 09 00 00` → `11000101 00001001 00000000 00000000`

Our goal is to press and release the jump button in the game. To simplify, I’ve assigned numbers to actions for keyboard and gamepad inputs. Check my *Scratch to Warcraft* grammar:  
[https://github.com/EloiStree/2024_08_29_ScratchToWarcraft?tab=readme-ov-file#xbox-xinput-version](https://github.com/EloiStree/2024_08_29_ScratchToWarcraft?tab=readme-ov-file#xbox-xinput-version)

For example, the A button (jump in-game) is:  
- Press A: `1300` (`00010100 00000101 00000000 00000000`)  
- Release A: `2300` (`11111100 00001000 00000000 00000000`)

Send these to the computer’s IP and port via XOMI with a slight delay, and your character will jump!

Other gamepad inputs you can simulate:  
- Press A button: `1300` (release: `2300`)  
- Press X button: `1301` (release: `2301`)  
- Press B button: `1302` (release: `2302`)  
- Press Y button: `1303` (release: `2303`)  
- Press left stick: `1306` (release: `2306`)  
- Press right stick: `1307` (release: `2307`)  
- Move left stick up: `1331` (release: `2331`)  
- Move left stick up-right: `1332` (release: `2332`)  
- Move left stick right: `1333` (release: `2333`)  
- Move left stick down-right: `1334` (release: `2334`)  
- Move left stick down: `1335` (release: `2335`)  
- Move left stick down-left: `1336` (release: `2336`)  
- Move left stick left: `1337` (release: `2337`)  
- Move left stick up-left: `1338` (release: `2338`)

Here are the game’s input mappings:  
<img width="1010" height="616" alt="image" src="https://github.com/user-attachments/assets/2e2b9810-d0f4-4352-b2ce-a66dfa744d11" />  
<img width="1140" height="807" alt="image" src="https://github.com/user-attachments/assets/3ce71096-d686-4131-8ce1-89dfea9b050b" />

- **B, Right**: Use  
- **A, Down**: Jump  
- **X, Left**: Attack 1  
- **Y, Up**: Needling  
- **Left Menu**: Inventory  
- **Right Menu**: Pause  
- **LT**: Harpoon  
- **RT**: Sprint  
- **LB**: Quick Map  
- **RB**: Skill/Tool  
- **Left Joystick/Arrow Keys**: Move  
- **Right Joystick Press**: Attack 2  

Before we start, we need a project and a way to save progress. As coders, we use **Git** to save our work—it’s essential!

Here’s how to set it up:  
- Watch this tutorial: [https://www.youtube.com/watch?v=k0aH_V2GrBs](https://www.youtube.com/watch?v=k0aH_V2GrBs)  
- Ensure Git is installed on your computer (if not using a Raspberry Pi): [https://git-scm.com/](https://git-scm.com/)  
- Create a *HelloSilksong* project in Godot with Git enabled. Save it near `C:\Godot\` on Windows.  
<img width="1144" height="821" alt="image" src="https://github.com/user-attachments/assets/3714b426-b611-4e76-b43a-e5d648c7fc7a" />

Enable hidden files and extensions in Windows:  
<img width="993" height="462" alt="image" src="https://github.com/user-attachments/assets/e1796e71-0cc6-4415-83cf-6906b98eb9aa" />

Some files in your project should be ignored. Check the community’s recommended `.gitignore` for Godot:  
[https://www.toptal.com/developers/gitignore/api/godot](https://www.toptal.com/developers/gitignore/api/godot)

To save your project:  
1. Create a GitHub account and a new repository:  
   <img width="1908" height="611" alt="image" src="https://github.com/user-attachments/assets/f0749b1b-3be5-4fad-bdf6-a9e453021635" />  
   <img width="782" height="760" alt="image" src="https://github.com/user-attachments/assets/3748c6b4-b42c-4ab3-bb2e-1c3048fcd0b1" />  
2. Copy the repository URL from the green HTTPS section:  
   <img width="929" height="308" alt="image" src="https://github.com/user-attachments/assets/1888ac25-8b49-4dec-bb90-23eeb0600d8e" />  
   Example:  
   ```
   https://github.com/EloiStree/HelloGodotSilksong.git
   ```
   ```
   git clone https://github.com/EloiStree/HelloGodotSilksong.git
   ```
3. Move the Git files into your Godot project:  
   <img width="707" height="240" alt="image" src="https://github.com/user-attachments/assets/86ff9975-3cac-4b58-9e95-03412eab7cba" />  
   <img width="725" height="439" alt="image" src="https://github.com/user-attachments/assets/7c223315-3160-4dd3-9ac3-8e6aad8828cf" />  
4. Open a terminal in the project folder by typing `cmd` in the Windows Explorer address bar:  
   <img width="1303" height="459" alt="image" src="https://github.com/user-attachments/assets/02822e8b-4855-4016-8d42-d6bd8cec4d23" />  
5. Check uncommitted changes:  
   ```
   git status
   ```  
   <img width="733" height="281" alt="image" src="https://github.com/user-attachments/assets/62a42b26-98d8-40d9-9fe3-bfef2f5bfddb" />  
6. Stage changes:  
   ```
   git add .
   ```  
   <img width="318" height="45" alt="image" src="https://github.com/user-attachments/assets/0c6c4a87-fb1a-4b70-ae0c-8ba9ebbd1840" />  
   <img width="474" height="255" alt="image" src="https://github.com/user-attachments/assets/43a272ee-bf82-42eb-807e-090e42b9c5af" />  
7. Configure your Git identity (if it’s your first time):  
   ```
   git config --global user.email "NotYourBiz@gmail.com"
   git config --global user.name "Eloi Stree"
   ```  
   <img width="745" height="74" alt="image" src="https://github.com/user-attachments/assets/dd1c792b-8376-48bc-ae13-110186a85f26" />  
8. Commit changes locally:  
   ```
   git commit -m "My first commit to save the project locally"
   ```  
   This creates a save point (commit) you can return to later.  
9. Pull updates from GitHub to avoid conflicts:  
   ```
   git pull
   ```  
   ⚠️ Always commit changes before pulling to avoid losing work.  
10. Push your changes to GitHub:  
    ```
    git push
    ```  
    Now your code is safely stored online. With collaborators or community help, it’s nearly impossible to lose!  

You can even revert to a specific commit later, like this:  
```
git clone https://github.com/EloiStree/HelloGodotSilksong.git BackInThePast
cd BackInThePast
git reset --hard 08913cf12163cb09fae6b77bcb8f95cf46f8d708
```

As my old students said: **"Git Good!"** 😎  

For added security, enable two-factor authentication (2FA) on GitHub. I’ll cover Raspberry Pi-specific Git setup later.

---

**Nice, we can save our project!**

> 🤓 **Tip**: Commit every 1–3 hours and push to GitHub before bed. Git takes practice, so be patient!

---

Welcome to the "white paper"!  
<img width="1912" height="1145" alt="image" src="https://github.com/user-attachments/assets/9b1684dc-22d2-4932-87de-4d91ffc3bdff" />

I’m not sure where to go next, but we need buttons for movement and jumping. Let’s explore:  

- Quick tutorial: [https://www.youtube.com/shorts/9c6pqt3wv7o](https://www.youtube.com/shorts/9c6pqt3wv7o)

Create a folder called `unstore` for 2D assets and scripts:  
<img width="668" height="476" alt="image" src="https://github.com/user-attachments/assets/e0dff7ce-ca6a-44f3-8220-cab9ea5ec2ff" />  
As beginners, we’re still learning how to organize and name files.

We want to build a **user interface**. Godot has a dedicated UI system:  
<img width="282" height="44" alt="image" src="https://github.com/user-attachments/assets/82678f15-aeca-4273-adbb-11af2f8977be" />  

Let’s research Godot’s UI system:  
[https://www.youtube.com/results?search_query=user+interface+godot](https://www.youtube.com/results?search_query=user+interface+godot)

We can drag and drop images and SVGs for buttons:  
[<img width="1290" height="719" alt="image" src="https://github.com/user-attachments/assets/f8e8eab3-ac67-4693-89a1-8686ed124d52" />](https://youtu.be/1_OFJLyqlXI?t=152)  
[https://youtu.be/1_OFJLyqlXI?t=152](https://youtu.be/1_OFJLyqlXI?t=152)

Let’s grab some 2D button assets:  
[<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6c997deb-24bb-4d2e-88cd-62a181306453" />](https://afuncan.com/)  
[https://afuncan.com/](https://afuncan.com/)

We’ll use Krita to remove backgrounds from assets:  
<img width="1899" height="777" alt="image" src="https://github.com/user-attachments/assets/078e21a4-bd1b-425a-8fcd-b5b564074781" />  

Here’s the cleaned-up asset:  
<img width="939" height="424" alt="image" src="https://github.com/user-attachments/assets/f605436e-1761-490e-a264-92ccc39bea40" />  

In Krita, separate each button into layers and export them:  
<img width="1898" height="487" alt="image" src="https://github.com/user-attachments/assets/20b53a93-a780-44e1-9ca0-271f53da8e1a" />  
Go to **Tools > Scripts > Export Layers** in Krita to save them.

Now we can drag and drop an `A` button in Godot:  
<img width="1914" height="1015" alt="image" src="https://github.com/user-attachments/assets/bbc74798-16e8-4f5b-87f0-0bb7bdb6c1ab" />  

Let’s add arrows and other main buttons. We might be doing this inefficiently since buttons share similarities, but we’ll optimize later.

To make the `A` button trigger a jump, add this GDScript:  
<img width="1900" height="1130" alt="image" src="https://github.com/user-attachments/assets/4a07d7d7-e562-4302-a465-a0a0b1ae11d4" />

I asked ChatGPT for a script to detect mouse clicks on a `Sprite2D`. It suggested this code and recommended creating a `control.tscn` scene:  
```gdscript
extends Sprite2D

# Designer can set a message in the Inspector
@export var custom_message: String = "Hello!"

func _input_event(viewport, event, shape_idx):
	if event is InputEventMouseButton and event.button_index == MOUSE_BUTTON_LEFT:
		if event.pressed:
			print("Press A")
		else:
			print("Release A")
			print(custom_message)
```

To understand this, let’s **RTFM** (Read the Fine Manual) 😁 and **LMGTFY** (Let Me Google That For You).  
<img width="489" height="212" alt="image" src="https://github.com/user-attachments/assets/0d64db05-722a-45e1-9594-6399aec69da4" />

Let’s test it by pressing **Play** in Godot:  
<img width="1649" height="731" alt="image" src="https://github.com/user-attachments/assets/816d4164-2ae4-469b-9e4f-75c53b30d943" />  

Godot prompts us to save the scene and set it as the project’s starting point.  

It doesn’t work yet because, as ChatGPT noted:  
> `_input_event` is triggered automatically when this `Sprite2D` is clicked (as long as it has a `CollisionShape2D`).  

Let’s add a `CollisionShape2D` by right-clicking the button and adding a node:  
<img width="1442" height="902" alt="image" src="https://github.com/user-attachments/assets/4b71bbae-ed53-4d4c-9602-bb51d3427734" />  

Uh-oh, I’m lost! Why? Because game development isn’t simple. We **need** to watch tutorials and read the manual to master Godot.

---

Okay, time to watch some tutorials and come back stronger!  
[<img width="491" height="524" alt="image" src="https://github.com/user-attachments/assets/0891cdd1-9618-4cf3-8c35-4492ccb67055" />](https://www.youtube.com/watch?v=pMLIQP46OwE)

----------

Next step: Learn to send a udp integer when press a sprite to a given ip and port for only one button.
