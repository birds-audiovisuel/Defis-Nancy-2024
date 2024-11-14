# Chapitre 1 : Bases de Python et Premiers Programmes

## 1. Les Variables

Une variable est un espace de mémoire qui contient une valeur. En Python, vous pouvez créer une variable en lui assignant une valeur avec le signe `=` :

```python
x = 10  # Variable de type entier
y = 5.5  # Variable de type flottant
nom = "Robot"  # Chaîne de caractères
```

## 2. Les Fonctions

Les fonctions permettent de structurer le code en morceaux réutilisables. Exemple de fonction qui affiche un message :

```python
def dire_bonjour():
    print("Bonjour, techno-footballeur!")
```

## 3. Les Commentaires

Pour rendre le code plus clair, utilisez des commentaires en commençant par `#` :

```python
# Ceci est un commentaire
```
<br>

# Pratique

## Exercice 1

1. Complétez les lignes de code ci-dessous pour assigner des valeurs aux variables :

   ```python
   # Complétez le code pour assigner des valeurs
   x = ___
   y = ___
   nom = "___"
   print("Valeur de x :", x)
   print("Valeur de y :", y)
   print("Nom :", nom)
   ```

## Exercice 2

2. Écrivez un script pour déplacer le robot en fonction de la position de la balle.

   - **Objectif** : Utilisez des variables pour stocker les coordonnées de la balle et du robot.
   - **Instructions** : Utilisez des conditions pour déterminer si le robot doit avancer ou pivoter.


```python
# Simulation simplifiée du déplacement d'un robot en fonction de la position de la balle

# Importer la librairie RSK nécessaire pour contrôler le robot
from rsk import *

# Connexion au client pour contrôler le robot
with Client(host='127.0.0.1', key='') as client:
    # Position initiale de la balle et du robot
    

```

Instructions pour compléter :
1. **Complétez le premier appel à `deplacer_robot(position_robot_x, ___)`** en remplaçant `___` par une valeur positive pour faire avancer le robot.
2. **Complétez le second appel à `deplacer_robot(position_robot_x, ___)`** en remplaçant `___` par une valeur négative pour faire reculer le robot.

3. **Notez vos commentaires** : Expliquez chaque étape pour clarifier votre logique.


<br> 

### 🌐 Défi N° 1 : Mission "Un monde de couleur" 🌐     (5pts)

Votre mission, si vous l'acceptez, est d'illuminer le monde digital avec une cascade de couleurs éblouissantes.
Armé de votre expertise et du puissant client RSK, vous allez plonger dans un univers où la couleur est reine.

##### 🎨 Lumière Verte, Action !

Une fois connecté, votre objectif est d’allumer les LEDS en vert éclatant.
Utilisez la combinaison de couleurs suivante pour créer un vert pur :

- Rouge (R) : 0
- Vert (G) : 255
- Bleu (B) : 0

Votre code ressemblera à ceci :

```python
import rsk

with rsk.Client() as client:
    while True:
        client.blue1.leds(0, 255, 0)
```

<br>

## Déplacements du Robot sur le Terrain

Pour ces exercices, nous utiliserons le système de coordonnées du Robot Soccer Kit. Le centre du terrain est l'origine (0,0), l'axe X s'étend horizontalement et l'axe Y verticalement. Les unités sont en mètres. 

### I) Se Positionner Face aux Cages

Pour que le robot se positionne face aux cages, il doit se déplacer vers une position spécifique sur l'axe X tout en maintenant son orientation vers l'axe Y positif.

```python
def se_positionner_face_aux_cages():
    # Position cible pour être face aux cages
    position_cible_x = ___  # Indice : Centre du terrain sur l'axe X
    position_cible_y = ___  # Indice : Près des cages adverses

    # Déplacer le robot vers la position cible
    robot.deplacer_vers(___, ___)

    # Orienter le robot vers l'axe Y positif
    robot.orienter_vers(0)  # 0 radian correspond à l'axe Y positif
```

### II) Déplacement le Long de Trois Couloirs

Le robot doit se déplacer le long de trois couloirs définis par les positions X : -0.45 m, 0 m et 0.45 m, tout en se déplaçant sur l'axe Y de 0 à 0.65 m, puis revenir.

```python
def deplacement_couloirs():
    positions_x = [-0.45, 0, 0.45]
    position_y_depart = ___  # Indice : Position de départ sur l'axe Y
    position_y_arrivee = ___  # Indice : Position d'arrivée sur l'axe Y

    for x in positions_x:
        # Aller vers l'avant
       
        # Revenir en arrière
       
```

### III) Déplacement Continu

Pour un déplacement continu, le robot peut suivre une trajectoire en boucle de chaque côté des buts afin de se positioner pour marquer...

```python

```





