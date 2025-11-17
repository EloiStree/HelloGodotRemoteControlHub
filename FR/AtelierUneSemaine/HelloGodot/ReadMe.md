
**Epilogue**

Mon nom est Eloi Stree et j ai commence a creer des jeux il y a 14 ans d ici. Un simple Mario et dimineur en Java puis un jeu en realiter virtuelle toujours en java.
Pour faire du jeux video, il vous faut tout creer de A a Z: notions de temps, physics, importer des fichiers, collisions, chargement de niveau...
Tres amusant mais impossiblement long, c est pour quoi j ai appris a utiliser Unity3D.

En septembre 2025, en tant qu enseignant, je decide de tester Godot car il s installerai apparemment sur des RaspberryPi 5 (des petits ordinateurs de 75-150euro).
Je m y essai et y prend gout. Je constast que l editeur pour tourner sur Andoid ! Et effectivement je peux travailler sur mon telephone. Je peux donc travailler dans un casque de realite virtuelle comme le Quest3 ;) ?
Effectivement.

Godot est un outil de creation de jeux video creer en argentine de maniere open source pour permettre a tous de savoir faire du jeux video peu importe la machine que vous aveza al maison.
Meme si vous etes sur un vieux Linux 32 bit !!!

La raison pour laquel je me suis mis a Godot est une suite logic:
- Scratch permet d apprendre la programmation mais est vite limitant
- Python est tres formateur mais devient vite compliquer quand le code grandi pour des debutants
- C# est un beau language mais sans interface graphique il faut savoir garder l attention de apprenand.
- Unity3D est la bonne solution pour apprendre mais il est trop lourd et trop complexe pour un petit atelier de quelque heures ou jours

Je cherhait une maniere d enseigner la programmation par le jeu video.

Godot a une force pour un enseignant en programmation: il est multilangue.
Celui-ci fonction avec son propgre language de `Gogot Script` tres facile a apprendre.
En plus de celui-ci, il possede un outil, le GDExtension, qui permettre de choisir son language 😁.
- [Python](https://github.com/niklas2902/py4godot): le language le plus connu au monde, pas tres rapide mais simple et versatile
- [C#](https://docs.godotengine.org/en/stable/tutorials/scripting/c_sharp/index.html): tres propre et utiliser dans de nombreux metier et entretenu par Microsoft
- [C++](https://docs.godotengine.org/en/4.4/tutorials/scripting/gdextension/gdextension_cpp_example.html): si vous desirez la puissance de mais compter etudier pendant 20 l optimisation
- [Rust](https://godot-rust.github.io): si vous aimez coder propre et pour longtemps
- [LUA](https://github.com/gilzoide/lua-gdextension): pour faire des jeux modificable par la communauter
- [Javascript](https://github.com/godotjs/javascript): si vous desirez faire un cartiere de webdeveloppeur par la suite.


Un outil de creation de jeux video:
- leger comme un plumb,
- sans compte
- gratuit
- open source
- multiplatform
- tourne sur Linux
- tourne sur Raspberry Pi 5
- tourne sur des vieux Window
- tourne dans les casques VR
- peu etre utiliser en C# et Python
- ...

Y a rien a dire, c est beau ;)


**Raspberry Pi 5 et Steam Machine**

Le Raspberry Pi est un mini ordinateur creer par le gouvement anglais pour apprendre a programmer et utilier un ordinateur a sa population.
Il est pas chere et orianter open source.

Depuis le Pi 5 est vraiment viable au points que j ai appris Godot pendant deux mois sur celui-ci pour voir ci cela est possible.
Et effectivement, je conseille vraiment cette achat a un etudiant ou jeune adutle.

Car en plus de permettre d apprendre, il ne consome que 6-18 watt et peu servir de serveur linux a la maison 👍🍻.

Mais a heure ou je redigue cette presentation d atelier pour apprendre a coder sur Godot, un nouveau joueur est arriver sur le macher: le casque VR desckard et la Steam Machine.

Aussi nommer la Gabe Cube, du nom de son createur, la steam machine est un ordinateur et une console de jeux.
Mais a la difference d une console qui vous enferme pour que vous achetiez des jeux.
Alors que la Gabe cube est simplement un ordinateur Linux avec juste ce qu il faut pour se sentire alaise sur la ventilastion et la puissance.
Un petit ordinateur de maison qui en un bouton se trouve etre un console de jeux actuelles, retro et Android.

C est litteralement un revolution a une epoque ou les consoles Xbox et PlayStation coutes le prix d un ordinateur.

Cette atelier, peu importe ca variation sur l exercice ou le contenue, a un simple bute:
Donner gout a la programmation sur Godot par le jeu video.

Pour cela, 4-12 Raspberry Pi sont mis a disposition des etudiants durant l atelier
Et, quand disponible, 1-2 Steam Deck seront present pour tester.

Si l apprendant un de ces appareils:
- une bonne tablette Android
- un ordinateur portable personnel (linux ou window)
- son propre raspberry pi 5
- une Steam Deck

Il peut decider de venir avec.
Godot exactement le meme sur tout les platformes.


# Deckard et Meta

Vous pouvez creer votre jeux video directement a l interieur du casque de Meta le Quest3 😮.
C est magique.

Une partie de latelier y sera dedier.
L avantage du Meta est qu il est abordable, 330euro.
Le desaventage: C est Mark Zuterber, anciennement proprieteaire de Facebook, qui a la main sur vous.
Avantage pour un createur: il y 4+ millions de Quest 2 et 1-3 millions de Quest 3 avec qui partager votre jeu.

Mais depuis le 14 Novembre 2025, vous avons un nouvelle allier:
le Steam Deckard de Valve.

C est un casque de realite virtuelle a l image du Quest3 mais sous Steam OS via Linux.
Un ordinateur qui est un casque VR et qui sait faire tourner des jeux Steam et Android.

Je peux vous dire que je suis impatient de mettre ma main dessus.

La capaciter que Godot a de pouvoir coder et construire un jeu directement dans le casque et de voir le resultat en meme temps.
Et magic sous Quest3 et l idee de pouvoir faire sa librement sur Linux en 2025 est merveilleux.

C est une belle annee pour apprendre l informatique en general.

-------------------------------------------

# L atelier.

- Day 1: C est quoi un Raspberry Pi et Godot.
- Day 2: Journee Brackeys
- Day 3: Bougeons un Drone
- Day 4: Creetons un niveau pour notre drone
- Day 5: Jouons a plusieur manette sur votre circuits.



**C est quoi Godot ?**
Godot (preferentially /ˈɡɒdoʊ/ ⓘ GOD-oh)[a] is a cross-platform, free and open-source game engine released under the permissive MIT license. It was initially developed in Buenos Aires by Argentine software developers Juan Linietsky and Ariel Manzur[6] for several companies in Latin America prior to its public release in 2014.[7] The development environment runs on many platforms, and can export to several more. It is designed to create both 2D and 3D games targeting PC, mobile, web, and virtual, augmented, and mixed reality platforms and can also be used to develop non-game software.
