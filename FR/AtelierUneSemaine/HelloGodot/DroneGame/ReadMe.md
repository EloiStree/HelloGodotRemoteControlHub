
# Apprendre a coder sur Godot par les drones

Mon but dans cette atelier en tant qu enseignant est de donner gout a la programmation via la creation de jeux sur Godot.
Le pilotage de drone est une passion qui peu vite couter cher, rendont la accessible.

Nous allons apprendre a coder un jeu de drone sur un outil gratuit et opensource: Godot.
https://godotengine.org/

# **L’atelier**

* **Day 1 :** C’est quoi un Raspberry Pi et Godot.
* **Day 2 :** Bougeons et creons un drone
* **Day 3 :** Créons un premier niveau pour notre drone
* **Day 4 :** Ajoutons de la decoration
* **Day 5 :** Ajoutons un tableau de score et un timer



# **C’est quoi Godot ?**




## Un peu de context

Mon nom est Eloi Stree et j’ai commencé à créer des jeux il y a 14 ans d’ici. Un simple Mario et démineur en Java, puis un jeu en réalité virtuelle, toujours en Java.  
Pour faire du jeu vidéo, il vous faut tout créer de A à Z : notions de temps, physique, importer des fichiers, collisions, chargement de niveau…  
Très amusant mais incroyablement long, c’est pourquoi j’ai appris à utiliser Unity3D.  

En septembre 2025, en tant qu’enseignant, je décide de tester Godot car il s’installerait apparemment sur des Raspberry Pi 5 (des petits ordinateurs à 75–150 euros).  
Je m’y essaie et j’y prends goût. Je constate que l’éditeur peut tourner sur Android ! Et effectivement, je peux travailler sur mon téléphone.  
Je peux donc travailler dans un casque de réalité virtuelle comme le Quest 3 ;) ?  
Effectivement.  

Godot est un outil de création de jeux vidéo créé en Argentine, de manière open source, pour permettre à tous de savoir faire du jeu vidéo, peu importe la machine que vous avez à la maison.  
Même si vous êtes sur un vieux Linux 32 bits !!!  

La raison pour laquelle je me suis mis à Godot est une suite logique :  
* Scratch permet d’apprendre la programmation mais est vite limitant  
* Python est très formateur mais devient vite compliqué quand le code grandit pour des débutants
* C# est un beau langage mais sans interface graphique il faut savoir garder l’attention de l’apprenant  
* Unity3D est la bonne solution pour apprendre mais il est trop lourd et trop complexe pour un petit atelier de quelques heures ou jours  

Je cherchais une manière d’enseigner la programmation par le jeu vidéo.  

Godot a une force pour un enseignant en programmation : il est multilingue.  
Il fonctionne avec son propre langage, le **GDScript**, très facile à apprendre.  
En plus de celui-ci, il possède un outil, le **GDExtension**, qui permet de choisir son langage 😁.  
* **Python** : le langage le plus connu au monde, pas très rapide mais simple et versatile  
* **C#** : très propre, utilisé dans de nombreux métiers et entretenu par Microsoft  
* **C++** : si vous désirez la puissance, mais comptez étudier pendant 20 ans l’optimisation  
* **Rust** : si vous aimez coder propre et pour longtemps  
* **Lua** : pour faire des jeux modifiables par la communauté  
* **JavaScript** : si vous désirez faire une carrière de web développeur par la suite  

Un outil de création de jeux vidéo :  
* léger comme une plume,
* sans compte,
* gratuit,
* open source,
* multiplateforme,
* tourne sur Linux,
* tourne sur Raspberry Pi 5,
* tourne sur de vieux Windows,
* tourne dans les casques VR,
* peut être utilisé en C# et Python,  
* …

Y a rien à dire, c’est beau ;)  

# **Raspberry Pi 5 et Steam Machine**  

Le Raspberry Pi est un mini-ordinateur créé par le gouvernement anglais pour apprendre à programmer et utiliser un ordinateur à sa population.  
Il n’est pas cher et orienté open source.  

Depuis, le Pi 5 est vraiment viable, au point que j’ai appris Godot pendant deux mois sur celui-ci pour voir si cela est possible.  
Et effectivement, je conseille vraiment cet achat à un étudiant ou jeune adulte.  

Car en plus de permettre d’apprendre, il ne consomme que 6–18 watts et peut servir de serveur Linux à la maison 👍🍻.  

Mais à l’heure où je rédige cette présentation d’atelier pour apprendre à coder sur Godot, un nouveau joueur est arrivé sur le marché : **le casque VR Deckard** et la **Steam Machine**.  

Aussi nommée la *Gabe Cube*, du nom de son créateur, la Steam Machine est un ordinateur et une console de jeux.  
Mais à la différence d’une console qui vous enferme pour que vous achetiez des jeux, la Gabe Cube est simplement un ordinateur Linux avec juste ce qu’il faut pour se sentir à l’aise niveau ventilation et puissance.  
Un petit ordinateur de maison qui, en un bouton, se trouve être une console de jeux actuels, rétro et Android.    

C’est littéralement une révolution à une époque où les consoles Xbox et PlayStation coûtent le prix d’un ordinateur.  

Cet atelier, peu importe sa variation sur l’exercice ou le contenu, a un simple but :  
**Donner goût à la programmation sur Godot par le jeu vidéo.**  

Pour cela, 4 à 12 Raspberry Pi sont mis à disposition des étudiants durant l’atelier.  
Et, quand disponible en 2026, 1/des Steam Machine(s) et un Deckcard seront présents pour tester.   

Si l’apprenant a un de ces appareils :  
* une bonne tablette Android  
* un ordinateur portable personnel (Linux ou Windows)  
* son propre Raspberry Pi 5  
* une Steam Deck  

Il peut décider de venir avec.  
Godot est exactement le même sur toutes les plateformes.  


# **Deckard et Meta**

Avec Godot, vous pouvez créer votre jeu vidéo directement à l’intérieur du casque de Meta, le Quest 3 😮.   
C’est magique.  

Une partie de l’atelier y sera dédiée.   
L’avantage du Meta est qu’il est abordable : environ 330 euros.  
Le désavantage: c’est Mark Zuckerberg, propriétaire de Facebook, qui a la main sur vous.  
Avantage pour un créateur: il y a 4+ millions de Quest 2 et 1–3 millions de Quest 3 avec qui partager votre jeu.  

Mais depuis le 14 novembre 2025, nous avons un nouvel allié :    
le **Steam Deckard** de Valve.    

C’est un casque de réalité virtuelle à l’image du Quest 3 mais tournant sous SteamOS via Linux.  
Un ordinateur qui est un casque VR et qui sait faire tourner des jeux Steam et Android.  
Je peux vous dire que je suis impatient de mettre la main dessus.  

La capacité que Godot a de pouvoir coder et construire un jeu directement dans le casque et de voir le résultat en même temps…  
C’est magique sur Quest 3, et l’idée de pouvoir faire ça librement sur Linux en 2025 est merveilleuse.  

C’est une belle année pour apprendre l’informatique en général.  

Ça va être une bonne année 2026 😛

---



