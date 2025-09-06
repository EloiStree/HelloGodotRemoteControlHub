

I was working on *World of Warcraft: Road to the Deadmines* when [Hollow Knight: Silksong](https://store.steampowered.com/app/1030300/Hollow_Knight_Silksong) suddenly appeared on the store.
[<img width="954" height="498" alt="image" src="https://github.com/user-attachments/assets/17e18bf6-2f1a-4418-bb44-64e3755c3814" />](https://store.steampowered.com/app/1030300/Hollow_Knight_Silksong)

So let’s dive into it!

To get started, you’ll need a Raspberry Pi with Godot installed:
[Step: Install Raspberry Pi with Godot](https://github.com/EloiStree/HelloGodotRemoteControlHub/blob/main/EN/EnRoutePourLesMortesMines/Day001/Step_InstallRaspberryPiWithGodot.md)

It’s the perfect setup for me to learn Godot while also having fun practicing GDScript through a game.


-------------------------

Ok, no idea where I am going.

First we need to install Silksong on Mini Window.
[https://store.steampowered.com/app/1030300/Hollow_Knight_Silksong/](https://store.steampowered.com/app/1030300/Hollow_Knight_Silksong/)


Be ban of a game can means be ban of Steam...  
⚠️ Buy the game on an alternative account.  

Now we can use an Arduino Leonardo to interface on the Mini PC.
But as my code is not ready and Silksong is here⌛.

I am going to use what works today, XOMI:
[https://github.com/EloiStree/2022_01_24_XOMI](https://github.com/EloiStree/2022_01_24_XOMI)

I did a french video on how to install it and use it here:  
[<img width="1902" height="1023" alt="image" src="https://github.com/user-attachments/assets/66c264be-c377-45f3-9efc-7b0aab5f6bff" />](https://youtu.be/_vMG_CROAi4)  
[https://youtu.be/_vMG_CROAi4](https://youtu.be/_vMG_CROAi4)   


Meaning that I can send by the WiFi of what we call UDP message.

Some small boxes containing stuff like this 10101001110101010101010101111101010101010.
If you use 32 bit 11111111 11111111 11111111 11111111 that what we call an integer.
A number between -2147483647 and 2147483647 .

That what we call, count in binary
0001 = 1
0010 = 2
0011 = 3
0100 = 4
0101 = 5

When you store from right to left it is call big endien
and left to right little endien.

Here is an example for both:
Big-endian, python: 00 00 09 C5 → 00000000 00000000 00001001 11000101
Little-endian, C#: C5 09 00 00 → 11000101 00001001 00000000 00000000

What we want to do it press the jump buttons in the game then release.

To make it easy in my adventure, I decided to associate a number to an action for keyboard and for gamepad.
So if you look at my grammar, Scratch To Warcraft: 
https://github.com/EloiStree/2024_08_29_ScratchToWarcraft?tab=readme-ov-file#xbox-xinput-version

You can see that A is 1300 to press and 2300 to release.
And in game A is jump

So if we send to the computer IP and Port of XOMI the message 
1300 :00010100 00000101 00000000 00000000
(With a bit of delay)
2300 :11111100 00001000 00000000 00000000

Your charater will jump.

Some other integers usable to simulate a gamepad:
Press A button	1300	2300
Press X button	1301	2301
Press B button	1302	2302
Press Y button	1303	2303
Press left stick	1306	2306
Press right stick	1307	2307
Move left stick up	1331	2331
Move left stick up-right	1332	2332
Move left stick right	1333	2333
Move left stick down-right	1334	2334
Move left stick down	1335	2335
Move left stick down-left	1336	2336
Move left stick left	1337	2337
Move left stick up-left	1338	2338

If we look at the game option we can see those input:
<img width="1010" height="616" alt="image" src="https://github.com/user-attachments/assets/2e2b9810-d0f4-4352-b2ce-a66dfa744d11" />
<img width="1140" height="807" alt="image" src="https://github.com/user-attachments/assets/3ce71096-d686-4131-8ce1-89dfea9b050b" />

Ok, nice.

B,Right: Use
A,Down: Jump
X,Left: Attack 1
Y,Up: Needolin
Left Menu: Inventory
Right Nenu Pause
LT: Harpoon
RT: Sprint
LB: Quick Map
RB: Skill / Tool
Joystick Left and Arrow = Move
Press Joystick Right: Attack 2


Before we start our adventure we need a projet and we need a way to save.
As coder the tools to save our progression is call git and is very important.

Let's me have a look:
- https://www.youtube.com/watch?v=k0aH_V2GrBs

Set the projet in Git Mode.
Verify that you computer if you are not on Raspberry pi has git installed
https://git-scm.com/

You can create a HelloSilksong project with Git mode trigger on.
Try to save your project near C on Window ( C:/Godot/ )
<img width="1144" height="821" alt="image" src="https://github.com/user-attachments/assets/3714b426-b611-4e76-b43a-e5d648c7fc7a" />



Display the hidden file and extension on Window
<img width="993" height="462" alt="image" src="https://github.com/user-attachments/assets/e1796e71-0cc6-4415-83cf-6906b98eb9aa" />


In your project there are file you want to ignore, you can ask the community what at those files:
[https://www.toptal.com/developers/gitignore/api/godot](https://www.toptal.com/developers/gitignore/api/godot)



To save it you need to create an account on GitHub.
Then create a repository
<img width="1908" height="611" alt="image" src="https://github.com/user-attachments/assets/f0749b1b-3be5-4fad-bdf6-a9e453021635" />
<img width="782" height="760" alt="image" src="https://github.com/user-attachments/assets/3748c6b4-b42c-4ab3-bb2e-1c3048fcd0b1" />

Copy the URL in the green http section 
<img width="929" height="308" alt="image" src="https://github.com/user-attachments/assets/1888ac25-8b49-4dec-bb90-23eeb0600d8e" />


Looking like this for me:
```
https://github.com/EloiStree/HelloGodotSilksong.git
```
```
git clone https://github.com/EloiStree/HelloGodotSilksong.git
```

Move those file in the godot project
<img width="707" height="240" alt="image" src="https://github.com/user-attachments/assets/86ff9975-3cac-4b58-9e95-03412eab7cba" />
<img width="725" height="439" alt="image" src="https://github.com/user-attachments/assets/7c223315-3160-4dd3-9ac3-8e6aad8828cf" />

Type CMD in the path on the top on Window
<img width="1303" height="459" alt="image" src="https://github.com/user-attachments/assets/02822e8b-4855-4016-8d42-d6bd8cec4d23" />

```git status``` will tell you what is not saved yet
<img width="733" height="281" alt="image" src="https://github.com/user-attachments/assets/62a42b26-98d8-40d9-9fe3-bfef2f5bfddb" />

```git add .``` add the files that changed to the next save
<img width="318" height="45" alt="image" src="https://github.com/user-attachments/assets/0c6c4a87-fb1a-4b70-ae0c-8ba9ebbd1840" />
<img width="474" height="255" alt="image" src="https://github.com/user-attachments/assets/43a272ee-bf82-42eb-807e-090e42b9c5af" />

If it is your first time, any save must be identify by someone to work in group.
So you have to give a mail and an name
```
git config --global user.email "NotYourBiz@gmail.com"
git config --global user.name "Eloi Stree"
```
<img width="745" height="74" alt="image" src="https://github.com/user-attachments/assets/dd1c792b-8376-48bc-ae13-110186a85f26" />

Let save your project localy on your computer
```git commit -m "My first commig to save the project on my computer"``` Make a save point name a commit.

If one day in 10 years you want to come back to this point, you can 🤓😁

We want to save
But to be sure that your friend did not help on the project you want to check the server
```git pull``` Bring all what is new from GitHub to your computer

🔔Alway have a commit saved before a pull "You can recovert what have not been saved"

Let's push that online to save it

```git push``` Try to push the code of your computer on the online server

Now it is hard to lose your code.
If a friend work with you, it is kind of impossible
If the community help you, not event Google and Microsoft can erase your code.
Because you can take any git and reupload it on other git server 😮🌟

"If you git it correctly, you can lost it."

For example this command is going to copy the project as empty as it is now at this save point exactly.
```
git clone https://github.com/EloiStree/HelloGodotSilksong.git BackInThePas
cd BackInThePas
git reset --hard 08913cf12163cb09fae6b77bcb8f95cf46f8d708
``` 

So like my old students said:    
**"Git Good !"**  


If you use Git, you also need to add extra step to have a double authentification and a browser check.
Did not add it here but will do it later for Raspberry Pi.



--------------

Nice we can save !!!

> 🤓 Save every 1-3 hours with git and push on the server when you go to sleep at least.
> It is going to take time to understand and pratice it.. Take the time you need.


------------------

Welcome to the "white paper".
<img width="1912" height="1145" alt="image" src="https://github.com/user-attachments/assets/9b1684dc-22d2-4932-87de-4d91ffc3bdff" />

I have no idea of where to go.

All I know is that we need button to be able to move and jump.
Let's look about that:

Let's me look around:
-  In short https://www.youtube.com/shorts/9c6pqt3wv7o


Let's create a folder that is call unstore and add 2D and script in it to store them later:
<img width="668" height="476" alt="image" src="https://github.com/user-attachments/assets/e0dff7ce-ca6a-44f3-8220-cab9ea5ec2ff" />
We are beginner and we dont know yet how to name, what to name and were to store stuffs.

What we want to learn is call "user interface".

And we can see a big green button for that;
<img width="282" height="44" alt="image" src="https://github.com/user-attachments/assets/82678f15-aeca-4273-adbb-11af2f8977be" />
So let's google it a bit and check what content creator are saying:
https://www.youtube.com/results?search_query=user+interface+godot


Apparently we can drag and drop image and what is call svg
[<img width="1290" height="719" alt="image" src="https://github.com/user-attachments/assets/f8e8eab3-ac67-4693-89a1-8686ed124d52" />](https://youtu.be/1_OFJLyqlXI?t=152)  
https://youtu.be/1_OFJLyqlXI?t=152  

On va donc aller chercher un peu d asset 2d pour les bouttons
[<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6c997deb-24bb-4d2e-88cd-62a181306453" />](https://afuncan.com/)  
https://afuncan.com/


Let's try to remove the background using Krita
<img width="1899" height="777" alt="image" src="https://github.com/user-attachments/assets/078e21a4-bd1b-425a-8fcd-b5b564074781" />

If we keep the one we need:
<img width="939" height="424" alt="image" src="https://github.com/user-attachments/assets/f605436e-1761-490e-a264-92ccc39bea40" />


After cutting each part in layer in Krita you can export them.
<img width="1898" height="487" alt="image" src="https://github.com/user-attachments/assets/20b53a93-a780-44e1-9ca0-271f53da8e1a" />
Godot have something to manage Sprite as we call those image but we don t have the level yet.
```Go to "Tools"->"Scripts"->"Export layers"``` To export them

Tada we can drag and drop an `A` buttons
<img width="1914" height="1015" alt="image" src="https://github.com/user-attachments/assets/bbc74798-16e8-4f5b-87f0-0bb7bdb6c1ab" />
Let's add the arrow and the main buttons.

I suppose that we are doing it wrong because all buttons will have some similarity between each other.
But for now I am gonna ignore it.

Let's just jump by adding a script code that jump
<img width="1900" height="1130" alt="image" src="https://github.com/user-attachments/assets/4a07d7d7-e562-4302-a465-a0a0b1ae11d4" />



If ask to Chat GPT to create an action when the Sprite2D is clicked by the mouse.
It give this code and request me to create a "control.tscn"
``` gdscript
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

So we are going to RTFM : "Read the Fucking Manual" 😁😋
And LMGTFY: "Let me google that for you"
To understand what happened.

<img width="489" height="212" alt="image" src="https://github.com/user-attachments/assets/0d64db05-722a-45e1-9594-6399aec69da4" />

But let's try for the fun to press play before
<img width="1649" height="731" alt="image" src="https://github.com/user-attachments/assets/816d4164-2ae4-469b-9e4f-75c53b30d943" />

Godot ask to save the current scene and to select it as the start point of our hub.


It does not work but if we listen to what the AI said in the commentary:
```_input_event → Triggered automatically when this Sprite2D is clicked (as long as it has a CollisionShape2D).```

Lets try it. by right cliking the button and adding a node
<img width="1442" height="902" alt="image" src="https://github.com/user-attachments/assets/4b71bbae-ed53-4d4c-9602-bb51d3427734" />

A boum I am lost... Why. Because Life is not simple and **Require** to watch tutorial and manual to begin with tools.

-----------------------------




