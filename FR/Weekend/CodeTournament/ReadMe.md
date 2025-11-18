

Brouillon de proposition d’atelier visant à enseigner la programmation par le jeu durant les week-ends de l’année.  

---

Ma volonté en tant qu’enseignant est de donner le goût de la programmation à travers le jeu et l’organisation de tournois de code.  
L’objectif de cet atelier est de mettre en place un club de programmation, ouvert à tous les âges, les week-ends.  

Comme je ne peux pas héberger les participants tous les vendredis et samedis ;)  
La structure serait organisée ainsi :  

### **Organisation du week-end** 

* **Vendredi — 12h :** Installation et préparation du matériel pour le week-end.  
* **Vendredi — 17h/18h à 21h :** *Tournoi Python Live* – Premiers pas en Python sur des Pico 2W à travers un tournoi permanent.    
* **Samedi — 9h à 12h :** *Introduction à Godot et GDScript* – Découverte de Godot et réalisation d’un petit « Hello World ».   
* **Samedi — 13h à 16h :** *Hackons un jeu* – Apprendre à simuler des touches avec un Pico 2W et à lire les pixels d’un écran.    
* **Samedi — 16h à 21h :** Atelier libre – Pratique et jeu autour du « jeu du week-end ».  
* **Dimanche — 9h à 18h :** Coaching Godot et Python avancé – Tournoi de code sur le jeu du week-end pour s’entraîner aux côtés des joueurs confirmés.  

### **Précisions**

* Les participants ne sont pas obligés d’être là les trois jours.  
* Le **vendredi** sert à se détendre et à prendre en main la programmation.  
* Le **samedi** est dédié :  
  * aux juniors qui souhaitent découvrir,  
  * aux anciens élèves qui veulent pratiquer pendant que j’enseigne aux débutants.  
* Le **dimanche** est centré sur la pratique en autonomie dans une ambiance orientée code autour du jeu du week-end ou du tournoi permanent.   

---

## **Le jeu du Week-end**

Configuration fixe :
* 4 mini-PC affichés sur un grand écran
* 4 Pico 2W connectés aux mini-PC pour simuler des touches de clavier
* 4 Arduino XInput pour simuler des manettes Xbox
* 8+ MiraBox branchées sur le grand écran via un switch pour fournir l’affichage aux élèves

### **Objectifs pédagogiques**

* **Débutants :** apprendre à bouger un personnage dans le jeu via du code
* **Avancés :** apprendre également à lire l’écran
* **Confirmés/Seniors :** réussir à terminer une partie du jeu sans intervention humaine

Un tutoriel est fourni pour que les élèves puissent pratiquer chez eux, à condition d’avoir une MiraBox, un Pico 2W et deux PC.

---

## **Tournoi Permanent**

Je souhaite mettre en place un tournoi de code permanent en Python.

Inspirations :

* **oGame :** le jeu tourne 24h/24 et 7j/7
* **Agar.io :** vous apparaissez, vous tentez de survivre, puis vous recommencez
* **CodinGame :** vous jouez uniquement par le code en laissant vivre votre/vos personnage(s)

L’apprenant dépose un script Python qui est ensuite chargé dans un Pico 2W.
Le Pico reçoit des informations du jeu en binaire et en texte, et peut générer des entrées clavier ou manette via le réseau.
